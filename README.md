# Project Kolaborasi Android

Ini adalah proyek sederhana untuk belajar kolaborasi menggunakan Git& Android Studio

👥 Tim
- Siswa 1 : Elsye Sukma Argita (Inisialisasi & Merge PR)
- Siswa 2 : Arrumi Asna Salsabilla & Hafidhah Nurina Amajida (Fitur TextView)
- Siswa 3 : Aditya Rasya Dafa Putra (Fitur Button)

📱 Fitur

Hasil Tampilan

<img width="169" height="484" alt="Screenshot 2025-07-30 155649" src="https://github.com/user-attachments/assets/cd0f82d2-5952-44ec-aa2c-7c83e32c5e15" />

- Menampilkan TextView
- Menampilkan Button yang dapat diklik

🔧 Teknologi
- Kotlin
- Android Studio
- Git + GitHub

💻 Penjelasan code penting

activity_main.xml
- Header Layout XML di Android
  a. <?xml version="1.0" encoding="utf-8"?> --> Baris pembuka file XML. Wajib ada di paling atas. Menandakan format teks-nya pakai UTF-8.
  b. <androidx.constraintlayout.widget.ConstraintLayout --> Jenis layout utama yang dipakai. Layout ini bisa atur posisi elemen dengan sistem “ngait” (constraint).
  c. xmlns:android="http://schemas.android.com/apk/res/android" --> Izin buat pakai atribut android: di dalam file XML.
  d. xmlns:tools="http://schemas.android.com/tools" --> Izin buat pakai atribut tools: (biasanya buat preview di Android Studio).
  e. xmlns:app="http://schemas.android.com/apk/res-auto" --> Izin buat atribut app:, contohnya untuk constraint atau material design.
  f. android:id="@+id/main" --> Ngasih ID ke layout utama, yaitu main. Bisa dipanggil lewat kode Kotlin/Java.
  g. android:layout_width="match_parent" --> Lebarnya mengikuti ukuran layar penuh (parent).
  h. android:layout_height="match_parent" --> Tingginya juga mengikuti layar penuh.
  i. tools:context=".iniSplash" --> Untuk preview di Android Studio, menunjukkan layout ini dipakai di file iniSplash.kt.
  j. android:background="#FFFFFF" --> Warna background layout-nya putih (#FFFFFF).

- LinearLayout
  a. android:id="@+id/contentLayout" --> Ngasih ID ke LinearLayout biar bisa dipanggil di kode Kotlin/Java.
  b. android:layout_width="0dp" --> Lebarnya diatur lewat Constraint (karena ini di dalam ConstraintLayout).
  c. android:layout_height="wrap_content" --> Tingginya ngikutin isi di dalamnya.
  d. android:orientation="vertical" --> Elemen di dalam layout ini bakal ditumpuk dari atas ke bawah.
  e. android:padding="24dp" --> Ngasih jarak ke dalam (padding) biar isi layout gak mepet pinggir.
  f. android:background="@android:color/white" --> Latar belakangnya warna putih.
  g. android:elevation="4dp" --> Bikin layout ini agak "naik" dikit, ada bayangan, kayak mengambang.
  h. app:layout_constraintTop_toTopOf="parent" --> Atas layout ini nempel ke atas layout utama (parent).
  i. app:layout_constraintStart_toStartOf="parent" --> Sisi kiri layout nempel ke sisi kiri parent.
  j. app:layout_constraintEnd_toEndOf="parent" --> Sisi kanan layout nempel ke sisi kanan parent.
  k. app:layout_constraintBottom_toBottomOf="parent" --> Bawah layout nempel ke bawah parent.

- TextView
  a. android:id="@+id/tvTitle" --> Ngasih ID tvTitle buat TextView ini, supaya bisa dipanggil di kode Java/Kotlin.
  b. android:layout_width="match_parent" --> Lebar TextView ngikutin lebar parent-nya.
  c. android:layout_height="wrap_content" --> Tingginya ngikutin isi teks (gak dipaksa tetap).
  d. android:text="Form Biodata Siswa" --> Isi teks yang ditampilin adalah "Form Biodata Siswa".
  e. android:textAlignment="center" --> Teksnya ditengahin secara horizontal.
  f. android:textSize="20sp" --> Ukuran teksnya cukup besar (20sp).
  g. android:textStyle="bold" --> Teksnya ditebelin (bold).
  h. android:textColor="#333" --> Warna teksnya abu-abu gelap (kode warna #333).
  i. android:layout_marginBottom="16dp" --> Dikasih jarak ke bawah sejauh 16dp dari elemen berikutnya.

- EditText
  a. android:id="@+id/etNama" --> Ngasih ID etNama supaya bisa dipanggil dari Kotlin/Java.
  b. android:layout_width="match_parent" --> Lebar EditText ngikutin lebar parent (full satu baris).
  c. android:layout_height="48dp" --> Tinggi kotaknya tetap, yaitu 48dp.
  d. android:hint="Masukkan Nama" --> Teks petunjuk (placeholder) yang muncul kalau belum diisi.
  e. android:inputType="textPersonName" --> Input-nya khusus buat nama orang (huruf kapital di awal otomatis).
  f. android:layout_marginBottom="12dp" --> Dikasih jarak 12dp ke bawah, biar gak dempet komponen lain.
  g. android:backgroundTint="#6200EE" --> Warna garis bawah/input-nya ungu (#6200EE), biasanya warna utama aplikasi.

- EditText
  a. android:id="@+id/etKelas" --> ID dari EditText ini yaitu etKelas, biar bisa dipanggil di kode.
  b. android:layout_width="match_parent" --> Lebarnya full satu baris (ngikutin lebar parent-nya).
  c. android:layout_height="48dp" --> Tingginya tetap, biar kelihatan rapi.
  d. android:hint="Masukkan Kelas" --> Teks petunjuk (placeholder) buat kasih tau user isi apa.
  e. android:inputType="text" --> Tipe input-nya teks biasa (misal: X RPL 1, XII TKJ, dll).
  f. android:layout_marginBottom="20dp" --> Dikasih jarak ke bawah 20dp, biar gak dempet sama elemen di bawahnya.
  g. android:backgroundTint="#6200EE" --> Warna garis bawah input-nya ungu (#6200EE).

- Button
  a. android:id="@+id/btnTampilkan"	ID tombol ini adalah btnTampilkan, bisa dipanggil di Kotlin/Java.
  b. android:layout_width="wrap_content"	Lebar tombol ngikutin panjang teks di dalamnya.
  c. android:layout_height="wrap_content"	Tingginya juga ngikutin isi.
  d. android:text="Tampilkan"	Teks yang ditampilin di tombol adalah "Tampilkan".
  e. android:textAllCaps="false"	Teks ditulis sesuai penulisan, gak diubah jadi HURUF BESAR semua.
  f. android:backgroundTint="#03DAC5"	Warna latar tombolnya biru kehijauan (turquoise).
  g. android:layout_gravity="center"	Ini buat ngatur posisi tombol di tengah, tapi hanya berfungsi di dalam LinearLayout.
  h. android:layout_marginBottom="24dp"	Dikasih jarak 24dp ke bawah dari tombol (kalau ada elemen di bawahnya).

- TextView
  a. android:id="@+id/tvHasil" --> ID-nya tvHasil, nanti bisa dipakai buat nampilin hasil input dari user (diubah lewat kode).
  b. android:layout_width="match_parent" --> Lebarnya full satu baris, ngikutin lebar parent-nya.
  c. android:layout_height="wrap_content" --> Tingginya menyesuaikan isi teks (kalau kosong, ya kecil).
  d. android:text="" --> Awalnya teks kosong. Nanti akan diisi lewat program (misal: nama & kelas).
  e. android:textSize="16sp" --> Ukuran teksnya sedang, biar enak dibaca.
  f. android:textColor="#333" --> Warna tulisannya abu-abu gelap (kode #333).
  g. android:padding="12dp" --> Dikasih jarak ke dalam biar teksnya gak mepet ke pinggir.
  h. android:background="#E0E0E0" --> Warna latar belakang abu terang, supaya teksnya kelihatan jelas.

📸 Screenshot

- Header Layout XML di Android
  <img width="944" height="324" alt="Screenshot 2025-07-30 150330" src="https://github.com/user-attachments/assets/9f8ca077-4735-4658-a5cb-a22b3c2bc690" />

- LinierLayout
  <img width="944" height="428" alt="Screenshot 2025-07-30 150759" src="https://github.com/user-attachments/assets/c407c9b1-dbb4-4560-ae33-f4e93d5c1118" />

- TextView
  <img width="944" height="393" alt="Screenshot 2025-07-30 151434" src="https://github.com/user-attachments/assets/ba9d6678-d78a-458f-b4a7-fa2119f44cbf" />

- EditText
  <img width="944" height="360" alt="Screenshot 2025-07-30 151830" src="https://github.com/user-attachments/assets/ca04c128-9353-473d-a83b-b2f288441d36" />

- EditText
  <img width="944" height="340" alt="Screenshot 2025-07-30 152111" src="https://github.com/user-attachments/assets/70523a75-e3f7-4833-8f99-9e1c3584e63e" />

- Button
  <img width="944" height="379" alt="Screenshot 2025-07-30 152317" src="https://github.com/user-attachments/assets/e38b9078-64f8-4533-9a3a-6cd19ea75ad2" />

- TextView
  <img width="944" height="422" alt="Screenshot 2025-07-30 152605" src="https://github.com/user-attachments/assets/9d4fae81-eb02-41a7-a2ed-8b0d4451c85e" />



  

