# Liitumine

## Taotluse esitamine
Business Central kasutab liidestamisel otsekanalit. Liitumiseks esitage vastav taotlus.

### Swedbank
[https://www.swedbank.ee/business/d2d/ebanking/gateway](https://www.swedbank.ee/business/d2d/ebanking/gateway)  

Toetatud teenused:
- Regulaarne konto väljavõte – panga poolt automaatselt saadetav eelmise päeva väljavõte.
- Kiirteavitused – panga poolt automaatselt saadetav teavitus iga tehingu kohta, mis vastab kehtestatud tingimustele (sisse/välja, valuuta, alates summast).

### LHV
[https://www.lhv.ee/et/connect](https://www.lhv.ee/et/connect)  

Toetatud teenused:
- Regulaarne konto väljavõte – panga poolt automaatselt saadetav eelmise päeva väljavõte.
- Kiirteavitused – panga poolt automaatselt saadetav teavitus iga tehingu kohta.

### SEB
[https://www.seb.ee/ariklient/igapaevapangandus/elektroonilised-kanalid/baltic-gateway](https://www.seb.ee/ariklient/igapaevapangandus/elektroonilised-kanalid/baltic-gateway)  

Toetatud teenused:
- Jooksva päeva väljavõte.   
  NB! seadistage Business Central väljavõtet laadima piisava sagedusega, et päeva lõpust ei jääks mõni tehing laadimata.

## Turvasertifikaat
Allolevate sertfikaaditegevuste teostamiseks palun pöörduge oma BC partneri poole.
- Sertifikaadipäringu (CSR fail) koostamine, sertifikaadi tellimiseks. NB! Sertifikaadipäringut ei pea koostama BC serveris (BC cloud versiooni puhul ei saagi).
- Sertifikaadi- ja privaatvõtmefaili liitmine pfx/p12 failiks ja parooli genereerimine
- pfx/p12 faili ja parooli seadistamine BC-s

Swedbank juhend:
[http://dev.swedbankgateway.net/content/general-info/doc/How-to-generate-CSR-and-convert-private-key-to-p12.pdf](http://dev.swedbankgateway.net/content/general-info/doc/How-to-generate-CSR-and-convert-private-key-to-p12.pdf)
