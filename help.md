
# PowerShell Beolvasás Példa  

## **1. Beolvasás a Konzolról**  

```powershell
# Szöveg beolvasása a felhasználótól
$nev = Read-Host "Add meg a neved"
Write-Output "Szia, $nev!"
```

**Magyarázat:**  
- `Read-Host` segítségével beolvashatunk adatokat a konzolról.  
- A felhasználó által megadott érték a `$nev` változóba kerül.  

---

## **2. Fájl Tartalmának Beolvasása**  

```powershell
# Fájl tartalmának beolvasása és megjelenítése
$tartalom = Get-Content "adatok.txt"
Write-Output "A fájl tartalma:"
Write-Output $tartalom
```

**Magyarázat:**  
- `Get-Content` segítségével egy szöveges fájl tartalmát olvassuk be.  
- A `$tartalom` változó tárolja az adatokat, amelyeket a konzolon kiírunk.  

---

## **3. Fájl Létrehozása és Írása**  

```powershell
# Fájlba írás
$tartalom = "Ez egy példa szöveg."
$tartalom | Out-File "kimenet.txt"
Write-Output "A fájl sikeresen létrejött!"
```

**Magyarázat:**  
- Az `Out-File` parancs fájlba írja a szöveget.  
- A `kimenet.txt` fájlban megjelenik a `$tartalom` változó értéke.  
