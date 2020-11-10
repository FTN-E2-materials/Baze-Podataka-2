# Prva normalna forma 

<details>
  
  <summary> Pretpostavka </summary>
  
  </br>

  - Predpostavljamo da uvek vazi
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
  <summary> Teorema </summary> <br>
  
  ![image](https://user-images.githubusercontent.com/45834270/98714921-c35bd800-2389-11eb-8b4c-22f47a164a9e.png)
  
</details>

<details>
  
  <summary> Primarna obelezja </summary> <br>

  - **PRIMARNA** obelezja su obelezja koja pripadaju bilo kom kljucu [mozemo imati vise kljuceva]
  - U literaturi se **primarna** obelezja oznacavaju sa skracenicom **KPR** . 

</details>

<details>
  <summary> Algoritam odredjivanja vazenja druge normalne forme </summary> <br>
  
### Tumacenje teoreme

  - Nadjemo kljuceve i posmatramo sva obelezja koja postoje u kljucu, odnosno sva obelezja podelimo u  **PRIMARNA**(pripadaju barem jednom kljucu) i **NEPRIMARNA** (ne pripadaju ni jednom kljucu)
  - Potom uzmemo bilo koje neprimarno obelezje A ( ne pripada ni jednom kljucu) i uzmemo bilo koji kljuc X
  - Znamo da svaki kljuc sigurno funkcionalno odredjuje svako obelezje a samim tim i svako ne primarno obelezje,
  - Stoga, kljuc X sigurno odredjuje neprimarno obelezje A 
  - Ali ako posmatramo svaki moguci podskup od X-a, recimo podskup Y, znamo sigurno da ne vazi da podskup kljuca odredjuje A

### Ukratko

Iteriramo i proveravamo da li su sve funkcionalne zavisnosti **POTPUNE**, ako nadjemo neku koja nije znaci ne ispunjava uslov Druge normalne forme.
  
</details> <br>

<details>
  <summary> Primer1 </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/98703503-d9629c00-237b-11eb-9fb1-44dd916a5b56.png)

  - dve funkcionalne zavisnosti: BRI -> PRZ + IME + BPI, OZP -> NAP
  - primarna obelezja su: BRI, OZP
  - neprimarna obelezja su: svi ostali

![image](https://user-images.githubusercontent.com/45834270/98704339-d320ef80-237c-11eb-8bed-1f082b0fc0bf.png)

  - Mozemo primetiti nepotpunu funkcionalnu zavisnost BRI + OZP -> NAP jer podskup skupa BRI + OZP je recimo OZP za kojeg vazi da odredju NAP 
  - Zbog ove nepotpune funkcionalne zavisnosti, mozemo reci da ova sema relacije nije u drugoj normalnoj formi 
  
</details>

<details>
  <summary> Primer2 </summary> <br>
  
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
  
  <summary> Algoritam odredjivanja vazenja trece normalne forme  </summary> <br>
  
Najlakse se proverava na sledeci nacin:

  - posmatramo sve funckionalne zavisnosti koje imamo  u skupu
  - gledamo da li se desava situacija da je negde sa desne strane neko neprimarno obelezje a sa leve strane nesto sto 
funkcionalno ne odredjuje ni jedan kljuc
  - ako immo tu situaciju to definitivno znaci da imamo neku tranzitivnu FZ od kljuca ka nekom neprimarnom obelezju

</details> <br>

# Bojs kodova normalna forma

<details>
  
  <summary> Algoritam odredjivanja vazenja Bojs kodove normalne forme </summary> <br>
  
Svaka netrivijalna FZ bilo kog atributa mora da sadrzi kljuc sa leve strane

</details> <br>

## Sve normalne forme

<details>
  <summary> Algoritam za rad sa normalnim formama </summary> <br>
  
  - [0 korak]: Nadjemo kljuceve i posmatramo sva obelezja koja postoje u kljucu, odnosno sva obelezja podelimo u  **PRIMARNA**(pripadaju barem jednom kljucu) i **NEPRIMARNA** (ne pripadaju ni jednom kljucu)
  - [1 korak]:
  - [2 korak]:
  - [3 korak]:
  
</details>
  
<details>
  <summary> Za sve normalne forme vazi </summary> <br>
  
**Sema BP** (CELA BAZA PODATAKA) je u nekoj od normalnih formi ako su **sve seme relacija** u nekoj od normalnih formi
     
</details>


## Beleske

Poslednji primer i po formi i po tezini odgovoara nekom tezem zadataku koji moze da dodje na kolokvijumu. Za drugi, trecu i bojskodovu normalnu formu obicno gledamo funkcionalne zavisnosti unutar seme relacije i onda posmatramo da li sve fz ispunjavaju neko pravilo, ako neka ne ispunjaava, onda odredjena normalna forma nije zadovoljena. A ako sve fz ispunjavaju neko pravilo onda kazemo da je ta normalna forma zadovljena.






















