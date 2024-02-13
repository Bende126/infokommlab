# 1

> A vm indítása után jelentkezzünk be a konzolon a korlátozott jogú felhasználóval. 
> A saját home könyvtáradban hozz létre egy 'linux-alapozo' alkönyvtárat, a mérés alatt ez legyen a munkakönyvtár. 
> Milyen jogosultságokkal rendelkeznek az egyes felhasználók a létrehozott könyvtárhoz?

```bash
mkdir linux-alapozo
ll
```
d mint directory

ugo -> user, group, others


> Lépj be a 'linux-alapozo' könyvtárba és hozz létre három tetszőleges tartalmú szöveges fájlt f1, f2 és f3 néven.
> Milyen védelmi kóddal jöttek létre a fájlok?
> Állítsd be úgy a jogosultságokat, hogy az f2 fájlra a csoportod többi tagja is rendelkezzen írási joggal.

```bash
cd linux-alapozo
touch f1.txt f2.txt f3.txt
chmod g+w f2.txt
```

> Hozz létre egy 'linkek' alkönyvtárat, majd ezen belül hozzál létre szimbolikus linkeket az előbb létrehozott három fájlra f1link, f2link, f3link névvel.
> (A target paramétert a teljes elérési úttal add meg mindhárom esetben!)


```bash
mkdir linkek
cd linkek
ln -s /home/usr/linux-alapozo/f1.txt f1link
ln -s /home/usr/linux-alapozo/f2.txt f2link
ln -s /home/usr/linux-alapozo/f3.txt f3link

cat f1link
```


# 2

```bash
#!/bin/bash

while IFS= read -r line; do
  echo "$line" | tr '[:lower:]' '[:upper:]'
done
```

```bash
touch upper.sh
vim upper.sh
chmod +x upper.sh
./upper.sh
```


# 3

```bash
#!/bin/bash

# Ellenőrzi, hogy a megadott könyvtár argumentumként van-e megadva
if [ $# -eq 0 ]; then
  echo "Használat: $0 <könyvtár>"
  exit 1
fi

directory="$1"

# Ellenőrzi, hogy a megadott könyvtár létezik-e
if [ ! -d "$directory" ]; then
  echo "Hiba: A megadott könyvtár nem létezik."
  exit 1
fi

# Fájlnevek módosítása a .htm kiterjesztésről .html kiterjesztésre
for file in "$directory"/*.htm; do
  if [ -e "$file" ]; then
    newfile="${file%.htm}.html"
    mv "$file" "$newfile"
    echo "A fájl neve módosítva: $file -> $newfile"
  fi
done

echo "Fájlcserék kész!"
```

# 4

## a

## b/c
```bash
df -h
```
## d
```bash
du -sh /usr
```

## e
```bash
top
```

# 5 

## a
## b
## c
## d
## e

# 6

## a 
```bash
ifconfig
```

## b
```bash
cat /etc/resolv.conf | grep "nameserver"
```
## c
```bash
ip route | grep default
```

## d




