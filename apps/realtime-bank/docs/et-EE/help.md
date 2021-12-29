# Reaalaja pank - Kasutusjuhend
## Sisukord

- [Seadistused](#seadistused)
- [Sissetulevad pangasõnumid](#sissetulevad-pangasõnumid)
- [Pangatehingute töötlemine](#pangatehingute-töötlemine)

## Seadistused

### Pangaühenduste seadistused

Võimalik on seadistada pangaühendused järgmiste pankadega:
1. Swedbank Gateway (momendil ainult on-prem)
2. SEB Baltic Gateway
3. LHV Connect

Liitumisjuhiseid leiab [siit](join.md).

Pangaühenduste seadistamiseks on Business Centralis igal panga kohta oma kaart, kus tuleb täita järgmised väljad:

Väli |  Selgitus | 
-- | --
Teenuse URL | Sisestage panga teenuse aadress
Seadmesertifikaadi failinimi | Sisestage oma pangalepingus näidatud sertifikaadi failinimi.
Seadmesertifikaardi parool | Sisestage panga poolt antud sertifikaadi parool.

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

Teenustasude ja teiste fikseeritud kontode sidumiseks on võimalik kasutada _Tekst-kontoks vastendamine_ funktsionaalsust või kirjeldada PR kontode vastavus "Tehingu tähiste" kaudu.
Kiirkastis olevale väljale _Tehingu tähis_ vajutades avatakse leht _Pangatehingu tähis_.

Lisage uus rida pangatehingu tähise ja sellele vastava PR kontoga. 
Seejärel vajutades nupule "Seo automaatselt". Vastava pangatehingu Sidumise olek muutus _Kõrge täpsus_.

Võimalik on korraga lisada mitu erinevat rida pangatehingu tähiste ja PR kontodega.


### Arvete sidumine

Arvetega sidumist saab lehel _Pangakonto tehingud_ teha kas automaatselt või käsitsi. 

Automaatseks sidumiseks käivitage protsess _Seo automaatselt_.
Kui töötlemise käigus leitakse hankija või kliendiga seotud maksmata arved (arve numbri, viitenumbri ja summa alusel), siis nende sidumise korral on _Sidumise olek_ "Kõrge täpsus".
Kui töötlemise käigus leitakse hankija või klient, kuid ei leita vastavat arvet, siis kuvatakse _Sidumise olek_ "Madal täpsus".
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
