# Metoda dekompozicije

<details>
  <summary> Provera ocuvanja ekvivalentnosti </summary> <br>
 
Kada uradimo dekompoziciju jednog cvora, moramo proveriti da li je unija funkcionalnih zavisnosti nova dva cvora ekvivalentna skupu funkcionalnih zavisnosti roditeljskog cvora.

### Beleske

Ako pretpostavimo da roditeljski cvor ima skup fz F1, a da su njegova deca cvorovi sa fz F11 i F12.
Testiranje ekvivalentnosti se zasniva na proveri da li je **skup fz roditeljskog cvora posledica unije fz dece** ( F1 posledica unije F11 i F12).

#### Nacin provere

  - detaljnije na direktorijumu koji objasnjava [**utvrdjivanje ekvivalentnosti dva skupa**](https://github.com/FTN-E2-materials/BazePodataka2/tree/main/2020-2021/Vezbe/v2)


</details>

<details>
  <summary> Objedinjavanje sema relacije sa ekvivalentnim kljucevima </summary> <br>

U literaturi ovo nije potrebno raditi ali u praksi je ovo nacin na koji vrsimo **optimizaciju projektovanja baze** .

Kada imamo situaciju da smo izgubili neku fz, nacin na koji je mozemo vratiti je **objedinjavanje sema relacije sa ekvivalentnim kljucevima**.
  
  ![image](https://user-images.githubusercontent.com/45834270/100943230-265e0c00-34fd-11eb-9ca5-6563656b6bea.png)
</details>

<details>
  <summary> Medjurelaciona ogranicenja </summary> <br>

<details>
  <summary> Seme relacije </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/100945265-2b24bf00-3501-11eb-84f5-f582b65b3bbd.png)
</details>

Za seme relacije date u primeru iznad, mozemo rezonovati ogranicenja stranog kljuca:
  - Ispit[BRI] podskup Student[BRI]
  - Povera[OZP] podskup Predmet[OZP]
  - Ispit[OZP] podskup Predmet[OZP] <-- ne pisemo jer je logicka posledica od Ispit na Povera i Povera na Predmet
  - Ispit[NAS] podskup Povera[NAS] <-- ovu necemo napisati jer je donja implicira
  - Ispit[(NAS,OZP)] podskup Povera[(NAS,OZP)] <-- na ovaj nacin obezbedjujemo da samo validni parovi (NAS,OZP) prolaze, tj smanjujemo mogucnost pojave anomalije

<!-- ALGORITAM ODREDJIVANJA MEDJURELACIONIH OGRANICENJA
### Algoritam odredjivanja medjurelacionih ogranicenja
  - iteriramo kroz svaku semu relacije
  - za svaku semu relacije uporedimo da li je obelezje (koje je pri tome **podskup slozenog kljuca**) **prost kljuc** u nekoj od ostalih sema realcije
  - ako jeste, pisemo: sema_relacije[kljuc] podskup sema_sa_kojom_smo_poredili[kljuc]
-->
</details>
