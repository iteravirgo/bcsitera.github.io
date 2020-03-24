# Avaliku sektori finantsarvestuse lahendus
Avaliku sektori finantsarvestuse lahendus BC-s võimaldab järgmist:
- Riigi kontode haldust
- Riigi tehingupartnerite haldust
- Saldoandmike haldust
- Saldoandmiku esitamist XML failiga Saldoandmike infosüsteemis
<br><br>

## Seadistamine
### Dimensioonid
Lahendus kasutab saldoandmike loomiseks pearaamatu kannete dimensioone, seega on vaja luua dimensioonid järgmise info tarbeks:
 - Tehingupartner
 - Tegevusala
 - Allikas
 - Rahavoog
 <br><br>

### Riigi raamatupidamise seadistus
Sektsioonis **Dimensioonid** määratleme lahenduse toimimiseks vajalikud dimensioonid:

|Väli|Selgitus|
|---|---| 
| Tehingupartneri dimensiooni tähis | Dimensiooni tähis, mis vastab dimensioonile **Tehingupartner**. |
| Tegevusala dimensiooni tähis| Dimensiooni tähis, mis vastab dimensioonile **Tegevusala**. |
| Allika dimensiooni tähis | Dimensiooni tähis, mis vastab dimensioonile **Allikas**. |
| Rahavoo dimensiooni tähis | Dimensiooni tähis, mis vastab dimensioonile **Rahavoog**. |
| Tingimuslik rahavoo dimensiooni väärtus | Määrab rahavoogude dimensiooni väärtuse (tavaliselt **01**), mis käivitab saldoandmiku koostamisel tingimusliku rahavoogude loogika lähtuvalt Riigi kontoplaani määratlustest. |

Lisainfot võimalike dimensiooniväärtuste osas saab <a href="https://saldo.fin.ee/" target="_blank">Saldoandmike infosüsteemist</a>.
<br><br>

Sektsioonis **Üldine** määratletakse :

|Väli|Selgitus|
|---|---| 
| Riigi saldoandmiku numbrid | Määrab **saldoandmike** numbriseeria. Väärtuse saab valida **Numbriseeriate loendist**.|
| Tehingupartnerite numbrid | Määrab **tehingupartnerite** numbriseeria. Väärtuse saab valida **Numbriseeriate loendist**.|
| Ettevõtte tehingupartneri kood | Määrab **ettevõtte enda tehingupartneri kood**i, mida kasutatakse saldoandmiku XML failis. *(Kui sobivat väärtust ei ole valikus, siis tuleb vastav dimensiooniväärtus tehingupartneri dimensiooniväärtustesse lisada.)*|
| Ettevõtte tegevusala kood | Määrab **ettevõtte enda tegevusala kood**i. Siin määratud väärtus lisatakse automaatselt vastavale PR kontole, kus Tegevusala dimensioon on nõutud, vaikedimensiooni väärtuseks. *(Kui sobivat väärtust ei ole valikus, siis tuleb vastav dimensiooniväärtus tehingupartneri dimensiooniväärtustesse lisada.)*|

<br><br>

### Riigi kontod
Esmase installeerimise käigus täidab lahendus riigi kontode tabeli vaikeväärtustega.
Riigi kontode tabel koosneb kontodest, millel on number, nimetus ning vastavate dimensioonide kohustuslikkuse määratlused vaadeldava konto osas.
Tehingupartner ja/või Tegevusala dimensioon võivad olla **tingimuslikult kohustuslik**ud - st vastav dimensioon on ainult siis kohustuslik lisada, kui tehingu rahavoo dimensioon on ettemääratud väärtusega (tavaliselt 01).

Seadista järgnevad väljad parema kasutajakogemuse ning täpsema saldoandmiku saamiseks:

|Väli|Selgitus|
|---|---| 
| Konstantne TP dimensioon | Määrab konstantse tehingupartneri dimensiooni väärtuse riigi kontole. **Riigi kontole määratud väärtus prevalveerib pearaamatu kandel oleva väärtuse üle**. Kasutatakse tavaliselt maksu kontodel, sest maksude tehingupartner saab olla vaid üks (Maksu- ja Tolliamet). <br> ***Märkus!** Kui siin on tehingupartneri kood määratud, siis puudub vajadus vastaval PR kontol Tähis kohustuslik vaikedimensiooni määratlemiseks.*|
| Kasuta konstantset TP dimensiooni pangakonto kaardilt | Määrab **kas lahendus kasutab saldoandmiku loomisel pangakonto kaardil määratud konstantset riigi tehingupartneri dimensiooniväärtust** pearaamatu kandel oleva tehingupartneri dimensiooniväärtuse asemel. Kasutatakse tavaliselt Arvelduskontod pankades kontol. <br> ***Märkus!** Kasutades pangakonto kaardil Konstantne riigi TP dimensioon väärtust ei tohiks pangakontol tehingupartneri vaikedimensiooni kasutada, sest võivad tekkida dimensioonikonfliktid laekumiste/maksete sobitamisel.*|

Kasutaja saab taastada riigi kontode tabeli vaikeväärtused nupust "**Lähtesta riigi kontod**". <br>
**Hoiatus!** Lähtestamine kaotab kõik Kasutaja tehtud muudatused riigi kontodes.
<br><br>

