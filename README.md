class NilaiMahasiswa:
  def __init__(self):
    self.data = []

  def tambah(self, nama, nilai):
    self.data.append({
      'nama': nama,
      'nilai': nilai
    })

  def tampil(self):
    for item in self.data:
      print(f"Nama: {item['nama']}, Nilai: {item['nilai']}")

  def hapus(self, nama):
    for item in self.data:
      if item['nama'] == nama:
        self.data.remove(item)

  def ubah(self, nama, nilai):
    for item in self.data:
      if item['nama'] == nama:
        item['nilai'] = nilai

# Diagram Class

![Diagram Class](https://i.ibb.co/sVHjdV7/Diagram-Class.png)

# Flowchart

![Flowchart](https://i.ibb.co/vhVnG6h/Flowchart.png)

# Penjelasan Program

Program ini dibuat untuk menampilkan daftar nilai mahasiswa. Program ini menggunakan class NilaiMahasiswa yang memiliki beberapa method, yaitu tambah(), tampil(), hapus(), dan ubah(). 

Method tambah() digunakan untuk menambah data mahasiswa, dengan parameter nama dan nilai.

Method tampil() digunakan untuk menampilkan data mahasiswa yang telah ditambahkan.

Method hapus() digunakan untuk menghapus data mahasiswa berdasarkan nama.

Method ubah() digunakan untuk mengubah nilai mahasiswa berdasarkan nam
