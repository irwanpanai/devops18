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

htop merupakan perintah untuk memonitoring sistem, kita dapat melihat penggunaan memory, cpu, swap. Berikut adalah contoh penggunaan :

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

Keterangan :

CPU adalah berapa jumlah core yang kita miliki.
Mem adalah total penggunaan memory.
Swp adalah Memory cadangan.
Tasks adalah aplikasi yang sedang berjalan di server.
Load average adalah rata-rata aplikasi yang berjalan.
Uptime adalah berapa lama server kita hidup.
PID adalah nomor proses id setiap proses yang berjalan di linux.
VIRT adalah memory yang terpakai.
Command adalah perintah apa yang sedang di jalankan.
