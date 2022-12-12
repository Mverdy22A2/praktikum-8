# praktikum 8
pertemuan ke 12

# Penjelasan Program

Program ini dibuat untuk menampilkan daftar nilai mahasiswa. Program ini menggunakan class NilaiMahasiswa yang memiliki beberapa method, yaitu tambah(), tampil(), hapus(), dan ubah(). 

Method tambah() digunakan untuk menambah data mahasiswa, dengan parameter nama dan nilai.

Method tampil() digunakan untuk menampilkan data mahasiswa yang telah ditambahkan.

Method hapus() digunakan untuk menghapus data mahasiswa berdasarkan nama.

Method ubah() digunakan untuk mengubah nilai mahasiswa berdasarkan nam

# algoritma program

1. buat class mahasiswa
2. buat method tambah()
3. buat method tampil()
4. buat method hapus()
5. buat method ubah()
6. buat variabel untuk menyimpan data mahasiswa
7. buat looping untuk mengambil data mahasiswa
8. buat kondisi untuk mengecek data mahasiswa
9. buat perintah untuk menambah, menampilkan, dan mengubah data mahasiswa
10. keluar dari looping
11. program selesai

# membuat class mahasiswa
class DaftarNilai:
    __listNilai = []
# masukan fungsi tambah
    def tambah(self):
        print("\nTambah Data Nilai\n")
        nama = input("Masukkan Nama    : ")
        nim = input("Masukkan NIM     : ")
        tugas = int(input("Masukkan Nilai Tugas  : "))
        uas = int(input("Masukkan Nilai UAS    : "))
        uts = int(input("Masukkan Nilai UTS    : "))
        akhir = int((tugas + uas + uts) / 3)
        data = [nama, nim, tugas, uas, uts, akhir]
        self.__listNilai.append(data)
        print("\nData berhasil ditambahkan\n")
# masukan fungsi tampil
    def tampil(self):
        print("\nDaftar Nilai Mahasiswa\n")
        print(
            "========================================================================")
        print("| No |   Nama    |     NIM    | Tugas |  UAS  |  UTS  |  Akhir  |")
        print(
            "========================================================================")
        no = 1
        for item in self.__listNilai:
            print("| {0:2} |   {1:8}|  {2:10}|{3:5}  | {4:5} | {5:5} | {6:7} |".format(no, item[0], item[1], item[2],
                                                                                     item[3], item[4], item[5]))
            no += 1
        print(
            "========================================================================")
# masukan fungsi hapus
    def hapus(self):
        print("\nHapus Data Nilai\n")
        nama = input("Masukkan Nama : ")
        for item in self.__listNilai:
            if item[0] == nama:
                self.__listNilai.remove(item)
        print("\nData berhasil dihapus\n")
# masukan fungsi ubah
    def ubah(self):
        print("\nUbah Data Nilai\n")
        nama = input("Masukkan Nama : ")
        for item in self.__listNilai:
            if item[0] == nama:
                nim = input("Masukkan NIM     : ")
                tugas = int(input("Masukkan Nilai Tugas  : "))
                uas = int(input("Masukkan Nilai UAS    : "))
                uts = int(input("Masukkan Nilai UTS    : "))
                akhir = int((tugas + uas + uts) / 3)
                item[1] = nim
                item[2] = tugas
                item[3] = uas
                item[4] = uts
                item[5] = akhir
        print("\nData berhasil diubah\n")
