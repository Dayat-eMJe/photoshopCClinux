
<div align="center" class="tip" markdown="1" style>

![screenshot](images/Screenshot.png)

![GitHub repo size](https://img.shields.io/github/license/Gictorbit/photoshopCClinux?style=flat) ![Tested on arch](https://img.shields.io/badge/Tested%20on-Archlinux-brightgreen)
![GitHub stars](https://img.shields.io/github/stars/Gictorbit/photoshopCClinux?style=sad) ![rep size](https://img.shields.io/github/repo-size/gictorbit/photoshopCClinux) ![bash](https://img.shields.io/badge/bash-5.0.11-yellowgreen)
</div>

# photohop CC v19 installer for linux
Scipt bash ini dipakai untuk menginstal Photoshop CC versi 19 di os Linux kalian menggunakan bantuan wine di belakang layar
dan mengatur beberapa komponen yang diperlukan untuk kinerja terbaik

## :rocket: Features
* mengunduh komponen yang diperlukan dan memasangnya (`vcrun`,`atmlib`,`msxml`...)
* mengunduh installer photoshop.exe dan instal secara otomatis
* membuat perintah photoshop dan entri desktop
* mengonfigurasi wine dengan mode gelap
* mendeteksi berbagai kartu grafis seperti (`intel`, `Nvidia`...)
* menyimpan file yang diunduh di direktori cache kalian
* Ini gratis dan Anda tidak memerlukan lisensi key apa pun
* bekerja pada semua distro Linux

## :warning: Requirements
1- gunakan edisi 64bit dari distro kalian <br>
2. pastikan wine sudah terinstall, jika kalian mendapatkan pesan error di wine sebelum menginstal photosop cc tetapi ini penting agar berhasil menginstal photoshop <br>
3. pastikan packages di bawah ini sudah terpasang di distro Linux kalian
* `wine`
* `winetricks`
* `aria2`

jika belum terinstal, kalian bisa menginstalnya menggunakan package manager kalian misalnya di Arch Linux
```bash
sudo pacman -S wine aria2 winetricks
``` 
atau untuk user ubuntu / linux mint . kali linux kalian bisa menjalankan perintah
```bash

sudo apt-get install wine
sudo apt-get install aria2 winetricks
```
3- Pastikan kalian memiliki ruang penyimpanan yang cukup di partisi `/home` sebesar `5 GiB`
> 1 GiB akan terpakai setelah pemasangan

4- Pastikan kalian memiliki koneksi internet dan lalu lintas sekitar 1,5 Gib untuk mengunduh photoshop dan semua komponen yang dibutuhkan untuk pertama kali instalasi

## :computer: Installation
Kalian bisa dengan mudah menjalankan skrip `setup.sh` untuk menginstal photoshop cc di distro linux kalian

```bash
chmod +x setup.sh
./setup.sh
```
rekomendasi nomor 1 menggunakan winetricks
<div align="center" class="tip" markdown="1" style>

![setup-screenshot](images/setup-screenshot.png)
</div>

selama tahap instalasi harap perhatikan pesan notifikasi dari script

> **NOTE :** pastikan versi OS di wine adalah windows 7



## :wine_glass: wineprefix Configuration
jika kalian perlu mengonfigurasi wineprefix dari photoshop, kalian bisa menggunakan perintah `winecfg.sh` dan cukup jalankan perintah di bawah ini
```bash
chmod +x winecfg.sh
./winecfg.sh
```
## :hammer: Tools

<details>
<summary>:sparkles: Liquify Tools</summary>
seperti yang kalian ketahui photoshop memiliki banyak alat yang berguna seperti `Liquify Tools`.</br>

Jika kalian mendapatkan beberapa pesan error selama bekerja dengan tools ini
Mungkin error dikarenakan graphics card.</br>

photoshop menggunakan `GPU` untuk menjalankan tools ini, jadi sebelum menggunakan tools ini, pastikan graphics card kalian `(Nvidia, AMD)` telah dikonfigurasi dengan benar di mesin Linux kalian.
</br>Solusi lainnya adalah kalian bisa mengonfigurasi photoshop untuk menggunakan `CPU` untuk pemrosesan gambar. untuk melakukannya, ikuti langkah-langkah di bawah ini:

* buka tab edit dan buka `preferences` or `[ctrl+K]`
* kemuan kalian kr tab `performance`
* di bagian pengaturan graphics processor, hapus centang `Use graphics processor`

![](https://user-images.githubusercontent.com/34630603/80861998-117b7a80-8c87-11ea-8f56-079f43dfafd9.png)
</details>

---
<details>
<summary>:camera: Adobe Camera Raw</summary>

another useful adobe software is `camera raw` if you want to work with it beside photoshop you must install it separately to do this, after photoshop installation run `cameraRawInstaller.sh` script with below commands:
```bash
chmod +x cameraRawInstaller.sh
./cameraRawInstaller.sh
```
then restart photoshop.you can open it from 
`Edit >>Preferences >> Camera Raw`

> **_NOTE1:_** the size of camera raw installation file is about 400MB


> **_NOTE2:_** camera raw performance depends on your graphic card driver and its configuration

</details>

## :hotsprings: Uninstall
for uninstall photoshop you can use uninstaller script with below commands

```bash
chmod +x uninstaller.sh
./uninstaller.sh
```


## :bookmark: License
![GitHub](https://img.shields.io/github/license/Gictorbit/photoshopCClinux?style=for-the-badge)
