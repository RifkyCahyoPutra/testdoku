# Deployment Project Laravel Filament dengan Ngrok

Panduan ini menjelaskan langkah-langkah melakukan deployment project **Laravel Filament** menggunakan **Ngrok** agar dapat diakses secara online dari perangkat lain.

---

## 📦 Persiapan: Download & Daftar Ngrok

1. **Daftar Akun:**  
   Buka [dashboard.ngrok.com](https://dashboard.ngrok.com/signup) dan daftar (Gratis).

2. **Download:**  
   Download aplikasi Ngrok sesuai sistem operasi (Windows/Mac/Linux).

3. **Extract:**  
   File yang didownload biasanya berupa `.zip`. Extract file tersebut, kamu akan dapat satu file bernama `ngrok.exe`.

4. **Connect Akun:**  
   - Di dashboard Ngrok website, cari menu **"Your Authtoken"**.  
   - Copy kode tokennya.  
   - Buka terminal (CMD/PowerShell) di folder tempat `ngrok.exe` berada, lalu ketik:

   ```bash
   ngrok config add-authtoken KODE_TOKEN_KAMU_DISINI



## Langkah 1: Jalankan Project Laravel (Localhost)
**Buka terminal di dalam folder project Laravel kamu (Visual Studio Code terminal juga bisa), lalu jalankan server lokal:**
 ```bash
php artisan serve
```
**Biasanya akan berjalan di http://127.0.0.1:8000.**


## Langkah 2: Jalankan Ngrok (Tunneling)
**Buka terminal baru (biarkan php artisan serve tetap berjalan). Arahkan ke folder tempat ngrok.exe tadi, lalu ketik:**
```bash
ngrok http 8000
```
**Penjelasan: Perintah ini membuat "terowongan" internet menuju port 8000 di laptopmu.**

**Jika berhasil, layar terminal akan menampilkan status hijau Online dan ada tulisan Forwarding, contohnya:**
```bash
https://a1b2-103-xx-xx-xx.ngrok-free.app -> http://localhost:8000
```

## Langkah 3: Konfigurasi Laravel (PENTING UNTUK FILAMENT)
**Filament dan Livewire sensitif terhadap URL. Jika kamu langsung membuka link Ngrok, kemungkinan besar tampilannya akan berantakan (CSS hilang) atau tombol tidak berfungsi.**

**Untuk mengatasinya:**
1.  Buka file .env.
2.  Cari bagian APP_URL.
3.  Ubah APP_URL menjadi link Ngrok yang kamu dapat tadi:
 ```bash
https://a1b2-103-xx-xx-xx.ngrok-free.app -> http://localhost:8000
```
4.  Restart Server Laravel :
   - Ke terminal php artisan serve, tekan Ctrl + C untuk stop.
   - Jalankan kembali dengan php artisan serve.
   - (Opsional) Jalankan php artisan optimize:clear untuk membersihkan cache.


## Langkah 4: Testing & Share
1.  Buka browser, masukkan link Ngrok tadi, misalnya:
https://a1b2-103-xx-xx-xx.ngrok-free.app/admin
2.  Login seperti biasa.
3.  Uji fitur CRUD dan fitur Log Activity yang sudah kamu buat.
4.  Bagikan link tersebut ke team. Mereka bisa mengakses web yang ada di laptopmu dari laptop/HP mereka sendiri!
