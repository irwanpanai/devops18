# Manage server in terminal
## Text Manipulation
Pada dasarnya kita bisa melakukan manipulasi pada sebuah file menggunakan terminal, tanpa menggunakan teks editor seperti nano.

**1. cat**

Cat adalah salah satu perintah yang berfungsi untuk membuat daftar konten atau isi file pada standard output (sdout). Yang kalian tahu pasti perintah cat hanya bisa untuk melihat isi dari suatu file, sebenarnya tidak hanya itu.

Contoh penggunaan :
```
cat (file-name)
```
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/5ae3c2cc-a329-4a73-9cb6-39739954f9bc)

keterangan : untuk melihat isi dari suatu file

```
cat > (file-name)
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/5a524ae4-cafe-4e95-8b88-f5bbdfb47218)

keterangan : untuk membuat suatu file baru serta memasukkan teks, Jika sudah menambakan teks kalian dapat keluar dengan klik CTRL + C.

```
cat file1 file2 > file3
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/4d003035-d99f-4ed4-8727-c13367bed271)

keterangan : untuk menggabungkan dua buah file, dan menyimpannya ke dalam file3

```
cat >> file1
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/ff7e8753-6d5d-433e-9e3c-f009f394b20e)

keterangan : menmambahkan teks ke file tanpa mereplacenya

**2. sed**

Sed adalah singkatan dari stream editor. Gunanya untuk memanipulasi teks dasar pada file. Dengan sed kita dapat mengganti teks dengan cepat.

Contoh penggunaan :

```
sed -i 's/hello/holla/g' file3
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/65853ea2-f978-4823-9bc8-51e0645b70e0)

keterangan : mengganti semua kata Hello menjadi Holla pada file3

**3. grep**

Grep merupakan perintah untuk melakukan pencarian sebuah text dalam sebuah file yang telah dibuat.

Contoh penggunaan :

```
grep dumbways file3
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/d648c410-9fa2-4577-88ea-fb8117352842)

keterangan : akan mencari kata Dumbways pada file3

```
grep -c dumbways file3
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/6d1aa7da-bf64-4920-b473-9333cd576be4)

keterangan : akan menghitung jumlah kata “Dumbways” pada filetiga

```
grep Dumbways *
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/7eaf89d6-507f-4cda-9b79-f8d3ffc08683)

keterangan : akan mencari semua file yang berisikan kata dumbways

**3. sort**

Sort untuk mengurutkan data, baik itu secara ascending atau descending.

Berikut adalah contoh penggunaan :

```
sort file4
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/67a9a7ca-81a3-46c3-a08e-0041402ed166)

keterangan : untuk mengurutkan berdasarkan ascending

```
sort -r file4
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/936c5d7a-75f1-41cf-bd33-1c6904aceb46)

keterangan : untuk mengurutkan berdasarkan descending

**5. echo**
Echo digunakan untuk mencetak string / pesan dari hasil perintah lain.

Berikut adalah contoh penggunaan

```
echo "Hello Dumbways!"
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/0eeaa73d-3c54-4f85-be31-d70bd6c461ef)

keterangan : untuk mencetak string **

```
echo "Hello Dumbways!" >> file3
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/860031c6-509f-4202-9617-3729f0431e43)

keterangan : untuk mencetak kata Hello Dumbways! di file3

```
echo "Replace semua data" > file5
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/2475e9c1-b223-479b-ae3c-82e10a597080)

keterangan : untuk mereplace semua data di file5 dan menggantinya dengan "Replace semua data"

## Tool htop dan nmon

**1.htop**

htop merupakan perintah untuk memonitoring sistem, kita dapat melihat penggunaan memory, cpu, swap.

Berikut adalah contoh penggunaan :

```
htop
```
Jika pada server kalian belum terinstall, maka dapat menjalankan perintah beriku:
```
sudo apt install htop -y
```
```
htop
```

![14](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/b156e913-24f4-40b2-8b8c-e917c9ccac52)

Keterangan :

- CPU adalah berapa jumlah core yang kita miliki.
- Mem adalah total penggunaan memory.
- Swp adalah Memory cadangan.
- Tasks adalah aplikasi yang sedang berjalan di server.
- Load average adalah rata-rata aplikasi yang berjalan.
- Uptime adalah berapa lama server kita hidup.
- PID adalah nomor proses id setiap proses yang berjalan di linux.
- VIRT adalah memory yang terpakai.
- Command adalah perintah apa yang sedang di jalankan.

**2. nmon**

Pada tampilan awal terdapat beberapa pilihan yang dapat kita gunakan, berikut hanyalah contoh penggunaannya :

Untuk instalasi nmon dapat menggunakan perintah berikut :

```
sudo apt install nmon
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/12d25569-f56d-4705-bbfb-62602a4a21a0)

Untuk menjalankan nmon kalian dapat menggunakan perintah dibawah ini

```
nmon
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/94010022-9414-43cc-85c1-362f29de73dd)

Keterangan : Disini kita dapat memilih ingin memonitoring apa saja, Disini kita coba saja untuk menampilkan beberapa saja.

- c adalah CPU
- m adalah Memory
- d adalah Disk
- n adalah network

Berikut adalah tampilan dari nmon untuk menampilkan cpu, memory, disk, dan network

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/268248b7-f052-4874-9fc5-39109a9f4485)

## BASH script untuk instalasi nGinx

Anda dapat membuat skrip BASH sederhana untuk menginstal Nginx dengan perintah berikut:

```bash
#!/bin/bash

# Periksa apakah script dijalankan sebagai superuser
if [ "$EUID" -ne 0 ]; then
    echo "Skrip ini harus dijalankan sebagai superuser (root)." >&2
    exit 1
fi

# Perbarui cache paket
apt update

# Instal Nginx
apt install -y nginx

# Mulai Nginx
systemctl start nginx

# Aktifkan Nginx untuk dijalankan saat boot
systemctl enable nginx

# Tampilkan pesan sukses
echo "Nginx telah berhasil diinstal dan diaktifkan."

exit 0
```

Simpan skrip ini dalam file dengan ekstensi `.sh`, misalnya `install_nginx.sh`, dan berikan izin eksekusi dengan perintah:

```bash
chmod +x install_nginx.sh
```

Kemudian, jalankan skrip tersebut dengan perintah berikut:

```bash
sudo ./install_nginx.sh
```

Skrip ini akan memeriksa apakah Anda menjalankannya sebagai superuser, kemudian memperbarui cache paket, menginstal Nginx, dan mengaktifkannya untuk dijalankan secara otomatis saat sistem boot. Setelah selesai, Anda akan melihat pesan bahwa Nginx telah berhasil diinstal dan diaktifkan.

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/0d1fa2f1-c714-4686-b651-4edb77f34129)

keterangan : kondisi jika skrip dijalankan tidak sebagai superuser(root)

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/e5a8c5f7-2744-4c52-acc9-8cf963ae5836)

keterangan : kondisi jika menjalankan skrip dengan superuser(root)

cek localhost
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/3518dcb1-39d4-4911-9e21-47ebe54815d4)


