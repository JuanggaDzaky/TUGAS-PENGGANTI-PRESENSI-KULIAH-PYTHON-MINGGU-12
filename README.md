# TUGAS-PENGGANTI-PRESENSI-KULIAH-PYTHON-MINGGU-12
In [1]:
#program utama
d = int(input("Masukkan jarak dalam kilometer adalh: "))
fc = int(input("Masukkan frekuensi 300 MHz-1000 MHz adalah: "))
area = input("Masukkan tipe area adalah: ")
ht = int(input("Masukkan tinggi antena pemancar 20-300 meter adalah: "))
hr = int(input("Masukkan tinggi antena penerima 1-20 meter adalah: "))
Masukkan jarak dalam kilometer adalh: 7
Masukkan frekuensi 300 MHz-1000 MHz adalah: 500
Masukkan tipe area adalah: urban
Masukkan tinggi antena pemancar 20-300 meter adalah: 150
Masukkan tinggi antena penerima 1-20 meter adalah: 5

In [2]:
import numpy as np

In [3]:
NtL = lambda x: 10*np.log10(x)

In [4]:
LtN = lambda x: 10**(x/10)

In [5]:
def rumusc1 (z):
  if z in range (400,1500):
    return 69.55

  elif z in range (1500,2000):
    return 46.3

In [6]:
def rumusc2 (z):
  if z in range (400,1500):
    return 26.16

  elif z in range (1500,2000):
    return 33.9
    
In [7]:
def rumuscm (area,fc):
  if area ==  "urban":
    return 0
  if area == "suburban":
    return -2*(np.log10(fc/28)**2 - 5.4)
  if area == "open":
    return -4.78*(np.log10(fc))**2 + 18.33*np.log10(fc) - 40.94
