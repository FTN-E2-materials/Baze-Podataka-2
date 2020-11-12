# Prva normalna forma 

<details>
  
  <summary> Pretpostavka </summary>
  
  </br>

  - Predpostavljamo da **uvek vazi**
  - Uglavnom ne dolaze zadaci koji ne ispunjavaju ovaj uslov, osim ako nije naznaceno da je neko obelezje skup, slog ili tako nesto

</details>

<details>
  
  <summary> Generalno </summary> <br>

Za sve ostale normalne forme (druga,treca,BK) obicno prvo ***gledamo sve funckionalne zavisnosti*** i da li one ispunjavaju neka pravila, ako **sve** ispunjavaju neka pravila onda je zadovoljena normalna forma u suprotnom nije
  
  </details>
  
<details>
  <summary> Potpuna funkcionalna zavisnost </summary> <br>
  
  Funckionalna zavisnost X->A je **POTPUNA** ako ne postoji podskup od X koji isto odredjuje A
  
</details> <br>

# Druga normalna forma 

<details>
  <summary> Definicija 2nf </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/98717036-d45a1880-238c-11eb-8c75-0c0211ccfd71.png)

  
</details>

<details>
  
  <summary> Primarna obelezja </summary> <br>

  - **PRIMARNA** obelezja su obelezja koja pripadaju bilo kom kljucu [mozemo imati vise kljuceva]
  - U literaturi se **primarna** obelezja oznacavaju sa skracenicom **KPR** . 

</details>

<details>
  <summary> Neprimarna obelezja </summary> <br>
  
  - **NEPRIMARNA** obelezja su ona obelezja koja ne pripadaju ni jednom kljucu
  - odnosno, ona obelezja koja se nalaze sa desne strane funkcionalne zavisnosti 
  
</details>

<details>
  <summary> Algoritam odredjivanja vazenja druge normalne forme </summary> <br>
  
### Tumacenje definicije

  - Nadjemo kljuceve i posmatramo sva obelezja koja postoje u kljucu, odnosno sva obelezja podelimo u  **PRIMARNA**(pripadaju barem jednom kljucu) i **NEPRIMARNA** (ne pripadaju ni jednom kljucu)
  - Potom uzmemo bilo koje neprimarno obelezje A ( ne pripada ni jednom kljucu) i uzmemo bilo koji kljuc X
  - Znamo da svaki kljuc sigurno funkcionalno odredjuje svako obelezje a samim tim i svako neprimarno obelezje,
  - Stoga, kljuc X sigurno odredjuje neprimarno obelezje A 
  - Ali ako posmatramo svaki moguci podskup od X-a, recimo podskup Y, znamo sigurno da ne vazi da podskup kljuca odredjuje A

### Ukratko

Iteriramo i proveravamo da li su sve funkcionalne zavisnosti **POTPUNE**, ako nadjemo neku koja nije znaci ne ispunjava uslov Druge normalne forme.
  
</details>

<details>
  <summary> Primer 1 </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/98703503-d9629c00-237b-11eb-9fb1-44dd916a5b56.png)

  - dve funkcionalne zavisnosti: BRI -> PRZ + IME + BPI, OZP -> NAP
  - primarna obelezja su: BRI, OZP
  - neprimarna obelezja su: svi ostali

![image](https://user-images.githubusercontent.com/45834270/98704339-d320ef80-237c-11eb-8bed-1f082b0fc0bf.png)

  - Mozemo primetiti nepotpunu funkcionalnu zavisnost BRI + OZP -> NAP jer podskup skupa BRI + OZP je recimo OZP za kojeg vazi da odredju NAP 
  - Zbog ove nepotpune funkcionalne zavisnosti, mozemo reci da ova sema relacije nije u drugoj normalnoj formi 
  
</details>

<details>
  <summary> Primer 2 </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/98706787-8ee31e80-237f-11eb-91fa-731b5c34c0fd.png)

