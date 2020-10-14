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

Pangaühenduste seadistamiseks on Business Centralis igal panga kohta oma kaart. Palun avage vastava pangaühenduse kaart ja täitke vajalikud väljad:

Väli |  Selgitus | 
-- | --
Teenuse URL | Sisestage panga teenuse aadress
Seadmesertifikaadi failinimi | Sisestage oma pangalepingus näidatud sertifikaadi failinimi.
Seadmesertifikaardi parool | Sisestage panga poolt antud sertifikaadi parool.

### Pangakonto seadistused
_Pangakonto_ kaardil valige väljale "Pangaühendus" vastav seadistatud pangaühendus.

### Reaalajas panga seadistused
_Reaalajas panga seadistus_ lehel täitke ära väli "Konteeritud tehingute nr.", määrates vastava numbriseeria.


## Sissetulevad pangasõnumid

### Pangasõnumite automaatne import

Pangasõnumite automaatseks impordiks tuleb vastava pangaühenduse lehel seadistada "Võta uued pangasõnumid" või "Tööjärjekorra kanded". 
Tööjärjekorra kannetena on võimalik seadistada 4 erinevat tegevust: pangasõnumite import, sissetulevate pangasõnumite töötlemine, pangakonto tehingute sidumine, pangakonto tehingute konteerimine.

Imporditud pangasõnumid kuvatakse lehel _Sissetulevad pangasõnumid_. Vaikimisi on lehel filtrid: Allikas ja Olek, kuvatakse ainult kirjed, mis on töötlemata ning vajavad tähelepanu - s.t. Olek on kas _Vastuvõetud_ või _Tõrge_.  
Kõikide sõnumite nägemiseks vajutage nupule "Näita kõiki sõnumeid".


### Pangasõnumite import käsitsi

Käsitsi on pangasõnumeid võimalik importida lehel _Sissetulevad pangasõnumid_ vajutades nupule "Impordi failist". Imporditud kirje Olek on _Vastuvõetud_.
Imporditud kirje töötlemiseks vajutage nupule "Töötle".
Kirje nägemiseks vajutage nupule "Näita kõiki sõnumeid", kirjel on nüüd Olek _Töödeldud_. Paremal olevas kiirinfos on näha _Salvestatud tehingute arv_.
Sellele numbrile vajutades on võimalik liikuda lehele _Pangakonto tehingud_.

## Pangatehingute töötlemine

### Pangatehingud

In Bank Account card there is a new field Balance in Bank. Drilldown in this field to open Bank Account Transactions. By default you can see unposted transactions which need to be applied before they can be posted.

### Teenustasude sidumine

You can use Text-To-Account functionality or describe the G/L account corresponding to the Transaction Code.

Click on the _Transaction Code_ field in the fast box _Bank Account Transaction Details._
Enter the new line with bank transaction code and G/L Account.

Then go back to transaction and press the Apply Automatically button.
The Application status is changed to _High Confidence_.

You can apply one or more transactions at once.


### Arvete sidumine
Appying can be done either manually or automatically.

For manual application, assign Applied Account No. and click Apply Manually. This will open the list of open ledger entries. Apply entries by clicking Process->Set Applies-to ID.

For automatic application run the action Apply Automatically.

### Konteerimine

Applied transaction can be posted to ledger entries by clicking Post action.

In addition Job Queue Entry can be configured, which posts transactions automatically when transaction has been applied and Application Status (quality) is 'High Confidence'.

---

### Kontaktinfo
Täpsema info saamiseks, palun võtke ühendust BCS Itera AS-ga:
<a href="https://www.itera.ee/" target="_blank">www.itera.ee</a>
