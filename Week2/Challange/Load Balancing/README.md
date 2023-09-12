# load balancing

## Menggunakan 2 server, jalankan Load Balancing yang berfungsi dengan baik

**1. menggunakan 2 server**

disini saya sudah memiliki 2 server dimana server utama ssh irwanp@192.168.1.155 server kedua ssh panai@192.168.1.240
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/2e903dfc-3af8-4389-a102-fd98f380dc83)

**2. buat konfigurasi ke dalam file Load_Balancing.conf**

menuju direktori /etc/nginx/dumbways kita buat file configurasi dengan memasukkan perintah
```
sudo nano Load_Balancing.conf
```
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/af77e4ad-a049-4415-90db-f235b1114f21)

**3. masukkan konfigurasi berikut**
```
upstream domain {
    server 192.168.1.155:3000;
    server 192.168.1.240:3000;
}
server {
    server_name dumbflix.xyz;

    location / {
             proxy_pass http://domain;
    }
}
```
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/1d40855c-7289-48bb-a81d-b9a81f7c23cf)

**4. Reload dan cek status nginx**
```
sudo systemctl reload nginx
```
```
sudo systemctl status nginx
```
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/7ae2ac10-d4ef-415f-8c62-765354d0e969)

**5. Jalankan Aplikasi dumbflix di kedua server kita**
```
npm start
```
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/efd5a3f2-ff82-4f38-84eb-4732b80cd243)

**6. Cek browser dan akses domain**

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/5f8b03d6-717b-48e5-95d7-79cdf9c8de93)

**7. Matikan salah satu server untuk mengecek Load Balancing berjalan dengan lancar**
tekan ctrl+c untuk menutup aplikasi
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/afaa10e4-58c2-4273-b3bd-a11bb69c0d77)
aplikasi masih bisa berjalan walaupun aplikasi sudah di tutup di server2 username irwanp

**8. Uji sebaliknya matikan aplikasi di server3 nyalakan di server2**
![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/aca0e752-0dcf-4651-b61d-c4db228bcb3c)
**load Balancing berjalam dengan lancar**



