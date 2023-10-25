# python-obfuscator
Obfuscate python code using method from : https://pypi.org/project/python-obfuscator/

## <p align="left">📚・Example・📚</p>

### Normal : *obfuscator.py*
```python3
# __author : Ferly Afriliyan
# Do not change the original author's name 

from colorama import Fore, init
import subprocess
import importlib
import os, sys

# Warna teks
k = Fore.YELLOW  # Warna Kuning
a = Fore.LIGHTBLACK_EX  # Warna Abu-Abu
m = Fore.RED  # Warna Merah
h = Fore.GREEN  # Warna Hijau
p = Fore.WHITE  # Warna Putih
b = Fore.BLUE  # Warna Biru
v = Fore.MAGENTA  # Warna Violet
u = Fore.CYAN  # Warna Ungu
j = Fore.LIGHTWHITE_EX  # Warna Jingga


# Clear Terminal
def clear():
    if 'linux' in sys.platform.lower():os.system('clear')
    elif 'win' in sys.platform.lower():os.system('cls')

# Memeriksa apakah modul python_obfuscator terinstal
try:
    clear()
    importlib.import_module('python_obfuscator')
    python_obfuscator_module_installed = True
except ImportError:
    python_obfuscator_module_installed = False

# Cek apakah modul python_obfuscator terinstal
if not python_obfuscator_module_installed:
    clear()
    print(f"{h}[{a}•{h}] {p}Modul Obfuscate belum terinstal. Anda perlu menginstal modul berikut {a}:")
    print(f"  {a}- {p}python_obfuscator (pyobfuscate)")
    print(f"{h}[{a}•{h}] {p}Ketik perintah: pip install {a}python_obfuscator {p}")
    exit()

# Meminta pengguna untuk memasukkan nama file input
clear()
print(f"{p}█ ▄▄ ▀▄    ▄   ▄▄▄▄▀ ▄  █ ████▄    ▄   ████▄ ███   ▄████ ▄      ▄▄▄▄▄   ▄█▄    ██     ▄▄▄▄▀ ████▄ █▄▄▄▄ ")
print(f"{p}█   █  █  █ ▀▀▀ █   █   █ █   █     █  █   █ █  █  █▀   ▀ █    █     ▀▄ █▀ ▀▄  █ █ ▀▀▀ █    █   █ █  ▄▀ ")
print(f"{p}█▀▀▀    ▀█      █   ██▀▀█ █   █ ██   █ █   █ █ ▀ ▄ █▀▀ █   █ ▄  ▀▀▀▀▄   █   ▀  █▄▄█    █    █   █ █▀▀▌  ")
print(f"{p}█       █      █    █   █ ▀████ █ █  █ ▀████ █  ▄▀ █   █   █  ▀▄▄▄▄▀    █▄  ▄▀ █  █   █     ▀████ █  █  ")
print(f"{p} █    ▄▀      ▀        █        █  █ █       ███    █  █▄ ▄█            ▀███▀     █  ▀              █   ")
print(f"{p}  ▀                   ▀         █   ██               ▀  ▀▀▀                      █                 ▀    ")
print(f"{p}                                                                                ▀                      ")
input_file = input(f"{h}[{a}•{h}] {p}Masukkan nama file Input {a}: {p}")
if not input_file:
    print(f"{m}[{a}!{m}] {p}File '{input_file}' tidak ditemukan.")
    exit()
    input_text = None
elif not input_file.endswith(".py"):
    print(f"{m}[{a}!{m}] {p}File harus memiliki ekstensi .py {p}")
    exit()



# Meminta pengguna untuk memasukkan nama file output
output_file = input(f"{h}[{a}•{h}] {p}Masukkan nama file Output {a}: {p}")
if not output_file:
    print(f"{m}[{a}!{m}] {p}Isi dengan benar {m}! {p}")
    exit()
elif not output_file.endswith(".py"):
    print(f"{m}[{a}!{m}] {p}File output harus memiliki ekstensi .py {p}")
    exit()

# Inisialisasi variabel result
result = None

# Jalankan perintah pyobfuscate untuk mengobfuscate file input dan tangkap output
try:
    result = subprocess.check_output(f'pyobfuscate -i {input_file}', shell=True, text=True)
    print(f"File {input_file} telah dienkripsi. Dan tersimpan di {output_file}")
except subprocess.CalledProcessError:
    print("Terjadi kesalahan dalam mengenkripsi file.")
    exit()

# Simpan hasil obfuscation ke dalam file output jika result tidak None
if result is not None:
    with open(output_file, "w", encoding="utf-8") as output_f:
        output_f.write(result)

    
```

