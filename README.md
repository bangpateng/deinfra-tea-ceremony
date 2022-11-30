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
|Sistem Operasi|Ubuntu 20.04 / 22.04|

### 🚨 PENTING : Hanya Kalian Yang Bisa Ikut, Yang Sudah Masuk Whitelist dan Mendapatkan Token Code di Bot Telegramnya

## 1 . Instal Package

```
sudo apt update
sudo apt upgrade
sudo apt install git
```

## 2 . Open Port

```
ufw allow 22 && ufw allow 1080 && ufw allow 1443 && ufw allow 1800
ufw enable
```

## 3 . Instal Erlang 24.3

#### 🟢(JIKA PAKAI UBUNTU 22.04)

```
apt install cmake clang gcc git curl libssl-dev build-essential automake autoconf libncurses5-dev elixir erlang
```
```
apt -y install erlang-base erlang-public-key erlang-ssl
```

#### 🟢(JIKA PAKAI UBUNTU 20.04)

```
sudo apt update
sudo apt install curl wget gnupg apt-transport-https -y
```
```
curl -fsSL https://packages.erlang-solutions.com/ubuntu/erlang_solutions.asc | sudo gpg --dearmor -o /usr/share/keyrings/erlang.gpg
```

```
echo "deb [signed-by=/usr/share/keyrings/erlang.gpg] https://packages.erlang-solutions.com/ubuntu $(lsb_release -cs) contrib" | sudo tee /etc/apt/sources.list.d/erlang.list
```

```
sudo apt update
sudo apt install erlang
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
./teaclient -n nickname aaaaa.bbbbb
```

| Variable | Ganti Dengan |
|----------|---------------------|
|Nickname|Nama Node Atau Nama Anda Bebas|
|aaaaa|Token Code Ada Nanti di Share dev di Group Telegram nya Setiap Jam 4 Sore dan Jam 8 Malem FCFS|
|bbbbb|Token Code Yang Kalian Dapet di Bot Telegram|

## 6. Siapkan dan Install SSL
```
apt-get install socat
curl https://get.acme.sh | sh -s email=youractiveemail
source ~/.bashrc
```

| `youractiveemail` |
|----------|
|Isi Email Anda|

Lalu Close VPS Kalian dan Buka Lagi Jalankan Perintah di Bawah

```
acme.sh --server letsencrypt --issue --standalone  -d your_node.example.com
acme.sh --install-cert -d your_node.example.com \
--cert-file /opt/thepower/db/cert/your_node.example.com.crt \
--key-file /opt/thepower/db/cert/your_node.example.com.key \
--ca-file /opt/thepower/db/cert/your_node.example.com.crt.ca.crt
acme.sh --info -d your_node.example.com
```

| `your_node.example.com` |
|----------|
|Ganti Dengan Nama Host Anda Yang ada di dalam File `node.config`|

Penting : Jika di Dalam File `node.config` Kalian Hanya Terdapat Private Key Saja, Anda Bisa Menjalankan Ulang `./teaclient -n nickname aaaaa.bbbbb`

Jika Kalian Mendapatkan output Sprti di Bawah Ini Jalankan `source ~/.bashrc` Lalu Ulangi Lagi Command di Atas

```
acme.sh: command not found
acme.sh: command not found
acme.sh: command not found
```



