##  Muhammad Rafi Albani Rasyin

## 312410316

## TI.24.A.4

## Bahasa Pemrograman 


# LATIHAN PRAKTIKUM

Tugas Praktikum

Buat program sederhana yang akan menampilkan daftar nilai mahasiswa, dengan ketentuan • Program dibuat dengan menggunakan Dictionary • Tampilkan menu pilihan: (Tambah Data, Ubah Data, Hapus Data, Tampilkan Data, Cari Data) • Nilai Akhir diambil dari perhitungan 3 komponen nilai (tugas: 30%, uts: 35%, uas: 35%) • Buat flowchart dan penjelasan programnya.

# ELEMEN

```python
list_a = [1, 2, 3, 4, 5]

print(list_a[2])

print(list_a[1:4])

print(list_a[-1])

list_a[3] = 10
print(list_a)

list_a[3:] = [11, 12, 13]
print(list_a)

list_b = list_a[:2]
print(list_b)

list_b.append("misalnya")
print(list_b)

list_b.extend([14, 15, 16])
print(list_b)

list_a.extend(list_b)
print(list_a)
````

## DAN HASIL PROGRAM TERSEBUT

![386233440-513a891b-0f79-4b90-997a-629ecc1c9bd8](https://github.com/user-attachments/assets/3f46cfa3-645b-43e5-ad06-f70f41a790ec)

# MENAMBAH DATA

```python
class Mahasiswa:
    def __init__(self, nama, nim, nilai_tugas, nilai_uts, nilai_uas):
        self.nama = nama
        self.nim = nim
        self.nilai_tugas = nilai_tugas
        self.nilai_uts = nilai_uts
        self.nilai_uas = nilai_uas

    def hitung_nilai_akhir(self):
        return (self.nilai_tugas + self.nilai_uts + self.nilai_uas) / 3

mahasiswa = []

while True:
    nama = input("Nama: ")
    nim = int(input("NIM: "))
    nilai_tugas = int(input("Nilai Tugas: "))
    nilai_uts = int(input("Nilai UTS: "))
    nilai_uas = int(input("Nilai UAS: "))

    mahasiswa.append(Mahasiswa(nama, nim, nilai_tugas, nilai_uts, nilai_uas))

    tambah_data = input("Tambah data (y/t)? ")
    if tambah_data.lower() == "t":
        break

print("-" * 80)
print("| No | Nama       | NIM  | Tugas | UTS  | UAS  | Akhir     |")
print("-" * 80)

for i, mhs in enumerate(mahasiswa):
    nilai_akhir = mhs.hitung_nilai_akhir()
    print(f"| {i+1:<2} | {mhs.nama:<10} | {mhs.nim:<4} | {mhs.nilai_tugas:<5} | {mhs.nilai_uts:<5} | {mhs.nilai_uas:<5} | {nilai_akhir:<9.2f} |")

print("-" * 80)
````

## penjelasan code menambah data

```python
class Mahasiswa:
    def __init__(self, nama, nim, nilai_tugas, nilai_uts, nilai_uas):
        self.nama = nama
        self.nim = nim
        self.nilai_tugas = nilai_tugas
        self.nilai_uts = nilai_uts
        self.nilai_uas = nilai_uas
````

__init__:konstruktor ini digunakan menginisialisasi objek mahasiswa dengan fungsi: nama,nim,nilai_tugas,nilai uts,nilai uas`

```python
def hitung_nilai_akhir(self):
        return (self.nilai_tugas + self.nilai_uts + self.nilai_uas) / 3
````

Metode ini mengembalikan nilai akhir dari program tersebut,dari nilai_tugas,nilai_uts,nilai_uas

```python
mahasiswa = []
````

daftar kosong untuk meyimpan objek mahasiswa yang di tambahkan

```python
while True:
    nama = input("Nama: ")
    nim = int(input("NIM: "))
    nilai_tugas = int(input("Nilai Tugas: "))
    nilai_uts = int(input("Nilai UTS: "))
    nilai_uas = int(input("Nilai UAS: "))

    mahasiswa.append(Mahasiswa(nama, nim, nilai_tugas, nilai_uts, nilai_uas))

    tambah_data = input("Tambah data (y/t)? ")
    if tambah_data.lower() == "t":
        break
````

meminta pengguna untuk memasukan data berulang kali apabila pengguna memasukan ya pada program tersebut dan apabila pengguna memasukan tidak maka program tersebut berhenti,setiap input digunakan untuk membuat data mahasiswa kemudian di tambahkan ke dalam daftar mahasiswa.

```python
rint("-" * 80)
print("| No | Nama       | NIM  | Tugas | UTS  | UAS  | Akhir     |")
print("-" * 80)

for i, mhs in enumerate(mahasiswa):
    nilai_akhir = mhs.hitung_nilai_akhir()
    print(f"| {i+1:<2} | {mhs.nama:<10} | {mhs.nim:<4} | {mhs.nilai_tugas:<5} | {mhs.nilai_uts:<5} | {mhs.nilai_uas:<5} | {nilai_akhir:<9.2f} |")

print("-" * 80)
````

Header tabel dicetak terlebih dahulu, diikuti oleh baris-baris data untuk setiap mahasiswa, Untuk setiap mahasiswa, metode hitung_nilai_akhir dipanggil untuk menghitung nilai akhir, lalu data ditampilkan dalam format tabel

## code program tersebut

![386243035-6eeeda03-6f56-4c86-96ce-0e7558be4f54](https://github.com/user-attachments/assets/e1f6d504-f256-45ef-84e0-90cbf88dee18)

## hasil program tersebut

![image](https://github.com/user-attachments/assets/c254b495-233e-425f-8a7e-1740eaa62f11)

## dan ini hasil flowchart nya

![386252127-4c457b90-a1c1-4801-b0f3-e77b21dd6411](https://github.com/user-attachments/assets/426908d3-4dee-4c0c-b45a-45f9d4a45577)

