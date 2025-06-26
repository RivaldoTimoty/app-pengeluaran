Deploy Aplikasi dengan Streamlit
-----

### Langkah 1: Pastikan Kode Aplikasi Anda Siap

1.  **File Aplikasi (`.py`):** Pastikan kode aplikasi Streamlit Anda (misalnya, `app.py`) sudah final dan berfungsi dengan baik saat Anda menjalankannya secara lokal (`streamlit run app.py`).
2.  **File Dependensi (`requirements.txt`):** Buat file bernama `requirements.txt` di folder yang sama dengan file `.py` aplikasi Anda. Cantumkan semua *library* Python yang digunakan dalam aplikasi Anda di file ini. Ini sangat penting agar platform hosting dapat menginstal semua yang dibutuhkan aplikasi Anda untuk berjalan.
      * **Contoh isi `requirements.txt`:**
        ```
        streamlit
        pandas
        plotly_express
        ```
      * *(Jika Anda menggunakan versi spesifik, cantumkan juga, misal: `streamlit==1.23.0`)*

-----

### Langkah 2: Unggah Kode Anda ke GitHub

1.  **Buat Akun GitHub:** Jika belum punya, daftar di [github.com](https://github.com/).
2.  **Buat Repositori Baru:** Buat repositori **publik** baru di GitHub (misalnya, `personal-expense-dashboard-app`).
3.  **Unggah File:** Unggah kedua file (`.py` aplikasi Anda dan `requirements.txt`) ke repositori GitHub yang baru Anda buat. Pastikan keduanya ada di *root* repositori atau dalam sub-folder yang akan Anda tentukan nanti.

-----

### Langkah 3: Deploy Aplikasi Anda ke Streamlit Community Cloud

Streamlit Community Cloud adalah cara termudah dan tercepat untuk membuat aplikasi Streamlit Anda *online* dan bisa digunakan oleh siapa pun.

1.  **Kunjungi Streamlit Community Cloud:** Buka [share.streamlit.io](https://share.streamlit.io/) di browser Anda.
2.  **Masuk dengan GitHub:** Klik "Sign up with GitHub" dan berikan otorisasi jika diminta. Ini akan menghubungkan akun GitHub Anda dengan Streamlit.
3.  **Deploy Aplikasi Baru:**
      * Di *dashboard* Streamlit Anda, klik tombol **"New app"** (biasanya di pojok kanan atas).
      * Sebuah formulir akan muncul. Isi detailnya:
          * **Repository:** Pilih repositori GitHub Anda yang berisi kode aplikasi dari *dropdown* (misalnya, `personal-expense-dashboard-app`).
          * **Branch:** Pilih *branch* yang berisi kode aplikasi Anda (umumnya `main` atau `master`).
          * **Main file path:** Masukkan jalur ke file aplikasi Streamlit utama Anda di dalam repositori (misalnya, `app.py`).
          * Anda bisa membiarkan opsi lainnya pada pengaturan *default* untuk memulai.
4.  **Mulai Deployment:** Klik tombol **"Deploy\!"**.
      * Streamlit akan mulai menginstal dependensi dari `requirements.txt` dan menjalankan aplikasi Anda. Proses ini mungkin memakan waktu beberapa menit.
      * Anda akan melihat log proses *deployment* secara *real-time*.
5.  **Aplikasi Siap Digunakan:** Setelah *deployment* selesai, aplikasi Anda akan otomatis terbuka di *browser* Anda dan Streamlit akan memberikan **URL publik** untuk aplikasi tersebut (contoh: `https://your-github-username.streamlit.app/your-app-name`).

Dengan URL ini, siapa pun yang memiliki tautan tersebut dapat mengakses dan menggunakan aplikasi dashboard pengeluaran pribadi Anda melalui *web browser*, tanpa perlu menginstal Python atau Streamlit di perangkat mereka.
