# Laporan Hasil Praktikum: Final Project Aplikasi Berbasis Container

## Identitas Mahasiswa

- **Nama:** I Komang Wibisana Nugraha W
- **NIM:** 2415354062
- **Kelas/Rombel:** TRPL 4B
- **Tanggal Praktikum:** 20 Mei 2026

---

## Teknologi & Tools yang Digunakan

- **Sistem Operasi:** Windows 11
- **Containerization:** Docker & Docker Hub
- **Bahasa Pemrograman / Framework:** Node.js
- **Database:** MySQL
- **Tools Lain:** VS Code, Git, Thunder Client

---

## Langkah-Langkah Praktikum & Dokumentasi

### Langkah 1: Pengujian Docker Compose, Volume, Network, Container
Menjalankan multi-container application (Backend Node.js & Database MySQL) menggunakan perintah `docker compose up`. Docker Compose otomatis membuat volume untuk persistensi data database dan custom bridge network agar kedua service dapat berkomunikasi.

**Dokumentasi/Screenshot:**

![Docker Compose](img/docker_compose.png)

![Volume](img/volume.png)

![Network](img/network.png)

![Container](img/container.png)



---

### Langkah 2: Pengujian Endpoint -> Request dan Response
Pengujian fitur CRUD REST API dengan mengirim HTTP request GET dan POST ke service backend yang mengekspos port 3000 ke host.

**Dokumentasi/Screenshot:**

![Pengujian Endpoint](img/users.png)

![Pengujian Endpoint](img/get.png)

![Pengujian Endpoint](img/put.png)

![Pengujian Endpoint](img/delete.png)

![Pengujian Endpoint](img/post.png)




---

### Langkah 3: Pengujian upload ke Docker Hub
Melakukan proses _tagging_ pada Docker image aplikasi lokal agar sesuai dengan format repository Docker Hub, lalu mem-push image tersebut ke registry publik.

**Dokumentasi/Screenshot:**

![Proses Push Berhasil](img/dockerhub.png)



---

## Kesimpulan
Praktikum berjalan lancar. Aplikasi backend Node.js dan database MySQL berhasil diisolasi dan dijalankan menggunakan pendekatan multi-container architecture. Docker network memfasilitasi komunikasi antar container tanpa terekspos langsung keluar, sementara environment variables di-manage dengan aman melalui file `.env`. Data pada database juga berhasil dipersistensi menggunakan Docker volume, sehingga tidak hilang meski container dihentikan.