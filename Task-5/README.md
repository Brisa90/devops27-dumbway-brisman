## TASK 5 : Aplication on server

1. Node JS
```https://github.com/dumbwaysdev/wayshub-frontend```
-  Deploy app wayshub-frontend
-  Berjalan di port 3000
-  Menggunakan NodeJS 10 & 12
## Jawaban
- install node 12 dan 10, dengan perintah ```nvm install 12``` & ```nvm install 10```, mengubah versi node masukan perintah "node current 10/12"
<img width="448" height="159" alt="2" src="https://github.com/user-attachments/assets/2abce852-6ae1-4b6d-8d8a-3b2406ab6f8c" /><img width="982" height="332" alt="3" src="https://github.com/user-attachments/assets/2f1ad30c-2e73-4678-b006-1092193d5c3e" />
- Melakukan kloning aplikasi dari github dengan perintah ```git clone https://github.com/dumbwaysdev/wayshub-frontend```
- melakukan instalasi npm pada direktori yang diunduh dengan perintah ```npm install```
- jalankan aplikasi dengan perintah npm start, dan buka browser dengan url ```localhost:3000```
<img width="1324" height="715" alt="1" src="https://github.com/user-attachments/assets/fa8da2be-5532-4697-95ba-1bba0f3c9ef6" />


2. pyhton
- Deploy app menampilkan text nama kalian!
- Berjalan di port 5000 & bisa dibuka melalui web
## Jawaban
- mengistall flask dengan perintah ```pip install flask```
<img width="986" height="423" alt="4" src="https://github.com/user-attachments/assets/bbc0f1e5-6b71-460c-a990-a1f0dc508cc4" />
- membuat file index.py dengan nano yang berisikan kodingan sederhana website python dengan flask dan arahkan ke port 5000:

```from flask import Flask

app = Flask(__name__)

@app.route("/")
def index():
        return 'Brisman Dumbways 27 dengan python'

app.run(host='0.0.0.0', port=5000)
```
- jalankan program dengan perintah ```python3 index.py```, dan buka website dengan url localhost:5000
<img width="769" height="289" alt="6" src="https://github.com/user-attachments/assets/7a4baa99-afd9-4f2f-9d2b-4524d36105c8" />


3. Golang
- Deploy app menampilkan text "Golang geming!"
## Jawaban
- buat file main.go dan isi kondingan sederhana yang mengeluarkan output "Golang geming!"
```
package main

import "fmt"

func main() {
    fmt.Println("Golang Gaming")
}
```
- jalankan program dengan perintah ```go run main.go``` output akan mengeluarkan kata "Golang geming!"
<img width="439" height="361" alt="10" src="https://github.com/user-attachments/assets/919f593b-1bb7-41b1-9568-0a878bce829f" />

## Status UFW dalam keadaan aktif
<img width="488" height="343" alt="7" src="https://github.com/user-attachments/assets/7c7aff12-e166-45fe-8786-4b65afd7a253" />

