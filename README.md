# 📊 Analisis Data Coffee Shop

Proyek ini berisi analisis data dari sebuah dataset Coffee Shop menggunakan Python dan *library* populer seperti Pandas, Seaborn, dan Matplotlib. Analisis ini bertujuan untuk mengekstrak wawasan mengenai preferensi pelanggan dan pola operasional outlet.

---

## ☕ Deskripsi Dataset

Dataset yang digunakan adalah `CoffeeShop_Dataset.db`, sebuah database SQLite yang mencakup beberapa tabel, antara lain:

* `sales outlet`: Informasi mengenai outlet penjualan.
* `pastry inventory`: Data inventaris pastry.
* `product`: Detail produk yang dijual.
* `generations`: Pemetaan tahun lahir ke generasi.
* `sales reciepts`: Catatan detail transaksi penjualan.
* `customer`: Informasi mengenai pelanggan.

Data ini dibaca dan dimanipulasi menggunakan Pandas setelah terhubung ke database SQLite.

---

## 📈 Tujuan Analisis

Analisis dilakukan untuk menjawab pertanyaan-pertanyaan berikut:

1.  **Identifikasi 3 outlet *pilihan utama (home store)* teratas** berdasarkan jumlah pelanggan unik dan analisis distribusi generasi pelanggan di outlet-outlet tersebut (misalnya, berapa banyak Baby Boomers, Gen Z, dll.).
2.  **Identifikasi jam kunjungan paling ramai** (berdasarkan jumlah transaksi) untuk 3 outlet *pilihan utama* teratas tersebut.

---

## 💡 Temuan Utama

### 1. Outlet Teratas & Profil Generasi Pelanggan 👥

* **Tiga outlet pilihan utama teratas** berdasarkan jumlah pelanggan unik yang menjadikannya *home store* adalah:
    1.  Outlet ID **5** (945 pelanggan)
    2.  Outlet ID **3** (800 pelanggan)
    3.  Outlet ID **8** (501 pelanggan)
* **Profil Generasi Pelanggan di Outlet Teratas:**
    * **Outlet 5:** Didominasi oleh **Millennials** (451 orang), diikuti oleh Generation X (200) dan Baby Boomers (172).
    * **Outlet 3:** Distribusi cukup merata antara **Generation X** (252), **Millennials** (250), dan Baby Boomers (229).
    * **Outlet 8:** Didominasi oleh **Millennials** (189), diikuti oleh Baby Boomers (128) dan Generation X (119).
    * Secara keseluruhan (di 3 outlet ini), **Millennials** merupakan kelompok pelanggan terbesar.

* *Visualisasi:* Distribusi generasi di 3 outlet teratas divisualisasikan menggunakan *countplot* dari Seaborn.

<img width="984" height="584" alt="image" src="https://github.com/user-attachments/assets/de81505c-a4d3-4c62-8ecb-2bf15aa71c6d" />


### 2. Jam Sibuk Outlet Teratas 🕒

* **Jam Kunjungan Paling Ramai** (berdasarkan jumlah transaksi) untuk masing-masing outlet teratas adalah:
    * **Outlet 5:** Jam **10 pagi** (dengan 2053 transaksi pada jam tersebut dari total 15994 transaksi).
    * **Outlet 3:** Jam **10 pagi** (dengan 1711 transaksi pada jam tersebut dari total 16829 transaksi).
    * **Outlet 8:** Jam **8 pagi** (dengan 2318 transaksi pada jam tersebut dari total 17071 transaksi).

* *Visualisasi:* Metrik kunci (Jam Teramai, Jumlah Kunjungan di Jam Teramai, Total Kunjungan) untuk 3 outlet teratas divisualisasikan menggunakan *barplot* dari Seaborn dalam subplot.

<img width="1384" height="984" alt="image" src="https://github.com/user-attachments/assets/f6c56643-5338-4bbd-a8e6-2b1639747bfc" />

---

## Library:

* `sqlite3`: Untuk koneksi ke database SQLite.
* `pandas`: Untuk manipulasi dan analisis data.
* `seaborn` & `matplotlib`: Untuk visualisasi data.
* `numpy`: Untuk operasi numerik (meskipun tidak secara eksplisit dominan dalam analisis ini).
* `os`: (Diimpor tapi tidak digunakan secara signifikan dalam analisis utama).

---

