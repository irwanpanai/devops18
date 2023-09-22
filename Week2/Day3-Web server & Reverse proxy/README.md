# Web Server & Reverse Proxy
## buat server tambahan buat nginx

**1. membuat 1 VM ubuntu seperti minggu pertama**

server baru dinamakan server3 dan memiliki username panai dan memiliki ip 192.168.1.240
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/34a46747-6023-4867-80d5-8036d48c443f)

**2. melakukan update dan upgrade**

melakukan update dan upgrade dapat memasukkan perintah berikut

```
sudo apt update; sudo apt upgrade
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/0c60a7d4-90cb-4556-b870-cad19398ac2d)

**3. menginstal aplikasi nginx**

menginstal aplikasi nginx dapat dilakukan dengan perintah ini

```
sudo apt install nginx
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/7fb2e726-85b2-4674-ae7e-3607b67d2df7)

**4. jalankan aplikasi nginx**

menjalankan nginx dapat dilakukan dengan pperintah ini
```
sudo systemctl enable nginx
```
```
sudo systemctl start nginx
```
dan untuk mengecek status nginx dapat dilakukan dengan perintah ini
```
sudo systemctl status nginx
```
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/6b07228c-b61f-4849-a56e-cb4fb421dbac)

**5. buka browser dan akses ip server anda**
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/bfbcc79d-d2a3-4b49-ad1d-6021f078f244)



## Jalankan aplikasi Dumbflix menggunakan PM2

**1.install PM2 dengan perintah berikut**

```
npm install pm2 -g
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/c24923eb-eb36-4820-a2a3-28212f20012e)

**2. masuk ke dirktori src pada dumbflix lalu jalankan PM2**

```
cd dumbflix-frontend/src
```

```
pm2 start index.js
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/1277cddd-f13f-472c-8f27-951a63671624)

## reverse proxy dengan directory /etc/nginx/dumbways

**1. masuk ke direktori /etc/nginx lalu buat direktori dumbways**

```
cd /etc/nginx
```

```
sudo mkdir dumbways
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/95666841-8136-4d5d-b243-c14c0384a769)

**2. diluar direktori dumbaways edit file nginx.conf**

```
sudo nano nginx.conf
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/d111ddd0-4afb-4d7c-8902-9e51789c71b4)

**3. di bagian include tambahkan direktori dumbways yang sudah dibuat tadi**

```
include /etc/nginx/dumbways/*;
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/8475e0cf-4be2-46fd-99c7-461a9dc8f5d3)

**4. masuk ke direktori dumbways lalu buat file konfigurasi berikut**

```
cd dumbways
```

```
sudo nano reverse-proxy
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/a3d8da79-e2c0-424a-a695-1814ac8c2c19)

**5. terus masukan konfigurasi berikut**

```
server { 
    server_name dumbflix.xyz; 
  
    location / { 
             proxy_pass http://127.0.0.1:3000;
    }
}
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/249873f7-cc78-48a7-a20f-ef33bce350f9)

**6. setting host pada windows**

buka file explorer lalu menuju direktori C:\Windows\System32\drivers\etc

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/719cf82f-69b7-46e9-a61c-74d26bb337b3)

**7. buka file host dengan notepad yang dijalankan sebgai admin lalu tambahkan ip server anda dengan domain**

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/ac55afef-b8e7-4694-acd6-d4891a07d09b)


**8. cek konfigurasi dengan menjalankan perintah**

```
sudo nginx -t
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/d13bdf2b-fc40-4b22-863c-bccb64808279)

**9. Jika sudah sekarang kita tinggal melakukan reload dan mengecek status Nginx**

```
sudo systemctl reload nginx
```

```
sudo systemctl status nginx
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/a8277d4d-619a-4d80-88f1-49e88c8d734b)

**10. buka browser dan akses domain yang sudah dibuat tadi**

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/a0c29b80-55ac-4907-b35e-8cc6c40cec4b)

**11. Jalankan perintah npm start di direktori dumbflix-frontend dan cek domain tadi**

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/29b93f2c-79e6-4795-b601-f1f2c28736b3)


