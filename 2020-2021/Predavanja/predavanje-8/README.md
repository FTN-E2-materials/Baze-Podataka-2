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
  <summary> Transformacija kanonickog pokrivaca </summary> <br>
  
</details>

<details>
  <summary> Formiranje relacione seme baze podataka </summary> <br>
  
</details>

<details>
  <summary> Ocuvanje spoja bez gubitaka </summary> <br>
  
</details>

<details>
  <summary> Fz kao posledica kljuca </summary> <br>
  
</details>
