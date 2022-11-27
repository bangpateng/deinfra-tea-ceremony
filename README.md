# Tutorial Runnig Deinfra Tea Ceremony

<p style="font-size:14px" align="right">
<a href="https://t.me/bangpateng_group" target="_blank">Join Telegram Bang Pateng<img src="https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png" width="30"/></a>
</p>

<p align="center">
  <img height="100" width="250" src="https://user-images.githubusercontent.com/38981255/204129082-37e5e673-ff9d-485f-958a-602755cf9d1a.JPG">
</p>

## Referensi

[Dokumen resmi](https://doc.thepower.io/docs/Community/phase-1/testnet-flow/#step-3-install-erlang)

[Telegram Group](https://t.me/thepower_chat)

[Details Event](https://medium.com/the-power-official-blog/deinfra-testnet-purpose-phases-participant-requirements-b06df0a14210)

## Persyaratan hardware & software

### Persyaratan software/OS

| Komponen | Spesifikasi minimal |
|----------|---------------------|
|Sistem Operasi|Ubuntu 22.04|

### 🚨 PENTING : Hanya Kalian Yang Bisa Ikut, Yang Sudah Masuk Whitelist dan Mendapatkan Token Code di Bot Telegramnya | TUTORIAL INI WAJIB DI JALANKAN DI UBUNTU 22.04

## 1 . Instal Package

```
sudo apt update
sudo apt upgrade
sudo apt install git
sudo apt install screen
```

## 2 . Open Port

```
ufw allow 22 && ufw allow 1080 && ufw allow 1443 && ufw allow 1800
ufw enable
```

## 3 . Instal Erlang 24.3

```
apt install cmake clang gcc git curl libssl-dev build-essential automake autoconf libncurses5-dev elixir erlang
```
```
apt -y install erlang-base erlang-public-key erlang-ssl
```

## 4 . Install Tea Ceremony client and token

```
wget https://tea.thepower.io/teaclient
```
```
chmod +x teaclient
```

## 5 . Start the Tea Ceremony client

```
screen -R tea
./teaclient -n nickname aaaaa.bbbbb
```

| Variable | Ganti Dengan |
|----------|---------------------|
|Nickname|Nama Node Atau Nama Anda Bebas|
|aaaaa|Token Code Ada Nanti di Share dev di Group Telegram nya|
|bbbbb|Token Code Yang Kalian Dapet di Bot Telegram|

1. `CTRL` + `A` + `D` (Lalu Untuk Berjalan di Background)
2. Jika Anda Ingin Kembali ke Screen Yang Sudah Jalan Sebelumnya Buka di Tab Lain Jalankan `screen -Rd tea`

#### 🚨 PENTING : 

1. Setelah Anda memulai klien, tunggu peserta lain. Tolong, JANGAN matikan klien Upacara Minum Teh selama 24 jam. (Karena Kita Menggunakan Screen jadi Bisa di Close Aja VPS Gak Ngapa)

WAITING LANJUTAN TUTOR
