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

