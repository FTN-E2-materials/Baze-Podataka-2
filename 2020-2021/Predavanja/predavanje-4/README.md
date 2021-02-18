## Teorema o spojivosti bez gubitaka

<details>
 <summary> Teorema </summary>
 
 <br>
 
 <details>
 <summary> Dato je </summary>
 
 ![image](https://user-images.githubusercontent.com/45834270/108108333-c9e8a280-7090-11eb-95ae-7e8865dcf72a.png)
 
 </details> 
 
  <details>
 <summary> Garantuje se </summary>
 
 ![image](https://user-images.githubusercontent.com/45834270/108108384-d967eb80-7090-11eb-9913-b6523cf51a4d.png)
 
 </details> 
 
  <details>
 <summary> Vazi ekvivalencija </summary>
 
 ![image](https://user-images.githubusercontent.com/45834270/108108420-e5ec4400-7090-11eb-9c12-591808aa2ec2.png)
 
 </details> 
 
 </details> 
 
 <details>
 <summary> Dokaz </summary>
 
 <br>
 
 <details>
 <summary> Dokazujemo teoremu </summary>
 
 ![image](https://user-images.githubusercontent.com/45834270/108109794-acb4d380-7092-11eb-8b39-6958d6fdc5ba.png)
 
 </details>
 
  - kada radimo dokaz neke ekvivalencije, moramo odraditi dokaz implikacije na obe strane
 
 <br>
 
 <details> 
 <summary> Desna implikacija </summary>
 
 <br>
 
   - prvo dokazujemo da pod pretpostavkom da vazi **barem jedna od ovih fz**, vazece i zavisnost spoja
 
 ![image](https://user-images.githubusercontent.com/45834270/108110429-87749500-7093-11eb-9aa9-31c7874938e0.png)

  - sta znaci da treba dokazati da vazi ova zavisnost spoja ? (tj. sta po definiciji znaci da je neka zavisnost posledica od nekog skupa zavisnosti)
    - to znaci da ako za bilo koju relaciju iz skupa svih mogucih relacija nad skupom obelezja u, vazi da ta relacija zadovoljava skup funkcionalnih zavisnosti F, onda ona mora zadovoljavati i moju zavisnost spoja (to mi treba da dokazemo, slika ispod)
    
![image](https://user-images.githubusercontent.com/45834270/108111939-b7bd3300-7095-11eb-9fd9-36c613d2d901.png)

<br>

  - po univerzalnoj konkretizaciji uzecemo bilo koju relaciju i predpostavicemo da ona bas zadovoljava moj skup funkcionalnih zavisnosti F
  
  ![image](https://user-images.githubusercontent.com/45834270/108113197-7f1e5900-7097-11eb-93fe-2279a9a549a3.png)

<br>


  - onda treba da dokazemo da ce ona zadovoljavati i zavisnost spoja, a da bi dokazali da ce ona zadovoljavati tu zavisnost spoja mi zapravo treba da dokazemo
  
![image](https://user-images.githubusercontent.com/45834270/108113234-8d6c7500-7097-11eb-8b84-5dae098b6e26.png)

<br>

  - posto imamo gore pretpostavku da ce vaziti barem jedna od te dve funkcionalne zavisnosti (fz), uzecemo nek je to prva da vazi(a posle cemo uzeti i drugu )
  - ako uzmemo da vazi prva, mi smo vec dokazali da ***ako je X->Y posledica od F-a onda vazi da je projekcija na xy spojeno sa projekcija na x unija u bez y jednako relaciji r***, onda to samo primenimo i na nas slucaj
  
![image](https://user-images.githubusercontent.com/45834270/108114822-91999200-7099-11eb-97bb-a964c4a8f224.png)

  - kada smo ovo dobili, to znaci da smo mi dokazali jednakost (pod predpostavkom da je vazila data fz)
  
<br>

  - potom uzmemo da vazi druga fz i na isti nacin pokazemo da vazi jednakost
  
![image](https://user-images.githubusercontent.com/45834270/108115365-4f248500-709a-11eb-84ce-a74fccea02d1.png)

<br>

### Zakljucak

  - dovoljno je jedna od fz da vazi da bi vazila zavisnost spoja a nas dokaz u ovu stranu je zavrsen


 <br>
 
 </details>
 
 <br>
 
  <details> 
 <summary> Leva implikacija </summary>
 
 <br>
 
  - u drugu stranu sad treba dokazati da ako imamo da je zavisnost spoja R1 i R2 posledica od F onda mora [jedna od ove dve](https://prnt.sc/zrmkgk) fz da vazi (kao posledica od F-a)
  - mi znaci dokazujemo ovo ispod (a predpostavljamo da ce nam vaziti zavisnost spoja)
  
![image](https://user-images.githubusercontent.com/45834270/108117046-bb07ed00-709c-11eb-8c6e-f911e9090873.png)

<br>

  - to dokazujemo tako sto predpostavimo da imamo relaciju koja zadovoljava F a onda ona mora zadovolji i bar jednu od [ove dve fz](https://prnt.sc/zrnxco)
 
 ![image](https://user-images.githubusercontent.com/45834270/108118035-0d95d900-709e-11eb-80f5-a4124f2c87f2.png)

<br>

  - posto sada hocemo preko suprotne pretpostavke to da dokazemo, mi cemo uzeti neku relaciju koja ce **zadovoljiti nase F i nece zadovoljiti ni jednu od te dve fz**
  - a kasnije cemo to oboriti kontradikcijom sa nasom polaznom pretpostavkom (vazi zavisnost spoja R1 i R2)
 
 ![image](https://user-images.githubusercontent.com/45834270/108118397-9876d380-709e-11eb-92d3-bd2c8a54a6ef.png)

<br>

  - relacija koja ce nam to omoguciti je relacija sa samo 2 torke i ona izgleda ovako: 
 
![image](https://user-images.githubusercontent.com/45834270/108119477-27382000-70a0-11eb-8d43-b347133123f5.png)

  - pri cemu su te dve torke jednake nad R1 presek R2 + s obzirom na F (zato ovo 0, 0)  a da su na ostatku **obavezno razlicite** (zato ovo 0, 1), odnosno: 

![image](https://user-images.githubusercontent.com/45834270/108119793-9877d300-70a0-11eb-8725-e57975b1feef.png)

  - ideja kada pravimo ovu relaciju je to da mi zelimo napraviti relaciju koja zadovoljava ceo skup fz F
  - i zadovoljice svaku onu fz iz R1 presek R2, u razlika R1 presek R2 ako je ona zapravo posledica od F
  - a oborice svaku R1 presek R2, u razlika R1 presek R2 koja nije posledica od F
  - i to je krajnja ideja 

<br>

  - prvo dokazemo da li nasa relacija uopste zadovoljava nas skup fz F
  - to uradimo tako sto uzmemo bilo koju fz iz F
  - a potom treba pokazati da je ova relacija zadovoljava

![image](https://user-images.githubusercontent.com/45834270/108120933-4d5ebf80-70a2-11eb-8e55-99db6dd1022a.png)

 <br>

  - neka uzmemo neku fz V->W, dva moguca slucaju (po zakonu iskljucenja treceg) su:
    - da je V podskup R1 presek R2 + s obzirom na F
    - da V nije podskup
    
 ![image](https://user-images.githubusercontent.com/45834270/108121155-a2023a80-70a2-11eb-921d-ecaeb8786855.png)

<br>

  - ako je V podskup, to znaci da je on funkcionalno zavisan od njih a zbog tranzitivnosti onda je i W 

![image](https://user-images.githubusercontent.com/45834270/108121353-fc030000-70a2-11eb-9acf-afe43f4370c1.png)

  - a posto su nase torke [jednake](https://prnt.sc/zrrzqu) nad R1 presek R2 plus, a ako su nase torke jednake nad V, sigurno ce onda biti jednake i nad W 
  - i posto su ovo jedine dve torke, jednake su na V, jednake su na W mi onda konstatujemo da ova relacija sigurno zadovoljava V u W 
  - (sada se vidi zasto je uzeta bas ovakva relacija, jer ona treba da ima sto manje torki )

![image](https://user-images.githubusercontent.com/45834270/108121839-b266e500-70a3-11eb-931b-337e4943023e.png)

<br>

  - a ako V nije podskup, onda trivijalno vazi V u W zato sto jedna strana implikacije nikad nije zadovoljena

![image](https://user-images.githubusercontent.com/45834270/108122084-0f629b00-70a4-11eb-8d9f-5cc784417546.png)

<br>

  - konacno, posto je ovo bilo koja fz, onda nasa relacija sigurno zadovoljava ceo skup fz

![image](https://user-images.githubusercontent.com/45834270/108122377-78e2a980-70a4-11eb-9231-d16c19dd5f4c.png)

<br>


  - sada krecemo dalje, odnosno, mi predpostavljamo da ta nasa relacija **ne zadovoljava ni jednu** od [nase dve fz](https://prnt.sc/zrt0e1) a **zadovoljava ceo F** 
  
![image](https://user-images.githubusercontent.com/45834270/108126078-ada52f80-70a9-11eb-9f86-5be458227b87.png)

![image](https://user-images.githubusercontent.com/45834270/108126325-01b01400-70aa-11eb-9e9e-f7fa800f206a.png)

<br>

  - torke su jednake nad [ovim](https://prnt.sc/zrxken)

![image](https://user-images.githubusercontent.com/45834270/108126526-3cb24780-70aa-11eb-87c2-345ec8a59eb3.png)

<br>

![image](https://user-images.githubusercontent.com/45834270/108126817-93b81c80-70aa-11eb-93f6-159e5041fef3.png)

<br>

### Zakljucak

  - iz cinjenice da nasa relacija ne zadovoljava zavisnost spoja a zadovoljava nas skup fz onda znaci da nasa zavisnost spoja nije sigurno posledica funkcionalnih zavisnosti a po polaznoj predpostavci je bila ( i dosli smo do kontradikcije, tj. oborili smo nasu suprotnu predpostavku i dokazali nase polazno tvrdjenje)

![image](https://user-images.githubusercontent.com/45834270/108126899-b1858180-70aa-11eb-8bc3-eebad177cc8a.png)















<br>

 </details>
 
 <br>
 
 </details>
 
 
# Normalne forme i normalizacija

 - Ova tema se jako lepo mapira na vezbe gde je sve lepo objasnjeno uz [detalje sa predavanja](https://github.com/FTN-E2-materials/BazePodataka2/tree/main/2020-2021/Vezbe/v3)


## Sablon narusavanja 3nf

![image](https://user-images.githubusercontent.com/45834270/98993706-1c18a580-252f-11eb-9b1a-15d4c5c0e2ce.png)