### Obfuscated : *main.py*
```python3
SSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSS = "oYPnmTSSmjPEUHLUVSjDGXlWqjBUOxDOsIhGWVGQSiOJeijyzinwOYpAlSUeFifzwHkCKQbuSNFCkXD"
k386 = 376
EdSaNNLevOaRjHIBEWosXCGPmmFdEJMbyhBBClcnBaJOvqGcyffzQhazgxndlrzIFFfCxwNPcYkHpZa384 = 225
lYZKikXiPWdqsxSEsKvMSARpgJqAzwrXSXKYsMlMKgddAvuvbmIZLxEyEFqArxwriulVkzHFOwOCyTa382 = "icgLHKbNMpopgScKuseXRhOVNwUuszxnmdtJwISjWKBWfUdXkmJHAGBAhnmzNJtXckLtbUMaoLYvMba"
lIllIllIIllllIlllllIIIIIllIlIIllIIIllIlIIIIlIlIIIlIIIIIIllIIIlIIlIIIlllllIIlIIIllllIIlIIllIIIllIIIIIlIllIlIIIlIlIIlIllllIIIIIlIlllIIlIIlIllIIIlllIlllIlIllllIlIIllIlIllIlIIlIIllIllllIlIlIlIIlIIlllllIllllIIIlllllllllIIIlIIIlIIlIllIIllllIIllIllllIllIIIllIIllIIIIllllIllIllIIlIlIllIIlllllIlIlIIllllIIllIIllIIIIlIlIllllIIllllIIIlIIIIIllllIIIlIIlIIlIIllIIIIIllIlIIIllIIllIllIIllIllllIll = 436
N378 = "ZPRtNCbInftFlRJaeqzyAEdODFrXOOllMoXdgaXpMFasxtATFHeTGNbTQbeJqrwIVdAJmiwHquicPHz"
E376 = "nwmNCKGzWLTlVeUQmFLwKaPmfLTBnabetXfTDRZimYLZbysjGxWzSGWvCrovbFQNDXlbECBOPJZjZNz"
i16982451640648017374 = 320
J16982451640648017372 = "DLkgrCnVGdICwpCvVtFcAzVuhLtLWOgurvOxqkxzhOCqASiWDKebdHmZTgogOmlnyBKNHhIETCvLHIw"
AAAaaaAaaAaAAaAAaaaAaaaaAaaaaAaAaaAAAaaaaaaaAaAaAAAAaAAAAaaaAAaaAaaaAAaaAAAaAaAAaAAaAAAaAaaaaaAAAAaaaaaaAaaAAaAaaAAaaAaaAAAaaaaAAAaaAaaAaaAAAAAAAAaaAaaAAaaaAaAaAAaAAAaaaaaaAAaaaAaaAaAaAaaaAaaaaAAaAAAAaaaAAaaAAAAaaaAAAAaAaaAaaaaAAaAAAAAAaAaaAAaAAaAaaAaaAaaAaaAaAaaAAAaAAaaaAaAaaAaAAaaAAaAaaaAAAAAAAaaAAaaaAAaaAaAaAaAAaaaaAaaAaAaAAAaAaaAAaaAaAaAaAAAAaAaAaAAAAaaAAaaaaAAAaA = "fdbbGgqGRXOspwZpDOyJNZAkqqxADjBYOlxNXiQYrRNshTzJsUdttGBDdCrdlYhadNbxdjrAjidxWSu"
B16982451640648017368 = 721
pttplLUOiNWVfAETcGlGGtiokHpWtLyNVHnysNNEgFTicWMQtHxUSoCAmvPOcvWgrAwGGtjhAujRZNw366 = 334
lIlllIIlllIllIlIlIlIIllIIIIlIIIIIIIlllIlllIIlIlIIIIIllllIlIIIIIllIIlIlIIlIlllIllIllIllIlIIIlllIIllIlIlIIIlllIlIllllIIlIIIIIIllIIlllllllIlIIlIIlIllllIIIIIIlIIlIllIIlIIlIIlIllllIIIllIlllIIIIlIlIIIIllIIIIIIlllIIlIllIlIIIlIIlllIIIIlIlllllIIllIllIIlIlllIIllllIIlIllIlIlIlIlIlIllIIllIIlllIIIlllllIIIIIlIlIlIlllIllllIlIIIIlIIIlIIlllIIllIIlIIllIIlIIlIllllIIIllIIllIllIllIl = 179
aAAaaAAAaAAaAaAaaaAAAaAAaAAaAAaaAaaaaaaaAAaaaaaaAAAAAAAAaAAaAAaaAaaAaaaaaAaaAaaAAAAaAAAAaaaaaAaaaaaaAAAAaAaAAAAaaaaaaAaaAaaAAAaAaaaaaaAaAAAAaAAaAaaaaaaAaaAAaaAaAAaaAAaAAAAAaaaaaAAaaaAAAaAaAaaaaAaaaaAaaaAAaaAAaAaAaaAaAaaAaAAAAaAAAaaAaAaAaAaaaAaAAAAaAAaAAaAaaAaAAaaAaaaaaAaAaAAAaaaaaAaAaaAaaaaAAAaaaaaAAAAaaAaAAaAaaaAAaaAAAaAAaAaAAaAaaaAaAAAaAaaaaaAaAAAAaaAaAAAAAa = 337
aAAaaAaaAAAAAAaAaAAaAAAAaaaAaAaAAAAAAaAaaAAaaaAaaAaaAaaAaaAaaaAaAAAAAAAaAaaaAaaaAaAAaAAAaaAaaaaAaaaaAAAaaaAaAaaAAaaAaAaaAaAaAAaAaAAAAaaAAAAaAAAAaAAaaAAaaAAAAAAaAAAAAAaAaAaAAaaAAaAAAAaAAAaaAAaAaAaaAAAAaaAAAAaAaAaaaAaAaAAAAAAaAaaAAAaaaAAaaaAAAaaaaAAAaaaAAaAAAAAaaAAAaaAaAaAAaaaaAaAAaAaaaAAaaaAaaaaAAaaaAAAaaAAaAAaAaAAAAAaaAaAaaaAAaaAaAAAAaAaaaaaaAaAaaaAaAAAaaAAA = 714
B1698245164061802358 = 517
lIIIIlIllIIlIIIIIIllIIlllllIIlIIlIIIIIIllIIlIIIlIIIIIlIlIIllIlIIllIIIIIlIlllIllIllIllllllIIIlIllIIIIIIIlIIlIllllIIIlIllIIIIIIllIIIIIIIIllIIllIIllllIllIIIllIlllIIlIlIlllllIllIlIllIIlllllIlIIlIllIIllIlllllIIIlIIllIllIIIIlIlllIlIIlIIlIIllIIIIlllIllIlIIlIlIIIIIIlIIIIllIIllIIIIIIIIIIlIllllIIllllIlIIIIlIllIIIlllllIlllIIlIlIlIlllIlllIIIIIIIIlIIlIIIIIllIllllIlII = 393
IlIlIIlIllIIllIllIlllllIllIlIIIIlIlIIIIlllllIIIllllIllllllIllIllllIlIlIlIlllllllIIIIlllIIlllllIIlIlIllIllIIIIIllIlIllIlllllIIIlIllIIIIlIlIIlIllIllIIIIllIllIIIlIllIlllIIllIIlIIIlIIIIllIIlIIIIIIlIlIllIIIllIIIIIIlIlIlIIlIlIlIlIlIIlIlIllIlIlIIIIIllllllIIllIlllIIIllIlIIIIlIllIllIIIIIIIlIIIIllIlIllIIllIIllllIlIllllIIllIIIIlIlIlIlIlIlIIIlIllIIllIlIIIlIIIIllll = 468
jjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjjj = 274
WWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWW = 466
aAaAaaaAaAAAAaaAaAaaAAAAAAaAaaAAAaaAAaAaAAaaaaaAaaAAaAaAaAaAAaaAAaaAAAaaAaAaAaaAAAaaAAaAaaaAAAAaAaAAaAaAAAAaAAAaAaaAaaAAAAAAaAAaAAaAaAAAAaAAAaAaAAAAAAAAaAaaaAAaaAaAaaaAAAAaaAAAaAAaAaAaAaaaaaAAAaaAaaaAaAaaaaAAAAaaAaAAaAAAaaAAAaaaAaAAaaAaaAAAaAaaaAaAaaaaaAAAaAAaAAAaaaAAAAAaAaAaAAaAAaaAaaAaAaAAAAAaAAAAaaaaAAAAAAaAAAaaaaaAAAAaAAAaAAaAAAAaAaaaaaAAaAAA = "nOoKlTRawaRviuHWFnImktmHwQSgkZbohBQJunvtXXkoIsrStsHZiaNYifdKcVLyovoxjyCjBbgAyTy"
IlIIlIIIIlllIllllIIIIlIIlIIllIIllIlIlIIlllllllIlIllIlllIIIlIlllIlIIlIlIlIlIllIllIlIIlIIlIIIIllIIllIIlIIllIllIllIIIIIIIIIIlIllIIllIllllIlIllllllIIllIlIIlIllIIlIlIIIIllIlIlIllIIlllIIIllIIIllllIlllllIllIlIlIIllIlIlIllIIllIIllIIlIIlIIIIIIllIIlIIIIllIlllllllIlIIIllIlllIIIIIIlIIlIlllIIIllIIlIlIlIlIlIIIllIlIlIIIIIIIIIlIIllllIlIllIlllIlIIIlIIIlllIIlIIl = "mQpWYFTIyoeasqnMQciyncYQahZHISRpYJHLBlsXSjgezDYqteMtORDbTfEtJSlpJYKxQNFAXUuxMvp"
aaAAAAaaAaaAaAAaAaAaAaAAAaaaAAaaAaaAaaaaAAAAaAaAaaAaaAaAAaAAAAaaaaaAaAaAaAAAAaaAAAAAaaaaAAaaaaAaaAAaaAaAaaAaaAAaAAAaaAAaAaAaaaAAaAAAaAAAaaAAaAaAAaaaAaAAaaaaaAAaAAAAAAAAAAAAAaAaaAaAaaAAAAaaaAaAAAaaAAaaAaAaaaaAaAaaAaAaAAAAaAAAAaaAAaAAAAAaaAAAAAAaAaaaaaaaaAAAaaaAaAAAaAAAAAaaaAAaAAaaaAaaaAaAaaaAAAAAAAAAaaAAAaAAAAAaaAAAaAAAAaaaaAaAaaAaAaAaaAaaAAAA = "TleIQFbrSyreFcJmTTWbvYwAPPiTcpCloTjMbaNPdqXDZFysQugdaRbPaJgOdMFxNGMyazHkcTyBcJM"
u16982451640596929342 = 680
YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY = 434
W16982451640596929338 = "YrRQZPgaNyhYufPhSVuzqdHLRlNASkrVLsGDVptIedGXNTWRBYHImYlZYmcRYOxXjIFYotHKYcidCFn"
eeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee = 665
r16982451640596929334 = 317
AAaAaAaAaAAAaaaaaAaAaAaAAAAaaAaaaaaaaAaAAAAaaaaAAaaaaaaaAaaAaAaaAAAAAAaaAaaaAaAaaaAAAAAaaaaAaaAAAAAAAAaAAaaaaaAaAAaaaAAaaaAaaAAAAaAaAaAaAAAAaaaAAAAaAAAAAAaaAAAAAAaaAAAaaaAAaaaAaaAAAaaAAaAaaAaAaaaaAAaAAAaAaAaAAAAaaAaaaaaaAAaaAAaaAAaAAAAaaAAAAAaaaAaAaAAAAaaAaAAAaAaAaaAAAAaaaAaAAAaaaAaaaaaAAaAAAaaaAAaaaaAaaAAaAaaAaaaAaAaAaAAaAAaaAaaA = 411
Z16982451640586934330 = "iDuUFVlYWCYlILDYkArwbIMoAMlkBxuWMHQIEHmkLypvBfSNeAVPUgvjOenbUVpsuADrCjxCCbZGZhr"
aaAAaaAAaAAAaAAaaaaaaaAaaAAAAaaAAAaaAAaaaaaAAaAaAaaAAAaaaAAaAAaaAAAAAaAaaaaaaAaaAAaaAAAaAaAaAAAAaaAAaaAAAaAaAAAAaaAAaAaAAaAAaaAaAAaAaAaaaaAaAAAAaaAaaAAaaaAaaaAAaAAAaaAAAAaAaaaaAaaaAaAaAaaAaAAAaaaaAAAaAAAaaaaAaAAAAAAaaaaaaAAAAaAAaAAaaAAAAaaaaAAaAAaAAaAAAAAaAaaAaaaAaaaAaaaAaAAAAaAaaaaAAaaAaAAAaaAaaaaAAaaAaAaAAAaaaaAaaaAaaaaAaaAA = 379
j16982451640586934326 = "JqTqHtibWWqToxdWQvXaxVoETsoNBBALlIBHhqsbfHAkfLFCXXPexMUBPLXofrFAbdPlBpRzAOWlWMX"
v324 = "EVUPvfJpyqyVuVpLAouwskWdPezXRaxEmDtYyZrdKomClFJBehxCGQrOxNGzrPcNVbtcpbYJGkOAhtq"
FkfIghOALsNLaKtKJVyUeWOURcnLTdPAChTysofvFsmTVeiIZXfAdNaMjOtrRPnrLxFOfTmRGutQgpN322 = 111
WFZrPrEplSAIMQVRyFgBSllVTWISloGnyfdFpjHrTVkaqkdqsHDLliHszGqfgwWLTOGgQVtpbDlxnsU320 = "kWxbGCHymMDqSAmzoAvwbSYMsvohXerBWkaOMZmgLCQXvMQjJBHoSYLwGbIlczTfGqQaRbWHbqizXLU"
KosfHWaNAVlfLisVuGwwAvxWrtmpSNHcKDcIEzFxRwMzEHHcLOGNhSAzZUwiSQOKjUtGWvbrSdsaFrM318 = 257
llIIIllIllIlllIIIllIIIlIlllIllIlllIlIlIllllIllIllIIllIIIIIIIIIlllIIllIIIIlllIlIIlIlIlIIlIIllIIIlIIIlIlIIIlIlIlllIlIIIlIIIlIIIIIlIIlIlIlIIIIIIIIIllIlIllIIlIIIlllllIIlIIIIllIlllIIIllIIlIIllIlIlIIIIlIllllIlIIllllllllllIIIIlIIIIIIlllIlIlllIlIIIIllIllIIlIllIllIllIllIllllIIIIIIIllllIIlIIIIlIIIllIlIlIIlIIlIllIlIlllIllIIII = 225
x16982451640566933314 = 202
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx = "SXGwlIXlwWGHvhyXIrIGGzTBJaWDbKcJMRxqKmERLqCeHKJioviyZwoDnjbddtfMUfaplbWTocwMSys"
lIIIIIlIIIIllIlIlIIIIIllIIlIllIllIIlIIlIIlIIllIIlIIIlIIllIIlIllIIlIlIlllIlIIIIIlllIllIllIlIIIllllIllIllIIIlIlIllIllIlllIIIIIIIlIlIlllIlIIlIIIllllIIlIIIIIlllIIlIIIIIlIIIllIIlllllIIlIIlIlllIIIlIIlIIllIIIIlllllIIlIIlIIIlIIIIIIlllIIllllIIlIlIIlIIIllllIIIIllIIlIlIIIllIlIIlIllIIIIlIIIIIlIIllIlIlIlIIllIlllIIIIIlIIIl = 686
m16982451640556934308 = "fibOQnvBxFkqOzVapbGulsCDArajcooKZHRZgjUvCkwenUsRqTGeNYKwRxaDjwcqLOuTxlmPSIsMaMo"
lllIlIIllIIIIIIIIIIIIIllIIIlIIlIIIIIIllllllIlllIIIIlIlIllllIlIIlllIIIlIIlIIllllIIIlIIIIlIIIllIIIIllIIIlIlllIIlIllIIllIIIIlllIIllIlIlIIIIIIlIlIIlIlIIlIIIIllIIIlIIllIIIIIIlllllIIIIlIIllIIIIlIIllIIIIlIlIIlllllIIIllIlIllIlIllIIllIllIIIlIIIIllllIIIlllIIlllIIllllIIIllIllIlIIllIIllllIlIlllIIIIIlIlIlllllIlIlIllll = "cnMRmcWTOkEGcgxpxzgxSrTWPkvBtTFcGUyYyCOoWSYxvPWrZsLBMXarHQtqqFwogYYpBNqNnkneckj"
lllllllIlIIIlllIlllIIIllIlIIlIIlIllIIIIIlIIlIIlIllIIIIlllIIIllllIlIllllIlllIIIIIlIlIIIlIIlIIIIlIlIIllIIlIIlllIIIIIIllIIlIIlIIIllIIIIlIIlIIIIIIllIIlIIIIIIIIlIlIIIIIIllIllIIlIlIIIIIlIIlIIllIIIlIIlIlllllIIllIlllllIlIlIIllIIlIIIlIIIlIIIllIlIIIlIlllllIlIIIlllIlIllIIIIIIlllIlIIIlIIIIllIIlIlIIllIIllllIIlIIIIll = 424
hteymsLDjcVAfQQNmOjJyeHntVFuWDxZlatIXgCPBjxWLdLRhOEGCZLuHWEFrRbrlyNOopjsBueyKjH302 = 162
iZHJExiUSEZgPVNOPUBdpEaiKpKXPhWAxBkxvPMALpQRVIlfhZYQFWTBsfKwXxoaSIVpvLPWkZsBMXA300 = 443
g298 = 450
r16982451640546932296 = 993
bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb = 573
i292 = 137
FFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF = "EAFqQcRQvOOgvLibGdZBqtxXcswtFdohzGUVhGajdjCDuGBQcfkfNjuKiMFDAkRLvHcKShHyGCexWcN"
x16982451640536926288 = 352
VaNYRIWJVdVRIusyQxBJFrxyXblApXREYhQNcelggywapjijjseLvRciyaDHoiQTSleAZfZjPMdNMLc286 = 167
LLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLL = "NdbGUQoiZDPQAWMiqdCmCOqVlCSvrxGmvekyBphhdnwOARMsDgsTkNlqfVuCBMMRWzOYgxSefydorFB"
AAaAaAaaaaAaaAAaaAAaAAAaaaAAaAAaaAAaaaaaAaaAaAAaAaaAAaaaaaaaaaAaaaaAAAAaaaaaAAAAaaAAaAaAAAAAaAAAaaAAAAaAAAAAaAaAAaaAaaaaaAAAaAaAaaaaaAaAAAAAaaAaAaAAaaAAAAaaaaaaaAaaAAAaAaaAaAaaaAaAaAAAAaaAaAAaaAaAaaaaaAaAAaAAaaAAaaAaaAAAaaAaAAaAaaaaAaAAAAAaAAAAaAaaAAAAaAaAAaAAaAAaAaAaAaaAaaaaaaaAAA = 286
tttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttt = 287
IIIlIlllIlllIlIIlIIlIIllllIlllIlIllIIIIIlIllIllIllIIIlIIIIlIIIIIIlllIIllIlllIlIlIIllllllllllIllIIIlllIlllIIIIIIlIIIIlIIIlIlIIIllIIIlIIIllllIlIIlIIllllllIlIllllIIllIIIIIIIIIllllllIlIlIllIIllIlIlIllIIlIlIlllIlIlIlllIllIllIlIlIIIIIllIIlIIIIIIllIIIIlIlIlllIllIIIlIllllIIIlllIlllIllI = "jYPAIVcrilqdiJqxOYHTQaTGWbnghSRbutRNpHnFidbuocLlaspWvZVuLdHXQWMFwRSOGyEGLQajFCW"
bumQHXQkiBQGVsVkcuuOstxanFRiEIvmVvzuBVmvrxPJJQxIQCqBwvIGjzCdKCmLTfPhcrLIYfkbOqF276 = "yEOFWmfrNoISLAEQfVkdQHpGUpaveqoLVUFUVSMKAyeUjaXiHpdqAjOHBCyoDFVGbcnNeFTJzTGidkS"
AaAAAaaaaaAAaaaaAAaaaAAAaaaAAaAAAaaAaaaaaAAAaaaaAaaaaaAAaAAaAaaAAaaAaAAAAAAAaaaAAaAaaAAAaaAaAaaAaAaAAAAaAAAaaaaaaaaaaAaaaAAaaAaAaaAAaAaAAaAAAAaAaaAAaAaaaAaaAaaaAaAAAaaAaaAaAaAAaaaaAAAaaaAAaAaaAAAaaAaAaaAAAAAaAAAAaAaaAAAaAAaaaAaAaAaAaaaAaAAaAAaaAaAaAAAAAAAaaaaAaaaAaAaAaAaaAA = 473
D16982451640516937272 = 802
zzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzz = 331
lIlIIlIllIIIIllllIlIIIIlllIllIllIlIlIlIlIIIlIlllIllllIllllIIlIIIIlIllIllIIlIlIlllIlIIIIlIllIIIlIlIllIlIllIllIIIllIlllIlllIllIIIllIllIIlIIIlllllIIIlIIIIIlIIIlIllIIIIlIllIIIIIlIlllIIllllllIlIIIIlIIlllIllllIlIlllIIllllIllIlIIIIIIIllllIlIIIIIllIlllIllIIIllIlIllIIIlIllIlll = 395
yQRVHRKfghFdHClhYTlpHnMDcDQHDHiThfAzLxGybnzXsGoUaUfIztJqBPQjgHsNRzfFyiPaTkvlWXT266 = 385
ZssMgWzyjaiZMNixcQnYKRwSqcMxfNAUtEqlWWdgvAgCftaxUZGspdViSdSzBJMEYHjmjQThcqUBGhr264 = 365
AAAaaAAaAaaaaaAaAaAaaAaAaAAAaAaAAAAAAAAAaAAaAaAAAaAaaaAaAaAAAaaAAaaAAAaAaaAAaAaAAAaaAAaaAAaAaaAAaaaaAaaAaaaAaaAAaaAAAAAaaaaAaAaaaAaaAAAaaAAAAAAAaAaaaAaaAAaAaaaAAaAAAaAAaaAAAaAaaAaAAAaaaAAaAAAAAaAaAAaAAAaAaAaAAaaAaaaAaaAAAaaAAAaAAAaAaAaAAAaaaaaaaaaAaaaAaAAAaAAAaA = "QMtuJRwCkOONawKgZOwpOBPSuTQNdFyqxvoADfzvXCDaQKMFtpyiNrxIJHtDQkpjXwbDGMTEFdKKFmc"
IIIIllIlllIlllIllllIlIlIlllIllIlIlIlIlIlIllIllIlIlIlIIIIlIIIlIlIllIIIIIllllIlIlllllIlllIIIlIIIIlIlIlIIIIlIlIIllIllIlllIIllIIlllllIIIlIIIIIllIllIlIllIlIlIlIlIlIlIIIlIlIllIllllllllllIllIllIIlIIIlIllllIIIlIIIllIIllIlIllllllIIIIIlIlllIIIIIIlIIIIIlllIlIlIIlIlIllIII = 490
aAAaAaAaaAaAAAaaAAaAaaaaaAaaaaaAaaaaaAAAaaAAAaAaaAaaAaAAaaAAaaAAAaAAaaaAAaaAAaAAaaaaaAAaaAAAaAaAAAAaAAaAaAaaaaaAaaAAaaAAaaaAAAAAAAaaAAaAaAAaAAaaAAAAAAAAAAAaAaaAaaaAAAAaAAaaaaaAaAaAAaAaAaaaaaAaaaAAAAAAaAAaAaaaaAaAAAAaAaaaaAaaaaAAaaAaaaAAAAaAAaaaaaaAAAAaAAaaAa = 339
J256 = 158
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx = 204
llllIllIIllllllllllllllIlIIlllIlIIllIIIIIIlllIIlIlIlIIlIlIlllIIlIIIIlIIIlIlIllIlIllIllIIllIIIIIIIIIlIlllIIIlIIllIIIIIIIllllllllIlIlIIlIIlIllIIIlIIIIIlllIIlIlIIlllIIIIIllIlllIIIIllIIlIIllllllllIllIllIllIIlIIlllIIlIIllIlIlIlIlIIIIllIllIllIIIIIIIIllIIIlII = 275
fPaRwvmEAjpevGjZNnWalLkUrqARzgaCGlcDSSacUlmkFolZJCYdVvwzjbZLrvpzWSijIoWMwiDMUVD250 = "xWdgzarhmXAOjQBlAwCMveoWpCBtfbSZlVRDeoSjeolVGpJMxqsJGAcXXoAKurCaYmflBsSaiJZLRxF"
llIlllIlIIlIlIIlllIIlIllIllllIlllIIIlIIIIIIIllIIlIlllIIlIlIlllIIlIIllIIIlIIIlIlIIIIlllIlllIIIIllllIllIIllllIlIIlllIIlIlIlIIIlIIllIIlIIlllIlIlIllllllIIIlIIlllIlllIIIIIIllllIIllIlIIIIllllIIIIllIIllIllIIIllllIllIIlllIIIIlIlIIIIllIllIIIIIIIIIIllllllIlI = 865
e1698245164048801246 = 691
G244 = "laZgBTiJHjsCTrwXMvVSnzLcKyoYNQwrgUjtJbMFZNPNyGcyIjUJGtKqSpMUmmhMbEIrOrrPyIeVOZP"
aaaaaaaAAaaaAaaaaAAaaAaaaaAAaaaAAAAAaAaAaaaaAAaaaaAaAaaAAaAAAaaaAAAaaAAaAAaaAaAaAAaAAAAAAAAAAaaAaAAAaaAAaAaaAAaAAAAAAAAAaAAAAaaaAaaAaaaAAAaAAAaaAaaAAAAaAaaAAAaaaaaAaAAaAAAAaAAaAaAaAaaaaaaAaAAaaaaaAAaAaaaAaaAaAAaAaAaaAAAaaaaaaaAAAAAAAaAaAAAAAa = 466
IIllIIlllIIIlIlIIlllIIlIlIIIlllIIllllIIIIIIIlIIIIIlIlIlIlIllllIlIIIlIlIIIlIlIllIlIIIllIlIIIIIlIIIIIIIlllllIllIIIIlIllIlllllIIlIIIlIIllIIlIIlIIllIIlllIIlIIIlIIIIlllIlIIlIlIlIlIIllIlIllIIlIIIIIlIIIlIIllIIIIIlIIIIllIllIllIIlllIIlIIlllllIlllllI = "ikWSIUphVkSBMkLsnqloeHNtYuHdDKOozSAbgQfMTcPtMuZXbBeTSLQWFhwNwPccHOWohBUtJxBsKGV"
RKOhrlFxATOVeFPhFSJcaCgSZQHcTzPBEqDBblfirndBEfqTPEpiYqQKaAWdhiygrOqtwGmuTJEDTad238 = "SNrxslmLeDezOSBpStGCBIuEcjCQXUZdyhtdxwmHhbuIsXSGMuldaeJkiGUFwAHooEXoZUbdvdjDVjy"
nnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnn = 292
SpnFWqhDSmyNOdmHxtWoTRdnkrhZIwBBlRLhcSffZiayidBxCkZJZIfUKAEtyJLzMfharkORuRTaTuL234 = "xxJkBGLDiupcaKEuNWFwcCjHuwriBUwhXBwuSkrMRDvrwQnVLLHYxzBgZkCxheZvYcRCywrNkyObAbi"
YpPmCHNTAexNYnucYFLIyZjqqvusHxXJqZLSBfQhGjIKLrapGrgkOXgWJuCOjmUXfgZbnKchUvHmjMQ232 = 191
aAaAaAaaAAAAaAaaAaAaaAaAAAAAAaaAaAaAaAAaaAAaAAAAaAaaaAAaAaAaaAaAaAaaaAAAAAAaaAaaaaAAAAaAAaaAAaAAaaaaAaaAaaaAAAaAaaaaAaAaaAAaAAAAAaAaaAAaaAaaAaAaAAAAaAaaaAaaAaaaAaAAaaAAaAAAaAaAAaAaaaaaaAAaAaAAaAAAAaaAAAaaAaAaaAaAAaAaaaAAAAaAAaaaaA = "bHIVyBCeHLNnDriEoCkXfoWSlcYeBVTNNuGyZFWHiycTsexRlEqULZfQAkYBxwsiCAUfqyJEwnTRDtZ"
IlIlllIIlIlIlIIllIllIllIIllIIlIIlllIIIIIIlIlllllIllIIIIIlllllIIIllIllIllIlIllIllIlIlllIIIIIlIIlIllIIIIIlIIIlIIllIIIIIIlIIIIIllllIlllllllIIIIllIIllIlIIlllIllIlIIIlIIIIlIlllIIIlllIlIlIlIIIIlllIIllIlllIllllIIlllIlllIIIIIlIIIlllIIll = 627
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA = "njuKNDVrwvvZQopYFQSfFKDbFwwAZRJVClpqXcvZzDLIxmOpTeKODmlbVxOCNxywbVsgzzApaTkERsF"
IIIllIIlIIllIllIIIIllIllllllIlIIIlllIlIIIIlIllllIlIIIllIIlIllIlIlIlIllllIlIIIIlllIIIllllllIIlIIlIIIIIlIIIlIIlllIIlIllIIlllIIlIlIIlIllllllIlIIllIllIIllIIIIIllIIllIllIIllllllIlIIlIlIIIllIllIlIlIIlllIIIIIlIIlIIIlIlllIIIlllIIlII = 319
llIlIlIllllIlIIlllIllllIlllIllIIIIIlIllIIIlIIlIlllIIIIIIIIlllllIIIIIlIlllIlllIIIlIlIIlIIlIIIIllIIIlllIIIlIIlIIllIllIIIIIlllIIllIlIIIlIIlIlllIIlIlIllIlIlllllIlIlIlIIIlIlIIlllIllIlIIlIIIIllIIllIlllllllllIIlIlllIllllIllIllIll = "dbmEjcIxIBxMPscylXarTQmzGfvHpttZiLOikiiFNeHAQGxqLcNWzDFTpyUNvCeCFRJgrgYqxHMeBXh"
hWOvkoZddGYpQzlsnUojbDGdKlnIldMBsCUCkCkaUHcYaooMAlyCJzatBhYdffzOCqEvgLecQZenPUs220 = "KDcCphlvXObNKKEXYfeQKXDOfmASwRYprHqXTlNXThicxDfmUyTFloWgUdLpRWOWpxGCNIKqiJUYfnT"
aaAAaaaAaAaaAaAAaaAAAAAaaAAaAAaAAAaAaaAaAaAAAaAAaAaaAaaAaAAaAaAaaaaAAaaAAAaaaaAaAAaaAAAaAAaAaaAaaaaaAAAaaaAaAaaaaaaAAAAAAAaaaaAAaaaAaAaAaAAAAAaaAAaAAAAAAaAAAaAaAaaAaaaAAaAAaAAAaaAAAAAAAaaaaaAaaAaaAAaAaaAaaaAAaAAaAaaaAA = 222
qqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqq = "HREZpBOKeyqdoAmjdNlBXVClyXHRBtFXHwqdJDGtDlJxTouEkTuBKTmOkSvDVsBakvkgdABRKJYtbNj"
aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa = 664
aDinRzzcdvLTWimTlQYZmdThGlRrsmdZFqNKMWTZRbzcGdlRkMcfTsIoKNmnnVmHLqcVGrlMWzhuXns212 = "SPmCBaHXVguBwFUzvHxzBbwBIcXuRxUIwCWNhhRooEdLAVrirzbAOCSobgcjdoaAHMDXBfwlKrgPOld"
KxlZKSQntzwveETMjqdKDqQBjIObaaUeQXShMpnvsGVJDyeExQysweTLhClJNrIiqNqWWQuhBxeLsDs210 = 279
i208 = 264
ZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZ = "mBBPSKvHtpPXFFbDUZLJvciqFdTXbLkAZeaBgYigZyBtLMsafYteAGfyazUzAnthetWVbvzTOuXXmiJ"
AaaAaAAaaAaaAAAaAAAAAaaaAaAaaaaaAAAAaaaAaaAaAAaAaAaAAAaAAAAAAaAAaaAaaaAAaaaAaaaAaAAaaAaaaaaaAAaaAaAaAAaAaAaaAaaaaAAAaAAaaAAaAAAAAAaaaaaaAaAaAAaAAAaAaAAaAAAaaaaaaaaAAaAaaaaAaAAAaAAAaAAaAaaaAAAaAAaAAaaAAaAa = "GYmWBKtCsDWehKADhgYZUXQZMUOefMpbJkQPhzSQEpxVeDJrNvJfTmAERCkfFbzXGhtoMYmYHNhSTBw"
AAAaAAaaaaAAAaaAAaAAaaaaaaAAAAaAAAAAaAAaaAAaAAaAAaAaAAaAaaaAaAaAaAaaAaAAaaaaaAaAaaaaaAaaAAAaaaaAaaAaAAAaaaAAaaAaAaaaAAAaAaAaAAaAaaaAAAaaaAAAaAaAaAAaaAAaAAaAAaAAAAaaaAaAaAaaaaaaaAAaaaaAaaaaAaaaaaAAaaaAaA = "OgNvFHCUVdHdMhnrkcSjYxWklcJMecRFQvTXJSHmNwqmejcuUaTInlaguTJfeQPTMrMotfSAWyzwyab"
g16982451640438023200 = 247
K16982451640438023198 = "wcXzTCcjQtsCNaCWEtUOIzjzVvqurWinYWFJDqZfnynDquYbpSbZFltJywNTHuhBxfoUHbWOAHeiMvb"
qJghllnqVTFdnJYOMWcqJQZtAFvJswtbcibcMjSIsNWqoZANumtsRbEnHZbRxbzcugXdwyuuRKtHdhU196 = "KMldhCxWbZxegdyedrEeDcyoxIGSfnMoprPzHsxgknKUoYxiwjouvRGLFiGKqSnlLWVNBUntmEMqByo"
iClWLyYobyCBnWTtMwdxfRWfqhlBJjeEIVYXTSsxfuTKXPahSpnmFDebZHURnVFquDPTGoNpHlNgOhJ194 = 554
oooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooo = "BwpEpBYNJyVDmHYoXwmTOeozgYpwxHNbrpLEnPIAaGKmkViOACkrAXbPfwwVRimWfOMdEtzkaMvSShU"
vGuEDpDumOAWTnSiRbWmNlDlGfUxWDGgEMgmhQrwFotkfuIWsgwlPtTzjjMFiRhDUIDtFOLBRJmJzwR190 = "OpuJkdzMQtXaAAynGlkFOKlKqScKKoGVNolJruoDStzLHVlqSnbRoZNvKgYyLzvlACRJMpPZhpNLgQU"
IllIIIIIlIlllIIIIllIIIIIlIlIllIIIlIIlIIIlllIllllIlIllIlIllIlIlIlIIIllllIIIIllIIlIIIIIIIIlIllllIllllllIlIIIIIlIllllIlIlIIllIIllIIlIIlIIlIlIllllllIIIIIIlllIIIllIlIllIlIIIIIIlIlIlIIllllIIlIlI = 757
lIIIIlIlllllIllIlllIIllllIIlIIlIlIlIlIlllllIIlIllIIIllIllIlIlllIllIIllIlIlIllIllllIllIIIlIIIIIllIlIIIIllIIIIIlIIIIlllIIlIlIIlIIIIlIllllllIlIllIIllIIlIlIlIIIllIlIIIIllIlIIIIllIIlIIIlIllll = 472
lllIIllIllIIlllIlIlIIIIIlllIIIIIlIIlIlllIIIIlIlIIIllIlIllIIllllIlllllIIIIIlllIlllIIllIlIlIlllIlIlIIlllIlllllIlIlIIlIIlllIIIllIIIIIlllIlIIIIlIlIlllIllIIIlllIlIIIIlllIIIlIlIlIllIIIIllIll = 399
rWSBDvSigJsdlqbUbEAzuQryPnCxDzhiUyIAzLtCfHmcozHXFjJZVFMWqJYRQTvEvJklhDSVGdZegFw182 = "JZGBneKBqupuQxrpMVKqhNZRcPuXDYcAEFPRPVmxEYYRsRsbrtYVcrhepLLZigcGypEKwmfXZlQEzew"
lIllIlIlIlIIIllllIlIllIIlIIlllIlIllIIllllIllIIIIlIIllIllIIIIIIIlIIIlllllIlIlllIIIlIllIlllllIIIIlllIllIIlIIllIIIIllIIlIlIllllIlllIIlIIlIlIIlIIllIllllllllIlllIlIllIIlllIlIllllIIlIlII = 367
AaAAAaAaaaaAAAAAAAAAaaaAaaAaaaAAaaaaaAAaAaAaAaAaAaAAAAaaaaaAAAAAaAAaAaaAAaaAAAAaaAAaaAAAAAAAAaAaaAAAaAAaaaAaAaAAaaAaaAaAaaAaAaaAAAaaaAAAAaaaAaAaaAaaaaaaaAAAaAaAaaaAAaaAaaAaaaaAAA = 513
LLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLLL = 166
I174 = 274
gLdLWbZBFSKxIfdQtfbuJWByMlLZWCgIBzZtnUyNFKUCqRguEGYTOHFqROcpscuzgGgNSVPUzBNnlWt172 = 353
NjXVkVyamxlkpQKTZsHyoWvAqPyMXLkZZOKDiOPoRPJCRaldfuKsfhkeRaAUCQtqmDZVDtfhsrXKJip170 = "onTenlOgZQaRxdmrRVJyFNGdwtGbMzrAtyfdTvRxDhIoADwmcAJMBjbrNTIkKlhEbmBejlZgrnwVobr"
bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb = "XjQAhjjVpWOBUBurwPdYaNistYVKohQzLPgZWDlLQQtymdMAOSTwHsHzbyitlnJXCYBQrQKdCqBpsyk"
zzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzzz = 604
BBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBBB = "BubyNyeQYETvnIuOgQJYvNlfLkHjHQxCXfreLnuUewjxUwnaQAfUxkByuXVHfRXwxNcWZTHAGksJkjJ"
lertTYqeMXhzHWJzGtTWLnQtMpZNUkbheIieAbInfpahGwsgzQYPjDltgLBXtnbEpxmUPjRTIFxdNAT162 = 582
AaaaAAAAAaAAAaAAaAAaAaaaaaaAaAaAAaaaAaAAaAAAaaaaaAAaaAaaAAAaaaAaAaaaaaaAaaaaaAAaaaaAaaaAAAaAAAaAAAAAaaaaaAAAAaaaAAAAaaAaaaAaAaAAAaAAAaaaaaAAaAaaaaAAAAAaAaAAAaaa = 346
p158 = 126
g16982451640408337156 = 483
aaaaAaAaaaAaaaaAAaaAAaAaAAAaAAaAAaaaaAAAaAAAAAAaaaAAaAAaAAAAaaAAaAaaaAaaaaAaaaaAAaAaaaaaAAaAAaaAaAaAAaaaAAaaAAaAaaaAaaaAAaAAAAaaAAaAaaaAaAaaAaaAaaAaAAaaAa = 310
YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY = 366
aaaaaaaAaaaAAAAaaaAAaaaAAaaaAaAAAAAAaAAaAaAaaAaAAaAaAaAaAAAaAAaAAaAaAaAaAaAaaAaaAaaaAAAaAaAAAAaAAaAaaaaAAaAAaAaaAaaaaAaaaAaaAaAAaAAaAaaAaAaaAAaaaaAaaA = 625
x16982451640396926148 = "zgIKvhyaorfjDYKzNqsCVSXlACXZPwpQrIVVKmdFYIDaVKkVGMAkNgDnyhKSDepvKOIlVfxvZKAmtqa"
NDSVgSmsieCdurKsobNtlqlXnAzlSTUoBoFLflyhbDwWEHSnQGosPgZUAkMQOfQjUwxzXjnTvWdTIwY146 = 432
lIIllIIlIIllIIIIllIIIlIIlIIIIIlIlIIlIlllIIIIIIlllllIIIIlIlIIlIIllIIIllIIIIIIlIllllllIlIlllIIlIllllllIIIlIllIlllIIlIIlIIlIIIllllIIllIlIIllIIIIIIl = 228
SSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSS = 364
IIIIIlIIlIlIIIlIlIllIIIlIlIllllIlIIIllllIIlIllllllllIlIlIllIllIIlIIIllllIIIIlIllIllIlIIIIIlIlllllIIIIIlIIIlllIIlllIllIllllIIIlIlIllIIlIllIIl = 898
aaaaAaaaAaAaaAAaAaAAAaaAaaaaaAaAaaaaAaAaaaaaaAaAaAAaAaAAAAaaaaaAAAaaAaaAaAaAaAaAAaaAaaAaaAaaAaaaAaaaAAAaAAaAaaAAAAAAaAAAAaAaaAaaAaAAAaAaAA = "badhwSKaXeYRshmKBaomyIsIhDUJBjUpfGNbYcEwgmyHuzDxmoRMaUcgdDpnkKPklmgRVidxWjYqwGe"
AaaAAaAAaaaAAaAaAaaaaAAaaaAAaAaaaaaAAAAaAaAaaAAAaaAAaAaaAAAaAAAaAAAaAaAaaAAaaaAAaAaAAaaAaaAAAaAaAAAAaaAaaaAaaaaAAaaAaAAaaAAaAaaAAaaAAaaA = "uviJqpbuZQLgZytGRppigMugTcAHzNfBJiFfaDVeAfZzAJHsyNdsByAFnlJpgvVDjBOPeORFyhWacuk"
eLvoQIvuVSUcJlSRQcthwwFWdaDUlTluscFORXoROFSEQCdCrnOzkozVQryapUASOUTNOEfEQyyqeVN134 = 433
P16982451640386927132 = "ImqsjMcPRRmwVQwTvqIGDJluoRNYbFWogymNeIrITsZZikpDVrLvhVtgpiuasueTduLOTNVKxDJqDcJ"
OOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOO = "YrqAnvqqpQorObIlzRxVQUGUcryqQBLXObSfFXXZILZQvSsJUEApBntCQEsYwjSLGjEoVUOpYupJkVb"
AAAAAaaAaaaAAAAaAaaaAAaaAaAaaaaAaaAAAAAAAaAaAaaAaAaAAaAAaaAaAAaaAAAaAAAAaaAaAAAaaAAAAAAAaaaAaAAAAAaAAaaaAAaaaaaaAaaAAaaAaAAaAAAa = "ifqnaeshcYKQruDdDteikeEQaFZOpTbiGsBQLGnaCuRvQgZlSFXUDhagCHPFaebpAIoyqRXLmZkjfRx"
z126 = 352
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA = 46
lIlIlIIIIIlIllllllllIIIIlIlIlIIIlIlIIlIIllIlIlIllIIlIIlllIllIlIlllllllIlllIllIIlIIIlllllIIIlIlIlIllIIIIIIIIlIlIIIllIlllIlI = "daHIIEXzwZNqKIddPLNMueRZdHTQtGeTtxMkthFEotvEuHGPKgEjTMFdIOWrNFoJqjwLCTkoKLamPjz"
iyhineBBZqApvguHgWvZWYYKzaRFuhBxqNHvRWMpdbftPlgTYQkwZxAGSXujeaFKKlcqVyiYuquYWZp120 = "ZigguiywhuRvLEmavhMBGfGkaXsMhaDMUkoooATxAKXqSonLKQqkBojjuhRDOdZNIblGduYqcHyDfcC"
a16982451640376923118 = 644
aAAAaaAaaAaAAAaaAAAaAAaAAaAAaaAAAaaaAAaaAaaaaAaaaAaAAaAaaAAAAaaAAaaAAAaAAaaaAAAaAaAAAaaaaAaAAaaAAAaAAAAAAaAAAaAaAAAA = "VbOYVSowrFYafikxAoKkOOzROiKRILgiGrnNDlYZiObPDhcNmkgrXUQihldpauiuImhdaHcpXfSEZRQ"
GGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGG = 278
aaaAaaAaaAaAaaAaaaaAaaaAAaAAaaaaaaaaAAAAAaAaaaaaAAaaaAaAAaaaaaAaAAAAaAAAaAAAaaaAaaAaAAAaaAaaaAaaaAAAAaaaAAaAaAAA = 624
IIIllIlIllIIlllllIlIlllIlIlIIllIllllIIllIllIIlIIIlIllIIllIlIlllllIlllIlIIIIllIlIIlIIIIIIlIlllIIlIllllIIlIlIlIl = 658
UKKTQsUbQYxWnvcNROTShUXrXwAIndGFPLFCEtDpzKRfmWVJJKkmDMWtfGgcSTkqMGKGDVGekookvrV108 = 216
AaAaaAaaAaaAaaAaaAaAaaAaaaaaaAaaaaAaaAaAaAAAaAaaaAAAAaAAAaAAaaaAaaaaaaAaaAaAAaaAaAAaaAaAAaAaAAAAAAAAAAAAAa = 410
SGMotmwLiOUAgZTORltzBOUuxCaJVPQzwgHYekViTOZnlwCjZEtlkfcqlnNumSUdiJTsFPvVvhESbBl104 = 279
y102 = "otLDeoJCmSFCPYhSeYZHxAeZWhliFUFizTXbQRuOslEurYAlBrJSvieLyDvFWfOXQyvENsNfiqoMFvx"
s100 = 257
u98 = "HUvkjSVPwBirPKtgWXiMMzRANjATNxaLQMJXxibFoEzmFEPBpdFWDiiSoIohhknkhGslFUyuGHVJfdB"
VNPkBcGuWoJyqMZPPLvYZugMNzdwecdjzNvLPRrwmzAyYihhqzEdqlYKXnEGsYSykjFDuyVlrTtkWDx96 = 481
UdMJYJzNpgwxOSGvdCKLzNSggsRFiYbeGQNEbkanznpLVssvJpWKyHWZYiSBCfZOpPbXvoBMMXgHozH94 = "zGonYVHKWBkaMMcrBIGbzTSDejMTPPzvoIeFziEgfRkycbxizUMgtRYFgICFnwuurdNoeasOLLKckWb"
IIllIllIIllIIlllIIlIIlIllllIIllIlllIlIllIllIIlIIIllIIllIlIlIllIIIlIIllllIIIIllIIllIIlllIIIIl = 575
IlIIlIIllIlllIIIllIIlIlllIllIlIIlIlIIlllIlIIllIIlIIIlllllIIlIllIIIllllllllIIlIIlllIlIIllII = "jKpGtwRiIsSljLZPbIDPIlXKmdVPYnrUFLexgAtNsTafAgzBMVEWmIVwznjZNFHuAHcUUHGnthOvKTI"
RRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRR = 723
D1698245164035691786 = 789
IllllIllIllllIIIIlIIlllIllllIllIIlIlIIllIllIlllllIIllIIllllIIIIIlIlIIlIIllllIlIlIllI = 347
d1698245164035691782 = 236
aAaaaAAAAAAAaaAAaAAaAAaaAaAaaaaAaAAAaAaAaAAAaaaaaaAaaAAaAAAaaAAAaaAAAAaaAaAaaAAA = "EZsWUzdqYpBavvGQjFoLFFPvATlvyqyFullXbYNuPuxcbbQDHxSUwDUVkqSNdZgJaMrStwBSJdqmERB"
IIIIIIllIlIIlIlllIllIIIIlllIIllIlllIIlIlllllIIIIIlllIlIIllIIIIIIIIllllIIlIlIll = 960
tttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttt = "vplxBODXNzmlciJUXrCzNYPstHUnEWIXYTOiLwXgApWDiDYBLtBtosGhdvbEjPAaMtPBrErijxpGhyQ"
b169824516403469274 = "grxBdncgaGiEFEnvAqwlgeVnypyhWXaVvokHONvUEQYhgQnfnXcziBjHdaGQjISWqDXTOZCUlbqDOky"
x169824516403469272 = "pZdcAAjYdXulHJqTXGmTUjAfkjsHvtOdeVhVniAyvAgdVTDqztSVcsMBRzyWOkWQwILfZEcAEVVRQKp"
a70 = "bGxgWuJoHOuUHwwIrlRiwgvLPVfHelESmjniRGKnBIXLFZrQGqWqppFuoRxHNrGFpExTaBKfhCHuBUu"
G169824516403469268 = 899
x169824516403469266 = "GwDlKWMWmJfmxBtbUEkmxYlXGDelkhIFjNklDXxJTpBbHSYkQXyLQKnLvVEJEviLuugYXWErjwKzlqo"
A64 = 177
W62 = 283
aaaAAAaAAAAaaaaAAaAaaaaaAaaAaAaAAAaAaaaaaaaAaaaAaaaAAaaaaAAA = 217
KVdIwVfAJeUVHLZJSwsGbuTGhFMkquHVWzGrVHIQLsrHqwNqEePvpqRRuFOKouvIDzRdCacZndxwAVV58 = "eqfMewZocviPILxdLlmjRZceqWwAZiGHfRZWaREExLCvTblfzowVgPhwMOgZyaAaGLyJTbsSFTkkgnp"
IllIllIlIIIlIlIIIlIllIIlIlIlIlllIlllIllIIllllllllIIlIIIl = "bSScHAgeRjcsZBPmeIkSZnbjAHsMXLzvoROUTydqFCWwZKAhEqtQbbTAFilYGGbzyfZMTnwQrjFHhJL"
fkApXXJzCNVeqxnGNUGGlPuVEITuKapudMQdZsAfMzoQOyadXwlZOyijsCISPbtRKMCPtzpqHThpTXl54 = "MqhgJPQvvKDBzjlFRwmRGWsPwkqpTVDFrXvWAKHuPYvWtONkDaRalvnoGjShnshvNzegghfVNUgaRIl"
gggggggggggggggggggggggggggggggggggggggggggggggggggg = "BvHWFQlrUPALhfqlczTrQMZTPdMnYPnpmrUGrNGnFRXnHvkuEKaANwReSZQXdOfKjHEbhPGTXSSFxin"
OOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOO = 237
qqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqqq = "udRcxFXwknGsMgWAZPgUYZINnKJLpRFbVUOrNlTJDimjoizqByDdtGYekPCZrZbIHfhpXAMgjtPGAtl"
I46 = 509
I44 = "yhuNmguDRpEZrmUGvtfLXZACJFuxUBMKvViCYqZWTuOdxnWKoCYbcRMiSwSouuVJkqqBNXucIdbkzAC"
lllIIllIlIIlllIIIIllIIlIlIIlIIlIllIIIIIIlI = 291
AAAaaAAaaAAAaAAaaAAAAAAAaAaaaAAAaAAAaAAa = "AfzXSlkXIPaPYPooQkSqgWPfugVPtktknbWaxvswPPeqBlpurmUfpIvNXUraPQntPkihSntgiCZZVjb"
g38 = 551
s36 = 415
ZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZZ = 244
jRowqSoOTccsYGOPCHYdvHgZutyauSondPjCAEuDeEaQLfahsIOmMomVOQmRUyKGOhFOrnYMIaHjfRZ32 = 342
X30 = "cLUOZUaVuriLRabDNqbWQoROpBWGryGXFkNWZMGFkSXCrvqijJIAJzyKEjiIAnbZkpMVNfnSCzAosdS"
AAAAAAAAAAAAAAAAAAAAAAAAAAAA = "aYpElCSBgrfiEQYaXNmPhZNLrLnhUBKxTNDauYXiZgQBXndDmRAVCYchHVFlxPMfcMirbyuaYyyLlmA"
R169824516403169326 = 103
Z169824516403169324 = 329
wwwwwwwwwwwwwwwwwwwwww = 292
BBBBBBBBBBBBBBBBBBBB = "IVuPGeSDhwTeZKZxSVoaajYfIMlkXQEoDmJdriIkKOgtgMQkRfsvpACdljJjWGVJpYJPViJyCTmXMDK"
T169824516403169318 = 413
QQQQQQQQQQQQQQQQ = "wgyVyoaZUQlmMjzYxDzogAALtwEkcYeKyoTtIPhbGwltqOFECxiaexptnkKmxhCQbFSWNDJSrsxSrEG"
M169824516403169314 = 224
CCCCCCCCCCCC = 126
r10 = 578
JZyNfSROYgYFsEHnKNBOsOWDnIpLZYCcnfoEuPLAvvrmAfRSLExZgIRAJfGSYTwhvPfSMNKRakKtQnL8 = "idfMCfpeRzHiWSfmFTqYYWrkGbLfIVYMUInCEUqyFdCXthqNPuhPcOgRVZqcMwNZMEnHKRNakURbGTY"
wwwwww = 207
u4 = 348
xx = 562

# __author : Ferly Afriliyan
# Do not change the original author's name 

from colorama import Fore, init
import subprocess
import importlib
import os, sys

# Warna teks
I = Fore.YELLOW  # Warna Kuning
m2 = Fore.LIGHTBLACK_EX  # Warna Abu-Abu
lII = Fore.RED  # Warna Merah
S4 = Fore.GREEN  # Warna Hijau
F16982451640248025 = Fore.WHITE  # Warna Putih
IlIlII = Fore.BLUE  # Warna Biru
MNWhMbeUWfRALUTGxNUDgfrmfKQKsjLDZRpVXmIrCrVywgmmctqKSXGWbQyCCSifJnNoVEhWXanCxxp7 = Fore.MAGENTA  # Warna Violet
aaAAAAAa = Fore.CYAN  # Warna Ungu
IuFVEDRQHUtJnPDjuviverPLTGHkDOQhntskPWXBJsOYJOMnIeIgaiJWrnVDhUiLYMDwoTGchdIdvzp9 = Fore.LIGHTWHITE_EX  # Warna Jingga


# Clear Terminal
def clear():
    if 'linux' in sys.platform.lower():os.system('clear')
    elif 'win' in sys.platform.lower():os.system('cls')

# Memeriksa apakah modul python_obfuscator terinstal
try:
    clear()
    importlib.import_module('python_obfuscator')
    IlIlIIIIII = True
except ImportError:
    IlIlIIIIII = False

# Cek apakah modul python_obfuscator terinstal
if not IlIlIIIIII:
    clear()
    print(f"{S4}[{m2}â€¢{S4}] {F16982451640248025}Modul Obfuscate belum terinstal. Anda perlu menginstal modul berikut {m2}:")
    print(f"  {m2}- {F16982451640248025}python_obfuscator (pyobfuscate)")
    print(f"{S4}[{m2}â€¢{S4}] {F16982451640248025}Ketik perintah: pip install {m2}python_obfuscator {F16982451640248025}")
    exit()

# Meminta pengguna untuk memasukkan nama file input
clear()
print(f"{F16982451640248025}â–ˆ â–„â–„ â–€â–„    â–„   â–„â–„â–„â–„â–€ â–„  â–ˆ â–ˆâ–ˆâ–ˆâ–ˆâ–„    â–„   â–ˆâ–ˆâ–ˆâ–ˆâ–„ â–ˆâ–ˆâ–ˆ   â–„â–ˆâ–ˆâ–ˆâ–ˆ â–„      â–„â–„â–„â–„â–„   â–„â–ˆâ–„    â–ˆâ–ˆ     â–„â–„â–„â–„â–€ â–ˆâ–ˆâ–ˆâ–ˆâ–„ â–ˆâ–„â–„â–„â–„ ")
print(f"{F16982451640248025}â–ˆ   â–ˆ  â–ˆ  â–ˆ â–€â–€â–€ â–ˆ   â–ˆ   â–ˆ â–ˆ   â–ˆ     â–ˆ  â–ˆ   â–ˆ â–ˆ  â–ˆ  â–ˆâ–€   â–€ â–ˆ    â–ˆ     â–€â–„ â–ˆâ–€ â–€â–„  â–ˆ â–ˆ â–€â–€â–€ â–ˆ    â–ˆ   â–ˆ â–ˆ  â–„â–€ ")
print(f"{F16982451640248025}â–ˆâ–€â–€â–€    â–€â–ˆ      â–ˆ   â–ˆâ–ˆâ–€â–€â–ˆ â–ˆ   â–ˆ â–ˆâ–ˆ   â–ˆ â–ˆ   â–ˆ â–ˆ â–€ â–„ â–ˆâ–€â–€ â–ˆ   â–ˆ â–„  â–€â–€â–€â–€â–„   â–ˆ   â–€  â–ˆâ–„â–„â–ˆ    â–ˆ    â–ˆ   â–ˆ â–ˆâ–€â–€â–Œ  ")
print(f"{F16982451640248025}â–ˆ       â–ˆ      â–ˆ    â–ˆ   â–ˆ â–€â–ˆâ–ˆâ–ˆâ–ˆ â–ˆ â–ˆ  â–ˆ â–€â–ˆâ–ˆâ–ˆâ–ˆ â–ˆ  â–„â–€ â–ˆ   â–ˆ   â–ˆ  â–€â–„â–„â–„â–„â–€    â–ˆâ–„  â–„â–€ â–ˆ  â–ˆ   â–ˆ     â–€â–ˆâ–ˆâ–ˆâ–ˆ â–ˆ  â–ˆ  ")
print(f"{F16982451640248025} â–ˆ    â–„â–€      â–€        â–ˆ        â–ˆ  â–ˆ â–ˆ       â–ˆâ–ˆâ–ˆ    â–ˆ  â–ˆâ–„ â–„â–ˆ            â–€â–ˆâ–ˆâ–ˆâ–€     â–ˆ  â–€              â–ˆ   ")
print(f"{F16982451640248025}  â–€                   â–€         â–ˆ   â–ˆâ–ˆ               â–€  â–€â–€â–€                      â–ˆ                 â–€    ")
print(f"{F16982451640248025}                                                                                â–€                      ")
gFhqisbvvvovpXpzVKcLBOvBuWUbfhBlUJYgAcisczmpAcBpbFjOcIUIulkbOKIgVOlegVmsEPetWcZ12 = input(f"{S4}[{m2}â€¢{S4}] {F16982451640248025}Masukkan nama file Input {m2}: {F16982451640248025}")
if not gFhqisbvvvovpXpzVKcLBOvBuWUbfhBlUJYgAcisczmpAcBpbFjOcIUIulkbOKIgVOlegVmsEPetWcZ12:
    print(f"{lII}[{m2}!{lII}] {F16982451640248025}File '{gFhqisbvvvovpXpzVKcLBOvBuWUbfhBlUJYgAcisczmpAcBpbFjOcIUIulkbOKIgVOlegVmsEPetWcZ12}' tidak ditemukan.")
    exit()
    SSSSSSSSSSSSS = None
elif not gFhqisbvvvovpXpzVKcLBOvBuWUbfhBlUJYgAcisczmpAcBpbFjOcIUIulkbOKIgVOlegVmsEPetWcZ12.endswith(".py"):
    print(f"{lII}[{m2}!{lII}] {F16982451640248025}File harus memiliki ekstensi .py {F16982451640248025}")
    exit()



# Meminta pengguna untuk memasukkan nama file output
lllIlllIIIllII = input(f"{S4}[{m2}â€¢{S4}] {F16982451640248025}Masukkan nama file Output {m2}: {F16982451640248025}")
if not lllIlllIIIllII:
    print(f"{lII}[{m2}!{lII}] {F16982451640248025}Isi dengan benar {lII}! {F16982451640248025}")
    exit()
elif not lllIlllIIIllII.endswith(".py"):
    print(f"{lII}[{m2}!{lII}] {F16982451640248025}File output harus memiliki ekstensi .py {F16982451640248025}")
    exit()

# Inisialisasi variabel AaaaAaAaAAAaAAA
AaaaAaAaAAAaAAA = None

# Jalankan perintah pyobfuscate untuk mengobfuscate file input dan tangkap output
try:
    AaaaAaAaAAAaAAA = subprocess.check_output(f'pyobfuscate -i {gFhqisbvvvovpXpzVKcLBOvBuWUbfhBlUJYgAcisczmpAcBpbFjOcIUIulkbOKIgVOlegVmsEPetWcZ12}', lIllIIlIIIIllllIl=True, O18=True)
    print(f"File {gFhqisbvvvovpXpzVKcLBOvBuWUbfhBlUJYgAcisczmpAcBpbFjOcIUIulkbOKIgVOlegVmsEPetWcZ12} telah dienkripsi. Dan tersimpan di {lllIlllIIIllII}")
except subprocess.CalledProcessError:
    print("Terjadi kesalahan dalam mengenkripsi file.")
    exit()

# Simpan hasil obfuscation ke dalam file output jika AaaaAaAaAAAaAAA tidak None
if AaaaAaAaAAAaAAA is not None:
    with open(lllIlllIIIllII, "w", lllIlIIlIlllIlIllll="utf-8") as output_f:
        output_f.write(AaaaAaAaAAAaAAA)

SPOEeqPiWztBMIavQFCOHWYdOKwPCANKWFbaZQhpokUlyhbkGdwmzRElIqOWLPNNIZoEWSkYqsEGajS1 = 567
aaa = 140
LhBdyumzZseJdbHzisWRrVBClhfOcSBswgrpocILuPFjCNFKrutLnFiofuXzlFYMJgckoVhCuqbuEoJ5 = "KRsEJGkJuDVWFnrbtIPvbDwUBKxilgzbqJQvvhGmahWObiBPJVYEhbJmaEhrrrrUTqMzxZGtRPYtzGy"
IIllllI = "DpfycgsufacqKlmlywvRuahEpBPmjEBVtfpxjaqSjddiSBdonrcwHacXlYqqXMuphWjjGCbbNtPEtYz"
IllIIllII = "CGKvTRArMBYynpJblWLRvVqtCwVGThzyJoaLrvQEOOqQAkflrdatxyNVYmrmDgkqbBlAMcdorvgjWla"
lIIllIllIlI = 502
qqqqqqqqqqqqq = 244
IIlIllIllIlIlIl = "aqQsPFDyFotjCZooHMnDuCTRJZeFMyGfhUxddWjCLSIVxGDTiqgYZTYrHCIJUYCSGCvuUZqqNnihkHP"
ywCffFgnaUqluEiCTlkoHJqOFbcllKprDaTtdnLdEdkDBbODicqZAaPEGcOPAnGpagROuqqBZtCtLAs17 = 529
IIIlIllllllIllIlIIl = "yCSeecgAtWJQbgEuhFqNbEpTrFtAJxrLjEzYckahpzJhHUYQEXuosSkVXUdsnIgGLKlrWTcDbocivwh"
llIIlIIIIlIllIlIlIIll = 331
llIllIlIlIllllIlIIlIIII = "TPyCqEopVRlPshRQWqXcWwlMoRVdYSpdsCajDDfvrQOaHPtxiiaSTgHYnSWUPlDUjIPRFVMSlFbCpus"
FleXqZTbGOinLHoRTYQJIMMJcGYtbTbjWniskSiDRvCUYmYIFwrxqlKbyDnVOITbQmpzudJwZlLfEtK25 = "aBstVNfPwWWlfgpMDmUszegZmDZqwEkMzlxRfeIrqHceKDEehSFRoEFwskndiGlqdquyOLOGLFRbuMB"
jcbexAnlesLZxxfjZciiLWtOOjaFAIAphPAyMycFXRGeDeJQuCDYpfezKghghOLzeSXZSNgZxUzZLmK27 = "CabXmAgSuYVLImenOSKSReUrgXhGPehmkmEtEFqURcPilgjCbigyUKNKFujBmzfnzivgfWuyJvKgpxB"
nGUBkDUZNfTXmYeiVeLuprNsQNISPBOzEalUfiNxdreDOnfqOvekvDvJrhXUDKpoSvWzpMqkIVcbYnO29 = "kqVnGBLIKlDizBMPNIhiAhsTbxoDkiwmcazqhrMNsjBteqQfmwepFcLLpCKhvHFFyyNuowLaByAREkl"
eeeeeeeeeeeeeeeeeeeeeeeeeeeeeee = "nPwmLEIRHCBMSBGYGCrlhGReulXXrQYiKmPkbEzYhtmCWOZaGLGVSxvJYEEtwsXSxJnxhZObShuerAK"
IIIIlIIIlIllIlIIIIlIIlIlIlIIlllIl = "IHPTSXDmpUXiwSHtQCcAcieJmcvfdJGOJNSAIdgYGjpxWcWzNliCDuhkpRyTQsYfqyJOQvRhrWZOqjX"
aAAAAAaAaAAAaAAAaAaAaaAaAAAAaAaaAAA = 263
IIlllIlllllIlllllIIlIlIlIlllIllllIlIl = "MSEutAQOMqMHgCmDvjGhzwDCaKnxvBxfZUbvbXNYbYUHxovBJhBFqICmfhygdAcraoDhdxeTkIMEChL"
AAaAaAaAAaAaAaaaaAaaAAaAAaaaaaAaaaaaaAa = 397
R41 = "XmkPpEzDDYDFtEbtjsIbuElZNdzOYHWMeIUSIBAVWOecZXgYXLMLAHyuPOltAIyszcSfebTRswPAGhB"
b1698245164032692443 = "bKzMbHjxgmAhmVSWqpVPmbVnRxtWqDTJRifjVQxeWXYsCVSZrbXJbPwMAcBIrednbRxzPUpWYHIWaee"
IlIIlIllIlIlIllIlllllIlIllIIIIlIllllIIIlIlIlI = 344
aAaAAaAAaaAAAaaaAAaAAAaaAaaAaaAaAaAAaAAaaAAAAAa = 762
IIIlIllllllIIIIIIlIllIllIlIIIllllIllIlIIllllllIII = 363
IIllIIllllIllIlIIIlIIIlIIllIllIIllllIIlllIIIIlIlIll = "KqEQGvFTZFkcSnZjikNXAbWtwtXEMtGMcNYLMSIyGXVZoORBKMAeqORkPgqydsZHdDbKmlEquIIrOIq"
g169824516403369253 = 366
CcOPpqrPLNUqSfwsJFBCYUKxAbxlCooiuiOBLadfxojhyKbHkSQWfCfEhlfrPIYgARruXHwJAkjExsG55 = "MAVPCPQbXYleeowPiXvKNYtUFTuvRezVQVdSXNRIpdPDGeOuWySdRscfwTlFrCJNJOCfUDguuoohZrW"
f169824516403369257 = "JczLOVvaOdPrCfMaJcvnnkqSPJOBEmIlPwwokKFwwrIkdkBysUfvwxjQhOuOoibkegUGSGRCzdxFHuN"
W169824516403469259 = "VPHdCrYVeStPqHeEMQFbXkYdHlhwgTmcBHDPiyfKlGJTraoTdMpQSSMXZGhgInbsBGHKOrwhHapzRjo"
aaaAaAAAAAAaaaaaAaAaAaaaAAAAAAAaaaAAAAAaaAAAAaAAaAaAAaAAaaAaA = "ADrXOZavYLTNoxDWsLfwbHbukXFDBvWCqrlVAirplthcHIXjaRKzAxaxyvIVUSHUBeqxsTiRRkmMsaM"
llllIlIIllIllIIIIlIIllllIllIIllIlIllIllIllllIIllllllIIIIlIIlIII = "mZTEYHzoZLbkZQADlrAiFYCHZaiRXpqeVLYtmyTMmkuCUVDcDbFLAxgiKEDArMuDoRioTfBgNYbfeTY"
aAAaaaaaaaaAaaaAaAaaAaaaAAaaAAAaAaaaaaaAAAaaAaAAAAaAaaaAaaAaaAaAa = 237
IIIlIlIlIIIIIlIIIIllIIlIlllllllIllllIlIIlIllllIllllIIIIlIllllIlIIIl = 264
X69 = "EIvcuBtQKVfFBxbsQloWKArjcFYSZiMCirZHIdVRvECahjXNnRRzWwSprfyVEMpWvcemyqdBUczTmvT"
z71 = 306
y169824516403469273 = 538
aAaaAaaAAAaaAAAAaAaaaaaAaAaaaAAAaaaaaAAaaAaAaAaaaAaAAaaAAaaaAaAaaaaAAAaaaAa = "TQvoEjGTkMmtALoyPoECAlYNAxVeCOsKqXHDxMVtXdZDovByQJXXUMTJupDlyFwPyfWRWohlwgOCwwM"
H1698245164035691777 = "HhuZHvuvXwAHBlUWNoXTYxYKUvmyHyIRDEOVbtbobZZJGIjZMjkHnvYekdDOSWDtvdstIiyoqRtxydS"
GGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGGG = "VicSRDJzJpkxnoBJujnNCvnbXWNqljuRVeWACGNoPoHmHlFskjEGngrIDiqygoOumPHbCETjgWmaSCb"
IlIIIlllllIllllIIIlIIllIIIIllllIlIIlIllIlIIlIlIIllIlIllIlllIlIlllIIlIlllIlIlIlIII = 928
KIIIglAJkmWFTdWkiXRsHXjyYPBBlcmNOueZFcjRLjQxjXClsgWxnrucqSOlxrJlrZTPypyBrHPxLsk83 = "yGbMdMuSSwJDPGHMvHutQrzouVrxHpsofMdPqmdXMgNBnxUHNWnDQZhuYuntYCuvxUEQDEIQtTCvGQX"
n1698245164035691785 = "ftACcaMIfXyuvCvjXwKJOPhxgleERlTGFuGOOtBRQiovNVmakmcasLncooVQKHnFJDkeDnBisNUKQYs"
VVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVV = "rrgxCslibIAxESjIWBuGpyDyZOVWdIRzMMLuCvVlhKjYZTbntXlDrbwgrGcwlBQqndkUVgetRPFbWuR"
WWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWWW = 286
sQgSInwmmJWoRwNKzLutxRkeljlCXRiLPqXIKNPAHNyYaDcONticzSkijNktElBhasNohsxSMbSoSVT91 = "ApzWzClUpQhDTEOlIpOiGZWoTVPBlSrRquiENyKiQZUqVsfgxiVsxdlLqYJsYEqtwlalwVxGPRlfQlv"
IIIllIllIllIllllIllIlllIlIIIllIlIlIlIIllIIIIlIlIlllIIIlIIlIlllIlIlIllIlIIIIIlIlIlIlIIlIIIIlII = 322
eJbLyFuXBFOWjgOkIcYSyzpXhgqsJqCVEDdkXhprrwmHTLzgWCyOTYIkHSFLVrAUSjRcfsnzRMePGBS95 = 424
c97 = "vKjFGwApWxgHgkqjhAeGGxqmEtwfkeqGvcpeWQIpcLPPszGawMpuSTIxnBAJaObIQvJtIlOSVcZnrWj"
lMsQmuhITOGIdZKqnfqGKunhhFwFiOhJsIbVOdRerpDWzuRUhQDuxeCZaPIKMVduEocynOeCPsDzETD99 = 332
ddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddddd = "yxBZTUbbUNIDyBZzgDgZTeTOTfScZycXfRwLaSmJoQqEeathdRfeXoBavrCbhyVkYrlSFVcpzmTaPmn"
v103 = 160
ogdadthVvadIkIqxsscwVaVZYIRlvNcYeqGOWZcGVyCWWiioFcqqKEpHPquXSePMaknRBmZvFMlEqGR105 = 278
aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa = 336
O16982451640366921109 = 478
F111 = 291
d16982451640376923113 = "UiiIBehyZgWkJxqEIhLiqrkGtrjwnxwrepUelCrcMguZoinxyeolqOpAyaTArVrmNEJvNLZULkbHQxy"
LeQCUlByfjZFKXUFOgFTeUxyoPEBTZplwnerNCSeMzNmkGgnJDBvLbacWDOGSZXrwVOIlBWEWjPVpvR115 = 740
AAaAaAAAaaAAAAaaAaaAaAaaaaaaaaAAAaAaAaAAAaaaAaAAAaAaaAAAaaAaAaAAaaaAaAaAAaaaAAAaaaaaAAAaAaaaAaAaAaAaAAaAaaaaAaaaaaAAA = 307
YqmmLeRToGIIWzIwdjtFXRFwoodXbmxDyeDQeSqMTOHiNtllhMZeBJelWHGrVyarKxiOBHKVQSFpzDt119 = 83
nnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnn = "KWkjacVFFLEhdDXMFYboRSQFgBSJQWRHiuRsqcPnqlTtaFFUrHNbFzcKXiHLAviFcuiAOGUSAUJjkGd"
MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM = "ZcJSAmNINDdOpDlUjcFqHdBHWxdcESmzEBjJjjBTkogDWRlmKkymaGdVdxddHcrfEntXYaCvzBXFScD"
nnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnn = 258
aAaAaaaAAAAaAaAaaaaAAaAaAAAaAAAAaAaAaaAAAaAaaaAAAaAaAaaAaaaaAAAaAAAAaAAAaAAaAAaAaAaAAaAAAAAaaaaAaaaAaAaAaaaAAAAaaAaaAAaaaAAaAaA = 308
obcGXeJnDxPAVGQYDjIweNATXFzWVYvFxPvYESwhsUqtxseOKyiECxZTpzsCDVRkrQvlCxrJylPeMMc129 = "gmxkOgnupqTqcuCJaAVncxRMThGKtAqqafqaDQIvNasbvehWRowXhEoNzVgjThatDaOPYdvzQTXLuga"
aAaaAaAAaAAaaaaAAAAaAaaaaaaAAaAaAaaaAaAaaAaaaAAaAaAAAAaaAAAaAaAAAaaaaAaAAaAaAAAaAaaaaAaaaaAaAaAAaAaaAaaaAaaaAAAaAAaAAaAaAAAaAAAAaaA = "weNGdbyibVPpHInWOZdwVyGbCCcHXrjcgVrhiFSiPTJdebNLnNAnNTzzngUvJqoQTxALjRraqkeVBkR"
Y16982451640386927133 = 294
p135 = "ScmarpHAVDsraOQyGctiMYcrhiUJbbReQrLSVTWkuzoJoSgvschpkqSovvMgaMEitKJiItRBvqCvXnV"
G137 = "IciQDnABFlIekmVCWBGSZpMWQwRgkDpjqSsvjWEgMNvHqMJunEQQrRbmuwyJNcOFxuzlbqbYqyhcqez"
c16982451640396926139 = "gxcKhACQVjgrXMOEPNkkBgikfJZsosiVpzqYORZkTvVCFBaMwnvaLwFWHizPATepEndvyIQybcsMast"
AAaAaaaAaaAaaAAaAAAAAAAAAAaAaaAaaaAAaaaAaaAaAaAaaaaaaAAaAaAAaAAAaAaaAaAaAAAAaaaaaaaaAaAAAAAAAAAaAaaaAAAAaaAaAAaAaAAAAaaAAaaaAAAaAAaaAaaaaaAaa = 289
u16982451640396926143 = "EvkclnGwVLXdCHuKHwEPlKrDsYTgffkqKuDBwdbrIPANrxnnSHccJjEZxRQDqsrjjyZLMxxrjvebOqC"
AAAaaaaaAaAAaAAAaaaAAAAAaaAAAAAaaaaaaAaAAAaAAaAaAAAaAAaAAaaAaaaAaaaAaAaaAaAAaAAAAaaaAaAAaAaaaaaaAaaaAAaaaaaAaAAAaAaaAaAaaaaAaaAaAaAaaaAaAaaAAAAaa = 713
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx = 246
F16982451640396926149 = 207
QQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQ = "QnUTazsvUexASwEdBictqSqqrkshGEaZsfTCqjGoZjlzzlOJQPtcAoSAmMrUmqaIneJAGYUfoOgahUy"
aaaaAaaaAAAaaAAaAaAaaaAAaaaAaAaAAAaAaaaaAAaaAAaAaaAaaaaAAaAaAAAAAaAaaaaAAaaaaaaaAAaAAAAaaAaAAAAaAaAAaAAaaaaaAAAAaaAaaaaAaAAaAAAAAaaAaAAaaaaaaaAaaaAaAaaaa = "wvDIyAItHHZJUFHnJUorrEJbtISjECellzrxOuLFqQjIqsuQsmAsxEGcIcqaLYksdDvUsZRYUPJzIjR"
sGZicvzDkQpfhLTdhTvdvVeWciFYFNwgWcoygOviATLzToTXdVXFkIVaSmoEPcAwtlLuBjdAASFfjCn155 = 682
SSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSSS = 357
P159 = 782
IlIIIlIllIIIIlllIlIIlIIlIlllIlIlllIIllIIIIlIIlIlllIIIIIlllIIIIIlIlIIIIlIllIlllIllIllIlIlIIIlIIIIIIlIIllIlIlIIlIIlllIlIlIllIlIllIIIllIIIIlIIIIllIIlIllIIIllIIIlIII = "zMypjrMYDpZKvnXjExQHlbxRnoZxpxyNMcUfWqCTWjKlHNNudKHNBfcpQHfBJUowpwMXsAlRSvWjnjA"
lIIlllIlIIlIllIlIIllllIIlllIIIlllIIIIllIIlllIlIlIlllIlIlIlIIIlIIIIlIlIllIIlIlIIIIIlllIllllIIIllllllIllllllIlllIIlllIIllIIlIIIlllIlllIlIIIIIlIlIIlIIlIIllIIlllIlllIl = 76
k165 = 539
IlIllIIIIIlllllIIIllIIIIlIIlIlIlIllIIIIIlIIllIllIlIlIIIlllllIlIlllIlIlllIIIIIIllIIIIIIlIllIlIlIllIIIlIlllIIIllllllIIlIIIlllIlIlllIIllIlIllIlIIllIIlllIllIIlIIlIllIlllll = 441
V169 = "ZYtPXXPgPUqSIGZVZbtKIAnRUBUtEpipqRiRkutrRxigwemLhqpNlRGpxKrqHeIzGjwnadzLsnZyJqG"
Z171 = 389
o173 = 357
vvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvv = 484
UNNmfeMySxagNdiEmXGQsUvQqTSRRQNtjwaoSPuunRPvVVpVOyvKmecgCIkFXXZZRxRiwTxVklLznQA177 = 165
s179 = 562
W16982451640418017181 = 320
aaAAAaAaaAAaaaAaaaaaaaaAAaAaAAAaaAaaaaaAAaAaaaAaAaAAAaAAaAAAaAaaAAaaAAaAAaaAaaAAaAAaAaAaAaAAAAaAaaAAaaAaaAaaaAaAAaAaaAAAaaaAaAAAAaAaaAAAaaAaaaAAaAaaaAaaaAAaaAaaaaAaaaaAAaAAAaaaAaaaaaa = 280
U185 = "NyBxIuWlSrNjIbVdKWTrXxTHMrhxWaekEgqyMNMZLjyWtsZVLqSfBuuYuMQOxBASQXZqCWnXJCSSvvA"
h187 = "VQlBnyuVxCndTtbhrvxHmBrkUxVeHDGAdIJmDMXVqXetdIrqdGWEKsDAZzUpmcgSiYGlgRVhGiNrKLf"
AAAaaaAAaaAAAAaAAAaAAAAAaAaAAaaaaaaAAAaaAAaaaAaAaAaAaAAAaaAaAAAaaAaaAAaAaAAAAaAaaAAAAaAaaaaaAaAAaaaaaAAAAaAAAaaAAAAAAaAaAAAAaaAAaAAAaaAaAaaAAaAaaAaAaAAAaAaAAaaAaAaaAAAaaAAaAAAaaaaAaaaaAaaaa = 201
AAaaaaAaAAaAaAaaAaaAAaAaAAAaaAaaaaaaaaAaAAAaAAaaaAaaAaaaAAaaaAAAaaaaAaaAaAAAAAAaaaAaaaAaAaaAaaaAaaAAaAaAaaAAaAAaAAaAaaaaAAaaaAaaaaAAAAAaAAaaaaAAAaaaAaaAAaAaaAAaaAAaaaaaaAAAaaAaaAAAAAAAAAaAAaA = "tJhAWUVVuFLwpmOohRAEjLhqrTAhhluBeIfHdMQNOfGcopDCPaLOkvkzETWRFsrvRmJdIMZQEGOsXwd"
p16982451640438023193 = 359
JGYUIOxAyLNbIOhqxwTmBoDqyTCvPPftwkXGeniYANXqhzCDtEsLbxYnsTMtRiqXSRzAVkRllHdafNV195 = 316
N197 = "HOnChQcUUtjpSPrwAgWnVPLqqxNEKSNMnFfrLifqxlXltynFUbaeBpVGjJgkfriANjdXwRGZGwfGlTE"
lIIlIllIIIIIlllIIIIlllIIlllIlIIlIllIlIlIlIlIIlIIlIllIlIIlIlllllllIlIIIlIIIIIllllIlIlIlIIlllllIIlIIIIllllllIlIlIIlllllIIlIllIIIIIllIlIIllIlIIlIlllIlIIllIIlIIlIlllIIlIIllIIIlIlIlIIIIlIIIIIlIIIlIlIIIIII = "SkSaqJiXmMvRAkNRTZkbYKAsEQajvTVguLTTumffdolxSLIzNdnFoIdGNMatLFAZnraIiXHKONldSIX"
AaaaAaaaaaaaAAAAAAaaaaaAaAAAAAaaAaaaaAAaAAAAaAAaAaAAAAAaaAAAAAaAaAAAAAAAaAaAaaAaaAaaaaAaaAaaAAaAAAAAAaaAaaaaAaaaAaaaaaAAAaaaaaaaaAAaAaAaaAAAAAaaAaAaaAAaAAaAaAaaaAAaaaAAaaAAaAAAaAAAAAAAaaAAaaAAAaaaAAAaA = "mfPpOdKXFVruYgtThbVXkcKtHpowrLdPjHsDgybTWwUhSmbceUPptHcUJtaalBLxlqCaTpWyKXNsnjU"
PPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPPP = 227
o16982451640448015205 = "eftOYNmxIprruboWqqmkFoGxUrsDzceKiTuUffkprdCWUjYqakhSlFLnthnZVecdoqLGlRVylLywOLP"
zXTlZgIVHwqcaJuAxdtCJMBkCscysVfdVcXenwzEAJKSLRkFcUJzETzFfOefVQwspcuuAwJYvkTJebG207 = 266
lllIlIlllllllIllllllIlIlIIIllllIlIIlIIlIIIlllIllIlIIIlIlllIIllIlllIlIIIlIIlIlllIIlIlIllIIIlIlllIIlIlllIlIIllIlIllIllIIIIIIllIlIlIlIlllIIlllIllIllIlllIIllIIlIllllIlIllIIIIlllllIlIllIIlIllIllllllIIlIIIIlIlIIllll = 82
a211 = 297
YAuxohberKzllfvjJGhJHlNAmzolidpYMvhZahLGioOLyLFGVUNSfhJTWaRrVEfrubbHAdvyXxgBccz213 = "jacWodXPIJNBEafKDybEMHGSeBgfhiBWRWAKzlwGdUyooiOgHdPOjGBhCLAWnvFLJtOTMgiUhqQjAiH"
GKRwNHQkQTQDTDPERpZGEUsJWeYCQiMrNDHdrJkyaEZgOMshNadbMrHFwitDWyOFyuQxlVwrPGWovwl215 = 317
IIIllIlIIIIlllIIlllIIllIlIllIllllIIIIIIIlIlIIllllIIllllIIIIlllllllllIIlIIlllIlIIIIIIIlllllllllIlllIlllllIIllIIIllIlIlllIllIIIlIllIIIllIllIIllllllIlIlIIlllllIIllIIllIlllIlllIlllIlIIIllIIlIlIIllIIlIIllIIlIlIlIIlllIIIlII = "jAFAmgTqsWYfIxuxMvjkoFqHlGTKQFYjgkpMaWumWgCYWNlgkRGouTPGgtoLmPzSeaLLdDwxMaEIvlc"
AaAaaaaaaAaaAaaAaAAAAAAaaaaAaaAAAAAaAaAaAaaaaAAAaaaAaaAaaaAaAaaaaAAaaAAAAaAAaAaaaaaAaAaAAAaaaAAaAAaAaaaAaaaAAAaAAAaAaAAAaAaaAAaAaaaaAAaAaAAaAaAAaaAaAAaAaAaaAaAaAAaaAaaAaAAAaaaAaAaaaAAaAAaaaAAaaaAaAAAaAAAAaaAaaaaAaAaaaaa = "vCsXGVxhLXqGZqmMGucILYfeimWXhNWcAChQfFjwBHAXdNDhgCCpqFxCuFTaidcsGufitKOKuYUpakw"
kYoxrngTKgfXzIssBMpRotwnuIrKPqjtEoQmGufyPhBoDhOqDMgYrChaqWeMyvDUQXxtKLOuxoYeTEb221 = "NxteZLKmALxerviJHJIchqBCVOZlUqAAePjPvPRdDVINFAyhDLRyYmYyEnIUFDEJQZEGcVzVEyEeCqu"
CCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCCC = 859
w1698245164046801225 = 802
MMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMMM = "aCOssPRWXMWmAobTyhzqwsJZhoANRsgrRBAdPVphgmqJPUByIALecMJRyFgKwSBAPUmIniibnGimoOu"
AAAaAAaaAAAaAaAaaaaaAaAaaaAaAaAaAaAaaAaAaAaaaAAaaaAaAAaAaAaaaaaAAAAAaAaAAAaaAAaaAAaAaaaAAAAAAAaaaaaaAaaAAAaAAAAaaAAaAAaAaaaAAaaaAAAAaAAaaAAAaAAaaAAaaAAaAAaAAaaaAaaaAaAAAAaaaaAaaaAaaAAaAaaAaaaaaAAaAaaaaAaaaAaAAaaAaaaAAaaAAAAAAAaaa = "urglLtCrrkRIEnDpRHiEyqTLAZjaEbyMSrWcChbUBONVnczPHxOEaLoUBCJIrcACcnytekSZIYkEEkb"
L231 = 378
l16982451640478022233 = "nixiIHFEwmDXcgrkIxuGswQxNXajjSjqeOMjVWlMAAOBVlSwIUDnHVfgApEyeziGfsiLvilfCtNWSRz"
aAAAAAaaAAaaaaaaaAaAaAAAaaAAAAAaaaAaaaAAAaAaAaaAaAaaaaAaAaAaaaaAaaAaAaaaaAAAaaaaaAAaaAAAaAaaAAaAaAAAaaaAAaAaaaaaAaAAAaaaAaAAAAAAaaaaaaaaAaaaAaaAaaaAaaAaAaaaaaAAAAAaaAaaaAAAAaAAaaaAAaAAAAaAaaaAaAaAAaAaaAAaAaaAaAAaaaaaaaaaaAAaAAaaAaAaaAA = "LjQjYdoOxbInoEgecDtsBZKPjreTZnuYepdCnCPfKdiSejHJIBVJKxCyYgBCAvAbUWNSHpwPBVBxAuv"
VVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVVV = 333
afmwBHsyWoFRNLYaZQwIYcwqoVIEOVafjzQxohFomjfTpSgZyrZGAFdTkbxCrQKPzgnFaHjSuaEcqAd239 = 234
DKCBsiDnEtwGHyPoMhlcLKVYwoUsVqjLtUznuHIxQIYdDlOtDJnvxrLGqTnKgvShSRWYFaUJFSzkPnt241 = 321
n1698245164048801243 = "EiNXAtDOHawSllMIFYZNoLRhkXUBZRKNWLDAIZIGImbqxzXQliDbRndNLzfdWFDCIpriHvxSAdKeiDw"
YYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYYY = 152
XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX = 319
i1698245164049803249 = "XdyzVAOOqDwNOQBBjWijdhwtGKvnABKWBBluPemvtHFqrjgtzFfWfYswryNYUhcpTerPVcInSEnRrFy"
TWANkpObmlVcIQSYRuVQlqytVTtnujcbnuQEyQksVMHxJOqztErYbWgOScELAxipHeFqwovYQOExnnA251 = "ogyVFzDTZZGMqfSxutqQrMrKsqMjdYAIdovmCXgJkQsDBtDnfOhrByqRuJWKYvGVqAPQVujmUfbwTwJ"
aAAaaAaaAaAAaaAAAAaAaAaaAaaAAAAAAAaAAAAAAAaAaAaAAaaAAaAAAAaAAaaaAAAaaAAaaAaAaaaAaaAaaAAaAaAaaaAaaaAaaaAAAAAAAaAAAAAaAaaaaAAAaaaAaaAAAAAaaaaAAaAaaAAAaaAAAaAAaaaaaAAaaaAAAAAaaaAaAAaAAaaaaAAAAaAAAaAaAaaAAaAaaAaaaAaAAaaaaaAAaaaAaAaaAaaAAAaAAAaAaaAaaaAAaAaaA = "AKmkOUhbHXXtFjZmhzUCKwBhuyrOtHqmxTCgnAuVjGdsAMkJKBTjWoGecZRCLKRqfFpjtYOUZiEicsy"
tIbJYWZtphIsOKeygcFSRmWHNVBmWsiZqODnHLiyFhxHtNcJBahMgJdkhhBYJJwyuxyJllsqewKYKyQ255 = 149
ppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppp = "YFWPEhwKsOkqeSIMkVHIZnhNKHDEEepCtTsUJVvWNrzWqTjFVwhvrrViTBhxUZeypobFvgtSophfpwu"
YCXFZOGPlzzFkiqZYKGsJCXAJMkmGKEGwNDEYxGNcAPNDcFJjITPHWOUTDEhADrVuYoicMjKUrJVtRz259 = "HNrCySXsMEgYJHlYIffAEHVlUkUHpQMeuCFqZOAHKscbjIuquMMNKgCfNsZVWyrdYnxQsCpzqCqhofR"
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA = "mWYNTAtQyHMPmUUKakoeVDcvAFUvSQuxFbhATWnZatoJsEEVmfUykxbyqftPbgUdLsPrGwGbPymscbi"
IIllIIIlllIIllIIIIlIIllIIlllIllIlllIllIIlIlllIIlIIIIIllIllIIIIIlllIlIIIllIllllIlIIllIllllIIIIlllllIlIIIIIIllllllIIllIlIlIIlIlllIIIlIllIIIlIIIlllllIIIIIIIIllllIllIIIIIIllllIIIIlIlIllllIIlIIIIIllllllIllIllIlllIIlIIllllllllIlIIlIlIIIllIIIllIIllllIIIlllIIIllIlIIlIllI = 170
w16982451640516937265 = 477
aAAaaaAAAAaaAAAaaAaaaaAaAAaaaAaaAaaaaaAAAaAaAAaAAAAaaAaaaAAAaaaaAAaaAaAAAAaAaAaaaaAaAAAaaAaAAAAAAaaAaAaaaAaaAaAAAaAAAAAaaaAAAAaaAaaaaAAaaaAaAAAaAaAaAAaAaAAaaaAAaAAAaaaaAAAAaAAaaaaaaAAaaaaAaAaAAaAAaaAAAAAAAaaAaaAAAAAaaAaAAaAaAaaaaAaaaaAAAAaAAaaAAAaAaaaAAaaaAAaAAAAaaAa = "iyPwCVqpghqcVsqAxHgTtWOeWKEDxUIxIQUewKUbfkOITZxqdYPgLpzKgTODNomDOjMFuLAqZAFSWcY"
AaaAaAAAaaAAaaaAAaaAaAAaAAAaaaaaAaAAaaaaAAaAAAAaAaAaaaaaAAaAaaAaAaaAAAaaAAaAAAAaAaAaaAaaAaaAaaAAAaAaaaAAaaAaaAaAAaaAaAaAAaaAaaAAAaaAAaAaAaaAaaaAaaAAaAAAaaaaaAAaaAaAaaAAaAAaaaaAaAAAaAaaaaaAaAAaaAAAAAaAAaAaAAaAAaAaaaaAAaaAaAaaaaAAAaAAaAAAaAaAaaAAaaAAaaaaaaAaAaAAAAaaAaaAa = 335
DkvURzkIRcNyZrqGixtNBJubvkeaTjtlFXMnvNCXpOwnJxaPAgTUXaBSlJkutpRRrzlvlRVYMsEQluC271 = 197
A273 = "opWewoWFktQSDZXLmlfWpzQjGCaJSdOqUyINKFvcCffkiAqXvWKnCUtOddibHYPCDodYcKdeHdufiGB"
AyfTghSqMXcwgmoWMQccvUKJphEFCqIdIdmtiunFlvFMclWyFGzaEAryUTzmtbRperQKKCZViYGCVPP275 = "cCQZdDtkGtfeMxeiFKaMVHnDSshJINkKCisgWTARrEZyNYlTeiiyhJMdNddkoJuMdriuJMJQWalFAkk"
AAaAAaAAaaaaaaaAAAaaaaaAAaAaAaaAaaaaaaAaaAAaaAaaaAAAaaaAAaAaAAaAAAaAAaAAaAAaaaaaaAAAAaAaAaAAaaAAaAaAaAAAaaaaAaAAAaAAaAaAaaAAaAaaAaAaaaaaAaaaAAAaaaaaaAaAaAaaaAaAaAAAAaaAaAaaAaAAaAAAAaAaaaAAAaAAaAAAaaaAaaAaAaaAAaAAaaAAaAAaaAAaaaaAAaaAAAAAAAAAAaaAAAaaaAaAaAaaAAAAAAaAaaAaaaAaAaaAa = 373
RRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRR = 264
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA = "UVYVYzmYUHFCnxPjNEvAhHrcMaeWJHfHjLFhNZVglPRHdERzNQomjzvivHLEBZdqRMPQHIJCXMwkNKI"
ttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttttt = "ZqUCRfJRkeSVFAYbFfCBQLMdTJlgQGNqxOTfYccyHaRCGaQRMyhtqkuEzWheAGEZHZxdPYpvcfHBwVJ"
aAAaAaaAAaAaaaAAaaAAAaaAaAaAAaAaaAaaaAaAAaaAAAAaaaAaaaAAAaAAaAAAAAAAAaAAAaAaaaAAAaAAAAaaAaaaaAAAaAaAaaAaaaAAaAaaaAAaAAaaAaaaaaaaaaAaaAaAAAAAaaaAaaaAaaAAaaaAAAAaAaAAAaAAaaAAaaAAaAAAaaAAAAAAAAAaAAaAAaAaaAaAAAAAaaAaaaAaAAAAAAaaAaAAAAAaAaAaAAAaaAAaaaaaAaaAAAAaAaaaaAaaaaAAaAaaAaaAAaAaaaaaA = 219
KKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKKK = "XfhqNWatiIXgEaEWBNncMnUTSLJbTQHeAAtRPHpAfTbYYQxBXHruplvMgUmHSFiZnJJfZhlBFVLhrro"
llIIIlllIllIIllIlllIllIlIlIlIIIllllIlIlllIlIIIIIIllIIlIIIllIIIIIllllllIlIIllIlIlIIllIIIlIlIIllIllIlIIllIllIlIlIIIlIllIllIIIIlIIIIIIIIlIIIIlIIIlllIlIIlIIlllIIlllIlIlIIIlllIllllIlIIllIllIlIllIlIlIllIIllllllllIlIIlIllIIlIlIIlIIllllIIIIlIIlllIIlIIllIIIIIlIlIIlIlllIIIIlIllllIllIIIlIlIlIIlIIlll = "DeYJZheXLyHTluRprscgixFwXqIvGcxvImJYQFEsPGFZbSAkwmYqFmfnEfHibFDfQveAsMHCWiiCyAT"
n291 = "nAzrcoaRKCxwEfysqLIDSVrwioLcOCZpFaSLpGYwVASJJcYdCaIcJACRezFRUcsXprDNryAPDDvPlnK"
r293 = "AtOqULYGmnTsxqwMSUzuPPWbqgGnagpfUZFznGdHEmcqXIeiFPtoEJmmCCNpHQAIBolEmJzXHFqvUkG"
nnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnn = 349
P16982451640546932297 = 490
mkqCTqXPNGcPOSQfmcrICEeovtkMDIkoJRkVCDIuNsuGIkHRWKbjGudYqQgeFdrjeGzJSjszhlAxoHP299 = 255
llIlIlIlIllIlIlIlllIIlIlIIllIIlIIIIIIlIIlIllllIllIIIllllIIlIIlllIIIIIllIllIlIlIlIIIllIlIIIIIlIIIlllIIIlIIlIlIIIlIIllIIIllllllIllIlIIIIllllllIlIIIIlIlllIIIllIlIIIIIlIIIIIIIllIlllllIllllIIIIllIIlllllllIIlllIllIIIIIIIlllllIlIIIIIIIlIllIllllIlIIlIIlllIIlIlIlIIIIllIlIlIllIlIIIIIllIlIlIIIlIlllIIIIIllIllllI = "YaTLaXJLIMVcMdQDxPeFMgWIOlsDQxqjnXXXCcurWGpuBbqBcgncTfnPpjWyxlEMCApwzRXUMnegflV"
aAAaaaAAaaAAAaaaAaAaaAAaaAAaaAAaaaaAAaaAAaAAAaaAAaaAAAaaAaaAAAAAaAAaAAaAaaaaaaAaAaaAaAaaAaaaAAAaaAaAAaaAaaaaAAAaaaaAAAaaaaaAAaaAaaAaAAaAaaAAaAAaAAaAAAaaaaAAAAaaaaaaAAAAAaAAaAAaAaAaaaaAAaAAaAaAaAaAaAAaaaaaAaAAaAAAaaAaAAAaaaaAAAaAAAaaaaaAAaaAaAAaaaaaAaAAAaAaaaAAaaaaAAAAaAaAAAAaaAAAaAAAAAAAAAAaAAaAAaAaAAA = 280
WEMLDgTzYCENpfjUpSjQMMNCSVQpwmUVyCjpLqwzBzDxHvoUgzYwsrziGaEXUKtwKzfZxLVgZAWtihl305 = "LZXhGaixStuxllOtDiTKMnjlhtEAcVQezRhmwVtHHehAkqCdvlGeUZerDIQnEpQGydpNEqqTKcOaKCl"
ULKYGGYFOuhNSuUJKYPfPqWZKkUPMXpxCCUcCGsCACeKdGdBZFcnXzxJJNvdVEmkVaGVKeereASslCY307 = 459
IlllllIllIIIlIlIIIIIlIIIlIlIIlIIIIlllIIIllllIIIIIlllllIllllIlIIIIIlllllIlIlIllIIlIIIllIlIIIIIllIIIIlIIlllIIlIIlllIlIIlIIllIlIlIlllIIIlIIIIIIlllIlllllllIIIIllIllIlIIllIlIlIIIIllIIIlIlllIIllIIIIIIllIIlIIIlllIIIIIIlIIlllIllIlIlllIlIIlIIIIIllIlIIIllllllIIlIIlIlIllIlIlIlllllIlllIIIIIIllIllIlIIlIlIllllIIlIIIlIlIlI = "qPuHhsaqYFGXvuwQTVXQpOpUuhVAqeAEDSgNsXTeEaccGqOPTaggpdUZcwJpaEUOLyrUpysDIQdbtQS"
AAAaaAaAAaAaAaAAAAAaAaAAaaaAAaAAAAaAaAAaaaAAaaaaaaaaaAAaAaaAAAaaaAaAaAaaAAAaaaAAaaAAAaaaAAAaAaAaAAAaaAaAaAaAaaaaaaaAaAAAaaaAAAAaAAAAAaaAaaAaaaAaaAaAAaaaaaaaAAAAaAAaaaaaaaaAaAaaaaaAAaAAAAAAAaaAAaAaaaAAaaaaaAaAAaAAaaAAaaaAaAAAAAAaAaaaaaAAaAaaaAaAaaaAaaaaAAaaaaaAaaAaaAaaaAaAaAaAaaaAaaaAaaaAaAAaAaaaAaAAaaAaAaAaAAa = "sXkbqJfNfdrBEjIjsgHmIYnKGaCkWssQbwoHozITdPPqrsyGfqmEjqXVTQKAEVCuFfYGvCdLMXhRDyq"
ccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccc = 184
lIlIIlllllIlIllIIlIIIIIIIlIIIlIIlIIIlllIIllIIlIlllIllIIIlllIIlIIIIIIlIllIIIlIIIIllIllIlIlllllllIllIlIIllIIIllIIllIIlllllIIlIIllIIlIlIlIIlIlIIIIlllIIIlIllIllIIllIIIlllllIIIlIIlllIlllllIIIlIlIlIIllIIIlllllIIIlllIlIIIIlIIIllllIIlIIllIIIIIlIIIlIIlIIIlIIIllIIlIIlIlllIIllIIlllIlIlIIIIIIlIIlIlIllIIIIlIIIllIIlIIIlllllllII = 235
AAaAaAAAaaaaAAaaAAaAaAAaAaaAAaaaAAaAAAaAaaaaaaaaAaAaAAAAAAAaaAaaaAAaaaaAaaAaAaAAaaaAaaaaAAaAAaaAaaaAaaAaaaAAaAaaaaaaAaaAaaaAaAaaAAaaaaaAAaAaAaaaAAaAaaAaaaAAaAAaAaaAAAaaaaAAaAAaAAAaAaAAAAAaAaaAAAAAAaAaaaaaAaaAAaAaAaaAAaaAaaAAaaAAAAaaaaaaaAAAAAAAAAAAAAAAAAAaAaaAaaaAAAAaAAAAAaaaaAaaAAaAaaAaaAaaAaaaaAaaaaAaaaaAAAaAaaaAA = "NRoAxFtnAZcVBATbYdVPNWdHVffbbqdbeuHligsscEhmgFcNwaRENQfbHpuLJFLlpoCsAwwGeZPXiem"
c16982451640576942319 = "oXPwQSrqeZVIUgMJHDWcGgWLHptBgptnWeKtEnoRIudwrXLCkjmDRVnFlDbcmRsUBhspZQLfDVruaHw"
a321 = 192
bzsxqOqCSXfiADOaHwgFsSdPlDdjxtGWEWRPAVPWoZlNOmkSeAbSnhXnoevoigLXkhPQCRCqsfuLyJn323 = 504
IIIIlIIlIIIIIllllllllIIlllllIIIIIIllllllllllIIlIllIllIlIlIllllIlIIllllllIIlIllIIlIlIllIlIIllllllIIIllllIIIIllIllIlIllIlIlllllIIllIIIIlllIlIlIlIlIIIIllIlIIIlIllIIlllIIlllIlIIllllIIIIllIlIllIIlIlIIllIlllIIllIlIllIIlIlIlIIlIlIllllIIIIIlllIllIIIlIlIlIIlIIIIIllllllIlIIllIIlIllllIlllIlIIIlllIIIlIlIlIIIllIIlIIllIIIllllIlllllIlIIIl = "bIITVnEwoKfwvyobIWNieoAhptXsHHpyyBwjRrRZgUqoaKeAmdockrfDgRqLihxgkFkfBiJkoXKrTkm"
aaAAaaaAAAAAaaaAAAAAaAaAAAaaaaaaaaaaaAaaaaaaAaAaaAaaAaaAaAaAaAaaaaAAaaaaaaaAAaAaaAaAAaAAaaaaaaaAAaaAaaAAAAaaaAAaaAaAAAaAaaaAaAaaAAAAAaaaAAAAaaaaaAaaAAaAAAaAAAaaAAaaAAAAaaaAaAAAAaaaaAAaaaAaaaaaAAAaAaaAAAaAaaaAaAAAAaaaaaaAAaAaaAaaaaaAaaaaaaAaAAAaaAaaaaAAaAaaaAaAAaAAAAaAAaaAaAAaAaaaAaAaaAaAAAaaAaAaAaaAaaaaaaAaAaAaaAaaaAaAAAAAAAA = 457
HHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHHH = 503
ppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppp = 478
QJNXdnkxpdoCvOSWGFdGuqVJYtQZfcwyiTjbtJEiJfvyOHwzNrvCtMLSTfMCFYysHmjeuunsnwQHKni333 = "UEsMHBxonDZBRbPLgwTULPpBrEaOhBWVceOgWkuTKjjXMguUyTUebApnvGJzTDDsZrOQWnkRygzhmLR"
yKbMZYPnMlLceocmSnVkcblfEzhTGHtCjHLEWHYMcBMpjMLQayZhsXvwxhXrxChBQXwVIKwgivwiqJf335 = "XIJNcxbouGeEhEjFDkvprgVGEUnMvLQhzTPUSVggqoXvayxpfrcjRoSNZeHBBiItupfvChyADgBVAMB"
n16982451640596929337 = "hKuRcvHxOQKETumNnNTcrYFjGgoyznWMVQCGLxAKVvbJnxNPvVTGleobXrPsZfHJqmDrtKmIwpBhJxh"
K16982451640596929339 = 757
F16982451640596929341 = 200
JJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJJ = "yIxEyrSZUqgDckLtKRBUNoVwjFocbBpNYYaqirKOBHoEOPUtscCKjkcQvWPjnUUYRbdPvIJfJRGszzY"
nJeByKwpTrAferEumnXbVmfcQrdhQXsfPtUHQDpNJVRHcyHdFNPlNBecsBjObkoyNBywosOppBHMxNI345 = 365
KvxtaDWFmEzhQVkeCooPKgBgIjidWNBYzoFYyvMVLYXaJHCvrJCJllARRMelllkTvJkkUEEonIxQgqL347 = "dDnDlsvwDNfjunkuXHwJahfYfxEABwCzWyPPVyEkHhGHoMhNgFPpCZYRFQnXquQnYJjHFjVVcHjmTSu"
nnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnnn = "QTkqPljxxPiXBicgyJjyxydGCrTQZOQHWetKTIkPJyMDyHwGUunOKrUzhriDcFdALEiOOeTYNqdUAnb"
lIIIllIllIlIIllIlllIIllIlIIIllIlIlllIlIlIllllIlIlIIIlIlIllIllIIlIllllIIIIlIIlIIlIlIIIlllllllllllIllIlIIllIlllIlIIIIlllIlIllllIIIlIIIllIllIlIlIIIIlIIlIIlIIlllllIIlIIIlIlllIlIllIIllllllllIlllIIIIlllIIllIIllllIlIllllIlIIlIIIIIIIllIlllIIIIIIIIlIIlllIIIIlIlIlllIIlIlIIlllllllIIlIIlIlIlIlIIIIIlllIlIIllIIIlllIIlIIIllllIIlllIlllIlIlllIIlllIIlIlllIIlllllIlIII = 203
j353 = "jxbncHzQhkwLfwBMFhpJXGwlbWzOEzhxgIxEVRhKTZlnAXBckuMfmUinKleFgtOwBkpAGkHynQCFZnR"
ppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppppp = 268
ylIeggRPWOePIESlBSNGMCKmOyvnBWfHfmQlOeBCExLBXiNnKvbJtPIDrhiIHDRcWPsphgPsMFaEjiI357 = 556
v359 = 173
AaAAaaaAAaaaAaAAAaAAAAAaaaAaAaAaaAaaaaAAAAAAaAaAaaAAaaAAaAaAAAAaaAaaAAaAAaaAaAAAaAAaaaAAAAAaaAaAaaaaaAAAAaaaAaAAAaaAaaAaAaAAAaAaaaaaaaAaaaaaaaAaAaAaaAAaAaAaaAaaAAAAaaAaAaaaAAaAAaAAAAaaAAaAAaaaAAaaaaAaAaaAAaaaaAAaaAAAaaAaaaAaaaaAaaaAAaaaAaaAaAaaaAAAaAAAaaaaAaAaaAaAaaAaAAAaaAAaAaaaAaAaaaAAAaaaaAAaAaaAAaaAaaaAaaAAAAaAAAAAAaAaAAaaAAaaAAAAaAAAaaAAaAAAaaaaAaAAAAaaa = 142
aAAaAaAaAaaAAaAAAaaaAAaAaAaaaaaAaAaaaaAaAaaAAaaAaaaAaAaAAAAaAAAAaAaaaaaaAAaaaAAaaAaaaaaaaAAAAAaAaAAaaAaaAaaaaaaAAaAaAaAaAAaAAaaaAaaaAaAaaaAaaaaAAAaaaAaaaAaaAAAaAAAAAAaAaaaAaAaaaAaAAAaAAaaaaaaaAAAAaaaaaAaAAAaAaAaAAAaaaaaaaAaAAaAaAaAaaAAaaAAaaaaAaAaAaAaaAAAaaaAaaAAAAaAAaaAaAAAaaaAaaaAaaAAAAAAAaaAAaaAAaAAaAAaAaaaAAAaaaAAAAAAAaAaaAAAAAaAAaAAAaAAAAaaAaaAAAaaAAAAaAaa = "JtUBWJoUoBoXDlGjarvzsurLeMAirEObLpYMUmSqTsKmRqITvXFjYXPEwmiUjEHScFcmEMojBxChzGq"
AAAaaAaaaaAAaaaaAAaaAAaAaaAAaaAAAaAaAAaAaaaaAaaaaaAAaAaaAaAaAAAaAAaAaAaAAaaAaAaaAaaAAAAAaAAaaAaAaAAAaaaAAaAaaAaAaaAAaAaaaaAAaaaAaaAaaAaAAaAAAAaAAaaaAaAAAAAAAAAAAaAaaaaaaAAaAAAAaAaAaAaAaaaAAAAaAaAaAAAAAAAaaaAaaAaaaaAaaAaaAAAAAAAAaaAAaaaaaAaaaAAAaaAaAAaAaAaaAaaAAaAaAaaaAAAAaaaAaaaaAAaAAaaAAaAaAAAAaAaaaaAaAAaaAAaaaaaAAaAAAAaaaAAAAaaaAaaaAaAAaaaAaAAAaaaaaaAaaaaaaAaAa = "fswAczCwcXumLBFepFyGVbXVxgpDmJyITBuZfClVZMGWdnCHmjMhxQcqwTEctfFmqyNkbRZHZhkVRKD"
IIlllIlIllIlIIllllllIIllIlIIllIIIIllIlllIllIIIlIlIIlIlIlIIllIlIIIllIIllIlIIlIlIlIIIIlllllIIlIIIIIlIIllIllllIIIlllllIllIIllIIllIlIIIllllllllllIIIlIIlIIIIIllIllIlIIIIIIlIlllIlIIlIIIIIlIlIIIllIIIlIlllllIlIlIIllIIlIlIllIlllIIIIIllIIIIlIlIllllIIlllIIlIllIlIlIIllIlllllIIllIllllllllllIIllllIlIlIIllIIIIIIIlIllIlIIIlIIIIIIIIlIlIIllllllIllIIIllIllIIlIlllIIIlIllIIlllIlIIIIIll = 449
FNfgCJdscETWJcylufrVGNNGSUcpoAlIBEwfbooyVZjcEfUxBuubIJPXmIOtpCFuMiDQalmOtgkftIj369 = "FPfULjHCmliHyTgJgTjCwqEewfECHZRLLWEPYwENtnteaXrsJCiIzrXeqIKkAPbItVKyAyxnFzJuIfF"
l16982451640648017371 = 584
TTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTTT = 335
QGnqnkOZdrANpzQbuxmXsAViIdffeNNTXQcqJKHvyhsAoPklAtxHKdvjZpKeOZwNBMhZwzhinHBBLwk375 = 571
IlIIIllIlIlIIIlllllllIIIIlllllIIllllIIIIlIlllIllllllllllIllIIlIIllIIlIIlIlIIIIlllIlIlIllIlIIllIllIIlIlIIlIlllllIIllIlIllIlIIllllllIllIIIlllIlIIIIlIIIIllIllIlIlllIIlllIIIIlIIllIIIIIIllllIlIlIllIIlIlIllllIlIIIlllIlllIllIlIlIlllllIIlIIllIIlIlIlIIllIlIIlllIllIIlIllIllIlllllIIIIllIlIIlIIIlllIIIlllIlIIIllIlIlIllIllIlIIIIllIlIlIIlllIIIlllllllIllIIIlIlllllIllIlIlIIlllIIllIIllIlIllII = 551
lllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllllll = "rPMnnukVAnIVYgLnpBOLxPghujENIZIphOwSaIBZAijFPAgVFCNVgBPyLsNURpuDDffOClZYfqnndTs"
P1698245164065802381 = 437
a383 = "wgJJpKpGELQEVCrJONWFfOJOPOFSlJMChKqTnOfEJDgstxxLnfToSFyTyjibbVLdivvvcHQndlYudBW"
u1698245164065802385 = 235
UUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUUU = "qchgooNiqwRfUGXLIufjqJbjaGmEXqvfrDcRajwBGivXStcbwhKhtVaZSHIsmrHeoWRZKRMNNjzfQvl"
aaaAAaAAaAAaAaAaaaAAAaAAAAaAaAaaaaAaaaAAaAAAaaAaAAAaAAAAaaAaAaAaAAAAAAaaaaaaAAAaAaAAAaAaAaAAAAAAAaAAaAAaaaaAaaaaAaaAaAaAAaaaaaAaAaAAAAAAaAaaAaAAaAaaaAaAAAAAAAAAaaaaaAAAaAaAAAAaAAAaAaaaaaAaAAaaaAAaAAAAaAaaAAaaAaAAaaAAaAaaAaAaaaAaaaAAaaAaaAaAAaAAaaaAaAaAAAAaaAAAaaAaaAAAAaaAAAaaaaAAAaaAAAaaAaaAaaAaaaaAAAAAaaAaaAaaAAAaAAaaAAaaAAAAAAAAaaaAAAAaAaaaaaaAAAaAAAaAaaAAAaaaAaAaaAaaAAaAaaAAaAAAAaAAa = 306


```
## - Run a Termux :
```python
$ termux-setup-storage
$ termux-change-repo
$ pkg update && pkg upgrade -y
$ pkg install git
$ pkg install python -y
$ pkg install python-pip
$ pip install colorama python_obfuscator
$ git clone https://github.com/ferlyafriliyan/python-obfuscator
$ cd python-obfuscator
$ python obfuscator.py
```


<br>

## <p align="left">📢・Informations・📢</p>
- `✅` Obfuscate python code using method from : https://pypi.org/project/python-obfuscator/
<br>

## <p align="left">⭐・Repository・⭐</p>
If you like this repository, **star** the repository And if you want to share your opinion, please go to **repository discussions**.
<br>

-----

<p align="center"><strong>By Ferly Afriliyan : <a href="https://github.com/ferlyafriliyan/">github.com/ferlyafriliyan</a></strong></p>
