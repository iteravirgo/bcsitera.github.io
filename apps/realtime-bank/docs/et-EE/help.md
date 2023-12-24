---
---
# Reaalaja pank - Kasutusjuhend
## Sisukord

- [Seadistused](#seadistused)
- [Sissetulevad pangasõnumid](#sissetulevad-pangasõnumid)
- [Pangatehingute töötlemine](#pangatehingute-töötlemine)

## Seadistused

### Pangaühenduste seadistused

Võimalik on seadistada pangaühendused järgmiste pankadega:
1. Swedbank Gateway
2. SEB Baltic Gateway
3. LHV Connect
4. Coop Pank Gateway

Liitumisjuhiseid leiab [siit](join.md).

Pangaühenduste seadistamiseks on Business Centralis igal panga kohta oma kaart, kus tuleb täita järgmised väljad:

Väli |  Selgitus | 
-- | --
Teenuse URL | Sisestage panga teenuse aadress: <br> Swedbank - https://swedbankgateway.net/ <br> SEB - https://api.bgw.baltics.sebgroup.com/ <br> LHV - https://connect.lhv.eu/ <br> Coop Pank - https://cpgw.cooppank.ee/  
Seadme- või autentimissertifikaadi failinimi | Importige sertifikaadi fail (pfx/p12 formaat). Sertifikaadi saate pangast.
Seadme- või autentimissertifikaadi parool | Sisestage sertifikaadi parool.
Krüpteermissertifikaat (Swedbank-i puhul) | Sertifikaadi saab laadida siit: http://dev.swedbankgateway.net/info#certificates

### Pangakonto seadistused
_Pangakonto_ kaardil saab määrata väljal "Pangaühendus" vastava seadistatud pangaühenduse.

### Reaalajas panga seadistused
Lehel _Reaalajas panga seadistus_ täitke ära väli "Konteeritud tehingute nr.", määrates vastava numbriseeria.


## Sissetulevad pangasõnumid

### Pangasõnumite automaatne import

_Pangaühenduse lehel_ on nupud "Võta uued pangasõnumid", mida saab kasutada pangasõnumite automaatseks impordiks. 
Vajutades nupule "Tööjärjekorra kanded", avatakse leht _Tööjärjekorra kanded_, kus on võimalik seadistada 4 erinevat tegevust: pangasõnumite import, sissetulevate pangasõnumite töötlemine, pangakonto tehingute sidumine, pangakonto tehingute konteerimine. 

Imporditud pangasõnumid kuvatakse lehel _Sissetulevad pangasõnumid_. Vaikimisi on lehel filtrid: Allikas ja Olek, kuvatakse ainult kirjed, mis on töötlemata ning vajavad tähelepanu - s.t. Olek on kas _Vastuvõetud_ või _Tõrge_.  
Kõikide sõnumite nägemiseks vajutage nupule "Näita kõiki sõnumeid".


### Pangasõnumite käsitsi import

Käsitsi on pangasõnumeid võimalik importida lehel _Sissetulevad pangasõnumid_ vajutades nupule "Impordi failist". Imporditud kirje Olek on _Vastuvõetud_.
Imporditud kirje töötlemiseks vajutage nupule "Töötle".
Kirje nägemiseks vajutage nupule "Näita kõiki sõnumeid", kirjel on nüüd Olek _Töödeldud_. Paremal olevas kiirinfos on näha _Salvestatud tehingute arv_.
Sellele numbrile vajutades on võimalik liikuda lehele _Pangakonto tehingud_.


## Pangatehingute töötlemine

### Pangatehingud

Pangakonto kaardil on uus väli "Saldo pangas". Selles summas kajastuvad kõik pangast imporditud tehingud, ka need, mis on veel töötlemata ning konteerimata. Seetõttu võib väljal "Saldo pangas" olev summa erineva väljal "Saldo" kuvatavast summast. 
Väljal "Saldo pangas" summale vajutades avatakse leht _Pangakonto tehingud_.
Vaikimisi kuvatakse need pangatehingud, mis on konteerimata, mida kasutaja saab üle vaadata, siduda ja konteerida.

### Teenustasude sidumine

Teenustasude ja teiste fikseeritud kontode sidumiseks on võimalik kasutada _Tekst-kontoks vastendamine_ funktsionaalsust.

### Arvete sidumine

Arvetega sidumist saab lehel _Pangakonto tehingud_ teha kas automaatselt või käsitsi. 

Automaatseks sidumiseks käivitage protsess _Seo automaatselt_.  

Kasutajal on võimalik näha, missuguse arvega on pangatehing seotud, klikkides väljal "Seotud summa". Kasutajal on võimalik siduda arve ringi. 
Juhul, kui kogu summat ei olnud võimalik arvetega siduda, siis väljal "Seotud summa" erineb väljal "Summa" näidatud summast.

Käsitsi sidumise korral valige real _Seotud konto nr._ ja seejärel vajutage "Seo käsitsi". Avatakse vastava kliendi/hankija andmiku kanded, kus kasutaja on võimalik valida õige arve ja siduda pangatehing vajutades Protsess ->Märgi seose ID.


### Konteerimine

Seotud pangatehingud on võimalik konteerida, vajutades nupule "Konteeri".

Võimalik on seadistada Tööjärjekorra kanne, mis konteerib kõik pangatehingud, mille _Sidumise olek_ on "Kõrge täpsus".

---

### Kontaktinfo
Täpsema info saamiseks, palun võtke ühendust BCS Itera AS-ga:
<a href="https://www.itera.ee/" target="_blank">www.itera.ee</a>
