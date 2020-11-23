<p align="center"><img src="https://c.top4top.io/p_1788a90au0.jpg"></p>

<p align="center">
<img src="https://img.shields.io/badge/Python-3-brightgreen.svg?style=plastic">
<img src="https://img.shields.io/badge/Docker-✔-blue.svg?style=plastic">
</p>

<p align="center">
  <a href="https://www.instagram.com/anxsecsyndicate/"><b>Instagram</b></a>
  <span> - </span>
  <a href="https://m.facebook.com/anxsecsyndicate/"><b>Facebook</b></a>
  <span> - </span>
  <a href="https://anxsec-syndicate.blogspot.com/?m=1"><b>AnXsec Syndicate Blog</b></a>
</p>

<p align="center">
  <br>
  <b>Available in</b>
  <br>
  <img src="https://i.imgur.com/1wJVDV5.png">
</p>

Konsep di balik AnonTrack sederhana, sama seperti kami menghosting halaman phishing untuk mendapatkan kredensial mengapa tidak meng-host halaman palsu yang meminta lokasi Anda seperti banyak situs berbasis lokasi populer.. Baca lebih lanjut di <a href="https://anxsec-syndicate.blogspot.com/?m=1"> AnXsec Syndicate Blog </a>.AnonTrack Menghosting situs web palsu di **In Built PHP Server** dan menggunakan **Serveo** untuk menghasilkan tautan yang akan kami teruskan ke target, situs web meminta Izin Lokasi dan jika target memungkinkan, kami bisa mendapatkan [NOT UNDERSTAND LANGUAGE INDONESIA?IM SORRY,YOU CAN USE GOOGLE TRANSLATE] :

* Longitude
* Latitude
* Accuracy
* Altitude - Not always available
* Direction - Only available if user is moving
* Speed - Only available if user is moving

Bersama dengan Informasi Lokasi, kami juga mendapatkan **Informasi Perangkat** tanpa izin apapun :

* Operating System
* Platform
* Number of CPU Cores
* Amount of RAM - Approximate Results
* Screen Resolution
* GPU information
* Browser Name and Version
* Public IP Address
* IP Address Reconnaissance

**Alat ini adalah Bukti Konsep dan Hanya untuk Tujuan Pendidikan, Pencari menunjukkan data apa yang dapat dikumpulkan situs web jahat tentang Anda dan perangkat Anda dan mengapa Anda tidak boleh mengeklik tautan acak dan mengizinkan izin penting seperti Lokasi, dll.**

## Apa bedanya dengan IP GeoLocation

* Alat dan layanan lain menawarkan Geolokasi IP yang TIDAK akurat sama sekali dan tidak memberikan lokasi target, melainkan perkiraan lokasi ISP.

* AnonTrack menggunakan API HTML dan mendapatkan Izin Lokasi lalu mengambil Bujur dan Lintang menggunakan Perangkat Keras GPS yang ada di perangkat, jadi AnonTrack berfungsi paling baik dengan Ponsel Cerdas, jika Perangkat Keras GPS tidak ada, seperti di Laptop, AnonTrack mundur ke Geolokasi IP atau akan mencari Koordinat Cache.

* Umumnya jika pengguna menerima izin lokasi, Akurasi informasi yang diterima adalah **sekitar 30 meter**, Akurasi Tergantung pada Perangkat.

**Catatan** : Di iPhone karena beberapa alasan, akurasi lokasi kira-kira 65 meter.

## Templates

Anda dapat memilih template yang akan digunakan oleh pencari dari ini:

* NearYou
* Google Drive (Suggested by @Akaal_no_one)
* WhatsApp (Suggested by @Dazmed707)
* Telegram

## Tested On :

* Kali Linux
* BlackArch Linux
* Ubuntu
* Kali Nethunter
* Termux
* Parrot OS

## Installation

### Kali Linux / Ubuntu / Parrot OS

```bash
git clone https://github.com/Anxsec-Syndicate/anontrack.git
cd anontrack/
chmod 777 install.sh
./install.sh
```

### BlackArch Linux

```bash
pacman -S anontrack
```

### Docker

```bash
docker pull Anxsec-Syndicate/anontrack
```

### Termux

```bash
git clone https://github.com/Anxsec-Syndicate/anontrack.git
cd anontrack/
chmod 777 termux_install.sh
./termux_install.sh
```

## Usage

```bash
python3 anontrack.py -h

usage: anontrack.py [-h] [-s SUBDOMAIN]

optional arguments:
  -h, --help                              show this help message and exit
  -s SUBDOMAIN, --subdomain Subdomain 	  Provide Subdomain for Serveo URL ( Optional )
  -k KML, --kml KML                       Provide KML Filename ( Optional )
  -t TUNNEL, --tunnel TUNNEL              Specify Tunnel Mode [manual]

# Example

# SERVEO 
########
python3 anontrack.py

# NGROK ETC.
############

# Di Terminal Pertama, Mulai pencari dalam mode Manual seperti ini
python3 anontrack.py -t manual

# Di Terminal Kedua Mulai Ngrok atau layanan terowongan lainnya di port 8080
./ngrok http 8080

#-----------------------------------#

# Subdomain
########### 
python3 anontrack.py --subdomain google
python3 anontrack.py --tunnel manual --subdomain zomato

#-----------------------------------#

# Docker Usage
##############

# SERVEO
########
docker run -t --rm Anxsec-Syndicate/anontrack

# NGROK
#######

# Step 1
docker membuat jaringan ngroknet

# Step 2
docker run --rm -t --net ngroknet --name anontrack Anxsec-Syndicate/anontrack python3 anontrack.py -t manual

# Step 3
docker run --rm -t --net ngroknet --name ngrok wernight/ngrok ngrok http anontrack:8080
```

## Mengetahui Masalah

* Layanan seperti Serveo dan Ngrok dilarang di beberapa negara seperti Rusia dll.,jadi jika itu dilarang di negara Anda, Anda mungkin tidak mendapatkan URL, jika tidak maka pertama BACA MASALAH TERTUTUP, jika masalah Anda tidak terdaftar, buat masalah baru.

## Demo

| Demo | Link |
|-|-|
| WhatsApp Template Demo | https://www.youtube.com/watch?v=dG0HkQmF4-A |
| What's new in v1.1.9 | https://www.youtube.com/watch?v=FEyAPjkJFrk |
| First Version | https://www.youtube.com/watch?v=ggUGPq4cjSM |

