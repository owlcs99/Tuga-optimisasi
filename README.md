1. Persiapkan Lingkungan
Instal Git : Pastikan Anda telah menginstal Git di komputer Anda.
Buat Akun GitHub : Jika belum memiliki akun, daftar di GitHub dan buat repositori baru untuk proyek Anda.
2. Kloning Repositori
Buka MATLAB dan buat folder baru untuk proyek Anda.
Di dalam MATLAB, gunakan perintah berikut untuk meng-clone repositori dari GitHub:
Bahasa Inggris Matlab
!git clone https://github.com/username/repo.git
Gantilah dengan nama pengguna dan nama repositori yang sesuai.username/repo
3. Buka Skrip di MATLAB
Setelah repositori berhasil di-clone, buka folder tersebut di MATLAB menggunakan:
Bahasa Inggris Matlab
cd('path_to_cloned_repo')
Gantilah dengan jalur ke folder yang telah Anda clone.path_to_cloned_repo
4. Jalankan Skrip
Temukan skrip MATLAB (file .m) yang ingin Anda jalankan.
Jalankan skrip tersebut dengan mengetikkan nama file (tanpa ekstensi .m) di Command Window:
Bahasa Inggris Matlab
script_name
Gantilah dengan nama skrip yang ingin dijalankan.script_name
5. Menggunakan GitHub Actions (Opsional)
Jika Anda ingin mengautomasi pengujian skrip MATLAB menggunakan GitHub Actions:
Buat file workflow YAML di dalam folder pada repositori Anda..github/workflows
Gunakan contoh berikut untuk membuat alur kerja:
teks
name: MATLAB CI

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v2

      - name: Set up MATLAB
        uses: matlab-actions/setup-matlab@v1

      - name: Run MATLAB script
        run: matlab -batch "run('your_script.m')"
Gantilah dengan nama skrip yang ingin dijalankan.your_script.m
6. Push Perubahan ke GitHub
Setelah melakukan perubahan atau menambahkan skrip baru, jangan lupa untuk melakukan commit dan push ke repositori menggunakan perintah:
Bahasa Inggris Matlab
!git add .
!git commit -m "Menambahkan skrip baru"
!git push origin main
Dengan mengikuti langkah-langkah ini, Anda dapat menjalankan skrip MATLAB dari GitHub dengan mudah dan efisien.
