# Metoda sinteze

<details>
  <summary> Ideja </summary> <br>
  
 ![image](https://user-images.githubusercontent.com/45834270/100949321-4811c000-350a-11eb-8e0e-ab3fa02943e7.png)
</details>


<details>
  <summary> Ulaz-izlaz </summary> <br>

![image](https://user-images.githubusercontent.com/45834270/100949600-ea31a800-350a-11eb-943d-35a22061de48.png)

### Podsetnik

Ulaz u [metodu dekompozicije](https://github.com/FTN-E2-materials/BazePodataka2/tree/main/2020-2021/Predavanja/predavanje-7) je (U,C). Pri cemu je C skup ogranicenja koji moze sadrzati: 
  - funkcionalne zavisnosti
  - viseznacne fz
  - zavisnosti spoja

## Napomena 

Algoritam **dekompozicije** nas moze dovesti cak do **5nf** ako koristimo viseznacne fz i zavisnost spoja. Dok kod algoritma **sinteze** mozemo doci samo do **3nf** i na ulazu je samo **skup fz** odnosno samo (U,F) a ne (U,C).
</details>

<details>
  <summary> Koraci algoritma </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/100950589-f1f24c00-350c-11eb-9028-9761d5350bba.png)
</details>

<details>
  <summary> Formiranje kanonickog pokrivaca </summary> <br>
  
  <details>
  <summary> Kanonicki pokrifac kp </summary> <br>
  
  ![image](https://user-images.githubusercontent.com/45834270/100950996-e5babe80-350d-11eb-9a22-79fd34a0a3ad.png)
 
</details>

### Redukciju s leve strane

  - skinemo neko obelezje s leve strane 
  - gledamo da li **zatvarac preostalog skupa** obelezja daje ono sto je bilo sa **desne strane**
  - i to radimo za svaku fz
  
### Izbacivanje redundatnih fz

  - za svaku fz proverimo da li se moze dobiti kao posledica ostalih 
    - to proveravamo tako sto nadjemo **zatvarac leve strane na osnovu preostalih funkcionalnih zavisnosti**
  - ukoliko moze, ostranimo je, odnosno ukoliko smo nasli da zatvarac preostalih fz daje R, mozemo izbaciti proveravanu fz

<br>

</details>

<details>
  <summary> Transformacija kanonickog pokrivaca </summary> <br><br>
  
<details>
  <summary> Motivacija koraka transformacije </summary> <br>
  
  ![image](https://user-images.githubusercontent.com/45834270/101056191-02490c00-358b-11eb-8e49-4f3a9e76d67f.png)
</details>

Transformaciju kanonickog pokrivaca radimo u cilju **dobijanja ekvivalentnih kljuceva**.

## Particioniranje kanonickog pokrivaca
  
### Particija skupa

Particija skupa je podela skupa na njegove podskupove, pri cemu unija svih tih skupova daje polazni skup a medjusobni presek tih skupova je prazan, odnosno svi su disjunktni.
  
<details>
  <summary> Slajd </summary> <br>
  
  ![image](https://user-images.githubusercontent.com/45834270/101057794-bb5c1600-358c-11eb-8925-2f344337d4c7.png)
<br>
</details>

  - svaka grupa se sastoji od funkcionalnih zavisnosti koje imaju **iste leve strane**
  - koliko imamo razlicitih levih strana => toliko imamo grupa

## Odredjivanje ekvivalentnih levih strana

<details>
  <summary> Slajd </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/101059265-5d303280-358e-11eb-997a-1ea24c01ecbf.png)
<br>
</details>

<details>
  <summary> Odredjivanje zatvaraca levih strana - primer </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/101060063-463e1000-358f-11eb-8808-d4ce45f112fc.png)
<br>
</details>

### Napomena

Bitno je napomenuti da nema stajanja sa proverom iako smo dobili situaciju da imamo uniranje grupa s ekvivalentnim levim stranam, jer bas ta nova grupa moze biti dalje ekvivalentna. Stoga, provera se nastavlja dok nemamo **ekvivalentnost zatvaraca levih strana** bilo koje dve grupe.


## Uklanjanje tranzitivnih zavisnosti

<details>
  <summary> Slajd </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/101060639-ee53d900-358f-11eb-847f-f97294614f71.png)
<br>
</details>

<details>
  <summary> Primer </summary> <br>
 
  - iz novo nastale grupe G(A,B) izbacujemo A->B, B->A funkcionalne zavisnosti
  - ostale fz **testiramo na suvisnost**, tj testiramo A->C, A->D, D->E, E->F
  
![image](https://user-images.githubusercontent.com/45834270/101061142-74701f80-3590-11eb-9c39-ed2f87a8ba23.png)
<br>
</details>

<details>
  <summary> Slajd </summary> <br>

![image](https://user-images.githubusercontent.com/45834270/101062221-ab930080-3591-11eb-9f3e-3ab341742f0a.png)
</details>

<details>
  <summary> Primer </summary> <br>

  - iz skupa UGxeG(Gx) testiramo svaku fz da li je suvisna u odnosu na skup M 
  - npr A->C testiramo da li je suvisna tako sto proverimo **zatvarac od A u odnosu na M bez A->C** 

![image](https://user-images.githubusercontent.com/45834270/101062470-f90f6d80-3591-11eb-93c6-77caef8a8e21.png)
</details>

## Rekonstrukcija particije kanonickog pokrivaca

Kada smo zavrsili sa trenutnom manipulacijom, sada ono sto je bilo u skupu J trebamo vratiti u odgovarajuce grupe.

<details>
  <summary> Slajd </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/101063808-8c956e00-3593-11eb-9163-28901e20aac1.png)
</details>

<details>
  <summary> Primer </summary> <br>
  
  - 3,4 grupa nisu dirane tkd tu nema sta da se vrati
  - tkd samo ona grupa koja je dirana ona se unira sa J
  - sada mozemo dobiti skup sema relacija na osnovu ovih grupa 

![image](https://user-images.githubusercontent.com/45834270/101064264-15aca500-3594-11eb-8f3d-0308cf6fa75e.png)
</details>


<br><br>

</details>

<details>
  <summary> Formiranje relacione seme baze podataka </summary> <br>
  
## Formiranje skupa sema relacije

  - za svaku grupu uniramo njen skup obelezja i to proglasimo za skup obelezja R
  - potom sve leve strane koje imamo u tim grupama proglasimo ekvivalentnim kljucevima, tj to je skup K 

<details>
  <summary> Slajd </summary> <br>
  
  ![image](https://user-images.githubusercontent.com/45834270/101064982-e21e4a80-3594-11eb-9a9d-18ed832d82bb.png)
</details>

<details>
  <summary> Primer1 </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/101065398-67a1fa80-3595-11eb-82af-dfd3a4fecc9b.png)
<br>
</details>

<details>
  <summary> Primer2 </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/101065630-aafc6900-3595-11eb-95dc-a62b2f3a17d4.png)
<br>
</details>

## Formiranje ogranicenja stranog kljuca

<details>
  <summary> Slajd </summary> <br>

![image](https://user-images.githubusercontent.com/45834270/101066008-2827de00-3596-11eb-8621-f0a4b1ec7258.png)
</details>

<details>
  <summary> Primer </summary> <br>

  - posto angazovanje+ 

![image](https://user-images.githubusercontent.com/45834270/101066201-602f2100-3596-11eb-9d4b-aabf1c237330.png)
</details>

<br><br>
</details>

<details>
  <summary> Ocuvanje spoja bez gubitaka </summary> <br>
  
</details>

<details>
  <summary> Fz kao posledica kljuca </summary> <br>
  
</details>
