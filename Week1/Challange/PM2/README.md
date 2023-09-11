# PM2
## Instalasi PM2 secara global

**1. Install PM2**

Pertama-tama kita perlu meng-install package PM2-nya terlebih dahulu dengan menjalankan perintah:

```
npm install pm2 -g
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/70f190f6-c065-4b91-9c0e-c7f314f4962e)

## Jalankan aplikasi menggunakan PM2

**1. Nodejs**

- Setelah PM2 ter-install, lalu kita menuju direktori src wayshub(nodejs)

```
cd app_nodejs/wayshub-frontend/src
```

- lalu kita coba jalankan NodeJS menggunakan PM2 dengan menjalankan perintah:

```
pm2 start index.js
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/227e8f95-8458-47b6-8da4-9d61a75dbc57)

Jika berhasil, maka akan muncul tampilan seperti diatas. Ini menandakan PM2 dapat menjalankan NodeJS dengan baik

**2. python**

-  menuju direktori python

```
cd app_python
```

- Kita coba jalankan Python menggunakan PM2 dengan menjalankan perintah:
```
pm2 start index --interpreter=python
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/5577946f-acb4-4714-98d6-8e80bbda9c7e)
Jika berhasil, maka akan muncul tampilan seperti diatas. Ini menandakan PM2 dapat menjalankan Python dengan baik
