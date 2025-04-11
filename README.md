# Fix Autoteenindus OÜ Veebilehe Ülesseadmine

## Failide Allalaadimine

Veebilehe failide allalaadimiseks on kaks võimalust:

### Failide Struktuur
Kopeeri kõik failid ühte kausta järgmise struktuuri järgi:
```
/fixautoteenindus/
├── index.html          # Avaleht
├── pages/             # Alamlehed
│   ├── meist.html
│   ├── teenused.html
│   ├── hinnakiri.html
│   └── kontakt.html
├── images/            # Pildid
│   ├── fixusrani.png
│   └── workshop.jpg
├── fixusringtee.png   # Logo
└── favicon.ico        # Veebilehe ikoon
```

### Failide Kontroll
1. Veendu, et kõik failid on õigetes kaustades
2. Kontrolli, et kõik pildid on olemas
3. Testi veebilehte lokaalselt enne üleslaadimist

## Veebilehe Ülesseadmise Juhend

### 1. Domeeni registreerimine
1. Mine veebilehele www.zone.ee või www.veebimajutus.ee
2. Registreeri domeen "fixautoteenindus.ee"
3. Vali sobiv makseperiood (soovituslik 1 aasta)

### 2. Veebimajutuse tellimine
1. Vali sama teenusepakkuja juures veebimajutus
2. Soovituslik pakett:
   - Kettaruumi min 1GB
   - Liiklus min 10GB/kuus
   - PHP tugi
   - SSL sertifikaat

### 3. Failide üleslaadimine

#### Variant 1: Läbi veebiliidese (lihtsaim)
1. Logi sisse oma veebimajutuse juhtpaneeli
2. Ava failihaldur
3. Lae üles kõik veebilehe failid:
   - index.html
   - Kaust "pages" kõigi alamlehtedega
   - Kaust "images" kõigi piltidega
   - favicon.ico
   - fixusringtee.png

#### Variant 2: Läbi FTP
1. Lae alla FTP programm (nt FileZilla)
2. Sisesta FTP andmed:
   - Host: sinu_server.ee
   - Kasutajanimi: sinu_kasutajanimi
   - Parool: sinu_parool
3. Lae üles kõik failid

### 4. SSL seadistamine (HTTPS)
1. Logi sisse veebimajutuse juhtpaneeli
2. Vali "SSL sertifikaadid" või sarnane valik
3. Aktiveeri tasuta Let's Encrypt sertifikaat
4. Vali domeen fixautoteenindus.ee
5. Kinnita sertifikaadi tellimine

### 5. Domeeni suunamine
1. Mine domeenihalduse paneeli
2. Lisa DNS kirjed:
   ```
   www.fixautoteenindus.ee -> sinu_server.ee
   fixautoteenindus.ee -> sinu_server.ee
   ```

### 6. Kontroll ja testimine
1. Oota 15-60 minutit DNS muudatuste rakendumiseks
2. Kontrolli veebilehte:
   - Ava www.fixautoteenindus.ee
   - Veendu, et kõik lehed avanevad
   - Kontrolli, et pildid on nähtavad
   - Testi kõiki linke
   - Veendu, et HTTPS töötab (roheline tabalukk brauseris)

### Probleemide korral

#### Levinumad probleemid ja lahendused:

1. **Leht ei avane**
   - Kontrolli domeeni DNS seadeid
   - Veendu, et failid on õiges kaustas
   - Kontrolli, kas index.html on olemas

2. **Pildid ei näy**
   - Kontrolli piltide asukohta serveris
   - Veendu, et piltide viited on õiged
   - Kontrolli piltide õigusi (chmod 644)

3. **HTTPS ei tööta**
   - Kontrolli SSL sertifikaadi staatust
   - Veendu, et domeen on õigesti seadistatud
   - Oota kuni sertifikaat aktiveerub (võib võtta kuni 24h)

### Abi saamiseks

Tehniliste probleemide korral:
1. Veebimajutuse tugi:
   - Zone.ee tugi: 6750 900
   - Veebimajutus.ee tugi: 699 9499

2. Fix Autoteeninduse kontaktid:
   - Ringtee: 7 471 900
   - Räni: 7 339 966

## Autoriõigused

© 2024 Fix Autoteenindus OÜ. Kõik õigused kaitstud.
