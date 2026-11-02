# Praktikum 7 - Haakimine
Operatsioonisüsteemide kursuse seitsmes praktikum. Aega kulus 2 tundi.

Praktikumi käigus tegelesin ketaste haakimisega Windowsi ja Ubuntu masinates. Seadistasin kettaid, lõin partitsioone
ning haakisin neid käsitsi, lisaks seadistasin Linuxis ketta arvuti käivitamisel automaatselt haakima.  
Juhend: https://courses.cs.ut.ee/2026/os/fall/Main/Praktikum7

## Tõestus
### Ülesanne 1: Andmekandjate lähtestamise vajadus
Uued andmekandjad vajavad lähtestamist, sest enne seda puudub kettal vajalik struktuur andmete salvestamiseks. Lähtestamise
käigus luuakse kettale partitsioonitabel, mis määrab, kuidas kettaruumi hallatakse ja jaotatakse. Seejärel saab luua
partitsiooni ning vormindada selle sobiva failisüsteemiga. Alles siis on andmekandja operatsioonisüsteemis
kasutamiseks valmis.

### Ülesanne 2: GPT eelised MBR'i ees
1. GPT toetab 4 miljardit korda suurema mahuga kettaid (9.4 ZB vs 2.2 TB).
2. GPT võimaldab luua kuni 128 partitsiooni, samas kui MBR-i maksimum on 4.
3. GPT salvestab partitsioonitabelist varukoopia. MBR-i puhul varukoopia puudub.
4. GPT ühildub tänapäevaste UEFI-põhiste arvutitega, MBR ühildub ainult BIOS-i arvutitega, mis on aegunud lahendus.

Allikas: https://medium.com/@nipunasan/mbr-vs-gpt-partitioning-schemes-explained-with-advantages-disadvantages-and-security-insights-456f5c9365bf

### Ülesanne 3: Windowsil haakimine
https://kodu.ut.ee/~carmenjoekalda/opsys/hdd.png

### Ülesanne 4: hdd.png Ubuntus
<img width="1082" height="1126" alt="image" src="https://github.com/user-attachments/assets/61db3812-b9bd-4f9f-a8b3-a3e4425ad091" />

### Ülesanne 5: mount parameetrite mõju
1. `-o ro` parameeter: andmekandja ühendamisel annab ainult lugemisõiguse
2. `-t auto` parameeter: tuvastab andmekandja ühendamisel automaatselt selle failisüsteemi tüübi

### Ülesanne 6: Mount käsu väljund
Ubuntu asendas auto parameetri väärtusega `vfat`.

### Ülesanne 7: Ketta automaatne ühendamine arvuti käivitumisel
<img width="1080" height="1126" alt="image" src="https://github.com/user-attachments/assets/4bbd11a3-651d-4194-9e2f-4e5c86a207d5" />
