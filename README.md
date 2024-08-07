# Cara buat repository github menggunakan git remote di linux mint, ubuntu, debian

## 1. Install git
```
sudo apt install git
```

## 2. Buatlah SSH Key Pair baru
```
ssh-keygen -t rsa -b 4096 -C "your_email"
```

Ini akan menghasilkan dua berkas baru dan berada di dalam folder .ssh:

- id_rsa: Kunci privat Anda (jaga agar tetap aman! Jangan pernah membagikan berkas ini dengan siapa pun)
- id_rsa.pub: Kunci publik Anda (Anda harus menyalinnya)

## 3. Tambahkan Public Key baru ke Github
## 1. Buka konten file id_rsa.pub
pastikan ada folder `.ssh`
```
ls -a
```
arahkan terminal ke folder `.ssh`
```
cd .ssh
```
buka konten dari file `id_rsa.pub`
```
cat id_rsa.pub
```
![gambar isi dari file id_rsa.pub](img/rsa.png)
salin teks tersebut
### 2. Buka pengaturan GitHub Anda dan arahkan ke bagian "Kunci SSH dan GPG".
### 3. Klik "Kunci SSH baru" dan tempelkan konten file id_rsa.pub Anda ke dalam bidang kunci.
### 4. Berikan judul deskriptif pada kunci Anda (misalnya, "New Private Key").
### 5. Klik "Tambahkan kunci SSH".

## 4. Buat repository Github