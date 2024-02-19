# Liitumine

## Taotluse esitamine
Business Central kasutab liidestamisel otsekanalit. Liitumiseks võtke ühendust oma kliendihalduriga või esitage taotlus panga kodulehel.

### Swedbank
[https://www.swedbank.ee/business/d2d/ebanking/gateway](https://www.swedbank.ee/business/d2d/ebanking/gateway)  

Toetatud teenused:
- Maksete edastamine panka (ootel e. allkirjastamata maksed).  
- Regulaarne konto väljavõte – panga poolt automaatselt saadetav eelmise päeva väljavõte.
- Kiirteavitused – panga poolt automaatselt saadetav teavitus iga tehingu kohta, mis vastab kehtestatud tingimustele (sisse/välja, valuuta, alates summast).

### LHV
[https://www.lhv.ee/et/connect](https://www.lhv.ee/et/connect)  

Toetatud teenused:
- Maksete edastamine panka (ootel e. allkirjastamata maksed).  
- Regulaarne konto väljavõte – panga poolt automaatselt saadetav eelmise päeva väljavõte.
- Kiirteavitused – panga poolt automaatselt saadetav teavitus iga tehingu kohta.

### SEB
[https://www.seb.ee/ariklient/igapaevapangandus/elektroonilised-kanalid/baltic-gateway](https://www.seb.ee/ariklient/igapaevapangandus/elektroonilised-kanalid/baltic-gateway)  

Toetatud teenused:
- Maksete edastamine panka (ootel e. allkirjastamata maksed).  
- Jooksva päeva väljavõte.   
  NB! seadistage Business Central väljavõtet laadima piisava sagedusega, et päeva lõpust ei jääks mõni tehing laadimata.

### Coop Pank
[https://www.cooppank.ee/gateway](https://www.cooppank.ee/gateway)  

Toetatud teenused:
- Maksete edastamine panka (ootel e. allkirjastamata maksed).  
- Regulaarne konto väljavõte – panga poolt automaatselt saadetav eelmise päeva väljavõte.
- Kiirteavitused – panga poolt automaatselt saadetav teavitus iga tehingu kohta.

## Turvasertifikaat
Kõigi pankade puhul tuleb lahenduses seadistada turvasertifikaat. Liitumisel annab pank teile sellekohased juhised. Kuna tegemist on üsna tehniliste sammudega, siis soovitav on pöörduda oma BC partneri poole, kes aitab need teha.

Kokkuvõtvalt on vajalik:
- Sertifikaadipäringu koostamine, sertifikaadi tellimiseks.
- Sertifikaadi- ja privaatvõtmefaili liitmine pfx/p12 failiks ja parooli genereerimine.
- pfx/p12 faili ja parooli seadistamine BC-s.

Swedbank juhend:  
[http://dev.swedbankgateway.net/content/general-info/doc/How-to-generate-CSR-and-convert-private-key-to-p12.pdf](http://dev.swedbankgateway.net/content/general-info/doc/How-to-generate-CSR-and-convert-private-key-to-p12.pdf)

LHV juhend:  
[https://partners.lhv.ee/en/connect/#certificates](https://partners.lhv.ee/en/connect/#certificates)

Coop Pank juhend:  
[https://www.cooppank.ee/s3fs-public/juhendid/Gateway_votmete_genereerimise_juhend.pdf](https://www.cooppank.ee/s3fs-public/juhendid/Gateway_votmete_genereerimise_juhend.pdf)