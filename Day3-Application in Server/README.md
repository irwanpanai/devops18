# Day3-Application in Server
## Deploy Aplikasi wayshub-frontend (NodeJS)
Repository : https://github.com/dumbwaysdev/wayshub-frontend

**1. Persiapan Awal**

- Pastikan server Ubuntu Anda sudah terpasang Node.js dan npm (Node Package Manager).
- Juga pastikan Anda memiliki Git terpasang untuk mengunduh repositori.

**2. Kloning Repositori**

Buka terminal di server Ubuntu Anda dan jalankan perintah-perintah berikut:
```
# Pindah ke direktori di mana Anda ingin menyimpan repositori
cd /path/ke/direktori/tujuan/

# Klon repositori dari GitHub
git clone https://github.com/dumbwaysdev/wayshub-frontend.git
```

**3. Instalasi Dependensi**

Pindah ke direktori repositori yang baru saja diunduh dan jalankan perintah untuk menginstal dependensi:
```
cd wayshub-frontend
npm install
```
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/b2ad10fb-637c-4d44-b92c-dd802e2d6595)

**4. Build Aplikasi**
Jika aplikasi frontend ini menggunakan build tools seperti Webpack atau Gulp, Anda perlu melakukan proses build sebelum menjalankan aplikasi:
```
npm run build
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/481066de-2630-4f7c-8e72-56cedef4b348)

**5.Menjalankan Aplikasi**
Setelah melakukan build, Anda dapat menjalankan aplikasi dengan perintah berikut:
```
npm start
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/69a2c9f1-9fe8-46b6-9d9f-597647944bcf)

**hasil deploy dapat diakses di localhost dengan port 3000**

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/28d0b559-94f9-4c6b-9c11-61b32e58187a)


## Deploy Golang 

Untuk melakukan deploy sebuah program menampilkan nama sendiri yang ditulis dalam bahasa pemrograman Go (Golang) di sistem operasi Ubuntu, Anda dapat mengikuti langkah-langkah berikut:

1. **Instalasi Golang:**
   Pastikan Anda memiliki Go terinstal di sistem Ubuntu Anda. Jika belum, Anda dapat mengikuti panduan di situs resmi Golang: https://golang.org/doc/install

2. **Membuat Direktori dan Kode Program:**
   Buatlah direktori untuk proyek Anda dan masuk ke dalamnya. Selanjutnya, buatlah file dengan ekstensi `.go` (misalnya `irwan.go`) dan tambahkan kode "Irwan Panai" berikut:

   ```go
   package main

   import "fmt"

   func main() {
       fmt.Println("Irwan Panai")
   }
   ```
   ![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/35213073-5345-46e2-9e77-ed97589cca75)


3. **Kompilasi dan Menjalankan:**
   Buka terminal, arahkan ke direktori proyek Anda, dan jalankan perintah berikut untuk mengompilasi dan menjalankan program:

   ```bash
   go run irwan.go
   ```
   ![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/5dc3637f-df2d-4e06-90d2-e2bb493ce4bb)

   Anda akan melihat keluaran "Irwan Panai" di terminal.

4. **Build Binary (Opsional):**
   Jika Anda ingin menghasilkan binary yang dapat dijalankan tanpa perlu menggunakan perintah `go run`, Anda dapat melakukan kompilasi dengan perintah berikut:

   ```bash
   go build -o irwan irwan.go
   ```

   Ini akan menghasilkan file binary bernama `irwan`. Anda dapat menjalankannya dengan:

   ```bash
   ./irwan
   ```
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/4f13e5ae-d88a-4970-8fc7-8760f95492c5)


## Deploy python

Untuk mendeploy skrip Python di Ubuntu Server dan menampilkan nama sendiri melalui localhost dengan port 5000, Anda dapat menggunakan kerangka kerja web seperti Flask. Berikut langkah-langkah umumnya:

1. **Instalasi Python:**
Pastikan Anda memiliki Python terinstal di Ubuntu Server Anda. Jika belum, Anda dapat menginstalnya dengan perintah:

```bash
sudo apt update
sudo apt install python3
```

2. **Buat Skrip Flask:**
Buat skrip Flask dengan menyusun aplikasi web sederhana yang menampilkan "Irwan Panai". Buat file dengan nama `irwan.py` dan tambahkan kode berikut:
```
nano irwan.py
```

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def irwan():
    return "Irwan Panai"

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000)
```

3. **Instalasi Flask:**
Pastikan Anda menginstal Flask di Ubuntu Server. Anda dapat melakukannya dengan perintah:

```bash
pip install Flask
```
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/788e28a9-ce6c-46c9-ba91-08508446a5fb)

4. **Jalankan Aplikasi:**
Jalankan aplikasi Flask dengan menjalankan perintah berikut di terminal:

```bash
python3 irwan.py
```
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/77cada14-1875-44c2-a456-eb36aeb40d53)

Aplikasi akan berjalan dan mendengarkan pada alamat `0.0.0.0` (semua antarmuka) dengan port 5000.

5. **Akses Aplikasi Melalui Web Browser:**
Buka web browser di komputer lokal Anda dan akses alamat IP dari Ubuntu Server dengan port 5000, misalnya: `http://alamat_ip_server:5000`. Anda akan melihat teks "Irwan Panai" muncul di halaman web.

Pastikan firewall pada server Anda memungkinkan koneksi ke port 5000 jika Anda mengalami masalah akses.
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/ecef374d-f599-43d8-915c-8033eab42c2d)


