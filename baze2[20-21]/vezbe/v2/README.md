# Projekcija skupa funkcionalnih zavisnosti

<details>
  <summary> Algoritam </summary> <br>
  
  - napisemo sve kombinacije polaznog skupa za kojeg pravimo projekciju
  - za svaku kombinaciju odredimo zatvarac 
  - ako u zatvaracu te kombinacije postoji obelezje(ili skup obelezja) iz polaznog skupa, zakljucujemo: **KOMBINACIJA -> OBELEZJE** tj kombinacija odredjuje to obelezje(ili taj skup obelezja)
  - ono sto posmatramo iz tog **obelezja(skupa obelezja)** su ona obelezja koja **nisu kombinacija** ali jesu obelezja iz polaznog skupa  
  - svaku trivijalnu fz ne pisemo, dovoljno je napisati samo *trivijalne* sto oznacava sve trijvijalne fz 
  - ono sto takodje ne pisemo je slucaj:
    - ako nam vazi A->nesto
    - i imamo W koje je nadskup od A
    - ne pisemo W->nesto
    - jer se **podrazumeva zbog prosirivanja**
  
  </details>
  
<details>
  <summary> Primer </summary> <br>
  
  - polazni skup je ADF i odredili smo sve njegove kombinacije, a potom i zatvarace od svake kombinacije
  - ako pogledamo zatvarac nad AD, vidimo da dobijamo ADBCEF, gde je AD bas kombinacija, BCE nisu obelezja iz polaznog skupa, a F je obelezje iz polaznog skupa, takodje, F nije obelezje u skupu kombinacije, te zakljucujemo da AD odredjuje F
  
  ![image](https://user-images.githubusercontent.com/45834270/98126565-06173f00-1eb6-11eb-9dc7-ddf3aedd3732.png)

  
  </details>

# Utvrdjivanje ekvivalentnosti dva skupa

<details>
  <summary> Algoritam </summary><br>

![image](https://user-images.githubusercontent.com/45834270/98127403-f64c2a80-1eb6-11eb-8dd5-05c619c3d3d1.png)


Iteriramo kroz svaku fz iz F1 i proveravamo da li su te fz **logicke posledice** u F2. Ako jesu, isto proverimo za sve fz i iz F2, tj da li su one logicke posledice u F1, ako jesu, skupovi funkcionalnih zavisnosti F1 i F2 su ekvivalentni. 
  
  </details>

<details>
  <summary> Primer </summary>

### Primer

  - Posmatramo recimo, prvu fz iz F2, sto je A->D
  - Proveravamo da li je ona [logicka posledica](https://github.com/FTN-E2-materials/BazePodataka2/tree/main/baze2%5B20-21%5D/vezbe/v1) nad F1 
  - Posto utvrdujemo da jeste, prelazimo na sledecu fz iz F2, sto je DB->A i opet proveravamo da li je ona logicka posledica u F1
  - itd...

![image](https://user-images.githubusercontent.com/45834270/98127855-783c5380-1eb7-11eb-9cc5-bce410ee08f7.png)

  
  </details>


<details>
  <summary> Napomena </summary>

## Napomena

U oba smera mora da vazi da svaka fz iz jednog skupa fz moze da se izvede iz drugog skupa fz! Ako se ispostavi da postoji jedan kontra primer, ta dva skupa fz nisu ekvivalentni.
  
  </details>
