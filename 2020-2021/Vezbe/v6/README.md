## Prevodjenje ER-a u relacioni model

<details>
  <summary> Pravila </summary> <br>
  
  - **Tip entiteta** se prevodi da bude **sema relacije**
  - Poveznik **n** naprema **1** se prevodi **prenosenjem kljuceva**
  - Kao rezultat zelimo skup sema relacija i skup ogranicenja
  - Bitno je ispisati sve seme relacija i sva medjurelaciona ogranicenja, ne treba obrazlozavati nista, redosled prevodjenja nije bitan 
  - Treba znati prevesti tipove entiteta, tipove poveznika sa svim mogucim kombinacijama kardinaliteta, gerundi, rekurzivni tipovi poveznika, isa hijerarhija, identifikacione zavisnosti. Trebamo znati **pravila za prevodjenje** ovoga.
  - Na testu dobijemo jedan ER dijagram i njega prevodimo.

  
</details>

<details>
  <summary> Zadatak 1 </summary> <br>
  
![image](https://user-images.githubusercontent.com/45834270/103576924-2a05f980-4ed4-11eb-9653-3f0ee367022e.png)

### Kako prevesti?
- Ne treba krenuti od tipova poveznika 
- Dobar savet je krenuti od tipova entiteta koji ka sebi nemaju tipove poveznika sa max kardinalitetom 1 (zato sto se 1 naprema n prevodi prenosenjem kljuceva a u tom trenutku ne znamo taj kljuc)
- Znaci krenuti od **tipa entiteta** takvog da su mu **svi poveznici maximalnog kardinaliteta N** (nema prenesenih kljuceva)

![image](https://user-images.githubusercontent.com/45834270/103577268-c29c7980-4ed4-11eb-83df-51ca834aebb7.png)

- Ako krenemo recimo od poveznika P_Y, potreban nam je kljuc i od P_X i od T_D, a nema smisla od njega da krenemo pa da racunamo i 10 drugih kljuceva ...
  
  
<br>
  
<details>
  <summary> Prenosenje kljuca </summary> <br>
  
<br>

  - Kada imamo situaciju 1-N, to se prevodi prenosenjem kljuceva.
  - U nasem primeru u T_A bi morali da prenesemo kljuc i od T_C, posto treba da znamo kljuc od T_C da bi preveli T_A, onda bas i nije dobro krenuti od T_A
  
![image](https://user-images.githubusercontent.com/45834270/103580519-a13e8c00-4eda-11eb-9ba8-e34eb269b1f6.png)

<br>
  
</details>
  

<br>
  
  - Za svaki tip entiteta se formira sema relacije pa tako i za T_C, prepisujemo sva obelezja vezana za njega, nema maksimalnih kardinaliteta 1 pa nema prenosenja kljuca, c1 podvuceno znaci c1 je primarni kljuc
- Ako imamo vise obelezja podvuceno, primarni kljuc je kompozitni kljuc sastavljen od svih podvucenih obelezja(ovo je vise napomena za projekat nego za kolokvijum 3 )

![image](https://user-images.githubusercontent.com/45834270/103581562-8b31cb00-4edc-11eb-9741-ccff10d724e2.png)


  - Kada prevodimo tip entiteta sa poveznikom ciji je maksimalni kardinalitet 1, to znaci da prevodimo tip poveznika ( u ovom primeru P_Q ) **prenosenjem kljuca N strane**, pored toga jos prenosimo u T_A i **obelezja iz poveznika** P_Q:

![image](https://user-images.githubusercontent.com/45834270/103582109-81f52e00-4edd-11eb-8cfb-24fcd9b8e3a2.png)

  - Necemo napisati c1 posto imamo dva tipa poveznika izmedju dva ista tipa eniteta, pa cemo zapisati c11 ( svako obelezje mora imati jedinstven naziv) 
  
  - c1 ne utice na kljuc kod T_A iz razloga sto imamo obican tip poveznika, kod indentifikacione zavinosti bi imalo uticaja

![image](https://user-images.githubusercontent.com/45834270/103582956-275cd180-4edf-11eb-911e-0940d05d54d7.png)

  - posto smo preneli kljuc moramo uvesti ogranicenje referencijalnog integriteta, svaki preneseni kljuc rezultuje jednim ogranicenjem referencijalnog integriteta, posto smo preneli samo jedan kljuc imamo jedno ogranicenje, da smo preneli 10 kljuceva imali bi 10 ogranicenja referencijalnog integriteta 

![image](https://user-images.githubusercontent.com/45834270/103583155-8884a500-4edf-11eb-8f91-57af8c9ad6ea.png)
  
  - Ono nam kaze da obelezje c11 iz T_A referencira vrednosti od obelezja c1 iz T_C. 
  
<br>
  
  - sledeci korak je da uvedemo **ogranicenja**  rezultovana **minimalnim kardinalitetom**

![image](https://user-images.githubusercontent.com/45834270/103583632-56277780-4ee0-11eb-9e81-a4002931ebb8.png)

  - zbog minimalnog kardinaliteta 1 u T_A sigurno moramo upisati vrednost za obelezje C11, tj u semi relacije T_A obelezje C11 ne sme da ima Null vrednost. 
  - ***PAZI***, ovo pravilo vazi zato sto nam je i maksimalni kardinalitet 1, da je max kardinalitet N pisalo bi se drugacije ogranicenje.
  - ***OVO VAZI SAMO ZA (1,1)!!!*** 
  - Minimalni kardinaliteti 0 ne izazivaju ogranicenja, ne moramo nista dodatno da pisemo.
  
<br>

- Sledeci korak je da prevedemo P_W, zbog maximalnih kardinaliteta N, N mi ga prevodimo kao **posebnu semu realcije**

![image](https://user-images.githubusercontent.com/45834270/103584437-9affde00-4ee1-11eb-93ea-27eacfa0fad7.png)

  - U semi relacije P_W imamo obelezja koja su preneseni kljucevi povezanih tipova entiteta, tj A1 i C1 i imamo W1 koje je povezano sa P_W, a kljuc dobijemo kao uniju kljuceva povezanih entiteta i dobijamo jedan kompozitni kljuc A1+C1

![image](https://user-images.githubusercontent.com/45834270/103584482-b23ecb80-4ee1-11eb-9041-094e76d540f6.png)

  - Nakon toga treba da dodamo ogranicenja referencijalnog integriteta, obratiti paznju ovde imamo dva prenesena kljuca to znaci imamo dva ogranicenja.

![image](https://user-images.githubusercontent.com/45834270/103584531-caaee600-4ee1-11eb-92d3-8471c8acf842.png)


  - Nakon toga proveravamo minimalne kardinalitete, sa strane T_C je nula to ignorisemo, sa strane T_A minimalni kardinalitet je 1 sto znaci da svaka pojav	a T_A mora da ucestvuje barem u jednoj pojavi P_W, zbog tog minimalnog kardinaliteta pisemo ogranicenje **INVERZNOG REFERENCIJALNOG INTEGRITETA** tj: 

![image](https://user-images.githubusercontent.com/45834270/103584569-ddc1b600-4ee1-11eb-949e-0a57bec775dd.png)

  - Bitno je napomenuti da ovo ogranicenje pisemo zato sto je **min kardinalitet 1 a max kardinalitet N** (zbog toga pisemo ovo ogranicenje, a ne not NULL ogranicenje). Ovo ogranicenje kaze da svaka vrednost unesena u T_A mora biti unesena i u P_W

<br>

  - Sada prevodimo ISA hijerarhiju iz razloga sto nam za sve ostalo trebaju kljucevi zbog minimalnih kardinaliteta 1
  - Kod prevodjenja ISA hijerarhije postoje 4 nacina, mi koristimo nacin da za **super klasu** napravimo **jednu semu relacije**, i za **svaku podklasu** pravimo **pojedinacnu semu relacije**, taj nacin je najlaksi i najlogicniji i uvodimo najmanje ogranicenja.
  - Savet za kolokvijum, kada krenemo da prevodimo ISU nemoj da prevedemo samo superklasu, nego vec kad smo se dotakli treba da prevedemo kompletno celu ISU sa podklasama. Da ne bi zaboravili neke uslove itd… 
  - Prvo prevedemo nadklasu i za nju uvdemo novu semu relacije, nemamo vezu gde je max kardinalitet 1 pa ne dodajemo nikakva druga obelezja. 

![image](https://user-images.githubusercontent.com/45834270/103586458-6beb6b80-4ee5-11eb-9161-5e3e257d0b27.png)

  - Svaku od podklasa prevedemo kao novu semu relacije. Kada prevodimo na ovaj nacin, sema relacije neke podklase mora da sadrzi i kljuc nadklase, pa pisemo i obelezje B1, **kljuc podklase je uvek preneseni kljuc iz nadklase**, jedna opcija za kljuc iz tog razloga je B1 a ekvivalentni kljuc je B11(za T_B1).

![image](https://user-images.githubusercontent.com/45834270/103586621-bff65000-4ee5-11eb-93fe-f2be197078fe.png)

<br>

  - sledeci korak je da uvedemo ogranicenja referencijalnog integriteta, preneseni kljuc nebitno zbog cega je nastao izaziva ogranicenja referencijalnog integriteta

![image](https://user-images.githubusercontent.com/45834270/103587731-3005d580-4ee8-11eb-9552-3c4794d53425.png)

  - Sada treba videti ogranicenja koja nastaju zbog kardinaliteta ISA hijerarhije, *minimalni kardinalitet* ISA hijerarhije moze biti nula ili 1 , *nula* je nesto sto smo zvali *nepotpuna ISA hijerarhija*, to znaci da mozemo pronaci osobu u sistemu koja nije student ni radnik a jeste osoba. 

![image](https://user-images.githubusercontent.com/45834270/103588041-b6221c00-4ee8-11eb-8238-6f758fc2efa6.png)

  - Minimalni kardinalitet 0 ne uvodi nikakvo novo ogranicenje, ali ako je minimalni kardinalitet 1 uvodi ogranicenje da je svaka pojava nadklase takodje i pojava neke od podklasa, to pisemo na sledeci nacin: 

![image](https://user-images.githubusercontent.com/45834270/103588094-cdf9a000-4ee8-11eb-9877-c5a18e36dcfd.png)

<br>

  - Posle toga nam preostaje da vidimo da li maksimalni kardinalitet uvodi neko ogranicenje. Ako je N kao u ovom primeru ne pisemo nista. Ako bi pisalo 1 za maksimalni kardinalitet **moramo pisati ogranicenje sa presekom**, u primeru sa studentom to bi izgeldalo ovako: 

![image](https://user-images.githubusercontent.com/45834270/103588291-2af55600-4ee9-11eb-8ac0-148127b9a0d7.png)

  - U ovom primeru zbog N max kardinalitet znaci nemamo dodatna ogranicenja.
  
  - Sada prevodimo P_X, posto su kardinaliteti N N prevodimo ga kao posebnu semu relacije. Da smo imali ka gerundu neki poveznik sa max kardinalitetom 1 morali bi da dodamo nova obelezja, ali u ovom slucaju svi max kardinaliteti su 1 pa nemamo taj slucaj.

![image](https://user-images.githubusercontent.com/45834270/103588367-54ae7d00-4ee9-11eb-8902-2f0bc7b1051c.png)

  - Ogranicenja referencijalnog integriteta se jos zovu i strani kljucevi.
  - T_D prevodimo: 
  
![image](https://user-images.githubusercontent.com/45834270/103588412-6b54d400-4ee9-11eb-84fa-f80a951859e5.png)

  - Prevodimo sada rekurzivni tip poveznika a gerund ostavljamo za kraj
  - P_D ima max kardinalitete N N pa to znaci da i za njega pravimo novu semu relacije, prenosimo kljuceve svih povezanih tipova entiteta, za jednu granu nam treba kljuc od T_D a takodje za drugu granu nam isto treba kljud od T_D, posto skup obelezja mora da ima jedinstvene vrednosti mi preimenujemo je D1 u D11, kljuc je kao kod svakog N N unija kljuceva povezanih

![image](https://user-images.githubusercontent.com/45834270/103588468-87f10c00-4ee9-11eb-89ca-144f7e8c9428.png)

  - Sada prevodimo P_Y:

![image](https://user-images.githubusercontent.com/45834270/103588507-a0612680-4ee9-11eb-9407-eb0958d1392e.png)

**OBRATITI PAZNJU!** Kod gerunda cemo dobijati ovako slozenije kljuceve:

![image](https://user-images.githubusercontent.com/45834270/103588548-b969d780-4ee9-11eb-8e22-2f8e22f74adc.png)

**OBRATITI I OVDE PAZNJU!** Ogranicenja se ne pisu na osnovu broja obelezja vec na onovu prenesenih kljuceva:

![image](https://user-images.githubusercontent.com/45834270/103588599-d4d4e280-4ee9-11eb-9351-b8110b58a25c.png)


</details>

<details>
  <summary> Zadatak 2 </summary> <br>
  
## Prevodjenje identifikacione zavisnosti 

![image](https://user-images.githubusercontent.com/45834270/103590554-73fbd900-4eee-11eb-9e70-87925a0e13c4.png)

  - Ako na testu ne pise kardinalitet (1,1) mi moramo da znamo koji je kardinalitet kod identifikacione zavisnosti, tj uvek je (1,1)
  - Posto je maksimalni kardinalitet 1 prenosimo kljuc tj u ovom primeru A1.
  - Kod skupa kljuceva imamo definiciju koja kaze da se kod slabog tipa entiteta ukljucuje kljuc jakog tipa entiteta.
  - Posto smo preneli kljuc pisemo standardno ogranicenje referencijalnog integriteta.
  - Zbog minimalnog kardinaliteta 1 pisemo null ogranicenje.

![image](https://user-images.githubusercontent.com/45834270/103590642-ad344900-4eee-11eb-9c4d-24aecb1ca77b.png)


</details>


