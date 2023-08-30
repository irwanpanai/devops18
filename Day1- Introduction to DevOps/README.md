# Day1-Introduction to DevOps

## Definisi DevOps

DevOps adalah suatu pendekatan dalam pengembangan perangkat lunak dan manajemen infrastruktur yang bertujuan untuk meningkatkan kerjasama antara tim pengembang (Development) dan tim operasi (Operations). Tujuan utama dari DevOps adalah untuk mengatasi hambatan tradisional antara tim pengembang yang ingin menghasilkan perubahan cepat dan tim operasi yang bertanggung jawab atas kestabilan sistem.

DevOps mengedepankan prinsip-prinsip seperti otomatisasi, transparansi, kolaborasi, dan pemantauan berkelanjutan. Pendekatan ini mengusahakan agar proses pengembangan, pengujian, dan penyebaran perangkat lunak menjadi lebih efisien dan dapat diulang secara konsisten. Dengan menerapkan praktik DevOps, organisasi dapat mengurangi waktu rilis perangkat lunak, mengidentifikasi masalah lebih cepat, dan memberikan pengalaman pengguna yang lebih baik.

Beberapa praktik umum dalam DevOps meliputi otomatisasi konfigurasi infrastruktur, pengujian berkelanjutan, otomatisasi dalam penyebaran perangkat lunak (continuous deployment), manajemen kode sumber menggunakan alat seperti Git, pemantauan kinerja sistem secara terus-menerus, dan penerapan konsep Infrastructure as Code (IaC) untuk mengelola infrastruktur sebagai kode yang dapat dikelola melalui repositori kode.

Secara keseluruhan, DevOps bertujuan untuk mengatasi kesenjangan antara pengembangan dan operasi, sehingga organisasi dapat mencapai rilis perangkat lunak yang lebih cepat, lebih andal, dan lebih responsif terhadap perubahan pasar dan kebutuhan pengguna.

## Lifecycle DevOps
![DevOps-Lifecycle](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/474fcb69-6453-449a-80de-dfbd52b2abe5)
Pendekatan DevOps melibatkan beberapa praktik dan siklus yang dikenal sebagai "Continuous X" (Berlanjut X), yang masing-masing fokus pada aspek tertentu dalam pengembangan perangkat lunak dan manajemen infrastruktur secara terus-menerus. Berikut adalah beberapa fase penting dalam siklus hidup DevOps:

1. **Continuous Integration (CI)**:
   Continuous Integration adalah praktik di mana para pengembang secara teratur menggabungkan kode mereka ke dalam repositori bersama. Setiap kali perubahan kode diunggah, sistem otomatis akan melakukan proses build, pengujian, dan integrasi untuk memastikan bahwa perubahan tersebut berintegrasi dengan baik dengan kode yang ada. Tujuannya adalah untuk mencegah masalah integrasi yang muncul terlambat dalam siklus pengembangan.

2. **Continuous Delivery (CD)**:
   Continuous Delivery melibatkan otomatisasi dalam proses pengiriman perangkat lunak ke lingkungan produksi atau produksi-seperti (staging) dengan cepat dan aman. Dalam fase ini, setiap perubahan yang melewati proses CI akan siap untuk diterapkan, dan tim dapat memutuskan untuk merilisnya atau tidak. Proses ini memastikan bahwa perangkat lunak selalu dalam keadaan yang siap untuk rilis.

3. **Continuous Deployment (CDeploy)**:
   Continuous Deployment adalah langkah lebih lanjut dari Continuous Delivery. Di sini, setiap perubahan yang melewati proses CI otomatis akan diterapkan secara langsung ke lingkungan produksi tanpa campur tangan manusia. Praktik ini memungkinkan untuk rilis yang sangat cepat dan responsif, tetapi memerlukan tingkat otomatisasi dan kepercayaan yang tinggi dalam proses pengujian dan deploynya.

4. **Continuous Testing (CT)**:
   Continuous Testing melibatkan otomatisasi dalam pengujian perangkat lunak sepanjang siklus pengembangan. Ini mencakup pengujian unit, integrasi, fungsional, kinerja, dan lainnya. Tujuannya adalah untuk memastikan bahwa perangkat lunak tetap stabil, andal, dan sesuai dengan kebutuhan pengguna selama perubahan terus-menerus.

5. **Continuous Monitoring (CM)**:
   Continuous Monitoring melibatkan pemantauan berkelanjutan terhadap kinerja dan kesehatan sistem yang berjalan dalam produksi. Tim operasi dapat melacak metrik penting, mendeteksi masalah potensial, dan merespons secara cepat jika ada gangguan atau penurunan kualitas layanan.

6. **Continuous Feedback (CF)**:
   Continuous Feedback adalah praktik untuk mendapatkan masukan dan umpan balik dari berbagai sumber, termasuk pengguna akhir, tim pengembang, dan tim operasi. Umpan balik ini digunakan untuk memperbaiki dan meningkatkan iterasi berikutnya dari perangkat lunak dan proses DevOps secara keseluruhan.

