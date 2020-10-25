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