![image](https://user-images.githubusercontent.com/45834270/98706859-a3bfb200-237f-11eb-8996-efc6b8735df9.png)

 
</details>

<details>
  <summary> Napomena </summary> <br>
  
  - Kada bismo uzeli **svaku funkcionalnu zavisnost** koja postoji u semi relacije ona bi **morala** da bude **POTPUNA** ( od kljuca ka nekom neprimarnom obelezju ). 
  - Ako **nemamo ni jednu funkcionalnu zavisnost** onda je normalna forma **ZADOVOLJENA**
  - Ako imamo situaciju da svaki kljuc ima samo **jedno obelezje**, znamo odma da je druga normalna forma **ZADOVOLJENA**, jer svaki kljuc ce odredjivati svako neprimarno obelezje, a ne postoje podskupovi kljuca, msm jedini podskup kljuca bi bio *prazna skup*
  
</details>

<details>
  <summary> Resavanje zadataka sa normalnim formama </summary> <br>

### Generalno resavanje zadataka sa nf

  - iz seme relacije izvlacimo funkcionalne zavisnosti koje unutra postoje, pa imamo semu relacije, obelezja i funkcionalne zavisnosti 
  - prvo **nadjemo kljuc**
  - **razvajamo primarna i neprimarna obelezja**
  - gledamo koju normalnu formu proveravamo, ako je recimo u drugoj normalnoj formi, moramo dati argumentaciju zasto je u drugoj normalnoj formi
    - U 2nf je jer ne postoje funkcionalne zavisnosti 
    - U 2nf je jer je kljuc prost i ne postoje potskupovi kljuca(a samim tim nije moguce da postoji nepotupna fz)
    - Nije u 2nf ako nadjemo kontra primer zbog kog nije u 2nf
    - U 2nf je jer smo proverili svaki moguci podskup svakog kljuca ka svakom neprimarnom obelezju i sve fz kljuca ka neprimarnom obelezju su potpune
    
</details>

<details>
  <summary> Ceste greske u 2nf </summary> <br>
  
  - Kolege krenu da proveravaju pravila za sva obelezja, dok kod 2nf se kaze da se pravilo odnosi samo na **NEPRIMARNA** obelezja sa desne strane funkcionalnih zavisnosti
  
</details> <br>
  
# Treca normalna forma 

<details>
  <summary> Definicija tranzitivnosti </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/98717624-99a4b000-238d-11eb-9a70-d3736686416c.png)

### Tumacenje

  - X->A nije tranzitivno ukoliko ne postoji bar jedna od dve grane (X-> Y grana i Y->A grana) ili ukoliko postoji grana Y->X
  
</details>

<details>
  <summary> Definicija 3nf </summary> <br>
  
### Definicija

![image](https://user-images.githubusercontent.com/45834270/98718216-6e6e9080-238e-11eb-92c3-ca73cfbd09c3.png)

### Tumacenje definicije
  - samo za **NEPRIMARNA** obelezja koja ne pripadaju ni jednom kljucu(nalaze se sa desne strane funkcionalne zavisnosti), kada uzmemo bilo koji kljuc, sada ce kljuc sigurno odredjivati to obelezje (znaci sigurno vazi X->A)
  - ukoliko postoji neko Y, tako da Y->A nije trivijalna fz (posto je X kljuc, X ce sigurno odredjivati i Y) onda sigurno mora vaziti da Y odredjuje X (tada je Y neki nadskup kljuca) 
  
</details>

<details>
  <summary> Algoritam odredjivanja vazenja trece normalne forme  </summary> <br>
  
Najlakse se proverava na sledeci nacin:

  - posmatramo sve funckionalne zavisnosti koje imamo  u skupu
  - gledamo da li se desava situacija da je negde sa desne strane neko neprimarno obelezje a sa leve strane nesto sto 
funkcionalno ne odredjuje ni jedan kljuc
  - ako imamo tu situaciju to definitivno znaci da imamo neku tranzitivnu FZ od kljuca ka nekom neprimarnom obelezju

</details>

<details>
  <summary> Primer 1 </summary> <br>

![image](https://user-images.githubusercontent.com/45834270/98723485-bc859300-2392-11eb-9385-f1d933efe99c.png)

  - kljuc seme je: OZN 
  - posto kljuc ima jedno obelezje, zakljucujemo da su sva **neprimarna** obelezja u **potpunoj** fz u odnosu na svaki kljuc (zbog toga je zadovoljena 2nf)
  - a posto postoji **tranzitivna fz** od **kljuca** do **neprimarnog** obelezja, srusili smo 3nf, jer da bi srusili 3nf, dovoljno je samo jedan kontra primer (bas kao ovaj) koji pokazuje **tranzitivnost** od **kljuca** ka **neprimarnom** obelezju

</details>

<details>
  <summary> Napomena </summary> <br>

  - Za 3nf nemamo neku precicu kao kod 2nf gde cim vidimo da kljuc ima jedno obelezje mi zakljucujemo da su sva **neprimarna** obelezja u **potpunoj** fz u odnosu na svaki kljuc
  - Najbolje za 3nf je da nadjemo *kontra primer* koji pokazuje **tranzitivnost** od **kljuca** ka **neprimarnom** obelezju i kazemo da zbog tog kontra primera, 3nf nije zadovoljena 
  - Ako imamo situaciju da nemamo neprimarna obelezja, samim tim nemamo tranzitivnost iz kljuca u neprimarno obelezje jer ga nema, te zakljucujemo da ako **nemamo neprimarno obelezje**, **zadovoljena** je 3nf
  - Ako imamo situaciju da **ne postoje funkcionalne zavisnosti**(trivijalne ne gledamo) onda je sigurno **zadovoljena** 3nf

</details> <br>

# Bojs Kodova normalna forma - BCNF

<details> 
  <summary> Definicija BCNF </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/98741568-2dd23f80-23ad-11eb-8546-78e05a493934.png)

### Tumacenje definicije

  - uzmemo **bilo koji** atribut
  - posmatramo **bilo koji** skup obelezja Y, tako da Y ne sadrzi A
  - u koliko postoji neka ne trivijalna fz Y->A onda postoji neki kljuc koji je podskup leve strane(podskup Y-a)

U zavisnosti od 3nf, BCNF je strozija bas zbog toga sto je rec o **bilo kom atributu** a ne samo o **neprimarnom atributu**
  
</details>

<details>
  
  <summary> Algoritam odredjivanja vazenja Bojs kodove normalne forme </summary> <br>
  
  - Svaka netrivijalna FZ **bilo kog atributa** mora da sadrzi kljuc sa leve strane

</details>

<details>
  <summary> Primer 1 </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/98748945-04b8ab80-23bb-11eb-8b6c-05afc1820a09.png)

