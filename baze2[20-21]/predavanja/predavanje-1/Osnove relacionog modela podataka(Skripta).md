# Osnove relacionog modela podataka(Skripta)

## Model podataka   
### - Strukturalna komponenta
Sadrži koncepte putem kojih gradimo šemu baze podataka.
### - Operacijska komponenta
Sadrži upitne jezike i jezike za manipulisanje i definiciju podataka.
### - Integritentna komponenta 
Bavi se definicijom i intrepetacijom ograničenja na nivou servera i uopšte na nivou šeme baze podataka.
### - Nivoi apstrakcije 
 - Nivo intenzije (konteksta) (Nivo tipa npr šema baze podataka)
 - Nivo ekstenzije (konkretizacije) (Nivo pojave tipa)
 
 ## Strukturalna komponenta I 
 - Primitivni koncepti u RMP:
   * Obelezje (Atribut) - reprezentuje osobinu tj svojstvo klase entiteta ili poveznika
   * Domen - reprezentuje skup mogucih vrednosti koje neka obelezja mogu da dobiju
 - Polazna predpostavka strukturalne komponente RMP na osnou koje se zasnivaju neke tehnike projektovanja relacione seme BP su:
   * Da je poznat univerzalni skup obelezja U = {A1,...,An}
   * Da je poznat univerzalni skup svih domena D = {D1,...,Dk}
 - Pravilo pridruzivanja domena obelezjima 
   * Svakom obelezju se pridruzuje tacno jedan domen
 - Primitivni koncepti nivoa intenzije:
   * domen
   * obelezje
 - Primitivni koncepti nivoa ekstenzije 
   * vrednost
  Sve ostalo se dobija kombinovanjem ovih primitiva.
  
<p align="center">
  <img src="https://user-images.githubusercontent.com/49925421/97113195-014dd080-16e9-11eb-95b0-bd47da426146.png" width="350" title="hover text">
</p>

- Torka 
  * Reprezentuje jednu pojavu entiteta ili poveznika, pomocu torke se svakom obelezju iz nekog skupa obelezja dodeljuje konkretna vrednost
- Relacija 
  * Reprezentuje **KONACAN** skup torki
  * Uobicajna predstava relacije je tabela (ovde napraviti terminolosku distinkciju, ne moze sve u zivotu biti tabela tj Relacije != Tabela) 
 ## Operacijska komponenta 
- Vrste teorijskih upitnih jezika u RMP 
  * relaciona algebra (zasnovana na teoriji skupova i skupovnih operacija)
  * relacioni racun (nad torkama i nad domenima)
- Osnovne skupovne operacije nad relacijama:
  * Unija 
  * Presek
  * Razlika 
<p align="left">
  <img src="https://user-images.githubusercontent.com/49925421/97113737-98685780-16ec-11eb-8283-f36a6a492877.png" width="350" title="hover text">
</p> 

**NAPOMENA za selekciju i projekciju bitan je matematicki zapis i bitno je znati protumaciti ga**
- Selekcija 
  * Vrsi odabir samo odredjenih torki po nekom definisanom kriterijumu
<p align="left">
  <img src="https://user-images.githubusercontent.com/49925421/97113911-9b177c80-16ed-11eb-8bf3-9b8116d8190c.png" width="150" title="hover text">
</p> 
<p align="left">
  <img src="https://user-images.githubusercontent.com/49925421/97113841-29d7c980-16ed-11eb-8cb8-ad0edc75f61e.png" width="350" title="hover text">
</p> 

- Projekcija 
  * Vrsi izdvajanje vrednosti pojedinih kolona iz relacije

<p align="left">
  <img src="https://user-images.githubusercontent.com/49925421/97114191-58ef3a80-16ef-11eb-9f7c-181b75eccfa8.png" width="180" title="hover text">
</p> 

**Tumacenje matematickog zapisa:** Projekcija je skup svih t od x-ova takvih da... pa onda ide predikat tj osobina

Projekcija ovako kako je definisana u relaciooj algebri odgovara SELECT naredbi onome sto je SELECT svih kolona iz X-a FROM TABLE, ne samo to nego i SELECT DISTINCT. Ovo se **MORA** znati. Studenti ovde ne znaju da ova definicja projekcije definise skup, a u skupu nema ponavljanja torki, tkd. to je ekvivalent SELECT DISTINCT-u.

<p align="left">
  <img src="https://user-images.githubusercontent.com/49925421/97114214-7c19ea00-16ef-11eb-8c94-ea6ac16dc677.png" width="350" title="hover text">
</p> 

- Prirodni spoj relacija

Spajanje torki razlicitih relacija po osnovu istih vrednosti zajedničkih obeležja
 Kako algoritamski izvršiti algoritamski? **(Luković napmenuo da je bitno)**
 
 Algoritam: (referenca : http://grdelin.phy.hr/~ivo/Nastava/Baze_podataka/predavanja-2004/07_pred.pdf)
 <p align="left">
  <img src="https://user-images.githubusercontent.com/49925421/97365082-64846200-18a5-11eb-8177-c7c7aeaf7d64.png" width="400" title="hover text">
 </p> 
 
Prvo provera da li postoje zajednički atributi istog imena i tipa?
Ako da, onda:
 1. Napraviti Dekartov proizvod R i S
 2. Identifikovati zajedničke atribute (kolone)
 3. Identifikovati zajedničke vrednosti zajedničkih atributa, njih zadržati, ostale odbaciti.
 4. Izbaciti (projekcija) duplikate zajedničkih atributa
Rezultat je prirodni spoj.

 <p align="left">
  <img src="https://user-images.githubusercontent.com/49925421/97363776-5cc3be00-18a3-11eb-9775-fe6bb035560c.png" width="400" title="hover text">
</p> 


- Dekartov proizvod relacija

Spajanje formiranje svih mogucih realcija 

- Theta spajanje relacija

Selektovanje torki po nekom kriterijumu iz dekartovog proizvoda relacija
 
## Strukturalna komponenta II
- Šema relacije 
  * Imenovani par N(R, O)
  * N je naziv šeme relacije
  * R je skup obeležja šeme relacije 
  * O je skup ograničenja šeme relacije 
  
- Pojava nad šemom relacije 
  * (R, O)
  * Bilo koja relacija r(R), takva da zadovoljava sva ograničenja iz skupa O
 
- Relaciona šema baze podataka
  * Imenovani par (S, I)
  * S je skup relacija 
  * I je skup međurelacionih ograničenja
  
- Relaciona baza podataka 
  * Jedna pojava nad zadatom relacionom šemom baze podataka (S, I)
  * Svakoj šemi relacije iz skupa S odgovara jedna pojava

- Konzistentno stanje BP 
  * Formalna konzistetnost - Formalno konzistentno je nešto što možemo matematički da dokažemo
    * zadovoljava sva ograničenja odgovarajuće šeme
    * zadovoljava sva međurelaciona ograničenja iskazana putem I
  * Suštinski konzistentno stanje 
    * kada se nalazi u firmalno konzistentnom stanju 
    * i kada predstavlja vernu sliku stanja realnog sistema
