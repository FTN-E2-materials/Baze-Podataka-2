## Metoda dekompozicije

<details>
  <summary> Teorema o spojivosti bez gubitaka </summary> <br>
  
Ako je **kljuc jedne migriran u skup obelezja druge** onda imamo spoj bez gubitaka

</details>

<details>
  <summary> Izbor fz za dekompoziciju </summary> <br>
  
<details>
  <summary> Uvod i algoritam </summary> <br>
  
  - **P1** kriterijum je najstroziji i najbolji kriterijum, onda ide **P2** i onda **P3** 
  - poenta je da nadjemo najbolju fz:
    - ***najbolja fz*** je ona koja je u ***najboljem kriterijumu*** (ako imamo vise fz npr u najboljem tj. u P1, onda mozemo uzeti bilo koju od njih )
 
### Kako se zapravo to odlucuje

  - uzmemo jednu fz i ispostavi se da je ona u P1 => *nema potrebe proveravati druge*
  - a ako uzmemo prvu fz i vidimo da je u ona u P2, onda ne mozemo po njoj deliti jer ne znamo u kom su kriterijumu ostale fz 
  
### Algoritamski

  - iteriramo kroz sve fz i trazimo par (*fz:kriterijum*) sa **najboljim kriterijumom** (sto manjim, najbolji i najmanji je P1)
  - cim nadjemo jedan par koji ima kriterijum P1, tu radimo *break* i tu fz koristimo za dekomponovanje
   
### Napomene

  - ako smo videli da je neka fz u P1, mozemo je odma napisati tj. odma podeliti po njoj 
  - a ako nemamo ni jednu u P1, onda *za svaku fz moramo pokazati da nije u P1* da bi mogli izabrati neku u kriterijumu P2  

<br>

</details>

<details>
  <summary> Tumacenje definicija </summary> <br>

## Kriterijum P1

<details>
  <summary> Definicija </summary><br>

![image](https://user-images.githubusercontent.com/45834270/102245526-f56ad780-3efd-11eb-9ddf-ed989c6c6710.png)

</details>

  - A nije podskup Y samo kaze da moramo imati netrivijalnu fz
  - R nije podskup Y+ kaze: fz **ne sadrzi kljuc sa leve strane**, ovo je bitno
    - jer kasnije imamo *spajanje sema sa istim kljucem* ( i onda dobijemo da zapravo nista nismo uradili...) [slika](https://prnt.sc/w3ct65)
  - nece se prilikom dekompozicije izgubiti ni jedna fz (F1 unija F2 ekvivalentno sa roditeljskim F-om)
    - kada hocemo da pokazemo ovu ekvivalenciju, nije potrebno da pokazemo citavu nego samo da na usnovu unije F1 i F2 mozemo da odredimo sve fz koje postoje u F-u a ne postoje u (F1 unija F2) [slika](https://prnt.sc/w3cxc8)

<br>

## Kriterijum P2

<details>
  <summary> Definicija </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/102245542-fa2f8b80-3efd-11eb-85b3-31af8cb8ef4b.png)

</details>

  - A nije podskup Y samo kaze da moramo imati netrivijalnu fz
  - AY pravi podskup od R kaze: sva obelezja s leve i s desne strane su podskup od R-a ali nisu ceo R
  - nece se prilikom dekompozicije izgubiti ni jedna fz (F1 unija F2 ekvivalentno sa roditeljskim F-om)
    - kada hocemo da pokazemo ovu ekvivalenciju, nije potrebno da pokazemo citavu nego samo da na usnovu unije F1 i F2 mozemo da odredimo sve fz koje postoje u F-u a ne postoje u (F1 unija F2) [slika](https://prnt.sc/w3cxc8)
    
<br>

## Kriterijum P3

<details>
  <summary> Definicija </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/102249208-66ac8980-3f02-11eb-9e79-b65b1eeeff3f.png)

  - A nije podskup Y samo kaze da moramo imati netrivijalnu fz
  - R nije podskup Y+ kaze: fz **ne sadrzi kljuc sa leve strane**

</details>


</details>


</details>


<details>
  <summary> Referencijalni integriteti </summary> <br>

  - u nasim zadacima je potrebno da vidimo samo koji strani kljucevi postoje
  - to utvrdjujemo tako sto posmatramo parove izmedju sema relacije i gledamo da li **kljuc jedne nalazi u skupu obelezja druge**
  
</details>


<details>
  <summary> Radjenje zadataka </summary> <br>

  - nadjemo kljuc univerzalne seme relacije 
  - ako vidimo da imamo gubitak fz, znamo da dekomponovanjem po toj fz nismo ni u P1 ni u P2
  - odredjivanje kljuca i nf ne moramo pisati postupno, to se podrazumeva da znamo
 
 <details>
  <summary> Primer 2 </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/102254215-a7a79c80-3f08-11eb-835b-ffaea7cfe623.png)
  
![image](https://user-images.githubusercontent.com/45834270/102254271-b55d2200-3f08-11eb-9173-8696b226af7c.png)

  
Dobili smo da zadovoljava P1, ono sto je bilo kljucno je da unija F-ova dece jeste ekvivalenetna sa roditeljskim F-om. E sad, zasto je tako ispalo:
  - kad posmatramo fz **A->B , vidimo da je B samo u ovoj fz s desne Z stane** i nigde se vise ne javlja, odnosno u ostalim fz nemamo B **sa leve strane**
    - to je fz ***na kraju lanaca izvodjenja***
    - B ima **jednu ulaznu granu i 0 izlaznih** i to znaci da je na kraju lanaca izvodjenja
  
</details>
 
</details>

<br> <br>

## Precice

  - najveca precica je kada imamo fz koja je na kraju lanca izvodjenja i tada cemo vrv biti odma u P1 i najlakse cemo naci projekcije skupa fz i najbrze cemo preci u narednu iteraciju dekompozicije 
  

## Saveti 

  - zbog nedostatka vremena najbolje prvo raditi sintezu, jer u dekompoziciji je najveci problem trazenje projekcija skupova fz (kojih ima gomila), pa onda ako imamo vremena, radimo postupno, u suprotnom radimo po *osecaju*
  
 
