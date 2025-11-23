# Praktikum5-Pertemuan10

Menggunakan kode program 

  data_mahasiswa = {}

  def hitung_nilai_akhir(tugas, uts, uas):
      return (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)

  def tambah_data():
      nim = input("Masukkan NIM: ")
      if nim in data_mahasiswa:
          print("NIM sudah ada.")
          return
      nama = input("Masukkan Nama: ")
      tugas = float(input("Masukkan Nilai Tugas (0-100): "))
      uts = float(input("Masukkan Nilai UTS (0-100): "))
      uas = float(input("Masukkan Nilai UAS (0-100): "))
      nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)
      data_mahasiswa[nim] = {
          'nama': nama,
          'tugas': tugas,
          'uts': uts,
          'uas': uas,
          'nilai_akhir': nilai_akhir
      }
      print("Data berhasil ditambahkan.")

  def ubah_data():
      nim = input("Masukkan NIM yang akan diubah: ")
      if nim not in data_mahasiswa:
          print("NIM tidak ditemukan.")
          return
      print(f"Data saat ini untuk {data_mahasiswa[nim]['nama']}:")
      tugas = float(input("Masukkan Nilai Tugas baru (0-100): "))
      uts = float(input("Masukkan Nilai UTS baru (0-100): "))
      uas = float(input("Masukkan Nilai UAS baru (0-100): "))
      nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)
      data_mahasiswa[nim]['tugas'] = tugas
      data_mahasiswa[nim]['uts'] = uts
      data_mahasiswa[nim]['uas'] = uas
      data_mahasiswa[nim]['nilai_akhir'] = nilai_akhir
      print("Data berhasil diubah.")

 # Menghasilkan seperti berikut
  <img width="384" height="399" alt="Screenshot 2025-11-23 220441" src="https://github.com/user-attachments/assets/dc9fbe45-2c18-4a18-9304-ed37d9d24bde" />

  # FlowChart
  <img width="1280" height="646" alt="image" src="https://github.com/user-attachments/assets/2a5d7ada-f5c0-4d46-8578-cbc6a7279c5b" />

  # Penjelasan Mengenai Kode yang dibuat

1. data_mahasiswa = {}: Ini adalah dictionary kosong yang berfungsi sebagai database sementara untuk menyimpan data mahasiswa. Kunci (key) dari dictionary ini adalah NIM      mahasiswa.
2. def hitung_nilai_akhir(tugas, uts, uas):: Fungsi ini menghitung nilai akhir mahasiswa berdasarkan nilai tugas (bobot 30%), UTS (bobot 35%), dan UAS (bobot 35%).
def tambah_data():: Fungsi ini memungkinkan pengguna untuk memasukkan data mahasiswa baru (NIM, nama, nilai tugas, UTS, dan UAS).
3. Fungsi ini memeriksa apakah NIM yang dimasukkan sudah ada dalam data_mahasiswa. Jika sudah, akan menampilkan pesan kesalahan.
Setelah data dimasukkan, fungsi ini memanggil hitung_nilai_akhir untuk mendapatkan nilai akhir dan menyimpannya dalam dictionary.
4. def ubah_data():: Fungsi ini memungkinkan pengguna untuk mengubah data mahasiswa yang sudah ada.
Fungsi ini meminta NIM yang akan diubah dan memeriksa apakah NIM tersebut ada dalam data_mahasiswa. Jika tidak, akan menampilkan pesan kesalahan.
5. ubah_data():
Fungsi ini meminta pengguna untuk memasukkan nilai tugas, UTS (Ujian Tengah Semester), dan UAS (Ujian Akhir Semester) yang baru untuk mahasiswa tertentu.
Nilai yang dimasukkan diubah menjadi tipe data float.
Fungsi ini memanggil fungsi lain bernama hitung_nilai_akhir (yang tidak terlihat di gambar) untuk menghitung nilai akhir berdasarkan nilai tugas, UTS, dan UAS yang baru.
Nilai tugas, UTS, UAS, dan nilai akhir yang baru kemudian diperbarui dalam kamus data_mahasiswa untuk NIM (Nomor Induk Mahasiswa) yang sesuai.
Pesan "Data berhasil diubah." akan dicetak setelah pembaruan selesai.
6. hapus_data():
Fungsi ini meminta pengguna untuk memasukkan NIM mahasiswa yang ingin dihapus datanya.
Fungsi ini memeriksa apakah NIM yang dimasukkan ada dalam data_mahasiswa.
7. Jika NIM tidak ditemukan, pesan "NIM tidak ditemukan." akan dicetak dan fungsi berhenti.
8. Jika NIM ditemukan, data mahasiswa dengan NIM tersebut akan dihapus dari kamus menggunakan perintah del.
9. Pesan "Data berhasil dihapus." akan dicetak setelah penghapusan selesai.
10. tampilkan_data():
Fungsi ini memeriksa apakah kamus data_mahasiswa kosong.
11. Jika kosong, pesan "Belum ada data mahasiswa." akan dicetak dan fungsi berhenti.
12. Jika ada data, fungsi ini mencetak header tabel yang rapi untuk kolom NIM, Nama, Tugas, UTS, UAS, dan Nilai Akhir.
13. Fungsi ini kemudian melakukan iterasi melalui semua entri dalam data_mahasiswa dan mencetak detail setiap mahasiswa dalam format baris tabel yang rapi.
14. Format pencetakan menggunakan f-string Python untuk perataan teks dan pemformatan angka desimal.
15. Fungsi cari_data(): Meminta input NIM, memeriksa keberadaan NIM dalam data_mahasiswa, dan mencetak detail mahasiswa (NIM, Nama, Nilai Tugas, UTS, UAS, Nilai Akhir) jika ditemukan.
16. Fungsi main(): Menampilkan menu pilihan (1-6) dan memproses input pengguna untuk memanggil fungsi manajemen data yang sesuai.
17. Struktur Menu: Menu tersebut mencakup opsi untuk "Tambah Data", "Ubah Data", "Hapus Data", "Tampilkan Data", "Cari Data", dan "Keluar".
18. Kode tersebut menunjukkan struktur kontrol if/elif/else yang digunakan untuk menangani pilihan menu dari pengguna.
Terdapat enam pilihan yang tersedia, masing-masing memanggil fungsi yang berbeda seperti tambah_data(), ubah_data(), hapus_data(), tampilkan_data(), dan cari_data().
Pilihan '6' digunakan untuk keluar dari program, sedangkan pilihan lainnya akan menampilkan pesan kesalahan jika tidak valid.
Di bagian bawah, terdapat blok if __name__ == "__main__": yang merupakan titik masuk standar untuk menjalankan skrip Python dengan memanggil fungsi main().

if __name__ == "__main__":
    main()
