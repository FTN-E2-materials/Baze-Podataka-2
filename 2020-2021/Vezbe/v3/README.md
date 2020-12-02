# Kretanje
  - gradivo vezano za **normalne forme** mozete pronaci [ovde](https://github.com/FTN-E2-materials/BazePodataka2/blob/main/2020-2021/Vezbe/v3/normalne-forme.md)
  - gradivo vezano za **spojivost bez gubitaka** mozete pronaci [ovde](https://github.com/FTN-E2-materials/BazePodataka2/blob/main/2020-2021/Vezbe/v3/spojivost-bez-gubitaka.md)


<details>
  <summary> Precice za proveru NF </summary>
  
## Precice 

- ako u sr **ne postoje funkcionalne zavisnosti**, ona je sigurno barem u **BCNF**
- ako sr nema **neprimarnih** obelezja, ona je sigurno barem u **3NF**
- cim svaki **kljuc** ima **jedno obelezje**, sr je sigurno barem u **2NF**
  
</details>


<details>
  <summary> Saveti za proveru NF</summary>
  
## Saveti
  - **prvo proveriti BCNF** jer ako je on zadovoljen, **SR je u BCNF**
  - **potom proveriti 2NF** jer ako on ne vazi, **SR je u 1NF**
  - na **kraju proveravati 3NF** jer za potvrdu netranzitivnosti, moramo proci kroz svako neprimarno obelezje i to pokazati
  
</details>

<details>
  <summary> Precice za proveru ocuvanja spojivosti bez gubitaka informacije </summary>
  
## Precice 

- (**OVO TREBA DOBRO PROVERITI, NISAM SIGURAN, ALI OVO SU NAPISALI U ZBIRCI**) Spojivost bez gubitaka informacija je ocuvana ako **jedna od sema relacija**( iz skupa sema relacija) **sadrzi kljuc polazne seme relacije** ( kljuc univerzalne seme relacije)
  
</details>


<details>
  <summary> Recnik </summary>
  
### Recnik
  
  - **SR**: sema relacije
  - **FZ**: funkcionalna zavisnost
  - **NF**: normalna forma
  
</details>
  
  
