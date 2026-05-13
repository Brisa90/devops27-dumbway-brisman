## TASK 6 : Web server dan load balance
Task :
1. Gambarkan sturktur web server menggunakan reverse proxy dan jelaskan cara kerjanya!
2. Buatlah Reverse Proxy untuk aplilkasi yang sudah kalian deploy kemarin. (wayshub), untuk domain nya sesuaikan nama masing" ex: ade.xyz .

## Jawaban
## 1. Struktur web server proxy

   <img width="526" height="297" alt="Proxy server drawio" src="https://github.com/user-attachments/assets/0817a446-b2eb-46af-bcc3-bfc84f16092f" />
   
  Web Proxy adalah server perantara yang bertindak sebagai perantara antara klien (pengguna) dan server tujuan (misalnya server web). Fungsi utama Web proxy adalah menerima permintaan dari klien dan meneruskannya ke server tujuan, serta mengirimkan kembali respons dari server tujuan kepada klien.
  Reverse proxy adalah server yang ditempatkan di depan satu atau lebih server web backend untuk mencegat, memeriksa, dan meneruskan permintaan dari klien (pengguna).
  
## 2. menkonfigurasi Domain lokal di komputer menggunakan nama brisman.xyz
- pastikan nginx atau web server sudah berjalan dibrowser dengan perintah ```systemctl status nginx``` atau memasukan IP Address server para browser
- untuk windows masuk ke direktori ```C:\Windows\System32\drivers\etc``` dan edit file host untuk memasukan IP Address server dan masukan domain yang di inginkan (bersifat lokal)
  <img width="616" height="513" alt="1" src="https://github.com/user-attachments/assets/18a86337-d876-40d7-b7a0-eea03f9cedf5" />
- untuk mengecek konfigurasi iP berhasil, bisa cek melalui browser. dan akan menampilkan website server
<img width="1030" height="264" alt="2" src="https://github.com/user-attachments/assets/ec127c24-e3e3-4b3c-9104-3016430b4ed7" />

- melakukan konfigurai nginx pada direktori ```/etc/nginx/sites-enable``` tambahkan file konfigurasi baru yang bernama websitenya serperti ```nano wayshub.conf```

- masukan konfigurasi
```
  server {
    listen 80;
    listen [::]:80;

    server_name brisman.xyz www.brisman.xyz;

    location / {
        proxy_pass http://localhost:3000; 
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }
}
```

- simpan dan restart nginx menggunakan perintah ```nginx -t``` dan ```systemctl restart nginx```
<img width="560" height="164" alt="3" src="https://github.com/user-attachments/assets/ee3dbf14-7d20-46ef-944f-9063a18db8a2" />

- jalankan node js di folder websitenya dengan perintah ```npm start``` dan coba buka website dengan domain lokal melalui browser
<img width="1366" height="664" alt="6" src="https://github.com/user-attachments/assets/e7cf2d45-ec69-4131-bd01-5b563167db57" />

- jika ingin melakukan load balancing web server, bisa wdit file ```wayshub.conf``` pada nginx, dan masukan blok upstream server seperti ini

```
upstream wayshub{
        server 192.168.0.208:3000; # alamat IP webserver1
        server 192.168.0.209:3000; # alamat IP webserver2
}

server {
    listen 80;
    listen [::]:80;

    server_name brisman.xyz www.brisman.xyz;

    location / {
        proxy_pass http://wayshub; #pastikan diganti dengan nama upstreamnya
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }
}
```
