# Projekcija skupa funkcionalnih zavisnosti

<details>
  <summary> Algoritam </summary> <br>
  
  - napisemo sve kombinacije polaznog skupa za kojeg pravimo projekciju
  - za svaku kombinaciju odredimo zatvarac 
  - ako u zatvaracu te kombinacije postoji obelezje(ili skup obelezja) iz polaznog skupa, zakljucujemo: **KOMBINACIJA -> OBELEZJE** tj kombinacija odredjuje to obelezje(ili taj skup obelezja)
  - ono sto posmatramo iz tog **obelezja(skupa obelezja)** su ona obelezja koja **nisu kombinacija** ali jesu obelezja iz polaznog skupa  
  - svaku trivijalnu fz ne pisemo, dovoljno je napisati samo *trivijalne* sto oznacava sve trijvijalne fz 
  
  </details>
  
<details>
  <summary> Primer </summary> <br>
  
  - polazni skup je ADF i odredili smo sve njegove kombinacije, a potom i zatvarace od svake kombinacije
  - ako pogledamo zatvarac nad AD, vidimo da dobijamo ADBCEF, gde je AD bas kombinacija, BCE nisu obelezja iz polaznog skupa, a F je obelezje iz polaznog skupa, takodje, F nije obelezje u skupu kombinacije, te zakljucujemo da AD odredjuje F
  
  ![image](https://user-images.githubusercontent.com/45834270/98126565-06173f00-1eb6-11eb-9dc7-ddf3aedd3732.png)

  
  </details>

# Utvrdjivanje ekvivalentnosti dva skupa

<details>
  <summary> Teorema </summary>

![image](https://user-images.githubusercontent.com/45834270/98117815-92236980-1eaa-11eb-8b26-6901f9badce7.png)


Uzmemo svaku fz i proveravamo da li su posledice od F1. 
  
  </details>

<details>
  <summary> Primer </summary>

### Primer

Nadjemo zatvarac od A ali PO F1 ( BITNO! ). itd...

![image](https://user-images.githubusercontent.com/45834270/98118161-137afc00-1eab-11eb-8c9d-0ca09e35b012.png)

A->D jeste logicka posledica od F1 (BITNO DA JE OD F1 )
  
  
  </details>



## Napomena

Mora da vazi u oba smera, odnosno, F1 mora biti lp F2 i **OBRNUTO** ! Ako se ispostavi da postoji jedan kontra primer, oni nisu ekvivalentni.
