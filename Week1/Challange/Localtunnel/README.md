# Localtunnel

## Wayshub-fronntend bisa diakses melalui Localtunnel

**1. melakukan instalasi localtunnel menggunakan npm yang sudah kita install.**

```
npm install -g localtunnel
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/17961145-5a13-4e6f-8977-642c84795dee)

**2. melakukan instalasi wayshub frontend**

```
git clone https://github.com/dumbwaysdew/wayshub-frontend.git
```

```
npm install -y
```

```
npm start
```

**3. cek wayshub kalo sudah berjalan atau belum**

Jika wayshub ter-install, Kita perlu mengecek wayshub sudah berjalan dengan benar dengan membuka IP server kita di web browser:

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/567e0c37-5534-4811-9e3a-8784b9f52500)


**4. menggunakan localtunel untuk untuk menjalankan aplikasi wayshub (nodejs) yang sudah kita install.**

Selanjutnya, buka terminal lain (jangan menutup terminal yang menjalankan aplikasi Anda). Untuk menggunakan LocalTunnel, jalankan perintah berikut:

```
lt --port 3000
```

Disini saya mengisi port 3000 karena wayshub-frontend (NodeJS) berjalan pada port 3000 lalu saya mendapatkan link:

```
https://fine-results-repair.loca.lt/
```

**5. membuka localtunnel yang sedang berjalan**

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/d36a2525-9819-43bb-9524-f09c362944b9)


Selanjutnya, kita membuka link yang tertulis di terminal dan akan terbuka tampilan seperti diatas lalu masukan IP Public yang kita miliki pada Endpoint IP setelah itu klik **Click to Submit**

```
https://ipv4.icanhazip.com/
```

**6. Localtunnel berjalan dengan baik**
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/82541386-60a2-4e07-bc91-e2d49d828eb3)

