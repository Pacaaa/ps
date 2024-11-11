# Bash Alapok

## Alap kezdés

```bash
#!/bin/bash
```

## Beolvasas

```bash
#!/bin/bash
while IFS='' read sor -r  || [[ -n "$sor"    ]]
do
done
```

## for ciklus

```bash
for i in $(seq 1 $n)
do
done
```

## számok 1..n-ig

```bash
$(seq 1 $n)
```

## kulso script futtatasa eredmenyt megkapom

```bash
a=$(./rande.sh)
```

## karakter torlese // -d helyre betu akkor csere

```bash
text=$(echo "$original_text" | tr -d '_')
```

## hány paraméter van

```bash
if [ $# -eq 0 ];then
fi
```

## random számok 1..6

```bash
echo $((RANDOM % 6 + 1))
```

## összeadás

```bash
sum=$((szam1 + szam2))
```

## éppen futo szriptek szamolasa

```bash
darab=$(ps | grep script.sh | wc -l)
```

## egy adat beolvasása

```bash
read -r szo1
```

## egy szo megforditasa

```bash
b=$(echo "$a"|rev)
```

## szám e

```bash
re='^[0-9]+$'
if [[ $1 =~ $re  ]];then
fi
```

## létezik e egy fájl

```bash
file=./e.in
if [ -f $file ]; then
fi
```

## egy fájl sorai száma

```bash
count=$(wc -l < e.in)
```

## lefuttatok egy fajlt annak az exitje

```bash
./d.sh
exit_code=$?
```

## dátum kiírása

```bash
date=$(date '+%Y-%m-%d %H:%M:%S')
```

## kerdes feltevés

```bash
read -p "Kerdes: " nev
```

## 1. Számokra vonatkozó relációs operátorok

| Operátor | Leírás               | Példa               |
| -------- | -------------------- | ------------------- |
| `-eq`    | Egyenlő              | `[ "$a" -eq "$b" ]` |
| `-ne`    | Nem egyenlő          | `[ "$a" -ne "$b" ]` |
| `-gt`    | Nagyobb, mint        | `[ "$a" -gt "$b" ]` |
| `-ge`    | Nagyobb vagy egyenlő | `[ "$a" -ge "$b" ]` |
| `-lt`    | Kisebb, mint         | `[ "$a" -lt "$b" ]` |
| `-le`    | Kisebb vagy egyenlő  | `[ "$a" -le "$b" ]` |

## 2. Sztringekre vonatkozó relációs operátorok

| Operátor | Leírás                   | Példa                |
| -------- | ------------------------ | -------------------- |
| `=`      | Egyenlő                  | `[[ "$a" = "$b" ]]`  |
| `!=`     | Nem egyenlő              | `[[ "$a" != "$b" ]]` |
| `<`      | Kisebb lexikográfiailag  | `[[ "$a" < "$b" ]]`  |
| `>`      | Nagyobb lexikográfiailag | `[[ "$a" > "$b" ]]`  |
| `-z`     | Üres sztring             | `[[ -z "$a" ]]`      |
| `-n`     | Nem üres sztring         | `[[ -n "$a" ]]`      |

## 3. Fájlokra vonatkozó relációs operátorok

| Operátor | Leírás                         | Példa            |
| -------- | ------------------------------ | ---------------- |
| `-e`     | Létezik-e a fájl vagy könyvtár | `[ -e "$file" ]` |
| `-f`     | Normál fájl-e (nem könyvtár)   | `[ -f "$file" ]` |
| `-d`     | Könyvtár-e                     | `[ -d "$file" ]` |
| `-r`     | Olvasható-e a fájl             | `[ -r "$file" ]` |
| `-w`     | Írható-e a fájl                | `[ -w "$file" ]` |
| `-x`     | Futtatható-e a fájl            | `[ -x "$file" ]` |
| `-s`     | Nem üres fájl-e                | `[ -s "$file" ]` |

## Csabika
https://github.com/csabisoos/szamrend_zh
