# Sumber dataset JudiScope

| Informasi | Catatan |
| --- | --- |
| Halaman sumber | [Judi Online — Kaggle](https://www.kaggle.com/datasets/yaemico/judionline) |
| Identifier Kaggle | `yaemico/judionline` |
| Akun pada URL | `yaemico`; bukan konfirmasi nama lengkap pembuat atau pengumpul asli |
| Asal informasi | URL disampaikan langsung oleh anggota kelompok |
| Tanggal pencatatan sumber | 19 Oktober 2026; bukan tanggal unduh atau tanggal publikasi dataset |
| File lokal | `data_komentar_dengan_prediksi - data_komentar_dengan_prediksi(2).csv` |
| SHA-256 file lokal | `6a31d1718093e45ad46b8083e94f64cc11f101dbe689b4428c0f5330bd0228e8` |

Judul dan keberadaan URL halaman sudah diperiksa. Deskripsi lengkap, lisensi, versi rilis, tanggal pengumpulan, metode anotasi, dan definisi label dari pembuat belum berhasil diverifikasi. Jangan menambahkan klaim tentang hal tersebut sebelum memperoleh dokumentasinya. Salinan lokal belum dibandingkan byte per byte dengan unduhan Kaggle saat ini.

## Salinan yang digunakan dalam penelitian

Audit file lokal menemukan 10.230 record komentar, dengan 6.021 label `0` dan 4.209 label `1`, berasal dari 32 video dan 18 channel. Pemetaan kerja adalah `0 = nonjudi` dan `1 = promosi judi`, berdasarkan contoh isi, sambil menunggu konfirmasi dokumentasi sumber.

Kelompok mempertahankan file mentah dan membuat hasil turunan terpisah:

- `outputs/cleaning/komentar_cleaned.csv`: 8.934 komentar asli setelah cleaning, penanganan konflik label, dan deduplikasi.
- `outputs/augmentation/komentar_synthetic_only.csv`: 1.066 komentar sintetis yang dibuat kelompok lewat generator.
- `outputs/augmentation/komentar_10000_with_synthetic.csv`: gabungan 8.934 komentar asli bersih dan 1.066 sintetis.

Angka file turunan dihitung dari eksekusi lokal. Komentar sintetis bukan bagian yang diunduh dari Kaggle dan tidak boleh diatribusikan kepada pengunggah dataset.

## Penulisan sumber pada paper

Contoh kalimat metode:

> Dataset awal diperoleh dari platform Kaggle melalui halaman “Judi Online” dengan identifier yaemico/judionline. Salinan lokal yang digunakan memuat 10.230 record komentar. Peneliti melakukan eksplorasi, preprocessing, pemisahan record berlabel bertentangan, dan deduplikasi sehingga diperoleh 8.934 komentar asli unik. Sebanyak 1.066 komentar sintetis dibuat secara terpisah untuk skenario augmentasi pada data latihan.

Cantumkan URL dataset pada daftar pustaka sesuai format jurnal. Lengkapi nama pembuat, versi, tahun, lisensi, DOI bila ada, serta tanggal akses/unduh yang sebenarnya setelah diverifikasi. Jangan mengisi tahun publikasi dengan tahun eksperimen atau menganggap tanggal pencatatan di atas sebagai tanggal unduh.

Untuk eksperimen ANN, SVM, dan Bayesian, ikuti [panduan dataset tim](../PANDUAN_DATASET_TIM.md) dan manifest pembagian yang sudah tersedia.
