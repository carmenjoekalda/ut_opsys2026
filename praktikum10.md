| Küsimus / Ülesanne | Linux | Windows | Linuxis kasutatud käsklus | Windowsis kasutatud tööriist ja väli |
| :--- | :--- | :--- | :--- | :--- |
| **1.** Mitu protsessi kokku arvutis käivitatud on? | 280 | | ps -ef \| wc -l | |
| **2.** Milline on kõige esimesena käivitatud protsess? | systemd | | ps -eo pid,comm --sort=pid | |
| **3.** Milliste kasutajate protsessid arvutis töötavad? | avahi, carmen, _chrony, colord, cups-browsed, messagebus, polkitd, root, rtkit, syslog, systemd-oom, systemd-resolve| | ps -eo user \| sort -u | |
| **4.** Kui kaua on arvuti järjest töötanud? | 26 min | | uptime | |
| **5.** Milline protsess käivitati viimasena? | kworker/1:1 | | ps -eo pid,comm,lstart --sort=-lstart| |
| **6.** Milline protsess võtab vaatlushetkel kõige rohkem protsessoriaega ja mitu protsenti protsessoriajast ta tarbib? | gnome-shell, 3.7% | | ps -eo pcpu,pid,user,comm --sort=-pcpu | |
| **7.** Milline on kõige rohkem virtuaalmälu võttev protsess? | gnome-shell | | ps -eo vsz,pid,user,comm --sort=-vsz | |
| **8.** Milline on kõige rohkem füüsilist mälu võttev protsess? | gnome-shell | | ps -eo rss,pid,user,comm --sort=-rss | |
| **9.** Kui palju füüsilisest mälust on vaba ja kui palju hõivatud? | available: 1.6Gi <br> used: 1.7Gi | | free -h | |
| **10.** Kui palju on põhikettal vaba ruumi mahult ja protsentuaalselt? | 6.1G, 26% | | df -h / | |
| **11.** Milline on kõige suurem arvutis olev fail ja kõige rohkem andmemahtu hõivav kaust? | `fail`: /swap.img, 3.6G <br> `kaust`: /usr, 8.8G | | `fail`: sudo find / -xdev -type f -size +100M -exec ls -lh {} + \| sort -k5,5 -h -r \| head <br>  `kaust`: sudo du -h --max-depth=1 / 2>/dev/null \| sort -hr  | |
| **12.** Test: protsessikasutus `sha1sum` käsu puhul | 1. us, 92.2% <br> 2. sy, 100% | - | <img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/03403b06-7431-4f93-8ae1-4e6af7c64d66" /> <img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/f54639ca-53f7-447e-825d-0465dd512085" /> | - |
| **13.1.** Milline protsess kirjutab kõige rohkem salvestusseadmele? | - | | - | |
| **13.2.** Millisesse faili eelmise küsimuse protsess kõige rohkem kirjutab? | - | | - | |
| **13.3.** Milline protsess loeb kõige rohkem salvestusseadmelt? | - | | - | |
| **13.4.** Millisest failist eelmise küsimuse protsess kõige rohkem loeb? | - | | - | |
| **14.** Millise protsessi tekitatud võrguliiklus on suurima mahuga? + detailid | - | | - | |
| **15.** Aeglase arvuti diagnostika | - | | - | |
