## Ellenőrző kérdések

1. Mit mond ki a mintavételi tétel?
    > Egy mintavételezett jelből az eredeti jel visszaállítható egy ideális aluláteresztő szűrő segítségével, ha a mintavételezett jel kétszer gyakoribb, mint a jel legnagyobb frekvenviája. 

    `Fs >= 2Fmax`
2. Mitől alakul ki az áljel (alias jel)?
    > az áljel a mintavételi tétel megsértéséből alakul ki. Az aluláteresztő átenged olyan frekvenciákat, amik sértik a mintavételi tételt.
3. Adott egy valós alapsávi jel, amelynek spektumát 300 Hz és 3600 Hz között az s(f)=7-f/900 képlettel írhatjuk le, míg 0 és 300 Hz között, illetve 3600 Hz fölött az értéke 0. Rajzolja le az jel spektrumát (negatív tartományban is)
![image](https://github.com/Bende126/infokommlab/assets/28264530/04ef94a4-2b10-4682-8463-53efbb730bd2)

4. Miből keletkezik a kvantálási zaj?
    > Az átalakításnál használt A/D átalakító nem tökéletes. Adott feszültség szinthez, adott kódot rendel. Pl.: 8-9 V -> 100b, ez azt jelenti, hogy 8.3 és 8.5 V is 100b-t fog adni. Ezt visszaállítási hibának is hívják.

5. Miért előnyös a logaritmikus kvantálás használata?
    > halk frekvenciákon finomabb, hangos frekvenciákon durvább a felbontás. Leginkább az emberi fül fizikai paraméterei miatt.
6. Mekkora a delta lépcsőméretű egyenletes kvantáló kvantálási zaja?

    `△ kvantálási lépcső = a hiba nagysága max. +- (△/2)`
7. Miért függ a kvantálási zajból számítható jel-zaj-viszony a kvantálandó jel csúcstényezőjétől?
    > Az SNR-t befolyásolja a jel teljesítmény. Annál jobb az SNR, minél nagyobb a jel teljesítménye a zajhoz képest. Az amplitúdó közvetlen hatással van az SNR és a csúcstényezőt tartalmazza az amplitúdó.

    `SNR = 3/c^2 * Fs/2*B * 2^(2n)`
8. Milyen jelet kapunk egy f=1 kHz frekvenciájú szinuszos jel túlvezérlésével? Milyen lesz a spektruma? (Rajzoljon!)
    > A szinuszos jel elkezd "négyzetes" lenni.
   ![image](https://github.com/Bende126/infokommlab/assets/28264530/07a395f9-622a-41c8-b2f1-8c7aa3b9cf19)

9. Mi történik, ha egy f=1 kHz frekvenciájú túlvezérelt szinuszos jelet szűrünk egy 3.4 kHz törésponti frekvenciájú ideális aluláteresztő szűrővel, majd a mintavételezzük 7 kHz-cel? Rajzolja le a -10-+10 kHz közötti tartományban a spektrumot a túlvezérlés után, a szűrés után illetve a mintavételezés után! (A rajz otthon előre is elkészíthető és névvel ellátva beadható!)
    > túlvezérelt szinusz négyszögjelre hasonlít -> szűrve torzul az éle/sarkai -> jelváltozások ezeken a pontokon -> mintavételi tétel nem sérül -> visszakapunk egy négyszögjelszerűséget.
    ![image](https://github.com/Bende126/infokommlab/assets/28264530/2630c9d7-3153-4bbb-aee8-b0f669020e72)

10. Hogyan képzelhetjük el egy időben egyenletesen növekvő frekvenciájú szinuszos jel időfüggvényét illetve spektrumát? Mi történik, ha egy ilyen jelet mintavételezünk? 
    > ???
    ![image](https://github.com/Bende126/infokommlab/assets/28264530/ea6370e0-d6ce-4d27-aa91-8d461efe99ec)
