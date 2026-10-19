# Praktikum 5 - Protsessid ja signaalid
Operatsioonisüsteemide kursuse viies praktikum. Aega kulus umbes 1-1.5 tundi.

Praktikumi käigus harjutasin Linuxi protsesse jälgimist, peatamist, taustal käivitamist ja signaalide abil juhtimist. Tegin läbi 
käskude sisendi ja väljundi suunamist ning torude kasutamist. Lisaks uurisin Windowsi sõnumeid, et paremini mõista, kuidas 
operatsioonisüsteem ja programmid omavahel suhtlevad.
Juhend: https://courses.cs.ut.ee/2026/os/fall/Main/Praktikum5

## Tõestus
### Ülesanne 1: Gedit'i ajutine peatamine
<img width="1917" height="1125" alt="image" src="https://github.com/user-attachments/assets/93e16d60-fe9a-43c3-a5ec-834808fce645" />

### Ülesanne 2: Gedit nohup'iga
<img width="1875" height="1132" alt="image" src="https://github.com/user-attachments/assets/682c6312-4a4a-41b2-8411-787d0499dc4e" />

### Ülesanne 3: Programminimed lisaparameetritega
<img width="1873" height="1127" alt="image" src="https://github.com/user-attachments/assets/bdbf735b-1db4-4e2b-b5a9-9c993ba184d4" />

### Ülesanne 4: IP-aadress faili
<img width="1919" height="1127" alt="image" src="https://github.com/user-attachments/assets/9955374e-39c1-40f7-8b7d-16a3e56ca319" />

### Ülesanne 5: Windowsi loodud logid
1. Logi: 20:48:23.991,33,"WM_MOUSEACTIVATE",131222,33619973  
   Tegin hiireklõpsu mitteaktiivses aknas. Windows saatis sõnumi, et otsustada, kas aken tuleb aktiivseks muuta ja kas hiireklõpsu töödelda.
   wParam: Näitab, millises aknas hiireklõps toimus.  
   lParam: Sisaldab infot hiireklõpsu tüübi ja selle kohta, millise aknaosa kohal klõps tehti.  
   [Allikas: WM_MOUSEACTIVATE](https://learn.microsoft.com/en-us/windows/win32/inputdev/wm-mouseactivate)
   
3. Logi: 20:48:25.136,132,"WM_NCHITTEST",0,15925576  
   Liigutasin hiirt programmi akna kohal. Windows saadab selle sõnumi, et teha kindlaks, millise aknaosa kohal hiirekursor asub,
   näiteks kas akna sisu, tiitliriba või serva kohal.  
   wParam: Selle sõnumi puhul ei kasutata, väärtus on 0.  
   lParam: Sisaldab hiirekursori koordinaate.  
   [Allikas: WM_NCHITTEST](https://learn.microsoft.com/en-us/windows/win32/inputdev/wm-nchittest)
   
   
