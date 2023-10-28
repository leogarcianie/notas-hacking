# Redaction gone wrong
## Objetivo
Now you DON’T see me. This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?
## Solución
```
┌──(kali㉿kali)-[~/Desktop/picoCTF]
└─$ wget 'https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf'
--2023-10-28 18:58:42--  https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.154.144.85, 18.154.144.103, 18.154.144.104, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.154.144.85|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34915 (34K) [application/octet-stream]
Saving to: ‘Financial_Report_for_ABC_Labs.pdf’

Financial_Report_for_ABC_Labs.pd 100%[========================================================>]  34.10K  --.-KB/s    in 0.06s   

2023-10-28 18:58:43 (570 KB/s) - ‘Financial_Report_for_ABC_Labs.pdf’ saved [34915/34915]

La bandera se encontraba en el documento pdf, solamente que se encontraba con un subrayado negro por lo que no se veía, y copeando el texto se encuentra:

Financial Report for ABC Labs, Kigali, Rwanda for the year 2021.
Breakdown - Just painted over in MS word.
Cost Benefit Analysis
Credit Debit
This is not the flag, keep looking
Expenses from the
picoCTF{C4n_Y0u_S33_m3_fully}
Redacted document.

picoCTF{C4n_Y0u_S33_m3_fully}
```
## Notas adicionales
## Referencias