### Kontoplaan
Igale PR kontole tuleb määrata vastav riigi konto number. *Väli on saadaval nii kontoplaanis, kui konto kaardil.*

Peale riigi konto lisamist kontrollib lahendus kohustuslike dimensioonide nõuet antud riigi konto osas. **Kui dimensioon on kohustuslik või tingimuslik, siis lahendus lisab riigi konto poolt nõutud vaikedimensioonide kohustuslikkuse** käesolevale PR kontole *(Väärtuse konteerimine määratluseks Tähis kohustuslik)*.<br>
***Märkus!** Kui Kasutaja hindab, et vastavale PR kontole ei tehta kunagi tehinguid rahavoo tingimusliku väärtusega (01), siis Kasutaja peaks eemaldama vastava PR konto vaikedimensioonidest "Tähis kohustuslik" nõude tehingupartneri ja/või tegevusala dimensiooni osas.*
<br><br>

### Riigi tehingupartnerid
Esmase seadistuse käigus peaks Kasutja looma tehingupartnerite loetelu.
Kasutaja saab **laadida alla tehingupartnerite XML fail**i Saldoandmike infosüsteemist nupuga "Lae alla partnerite XML".
Kasutaja saab importida/uuendada* tehingupartnerid XML failist nupuga "Impordi partnerid XML failist".<br>
****Märkus!** Kuna riigi poolt loodud tehingupartnerite XML failis puudub unikaalsuse tunnus, siis uuendamine õnnestub vaid kirjetega, milledel on olnud muutumatu kombinatsioon Kood + Nimetus + Kehtiv alates. Vastasel juhul luuakse uus kirje.*
<br><br>

### Kliendid/Hankijad
Iga **Kliendi/Hankija kaardile tuleb määrata vastav riigi tehingupartner**. *Seda saab teha sektisoonis Riigi raamatupidamise info.*
Kui tehingupartneri id valitakse, siis lahendus lisab vastava tehingupartneri koodi tehingupartneri dimensiooni üheks väärtuseks ning ühtlasi lisatakse tehingupartneri kood Kliendi/Hankija vaikedimensiooniks (Väärtuse konteerimine määratluseks Sama tähis).
<br><br>

### Pangakontod
Kasutaja peaks igale pangakontole **määratlema Konstantne riigi TP dimensioon väärtuse**. Seda saab teha pangakonto kaardil. *Nii toimides **puudub vajadus pangakontole vaikedimensiooni määramiseks**.*
Määratlust kasutatakse riigi saldoandmiku koostamisel, kui riigi kontoplaanis on märgitud väli "Kasuta konstantset pangakonto TP dimensiooni pangakonto kaardilt".<br>
***Märkus!** Kui väli Konstantne riigi TP dimensioon on kasutusel, siis tuleks vastavalt PR kontolt (leitav pangakonto konteeringurühma kaudu) eemaldada Tähis kohustuslik vaikedimensiooni nõue Tehingupartneri dimensiooni osas.*
<br><br>


## Kasutamine
### Pearaamatu kanded
Kontoplaanis määratud kohustuslikud vaikedimensioonid tuleb lisada igale PR kandele. Lisaks salvestatakse kandele riigi konto number. Vastava info abil loob lahendus riigile esitatava saldoandmiku.
<br><br>

### Riigi saldoandmikud
Uue saldoandmiku loomiseks tuleb Kasutajal määratleda aruandeperioodi aasta ning kuu (lõpu kuu). Saldoandmik arvutatakse kumuleeruvalt alates aruandeperioodi kalendriaasta algusest kuni lõpu kuu viimase päevani.
Saldoandmiku **ridade loomiseks tuleb Kasutajal vajutada nuppu "Arvuta read"**. *Read luuakse iga riigikonto tarbeks kombinatsioonis tehingupartner, tegevusala, allikas ning rahavoog.*

Kontrollimaks, millistest pearaamatu kannetest on saldoandmiku rida loodud tuleb kasutada nuppu "**Näita aluskandeid**" *(nupu leiab Ridadest, Halda nupu alt)*. Kõikide dimensioonidega kannete vaatamiseks tuleb avanenud pearaamatu kannetest vajutada Kanne -> PR Dimensiooni ülevaade ning seejärel juba Kuva maatriks.
<br><br>
Kui mõnel saldoandmiku real on ebatäpsed väärtused tänud ekslikult määratud dimensioonile, siis kannete korrigeerimiseks saab kasutada <a href="http://apps.itera.ee/apps/dimension-correction-tool/docs/et-EE/app.html" target="_blank">Dimensiooniparandaja</a> lahendust.
Peale paranduste tegemist kannetes, tuleb Kasutajal uuesti vajutada nuppu "Arvuta read", mis seejärel arvutab uuesti saldoandmiku read.
<br><br>
Vabastatud saldoandmiku korral saab nupust "**Loo XML fail**" luua ning salvestada saldoandmiku XML kujul, mille saab importida saldoandmiku infosüsteemi.

---

Täpsema info saamiseks, palun võtke ühendust BCS Itera AS-ga: <a href="https://www.itera.ee/" target="_blank">www.itera.ee</a>
