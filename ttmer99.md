# TTMER99: Programfejlesztő eszközök

## Ellenőrző kérdések

1. Jellemzően mely szövegszerkesztők alapvető részei a Linux/Unix rendszereknek?
> THE (The Hessling), vi, vim, nano

2. Az egyik válaszott szövegszerkesztőben milyen paranccsal/billentyűkombinációval menthetünk el fájlt új néven?
```bash
vim hello.c
:wq new_hello.c
```

3. Milyen paranccsal hozunk létre tárgykódokat tartalmazó archívumot? (példával)
```bash
gcc hello.c -o hello.out
ls -a
```
> a hello.out lesz a megoldás

4. Írjon egy minimális C forráskódot, amely kiírja a konzolra a `hello world` karaktersorozatot, majd adja meg a parancsot, amivel futtatható állomány készíthető belőle.
```bash
vim hello.c
gcc hello.c -o hello.out
ls -a
./hello.out
```
A C kód:
```c
#include<stdio.h>

int main(){
        printf("Hello world");
        return 0;
}
```

5. Milyen függvényt, ill. szimbólumot kell tartalmazzon minden futtatható programkód?
> main függvényt vagy belépési pontot, ahol a program futása kezdődik.
7. Mire szolgál a tárgykód és hogyan készíthető?
> A fordítóprogram feladata a forráskód előfeldolgozása (preprocesszor, a
makrók, include-ok kifejtése), szintaktikai elemzése (a hibák kijelzése
mellett), és a fordítás során a linker által elfogadott tárgykódú modul
(object) előállítása.
> magyarul:
> ez a futtatható állomány linuxon belül, ami már assembly utasításokat tartalmaz. (digit2)
8. Milyen eszközzel vizsgálhatjuk meg a tárgykódot? (példával)
```bash
objdump -hs hello.out
```
> vannak más nevei, mert who knows: tdump, dmpobj
9. Írjon le legalább két, a tárgykód kivonatában található szekciót! Mit lehet tudni róluk?
> bemagolni. digit2 flashbackek

| Szekció                        | Leírás                                              |
|--------------------------------|-----------------------------------------------------|
| .text, .code                   | program kód.                                        |
| .data                          | írható, olvasható adatterület – lehet inicializálva |
| .bss                           | nem inicializált adatterület                        |
| .rodata, .const, .rdata, .init | csak olvasható, inicializált adatterület            |
| .vector                        | Interrupt vector table                              |
| .stack                         | Stack                                               |


10. Mire szolgál a shared object vagy DLL?
> A shared object (SO) és a Dynamic Link Library (DLL) olyan dinamikusan betölthető könyvtárak, amelyek funkciókat vagy kódot tartalmaznak, és ezeket a könyvtárakat más programok vagy folyamatok a futás idején tudják betölteni és használni.
12. Mi történik a linkelés folyamatakor?
> bemagolni
> A linker feladata a tárgykódú modulok
és könyvtárak összefűzése a
célrendszer által betölthető (DOS/Windows esetén EXE file-ok, Linux
esetén ELF (Executable and Linkable Format) formátumú, vagy az abszolút
módon elhelyezett objektumok esetén közvetlenül égethető/futtatható (pl.
Intel-hex formátumú file) kóddá oly módon, hogy az egyes modulok
objektumai a megfelelő programszekciókba kerüljenek, és a
kereszthivatkozások a megfelelő elhelyezési információk (relocation)
birtokában feloldódjanak
13. Mire használható a gdb?
> egy cli (command line interface) debugger
14. Milyen eszközzel automatizálható a fordítási folyamat?
> Make (Program maitenance utility) vagy CMake ha c kódról van szó
> A Program Maintenance Utility (Make) -
feladata egy programrendszer elemeinek
naprakészen tartása, a teljes technológiai
lánc függőségi viszonyainak
figyelembevételével. Vezérléséhez létre kell hozni egy - a teljes
technológiai folyamatot leíró - file-t (neve többnyire Makefile, vagy *.mak)
amely három részre tagolható.

## Labor Feladatok
1 
```bash
vi hello.c
:wq
du -sh hello.c
```

2 
```bash
vi valami.txt
v mint visual
G a.k.a ctr+a
:sort valami
```

3
```bash
vi neptunmsg.c
:wq
du -sh neptunmsg.c

vi msg.h
du -sh msg.h

vi printmsg.c
du -sh printmsg.c
```

4
```bash
gcc msg.c printmsg.c -o hello.out
objdump -d -M a.out
```



