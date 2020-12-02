# Metoda dekompozicije

<details>
  <summary> Postupak </summary> <br>
  
Postupak je iterativan, zapocinje pravljenjem stabla i pocinje od korena stabla koji je za nas univerzalna sema relacije. **Uslov iteracije** je:
  - proveravamo za nas cvor da li **zadovoljava ciljnu normalnu formu**
  - ako **zadovoljava** -> **postupak zavrsen**
  - ako **ne zadovoljava** -> **postupak se iterativno nastavlja**
  - tako sto **biramo neku fz** po kojoj vrsimo **dekompoziciju** cvora

Postupak se **zavrsava** kada su svi listovi u stablu takvi da **zadovoljavaju zeljeni uslov normalne forme**.

<details>
  <summary> Korak rastavljanja pri dekompoziciji </summary><br>

![image](https://user-images.githubusercontent.com/45834270/100919436-154fd380-34da-11eb-9c64-ff91c5be0c71.png)

</details>
  
</details>

<details>
  <summary> Zadovoljenje spojivosti bez gubitaka </summary>  <br>

Skup sema relacija (listova) ce zadovoljavati spojivost bez gubitaka onda kada **kljuc univerzalne seme relacije** bude **sadrzan** barem u jednoj od tih semi relacije.
</details>

<details>
  <summary> Kriterijumi po kom vrsimo dekompoziciju </summary><br>
  
<details>
  <summary> Slajd </summary><br>

![image](https://user-images.githubusercontent.com/45834270/100921534-fb63c000-34dc-11eb-9a9c-1667beb76673.png)
</details>

Voditi racuna da **ne gubimo** funkcionalne zavisnosti. (B iz slajda) Za svaku drugu fz(ne gledamo X->Y fz) W->V takvu da je zatvarac od X-a razlicit od zatvaraca od W onda ne sme da vazi X->W. Odnosno, ako X odredi Y, fora je da Y dalje ne odredjuje nista, tj. da X odredjuje Y i nema dalje, to znaci "**na kraju lanca izvodjenja**"
  
</details>

<details>
  <summary> Strategije izbora fz X->Y </summary><br>
  
<details>
  <summary> Slajd </summary><br>
   
![image](https://user-images.githubusercontent.com/45834270/100929464-f6583e00-34e7-11eb-8752-f18524d3f894.png)
</details>
  
</details>
  
