# NodeJS BASH Script

## Install nodeJS using BASH Script

**1. Buat file script dengan extensi .sh**

Buat File Script dengan nama install_nodejs.sh dengan menjalankan perintah:

```
nano install_nodejs.sh
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/bca31a62-0a55-420d-b6dd-3c6eaa4b78eb)

**2. isi file script**

```
#!/usr/bin/env bash

sudo apt update
sudo apt install nodejs -y
node -v
sudo apt install npm -y
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/e5b47008-5787-4755-8470-ae5a0fe25204)

Terdapat 4 perintah pada Script diatas yaitu, Update Repository, Install NodeJS, Cek Versi NodeJS, Install NPM

**3. Jalankan script**
script dapat dijalankan dengan memasukkan perintah:

```
sh install_nodejs.sh
```

![image](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/02a9fcf5-2415-4b9f-8d02-e41d0e22f61c)
