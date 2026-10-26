# Praktikum 6 - Failiõigused Linuxis
Operatsioonisüsteemide kursuse kuues praktikum. Aega kulus 2 tundi.

Praktikumi käigus katsetasin erinevaid Linuxi kasutajate, gruppide ja failisüsteemi ligipääsude haldamisega seotud harjutusi.
Sealhulgas käsitlesin näiteks vaikimisi määratavaid õigusi, maski, ACL, sticky biti ja lisaatribuutide kasutamist
Juhend: https://courses.cs.ut.ee/2026/os/fall/Main/Praktikum6

## Tõestus
### Ülesanne 1: Vajaminevad õigused
a) Faili lugemiseks on kaustal vaja `execute` ja failil `read` õiguseid.  
b) Faili kustutamiseks on kaustal vaja `execute` ja `write` õiguseid. Failil pole õiguseid vaja.

### Ülesanne 2: Puuduv õigus
`chmod a=x Kaust3/skript.sh` ei ole piisav, kuna see annab kõigile kasutajatele execution õiguse, kuid võtab ka read õiguse, mis on
samuti shellile vajalik skripti käivitamiseks.

### Ülesanne 3: Kasutaja privaatgrupp
Linuxis luuakse kasutajatele privaatgrupid, et kasutaja failid ja kataloogid oleksid vaikimisi tema kontrolli all ning teiste
kasutajate ligipääs oleks piiratud. `Umask` määrab, millised õigused edaspidi uutele failidele ja kaustadele andmata jäetakse.

### Ülesanne 4: uusfail.txt õigused
<img width="958" height="1125" alt="image" src="https://github.com/user-attachments/assets/60ce1a02-aa30-4985-bd33-019e8300dc36" />

### Ülesanne 5: opetaja/klass failide õigused
`setuid` õigust on vaja, et faili käivatmise ajal rakenduksid faili omaniku, mitte käivitaja õigused.
  
<img width="952" height="1126" alt="image" src="https://github.com/user-attachments/assets/9e768dfa-1f4c-44bc-a1e7-51dc37ea86b2" />

### Ülesanne 6: Setuid plussid ja miinused
`Setuid` on kasulik, sest see võimaldab tavakasutajal kasutada programmi, mis vajab ligipääsu failidele, mida ta ise lugeda
ei saa. Samas on see ohtlik, sest nii võib kasutaja näha andmeid, mida ta tegelikult näha ei tohiks.  
Seega oleneb setuid kasutamise mõju süsteemi turvalisusele sellest, mida programm teeb. Kui programm otseselt ei avalda
kasutajale failide sisu, millele tal ligipääsu pole, vaid näiteks näitab statistikat nende põhjal, oleks see turvaline.
Kui kasutaja aga näeks algandmeid, siis see enam turvaline ei oleks.

### Ülesanne 7: Sticky bit
Antud näites saavad faile kustutada root kasutaja, kausta omanik ning faili omanik, ehk `root, opetaja ja peeter`.

### Ülesanne 8: ACL
`ls- la` käsu tulemuse õiguste lõpus on `+` märk.
  
<img width="956" height="1125" alt="image" src="https://github.com/user-attachments/assets/62d1dbed-20fc-4639-a966-86354e0a927e" />

### Ülesanne 9: Failisüsteemi täiendavad atribuudid
a) Keegi ei saa `+1` atribuudiga faili sisu muuta, isegi mitte root.  
b) Faili saaks kustutada peale seda, kui sellelt `+1` atribuut eemaldakse, ehk:
  1. `sudo chattr -i testfail-2`
  2. `sudo rm testfail-2`

 
