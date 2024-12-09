```powershell
Get-Help Get-Content
```

```powershell
[Parameter(ValueFromPipeline=$true)]
```

```powershell
$nev = Read-Host "Add meg a neved"
```

```powershell
$tartalom = Get-Content "adatok.txt"
```

```powershell
Write-Output "Teszt1" | Out-File "output.txt"
Write-Output "Teszt2" | Out-File "output.txt" -Append
```

```powershell
$data = Import-Csv -Path "data.csv" -Delimiter ";"
$csvContent = Import-Csv -Path "adatok.csv" -Delimiter ";" -Header "ID", "Name", "Age"

```

```powershell
$data | Where-Object { $_.Age -gt 26 } | Export-Csv -Path "filtered_data.csv" -NoTypeInformation
```

```powershell
foreach ($sor in $tartalom) {
    $adatok = $sor -split ","
    Write-Output "Name: $($adatok[0]), Age: $($adatok[1]), City: $($adatok[2])"
}
```

```powershell
$inputArray = @()
while ($line = Read-Host) {
    $inputArray += $line
}
```

```powershell
$fileContent = Get-Content "adatok.txt" -Filter "1"
$parsedData = @()

foreach ($line in $fileContent) {

    $fields = $line -split ";"
    $parsedData += ,$fields
}


foreach ($array in $parsedData) {
    foreach ($element in $array) {
        Write-Host -NoNewline "$element "
    }
    Write-Host " "
}
```

```powershell
$random = Get-Random -Minimum 1 -Maximum 11
```

```powershell
param (
[Parameter(Mandatory=$true)]
[int]$lomb,
[int]$torzs=1
)


$lomb = $lomb-1
$torzs = $torzs-1

0..$lomb | %{
    $text = " "*($lomb-$_) + "#"*$_ + "#" + "#"*$_
    Write-Host $text -ForegroundColor Green
}

0..$torzs | %{
    $text = " "*($lomb) + "#"
    Write-Host $text -ForegroundColor Gray
}
```

```powershell

function Add-Numbers {
    param (
        [int]$Number1,
        [int]$Number2
    )

    return $Number1 + $Number2
}

$result = Add-Numbers -Number1 5 -Number2 7

Write-Host "The result is: $result"

```

```powershell
1..90 | Sort-Object {Get-Random} | Select-Object -Last 5
```

```powershell
Get-ChildItem -Path . -Recurse
$a = Get-ChildItem -Path . -Filter "*.txt"
```

```powershell
for ($i = 0; $i -lt $numRolls; $i++) {
}
```

```powershell
$number = 5
$greeting = "The number is: $($number * 2)"
Write-Host $greeting
```

```
https://github.com/AttilaMagyar/PowerShell?fbclid=IwZXh0bgNhZW0CMTEAAR2N0EBMyaC5VE_DQYQyn08KpkFhQvnYwclIqeYNrdbeu4I5_fFOh_2ELEY_aem_YnYGOPWBpRxBIt8ZS0gONA
```

```
https://github.com/Valentinusz/elte-ik-bsc
```