</details>

<details>
  <summary> Primer 2 </summary><br>
  
![image](https://user-images.githubusercontent.com/45834270/98749286-97f1e100-23bb-11eb-9d3f-947caed63861.png)
</details>

<details>
  <summary> Napomena </summary> <br>
  
  - iteriramo kroz svaku fz, i svaka od njih sa leve strane mora da ima bar jedan **CITAV** kljuc(tipa ako je kljuc AC, a imamo fz A->D, bcnf nije zadovoljena jer sa leve strane ove fz se ne nalazi **CITAV** kljuc nego samo njegov deo, tj A)
  
</details>

<br>


# Sve normalne forme

<details>
  <summary> Algoritam za rad sa normalnim formama </summary> <br>
  
  - [0 korak]: Nadjemo kljuceve i posmatramo sva obelezja koja postoje u kljucu, odnosno sva obelezja podelimo u  **PRIMARNA**(pripadaju barem jednom kljucu) i **NEPRIMARNA** (ne pripadaju ni jednom kljucu)
  - [1 korak]:
  - [2 korak]:
  - [3 korak]:
  
</details>
  
<details>
  <summary> Za sve normalne forme vazi </summary> <br>
  
  - **Sema BP** (CELA BAZA PODATAKA) je u nekoj od normalnih formi ako su **sve seme relacija** u nekoj od normalnih formi. 
  - Ako posmatramo 'redosled' normalnih formi [1nf, 2nf, 3nf, bcnf, 4nf, ...] znamo da ako vazi recimo 3nf, mora da vazi 1nf i 2nf, odnosno ako vazi jedna normalna forma, sve one pre nje moraju da vaze
   moze
     
</details> <br>

## Vezbanje

<details>
  <summary> Primer 1 </summary> <br>
  
#### Zadatak

![image](https://user-images.githubusercontent.com/45834270/98749985-29158780-23bd-11eb-9a5f-17b80bcfeb70.png)


#### Resenje

![image](https://user-images.githubusercontent.com/45834270/98750002-33378600-23bd-11eb-9af5-de34b3c63190.png)

  - nije u 2nf jer podskup kljuca moze da izvede neko neprimarno obelezje, npr BRI -> IME
  - nije u 3nf jer imamo tranzitivnost kljuca ka neprimarnom obelezju, npr BRI -> NAZSMER
  - posto je palo vec na 2nf, nije ni bilo potrebe ispitivati 3nf ( to je bilo cisto iz edukativne potrebe)
  - a ostaje nam jedino 1nf, za koju uvek **predpostavljamo da vazi**
  
</details>

<details>
  <summary> Primer 2 </summary> <br>

#### Pitanje

U kojoj je normalnoj formi baza ?

#### Odgovor

Posto se baza sastoji od vise sema, gledamo koja je *najlosija* nf koju sve seme zadovoljavaju. Ako imamo 3 seme koje su u bcnf i jedna u 2nf, nasa baza je u 2nf.

</details>

<details>
  <summary> Primer 3 </summary> <br>

![image](https://user-images.githubusercontent.com/45834270/98754927-eb6a2c00-23c7-11eb-988d-ce671b2007b6.png)

</details>

<details>
  <summary> Primer 4 </summary> <br>

  - fora kada **NEMAMO NEPRIMARNA OBELEZJA**
  - primetili smo da imamo 2 kljuca
  - svako od obelezja se nalazi unutar jednog od kljuceva 
  - to znaci da nemamo neprimarna obelezja 
  - u tom slucaju automatski znaci da 2nf i 3nf vaze 

![image](https://user-images.githubusercontent.com/45834270/98755051-1fdde800-23c8-11eb-98f1-064b2234ef31.png)       

</details>

<br>

## Podsetnik

<details>
  <summary> Odredjivanje svih fz u semi relacije </summary> <br>
  
Npr. da bi odredili koje sve fz postoje u semama relacije na slici ispod:
  - pogledamo polazni skup funkcionalnih zavisnosti F
  - onda uradimo njegovu [projekciju](https://github.com/FTN-E2-materials/BazePodataka2/tree/main/baze2%5B20-21%5D/vezbe/v2) po skupu obelezja seme relacije (Student i Prijava u nasem primeru)
  - tada dobijamo skup funkcionalnih zavisnosti koji vazi unutar te male seme relacije 

![image](https://user-images.githubusercontent.com/45834270/98753326-5a458600-23c4-11eb-9433-a050ec1b1ee2.png)

  
</details>

<br>

## Beleske

Poslednji primer i po formi i po tezini odgovoara nekom tezem zadataku koji moze da dodje na kolokvijumu. 





















