# Version Control System with Git
## Penjelasan Distributed Version Control

Sistem kontrol versi terdistribusi (Distributed Version Control System atau DVCS) adalah jenis sistem kontrol versi yang memungkinkan pengembang untuk mengelola perubahan dalam kode sumber secara terdistribusi di seluruh tim pengembangan perangkat lunak. Berikut adalah penjelasan lebih rinci tentang DVCS:

1. **Tersebar (Distributed):** DVCS memungkinkan setiap anggota tim memiliki salinan lengkap dari seluruh repositori proyek, termasuk semua sejarah perubahan. Ini berbeda dengan sistem kontrol versi sentral (Centralized Version Control System atau CVCS), di mana ada satu server sentral yang menyimpan semua informasi versi dan anggota tim hanya memiliki salinan kerja.

2. **Repositori**: Repositori adalah tempat penyimpanan utama untuk kode sumber proyek. Setiap anggota tim memiliki repositori penuh di komputernya, yang mencakup sejarah perubahan dan cabang (branches) proyek. Ini memungkinkan setiap anggota untuk bekerja secara independen dan secara lokal.

3. **Cabang (Branching):** Salah satu fitur utama DVCS adalah kemampuan untuk membuat cabang. Cabang adalah salinan independen dari kode sumber yang dapat dimodifikasi tanpa memengaruhi kode sumber utama. Ini memungkinkan pengembang untuk bekerja pada fitur atau perbaikan bug tanpa mengganggu kode utama dan kemudian menggabungkan perubahan mereka ke kode utama saat mereka siap.

4. **Penggabungan (Merging):** Setelah selesai bekerja pada cabang, pengembang dapat menggabungkan perubahan mereka ke dalam cabang utama atau cabang lainnya. Proses ini disebut penggabungan (merging), dan DVCS memiliki algoritma yang cerdas untuk mengatasi konflik dan menggabungkan perubahan dengan aman.

5. **Pengunduhan (Cloning):** Saat seorang pengembang bergabung dengan proyek yang ada, dia dapat mengunduh seluruh repositori dan sejarahnya ke komputernya, yang disebut pengunduhan (cloning). Ini memberikan pengembang akses penuh ke kode sumber dan sejarah perubahan proyek.

6. **Pengiriman (Pushing) dan Penarikan (Pulling):** Pengembang dapat mengirim (push) perubahan mereka ke repositori yang terdistribusi, sehingga perubahan tersebut dapat diakses oleh anggota tim lainnya. Mereka juga dapat menarik (pull) perubahan dari repositori lain ke repositori lokal mereka.

7. **Riwayat Perubahan yang Kuat:** DVCS menyimpan riwayat perubahan yang kuat, sehingga Anda dapat melacak setiap perubahan kode sumber dari awalnya. Ini sangat berguna untuk menganalisis sejarah proyek, mencari sumber bug, dan memahami bagaimana proyek telah berkembang seiring waktu.

Contoh DVCS yang populer adalah Git, yang dikembangkan oleh Linus Torvalds dan banyak digunakan di seluruh dunia. Git memungkinkan pengembang untuk bekerja dengan repositori lokal dan repositori jarak jauh (remote) secara efisien, menjadikannya salah satu DVCS yang paling populer dan kuat yang tersedia saat ini.

## Buat repositori dengan nama makanan kesukaan dan berisi 3 file yang berbeda

1. Pada menu repositori klik new lalu pada kolom repositori name isi dengan nama makanan kesukaan misalnya ayam_geprek lalu klik create repositori![14](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/805fefd4-6f9d-4511-93be-44b9caaaa2cb)  ![17](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/50f92d4a-8bda-4da4-b3ef-609c5f256a23)
2. Berikutnya pada terminal kita membuat directory terlebih dahulu, setelah itu baru melakukan inisialisasi untuk directory tersebut :
```
mkdir ayam_geprek
```
```
cd ayam_geprek
```
```
git init
```
![18](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/f9226dff-b419-488b-99a9-b1859c32a0ca)

3. kita hubungkan repositori github dengan terminal ini dengan cara :
```
git remote add origin git@github.com:irwanpanai/ayam_geprek.git
```
![21](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/79b8c898-5b69-43e8-9b57-8ce1f2742927)

4. kita buat 3 file berbeda misalnya paha, dada, sayap
```
touch paha dada sayap
```
kita gunakan ``` git status ``` untuk melihat kondisi file sudah di tahap apa
![22](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/48b111d4-75d0-431c-9ebb-b4109c7169c5)

5. berikutnya ke3 file tersebut kita buat ke tahap Staged dengan cara:
```
git add .
```
![23](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/fc2990a7-9780-4ff3-8ccf-18ac9e5035c7)

6. berikutnya file tersebut kita commit sehingga tersimpan ke database git
```
git commit -m "dimasak"
```
![24](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/e38303a2-63e2-4712-bee6-4df804ec6b6e)

7. setelah tersimpan di database git selanjutnya kita push atau mengupload file tersebut di github dengan cara
```
git push origin master
```
![25](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/2dec5b0c-746b-4133-8bed-cdc9799a600a)
![26](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/b965a799-e70c-4720-a27b-9cf65245c1ac)

## Membuat 2 Branch Baru

untuk membuat branch baru ketik perintah
```
git branch (nama branch)
```
![27](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/aa795d90-c29a-430f-8c70-0787ecda06a8)

untuk melihat isi branch yang dimiliki ketik
```
git branch -a
```
![28](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/b11674ee-749b-47e5-af37-cc6d79c84a61)

untuk push ke github ketik
```
push origin (nama branch)
```
![30](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/581a0c33-5d5c-47e2-a670-dab32560e2a5)
![31](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/59cd82f0-4da1-4cb6-97f4-7471a62f6d1d)
![32](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/d619fbf0-9096-4f6f-9b7f-748c3c8e290b)

## 3 command git
**1. git log**
```
git log
```
Perintah ini digunakan untuk melihat riwayat komit dalam repositori Anda. Ini menampilkan daftar komit beserta informasi terkait seperti penulis, tanggal, dan pesan komit.
![33](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/4b8df888-1371-4c82-90ba-ecd4a5d76593)

**2. git help**
```
git help
```
```
git [nama_perintah] --help
```
perintah ini digunakan untuk mendapatkan bantuan tentang penggunaan setiap perintah tersebut.
![34](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/8e727e5d-ec51-4c07-ad61-eadd3af4d877)

**3. git clean**
```
git clean
```
Perintah git clean digunakan untuk menghapus berkas yang tidak dilacak oleh Git dari direktori kerja Anda. Ini berguna untuk membersihkan berkas yang tidak diinginkan atau sementara, seperti berkas yang dihasilkan oleh kompilasi kode atau berkas yang telah dihasilkan selama pengujian.
![35](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/95b995a9-b92a-47bc-8573-d7520a068e55)
