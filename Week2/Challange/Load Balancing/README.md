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

**5. **
