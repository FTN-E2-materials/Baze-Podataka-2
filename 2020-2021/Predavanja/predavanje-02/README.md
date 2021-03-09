<!-- Summary snippet

<details>
 <summary> Name of Summary </summary> 
  
Some snippet of text
 
</details>


-->

### Teorema

Ako vazi fz(funkcionalna zavisnost) x u y u relaciji r, tada bas ovaj prirodni spoj xy od r i  x(u bez y) od r ce dati polaznu relaciju r

![image](https://user-images.githubusercontent.com/45834270/97109370-2cc5c080-16d3-11eb-82e2-f818c7a264c3.png)

### Analiza teoreme

x je ponovljen u obe projekcije, u levoj imamo xy a u desnoj imamo sve bez y i naravno ponovljeni delovi x koji bi postojali u y ako bi ih bilo

### U opstem slucaju ne vazi obrnuto

![image](https://user-images.githubusercontent.com/45834270/97109690-e7a28e00-16d4-11eb-9783-f44d0070b46e.png)

</br></br>

# Viseznacna zavisnost ( skraceno vz ) 

X dvostruka strelica u Y, citamo kao X viseznacno odredjuje Y, gde su ponovo X i Y (skupovi obelezja) koji su neki podskup univerzalnog skupa obelezja u

![image](https://user-images.githubusercontent.com/45834270/97110286-b1ffa400-16d8-11eb-9b8c-1c9616af72e4.png)

Da bi utvrdili sta vz znaci, moramo uvesti pravilo kako vrsimo proveru vazenja vz u realciji

### Pravilo

![image](https://user-images.githubusercontent.com/45834270/97113031-f47cad00-16e7-11eb-9cbf-353c9c9d9466.png)

Nasa relacija r zadovoljava nasu vz, x viseznacno odredjuje y kada je zadovoljeno sledece:

![image](https://user-images.githubusercontent.com/45834270/97113039-02cac900-16e8-11eb-85bf-bd1ad7bd1120.png)

Ukoliko za svake 2 torke u i v iz moje relacije r vazi sledece: kada su te torke u na x i v na x jednake, tada vazi

<details>
 <summary> kod fz(funkcijalna zavisnost)  </summary> 
 
 </br>
 
Da su onda jednaki i na y tj u[y] = v[y]
 
</details>

<details>
 <summary> kod vz (slika iznad)  </summary> 
 
 </br>
 
Se ne zahteva jednakost na y, nego se zahteva egzistencija neke torke, koja moze biti potpuno nova u odnosu na torke u i v ali formula ne trazi to, formula trazi da je to samo neka torka iz relacije r koja mora postojati, sto znaci da nije zabranjeno da ona bude jednaka torci u ili torci v ali ne mora biti, to je takva **nova torka da je u na xy jednako t na xy i da je v na x unija u bez y jednako t na x unija u bez y**

Sada zahtevamo da u slucaju jednakosti bilo koje dve torke na x mora postojati takva torka koja na prvim parcetom xy jednaka prvoj torci a na drugim parcetom x u bez y jednaka ovoj drugoj torci.
 
###### Definicija koja se pita !!
</details>

### Pitanje sa usmenog

<details>
 <summary> pitanje </summary> 
 
 </br>

Data je relacija sa puno torki(nije bitno koliko), kako cemo proveriti algoritamski, da li je zadovoljena fz X u Y

</details>

<details>
 <summary> odgovor </summary> 
 
 </br>

  - u postavimo na jednu torku fiksno, a v koristimo za prolazak kroz ostale torke u nasoj relaciji
  - onda proveravamo ispunjenost uslova za svake dve kombinacije 
  - isti taj proces uradimo i kada je v fiksno a u sluzi za prolazak kroz ostale torke relacije
  
Odnosno, proveravamo svaku sa svakom i gledamo ispunjenost uslova tekuce kombinacije

</details>


### Primer vz zavisnosti

<details>
 <summary> primer </summary> 
 
 </br>

![image](https://user-images.githubusercontent.com/45834270/97114318-24c84980-16f0-11eb-8a8b-d089476e6e55.png)

**Svako mora sa svakim da prodje u kombinaciji i mora ispuniti uslov**

#### Prva kombinacija: Ako uzmemo prvu torku a1, b1, c1 i drugu torku a1, b2, c2 

Da li postoji torka koja je jednaka prvoj na AB i drugoj nad AC. 

Pa postoji, to je treca a1, b1, c2. Jer nad AB su prva i treca torka jednake tj. a1, b1 su iste (sto se i trazi jer se gleda samo nad AB, tj nije potrebno gledati C kolonu) a takodje je treca torka jednaka drugoj torci nad AC odnosno jednaki su a1, c2.

#### Druga kombinacija: Ako uzmemo prvu a1, b1, c1 i trecu a1, b1, c2 torku

Da li postoji torka koja je jednaka prvoj na AB i trecoj nad AC. 

Postoji, i to je treca. Jer nad AB su prva i treca torka jednake, a i nad AC su jednake jer su treca i treca nad AC jednake. Bitan zakljucak iz ovoga je :
  - **ITERIRANA TORKA MOZE BITI ONA KOJU POSMATRAMO KAO TRENUTNU tj nije nuzno da torka t uvek bude RAZLICITA !**

#### Treca kombinacija: Ako uzmemo prvu i cetvrtu torku

Da li postoji torka koja je jednaka prvoj na AB i cetvrtoj nad AC. 

Postoji, to je prva, koja je jednaka prvoj nad AB i jednaka cetvrtoj nad AC.

#### Kombinacije se dalje nastavljaju ! Sada drugu torku ispitujemo sa svakom SLEDECOM

Da li postoji torka koja je jednaka drugoj na AB i TRECOJ nad AC.

Postoji, to je druga torka, koja je jednaka drugoj nad AB i trecoj nad AC.

###### Itd... cemo proci kroz sve i pokazati da A viseznacno odredjuje B

</br>
</br>

</details>

### Zakljucak

Pojam viseznacne zavisnosti, nije to da se izjednacuje dve torke na desnoj strani kada su one jednake na levoj (kao kod obicne fz) nego trazi neku novu torku koja je na jednom parcetu **jednaka prvoj** a na drugom parcetu **jednaka drugoj** torci.

</br>
</br>

## Teorema - cesto pitano na testu ! 

Koja odgovara na pitanje zasto vz postoji 

![image](https://user-images.githubusercontent.com/45834270/97120392-ea25d780-1716-11eb-8b90-8277b6425d9a.png)

Zadovoljenje vz u relaciji r ekvivalentno je tome da je prirodni spoj relacija jednak originalnoj relaciji. Sada imamo ekvivalenciju! Sto znaci da kada vazi jedno onda vazi i drugo !


### Napomena

Bitno je napomenuti i da **fz implicira vz** ali ne i obrnuto ! Voditi racuna da ako ne vazi fz to ne znaci da ne vazi i vz. Jer **vz moze da vazi i bez fz** !

![image](https://user-images.githubusercontent.com/45834270/97120729-83ee8400-1719-11eb-9bbb-6e035af27ea7.png)

# Test pitanja

<details>
 <summary> pitanje-1 </summary> 
 
 </br>

Dobijemo jednu relaciju i pitanje je da li u toj relaciji vazi neka vz.

</details>

<details>
 <summary> odgovor-1 </summary> 
 
 </br>

 Najbrzi nacin da odgovorimo na to pitanje je da napravimo prirodni spoj projekcija i vidimo da li je jednako sa r.
 
 Znaci dobijemo relaciju sa 5,6 torki, obelezja a,b,c,d  i pitanje je da li vazi b viseznacno u d. Znaci napravi se projekcija na bd, projekcija na abc(bitno da je pocetni skup bez d jer je pitanje da li vazi b viseznacno u d) i vidimo da li ce prirodni spoj te dve projekcije vratiti istu relaciju, ako vrati istu relaciju onda vazi vz ako ne onda ne vazi.
 
 </br>

</details>

<details>
 <summary> pitanje-2 </summary> 
 
 </br>

Dobijemo relaciju x viseznacno odredjuje y, dopuniti relaciju da zadovoljava vz. 

</details>

<details>
 <summary> odgovor-2 </summary> 
 
 </br>

Opet napravimo projekciju nad xy i projekciju na x unija u bez y, spojimo te 2 projekcije (uradimo **prirodni spoj**). Tada cemo dobiti i torke koje su nedostajale u polaznoj relaciji.

</details>

<details>
 <summary> pitanje-3 </summary> 
 
 </br>

Ako vazi A u B da li vazi viseznacno A u B i da li iz viseznacnog A u B vazi A u B, tu je potrebno odgovoriti samo za da ili ne.

</details>

<details>
 <summary> odgovor-3 </summary> 
 
 </br>

Ako vazi A u B onda vazi viseznacno A u B ali ne i obrnuto, tj iz viseznacnog A u B ne vazi A u B

</details>
