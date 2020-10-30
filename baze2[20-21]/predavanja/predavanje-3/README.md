<!-- Summary snippet

<details>
 <summary> Name of Summary </summary> 
  
Some snippet of text
 
</details>


-->


# Nastavak sa predavanja-1

### Zavisnost spoja

![image](https://user-images.githubusercontent.com/45834270/97297208-f95d7000-1851-11eb-9d8e-5de483c7c83d.png)



# Novo gradivo

## Osnovni projektantski kriterijumi

 - **K1**: Ne smemo gubiti i dobijati obelezja 'usput'. Obelezja ce postojati i gubiti se, ali u **postupku projektovanja** to ne sme da se dogodi. Sto znaci da projektant sme da zada drugaciji ulaz ali algoritam sam po sebi ne sme biti falican, odnosno, unutar njega se ne smeju menjati obelezja. Tacnije ako je na ulazu jedan skup obelezja i na izlazi mora biti isti skup obelezja.
 
 - **K2**: Prirodnim spojem svih nasih relacija nase relacione baze podataka zelimo da nadoknadimo tacno nasu polaznu univerzalnu relaciju a to u zivotu i nije bas moguce. Ovo je jedan idealizovan kriterijum o kome cemo takodje brinuti.
 
 - **K3**: Onako kako smo ocuvavali nas polazni skup obelezja, tako smo i u obavezi da ocuvamo nas polazni skup ogranicenja. Nasa Sema BP (S, I) u S sadrzi skup sema relacija a u I sadrzi skup medjurelacionih ogranicenja. To znaci da ce nas postupak projektovanja relacione seme baze podataka transformisati nas polazni skup ogranicenja na nacin da nas dovede do lokalnih ogranicenja svih nasih sema relacija to su skupovi Oi, ako svaku semu relacije posmatramo (Ri, Oi) gde je Oi njen skup ogranicenja, onda kada uniramo sva ogranicenja iz lokalnih skupova ogranicenja nasih sema relacija i kada tome pridodamo(uniramo) i nas skup medjurelacionih ogranicenaj I, mi moramo u logickom smislu ocuvati ekvivaletnost sa nasim polaznim skupom ogranicenja.
 ![image](https://user-images.githubusercontent.com/45834270/97714732-d2a57080-1ac1-11eb-83d6-2f2bce5d426d.png) 
 Ocuvati medjusobnu ekvivalentnost znaci samo da sve sto moze da se izvede iz jednog skupa ogranicenja moze da se izvede onda iz drugog i obratno( sve sto moze iz drugog da se izvede onda moze i iz prvog).

- **K4**: Sve anomalije azuriranja trebaju biti uklonjene

### Napomena

Sva cetri kriterijuma u praksi nisu uvek zadovoljena

## Spojivost bez gubitaka

Kada uzmemo jednu relaciju nad nekim skupom obelezja i napravimo projekciju nad jednim podskupom i projekciju nad drugim podskupom(unija ta dva podskupa je orginalni skup), njihov prirodni spoj treba da vrati celu univerzalnu realciju. Ako se to desilo i ako nemamo visak torki, onda imamo **spojivost bez gubitaka**.


