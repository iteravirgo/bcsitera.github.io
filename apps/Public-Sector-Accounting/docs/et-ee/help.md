# Üldine 
Avaliku sektori finantsarvestuse lahendus võimaldab süsteemist väljastada riigile esitatava Saldoandmiku. 

# Seadistamine
1.	Riigi raamatupidamise seadistus täita
2.	Riigi kontod täita (Riigi kontoplaaniga)
3.	Kontoplaani määrata PR kontodele külge Riigi kontod (Vaikedimensioon nõutud dimensioonidele tekib automaatselt)
4.	Riigi tehingupartnerid täita (importida tehingupartnerid)
5.  Klientidele määrata külge Riigi tehingupartnerid (Vaikedimensioon tekib automaatselt)
6.  Hankijatele määrata külge Riigi tehingupartnerid (Vaikedimensioon tekib automaatselt)
7.  Pangakonto kaardile määrata tehingupartner ning panna vastav linnuke Riigi kontodes

# Tööpõhimõte
PR kannetele läheb kaasa vastav riigi konto ning nõutud dimensioonid. Dimensioonide alusel luuakse Riigi Saldoandmik.

# Riigi saldoandmiku loomine
1.  Avada Riigi saldoandmikud
2.  Luua uus Saldoandmik, valides aruande perioodi (aasta ning perioodi lõpu kuu)
3.  Nupuga Arvuta read arvutab süsteem saldoandmiku read
4.  Nupust Loo XML fail saab süsteemist XML faili, mida importida Saldoandmike infosüsteemi