Keseluruhan siklus "Continuous X" ini bekerja secara sinergis untuk menciptakan lingkungan pengembangan yang cepat, andal, dan adaptif, yang menghasilkan perangkat lunak berkualitas tinggi dengan kecepatan dan efisiensi tinggi.

## Instalasi Ubuntu Server dengan VMWare
Berikut adalah langkah-langkah untuk menginstal Ubuntu menggunakan VMware Workstation:

Langkah 1: Persiapan
1. Unduh installer Ubuntu terbaru dari situs resmi: https://ubuntu.com/download/server
2. Unduh dan instal VMware Workstation dari situs resmi: https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html

Langkah 2: Membuat Mesin Virtual Baru
1. Buka VMware Workstation.
2. Klik "File" > "New Virtual Machine" untuk memulai wizard pembuatan mesin virtual.
3. Pilih "Typical" untuk memudahkan proses instalasi.
4. Pada langkah "Installer disk image file (iso)," pilih "Browse" dan arahkan ke file ISO Ubuntu yang telah Anda unduh sebelumnya.
5. Beri nama untuk mesin virtual Anda dan tentukan lokasi penyimpanan.
6. Pilih ukuran disk virtual (direkomendasikan minimal 20GB).
7. Klik "Finish" untuk membuat mesin virtual.

Langkah 3: Konfigurasi Mesin Virtual
1. Klik kanan pada mesin virtual yang baru dibuat dan pilih "Settings."
2. Atur jumlah CPU 1 CPU atau 2 CPU jika kuat dan RAM 1 GB 
3. Pada bagian "Network Adapter," pastikan opsi "Bridged" atau "NAT" terpilih untuk mengaktifkan konektivitas jaringan di dalam mesin virtual.
4. Klik "OK" untuk menyimpan konfigurasi.

Langkah 4: Instalasi Ubuntu
1. Klik kanan pada mesin virtual dan pilih "Power On" untuk menjalankannya.
2. Mesin virtual akan mulai boot dari file ISO Ubuntu. Pilih "Install Ubuntu" pada layar awal.
3. Pilih bahasa yang diinginkan dan klik "Continue."![18](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/aed6744c-1534-457f-a12d-cec678f36dab)
4. Pada layar "Installer update available" Anda dapat memilih opsi seperti update to the new installer atau continue without updating sesuai preferensi Anda.![19](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/e4286792-c5e2-4ddc-9eb8-10c2ac993620)

5. Pada layar "keyboard configuration," pilih layout dan variant keyboard sesuai preferensi anda lalu done![20](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/23f3b2b4-a9f4-4409-a130-326e3651dffa)
6. Pada layar network "connections" secara default ip anda akan di setiing dhcp dan anda akan mengubahnya ke statis agar suatu saat kita mengakses server ipnya tidak berubah-rubah. untuk mengubahnya pilih ens33 lalu edit IPv4![21](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/f8b7bb05-f4dd-4799-9327-fb963bd83705)

7. IPv4 Method diubah ke manual dan konfigurasi subnet, address, dan gateway berdasarkan jaringan yang anda pakai (dapat dilihat lewat ipconfig dari command prompt) dan name serversnya kita pilih 8.8.8.8, 8.8.4.4 yang mana ini adalah name server dari google setelah selesai klik save dan done![22](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/5936f957-8708-430a-9a17-e6002ec074c3)

8. Pada layar Guided storage configuration centang custom storage layout![26](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/9710dde9-6373-4668-9b7c-18b008af29dc)

9. Buat partisi dari storage anda yang pertama buat 15G dengan format ext4 dan moun point di / yang kedua buat partisi sebesar 4G dengan format SWAP setelah selesai klik done dan continue![30](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/b1796647-9279-4495-9cd1-221e1572f754)

10. buat profil setup anda berupa nama, nama server, username, password. pilih done setelah selesai![32](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/8f4967c8-ef02-4ba3-86c2-3c2dc4e2d886)

11. pada layar SSH setup centang Instal OpenSSH server lalu done![33](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/1e48ab10-30ce-4cd9-8af1-8c62a62370bb)

12. pada layar Featured server Snap terdapat beberapa fitur yang anda bisa tambahkan dengan mencentangnya setelah selesai pilih done![34](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/387da54d-6c03-448c-bff4-9d4ba532517c)

13. proses installing berjalan dan tunggu beberapa menit ![35](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/574ad0d9-6b1f-4058-b6b3-9685e36533e7)

14. setelah selesai restart VMware anda![37](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/e1d41a69-bd7c-4eca-85e6-d6ba4375ea37)

15. setelah masuk ubuntu ketik username lalu enter dan masukkan username dan password yang telah dibuat tadi![39](https://github.com/irwanpanai/devops18-dumbways-irwanpanai/assets/89429810/633a12a6-488f-4c45-a166-e45e89199706)

Selamat, Anda telah berhasil menginstal Ubuntu menggunakan VMware Workstation! Pastikan Anda memahami bahwa panduan ini bisa saja mengalami perubahan tergantung pada versi VMware Workstation dan Ubuntu yang digunakan.
