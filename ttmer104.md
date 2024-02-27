## Beugró kérdések
1. Milyen feladatokat kell megoldani a mérési gyakorlaton?
  > DNS lekérdezés és válasz
webes forgalom elemzése: teljes oldalletöltés vizsgálata, TCP szintű elemzés
VoIP hívás elemzés: hívás vizsgálata, hívás közben átvitt médiafolyam vizsg.
Nagy mennyiségű adatátvitel vizsgálat: hálózati paraméterek, átviteli karakterisztika vizsgálat

2. Ismertesse vázlatosan a DNS működését!
   > DNS: domain name service jelentése, feladata feloldani az ip és url-ek közötti hozzárendelést.
   > Az internet szótára

3. Adja meg a TCP/IP protokolstack rétegeit! Mi az egyes rétegek feladata?
   > TCP/IP rétegek:
  • Physical PHY – fizikai réteg
  • Data Link Control – Adatkapcsolati réteg
  • Network – Hálózati réteg
  • Transport – Szállítási réteg
  • Application – Alkalmazási réteg

4. Ismertesse az Ethernet keret szerkezetét! Mekkora lehet a keret maximális mérete?
   > max 1526 byte
   > min 72 byte
   > ![image](https://github.com/Bende126/infokommlab/assets/28264530/4ea6adb0-a31b-4d5e-b52c-ae8884d846ec)

5. Ismertesse az IP fejléc szerkezetét! Mekkora lehet az IP csomag maximális mérete?
  > 2^16 byte max méret
> • hálózati réteg protokoll, csomagkapcsolt hálózatot valósít meg.
• összeköttetésmentes (datagram) protokoll
• hibadetektálás, hibajavítás nincs
• fragmentálás, reassembly
• verziók: IPv4, IPv6

6. Mi a különbség az MSS és a MTU között?
   > MSS: maximum segment size, MTU rétegnek a szoftveres modellje/koncepciója
   > MTU: maximum transmission unit, hálózati fizikai réteg

7. Ismertesse a TCP szegmens fejlécének szerkezetét! Mekkora lehet a TCP szegmens maximális
mérete?
  > legalább 20 oktetből áll

8. Soroljon fel 5 eltérő tulajdonságot a TCP és az UDP között!
 • Sorrendhelyes adatátvitel - a célcsomópont sorbarendezi a szegmenseket a sorszám
alapján.
• Elveszett csomagok újraküldése - a célcsomópont kumulatív nyugtát küld, a nem
nyugtázott adatokat újraküldi a forrás.
• Duplikált csomagok eldobása
• Hibamentes adatátvitel - CRC használata a fejlécben.
• Folyamvezérlés - a lassú vevő korlátozni tudja a küldő sebességét.
• Torlódásszabályozás - a hálózat túlterhelése esetén korlátozza a küldő sebességét.

9. Mik azok a portszámok, mire használatosak?
   > két ip közötti kommunikációs interfészek, pl 80: http, 443: https

10. Ismertesse a TCP kapcsolatfelépítési folyamatát!
  > kliens a szervernek: szinkronizáció?
> szerver kliensnek: igen, vettem-vettem
> kliens szervernek: vettem-vettem

11. Ismertesse a TCP kapcsolatlezárási folyamatát!
    > kliens szervernek: vége?
    > szerver kliensnek: vettem-vettem
    > szerver kliensnek: vége
    > kliens szervernek: vettem-vettem

12. Hogyan működik a TCP-ben a folyamvezérlés? Hogyan számítjuk a küldő ablakát?
    > amikor egy gyors küldő nem tudja elárasztani a lassú vevőt
    > ablakozás magic

13. Mire használatos az ún. „Window Scale” TCP opció?
    > megmondja h mennyi adatot képes fogadni még a vevő, mielőtt elkezdi eldobálni őket

14. Mire használatos az ún. „Timestamp” TCP opció?
  > küldött/fogadott szegmens időbélyege, segít megkülönböztetni a nagy ablakméret mellett is, az azonos sorszámmal érkező szegmenseket

15. Mi a pszeudófejléc és mi a szerepe?
    > 96bit ellenörzőösszeg számításhoz használjuk
17. Hogyan működik a kumulatív nyugtázás?
    > nyugta az összes eddig elveszett adat csomagról, 
18. Hogyan működik a szelektív nyugtázás?
    > ha mindent logolunk akkor leterheljük a hálózatot, csak bizonyos vagy ismert hibákat logolunk
19. Mit jelent az Additive Increase/Multiplicative Decrease? Rajzolja le két versengő TCP folyamra!
    > 
21. Mit jelent a TCP esetén a „slow start” (lassú indulás)?
    > Eleinte kisebb ablakszélességgel és minden szegmens után acknowledge-al indul, majd egyre jobban "belejön" és megnő az ablakméret a maximális értékre, amíg csomagvesztést nem tapasztalunk.
22. Milyen lesz a TCP összeköttetés hosszútávú képe, ha a torlódás korlátozza az átvitelt? Rajzoljon! Hogyan határozná meg a várható átlagsebességet (throughput)?
23. Mit jelent a TCP esetén a „congestion avoidence” (torlódás elkerülés)?
    > A hálózaton elkerüljük a hálózat instabilitását, ezért használjuk ezt a fázist
24. Mire használatos az RTP protokoll? Mit nyújt a felhasználó számára?
    > real time transport protokoll, valós idejű digitális hang és kép küldése, pl élő adás youtubeon.
