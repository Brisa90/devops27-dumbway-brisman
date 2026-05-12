# Task 4 : Version Control System with GIT

## Penujelasan Github
GitHub adalah sebuah platform berbasis web yang digunakan untuk mengelola proyek perangkat lunak dengan sistem kontrol versi Git. Fungsinya bukan hanya menyimpan kode, tetapi juga memfasilitasi kolaborasi antar developer.

## mengcopy repositori tugas dumbways ke linux
- menggunakan perintah git clone https://github.com/Brisa90/devops27-dumbway-brisman.git

## Membuat 3 file menggunakan terminal linux ke dalam folder tugas
<img width="813" height="488" alt="1a" src="https://github.com/user-attachments/assets/1ea08979-b132-4ff7-a5bb-92bd64afc583" />

## menage repository di terminal
- memngecek status dengan perintah 'git status'
  <img width="653" height="251" alt="2b" src="https://github.com/user-attachments/assets/95838b6f-388d-459e-9a5a-dd55182877dd" />

- melakukan penambahan ke state dengan perintah 'git add .'
  <img width="571" height="266" alt="3a" src="https://github.com/user-attachments/assets/e4951182-749e-4267-94ad-6f3e9c4b41c2" />

- melakukan commit dengan pesan menggunakan perintah 'git commit -m "Pesan"'
  <img width="781" height="112" alt="4a" src="https://github.com/user-attachments/assets/83e21ba1-e5f1-4a23-8666-ad6da40b105b" />

- melakukan remote ssh ke jalur repositori tugas denggan perintah 'git remote set-url origin https://github.com/Brisa90/devops27-dumbway-brisman.git'
- melakukan push dengan perintah "git push -u origin main"-
  <img width="990" height="390" alt="5a" src="https://github.com/user-attachments/assets/f2ad977b-a0dd-42f5-a6bc-1dded4f6019c" />


## cara melakukan cek perubahan file di github
- ubah isi file yang dibuat
- melakukan git status untuk melihat status dan perubahannya, jika ingin mengembalikan file yang diubah masukan perintah 'git restored'
  <img width="990" height="390" alt="5a" src="https://github.com/user-attachments/assets/c787aceb-79b0-4844-bb23-188fa3234eba" />
- atau lanjutkan masukan perintah git add file dan git commit
  <img width="1065" height="250" alt="8a" src="https://github.com/user-attachments/assets/b6825ba8-6633-42bc-be86-3575ca502d3f" />
- lakukan push dengan perintah  "git push -u origin main"
  <img width="1034" height="153" alt="9a" src="https://github.com/user-attachments/assets/3ab6d170-aa6d-4831-97ac-13cb4813ba85" />
- untuk melihat log aktifias perubahan file bisa dengan messukan perintah "git log" atau lebih spesifik "git log -p file3"
  <img width="820" height="488" alt="7a" src="https://github.com/user-attachments/assets/24f379b0-c75c-4124-ad0d-f3a22f7d93c7" />
dari gambar tersebut terilihat isi yang diganti dan diubah di dalam file, termasuk tanggal, pesan commit, dan jumlah karater yang diubah
