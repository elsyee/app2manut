# Project Kolaborasi Android

Ini adalah proyek sederhana untuk belajar kolaborasi menggunakan Git& Android Studio

👥 Tim
- Siswa 1 : Elsye Sukma Argita (Inisialisasi & Merge PR)
- Siswa 2 : Arrumi Asna Salsabilla & Hafidhah Nurina Amajida (Fitur TextView)
- Siswa 3 : Aditya Rasya Dafa Putra (Fitur Button)

📱 Fitur

- Menampilkan TextView
- Menampilkan Button yang dapat diklik

🔧 Teknologi
- Kotlin
- Android Studio
- Git + GitHub

💻 Penjelasan code penting

activity_main.xml

1. Header Layout XML di Android
  - <androidx.constraintlayout.widget.ConstraintLayout ...> --> Ini adalah layout utama. Jenisnya ConstraintLayout yang fleksibel untuk atur posisi elemen pakai “ngait-ngaitin”.
  - xmlns:android="http://schemas.android.com/apk/res/android" --> Biar bisa pakai atribut android: di dalam layout.
  - xmlns:app="http://schemas.android.com/apk/res-auto" --> Supaya atribut app: bisa dipakai, contohnya buat constraint.
  - xmlns:tools="http://schemas.android.com/tools" --> Supaya bisa pakai tools: untuk preview di Android Studio.
  - android:id="@+id/main" --> Ngasih ID ke layout ini, namanya main. Bisa dipanggil di kode Kotlin/Java.
  - android:layout_width="match_parent" --> Lebarnya mengikuti layar penuh (dari parent).
  - android:layout_height="match_parent" --> Tingginya juga penuh, ngikutin tinggi layar.
  - android:background="#F5F5F5" --> Warna background-nya abu muda (#F5F5F5).
  - tools:context=".MainActivity"  --> Menandakan layout ini dipakai di file MainActivity.kt, buat preview di Android Studio.

2. LinearLayout
  - android:id="@+id/contentLayout" --> Ngasih ID ke LinearLayout biar bisa dipanggil di kode Kotlin/Java.
  - android:layout_width="0dp" --> Lebarnya diatur lewat Constraint (karena ini di dalam ConstraintLayout).
  - android:layout_height="wrap_content" --> Tingginya ngikutin isi di dalamnya.
  - android:orientation="vertical" --> Elemen di dalam layout ini bakal ditumpuk dari atas ke bawah.
  - android:padding="24dp" --> Ngasih jarak ke dalam (padding) biar isi layout gak mepet pinggir.
  - android:background="@android:color/white" --> Latar belakangnya warna putih.
  - android:elevation="4dp" --> Bikin layout ini agak "naik" dikit, ada bayangan, kayak mengambang.
  - app:layout_constraintTop_toTopOf="parent" --> Atas layout ini nempel ke atas layout utama (parent).
  - app:layout_constraintStart_toStartOf="parent" --> Sisi kiri layout nempel ke sisi kiri parent.
  - app:layout_constraintEnd_toEndOf="parent" --> Sisi kanan layout nempel ke sisi kanan parent.
  - app:layout_constraintBottom_toBottomOf="parent" --> Bawah layout nempel ke bawah parent.

3. TextView
  - android:id="@+id/tvTitle" --> Ngasih ID tvTitle buat TextView ini, supaya bisa dipanggil di kode Java/Kotlin.
  - android:layout_width="match_parent" --> Lebar TextView ngikutin lebar parent-nya.
  - android:layout_height="wrap_content" --> Tingginya ngikutin isi teks (gak dipaksa tetap).
  - android:text="Form Biodata Siswa" --> Isi teks yang ditampilin adalah "Form Biodata Siswa".
  - android:textAlignment="center" --> Teksnya ditengahin secara horizontal.
  - android:textSize="20sp" --> Ukuran teksnya cukup besar (20sp).
  - android:textStyle="bold" --> Teksnya ditebelin (bold).
  - android:textColor="#333" --> Warna teksnya abu-abu gelap (kode warna #333).
  - android:layout_marginBottom="16dp" --> Dikasih jarak ke bawah sejauh 16dp dari elemen berikutnya.

4. EditText
  - android:id="@+id/etNama" --> Ngasih ID etNama supaya bisa dipanggil dari Kotlin/Java.
  - android:layout_width="match_parent" --> Lebar EditText ngikutin lebar parent (full satu baris).
  - android:layout_height="48dp" --> Tinggi kotaknya tetap, yaitu 48dp.
  - android:hint="Masukkan Nama" --> Teks petunjuk (placeholder) yang muncul kalau belum diisi.
  - android:inputType="textPersonName" --> Input-nya khusus buat nama orang (huruf kapital di awal otomatis).
  - android:layout_marginBottom="12dp" --> Dikasih jarak 12dp ke bawah, biar gak dempet komponen lain.
  - android:backgroundTint="#6200EE" --> Warna garis bawah/input-nya ungu (#6200EE), biasanya warna utama aplikasi.

5. EditText
  - android:id="@+id/etKelas" --> ID dari EditText ini yaitu etKelas, biar bisa dipanggil di kode.
  - android:layout_width="match_parent" --> Lebarnya full satu baris (ngikutin lebar parent-nya).
  - android:layout_height="48dp" --> Tingginya tetap, biar kelihatan rapi.
  - android:hint="Masukkan Kelas" --> Teks petunjuk (placeholder) buat kasih tau user isi apa.
  - android:inputType="text" --> Tipe input-nya teks biasa (misal: X RPL 1, XII TKJ, dll).
  - android:layout_marginBottom="20dp" --> Dikasih jarak ke bawah 20dp, biar gak dempet sama elemen di bawahnya.
  - android:backgroundTint="#6200EE" --> Warna garis bawah input-nya ungu (#6200EE).

6. Button
  - android:id="@+id/btnTampilkan"	ID tombol ini adalah btnTampilkan, bisa dipanggil di Kotlin/Java.
  - android:layout_width="wrap_content"	Lebar tombol ngikutin panjang teks di dalamnya.
  - android:layout_height="wrap_content"	Tingginya juga ngikutin isi.
  - android:text="Tampilkan"	Teks yang ditampilin di tombol adalah "Tampilkan".
  - android:textAllCaps="false"	Teks ditulis sesuai penulisan, gak diubah jadi HURUF BESAR semua.
  - android:backgroundTint="#03DAC5"	Warna latar tombolnya biru kehijauan (turquoise).
  - android:layout_gravity="center"	Ini buat ngatur posisi tombol di tengah, tapi hanya berfungsi di dalam LinearLayout.
  - android:layout_marginBottom="24dp"	Dikasih jarak 24dp ke bawah dari tombol (kalau ada elemen di bawahnya).

7. TextView
  - android:id="@+id/tvHasil" --> ID-nya tvHasil, nanti bisa dipakai buat nampilin hasil input dari user (diubah lewat kode).
  - android:layout_width="match_parent" --> Lebarnya full satu baris, ngikutin lebar parent-nya.
  - android:layout_height="wrap_content" --> Tingginya menyesuaikan isi teks (kalau kosong, ya kecil).
  - android:text="" --> Awalnya teks kosong. Nanti akan diisi lewat program (misal: nama & kelas).
  - android:textSize="16sp" --> Ukuran teksnya sedang, biar enak dibaca.
  - android:textColor="#333" --> Warna tulisannya abu-abu gelap (kode #333).
  - android:padding="12dp" --> Dikasih jarak ke dalam biar teksnya gak mepet ke pinggir.
  - android:background="#E0E0E0" --> Warna latar belakang abu terang, supaya teksnya kelihatan jelas.

activity_ini_splash.xml

1. Header Layout XML di Android
  - <androidx.constraintlayout.widget.ConstraintLayout --> Jenis layout utama yang dipakai. Layout ini bisa atur posisi elemen dengan sistem “ngait” (constraint).
  - xmlns:android="http://schemas.android.com/apk/res/android" --> Izin buat pakai atribut android: di dalam file XML.
  - xmlns:tools="http://schemas.android.com/tools" --> Izin buat pakai atribut tools: (biasanya buat preview di Android Studio).
  - xmlns:app="http://schemas.android.com/apk/res-auto" --> Izin buat atribut app:, contohnya untuk constraint atau material design.
  - android:id="@+id/main" --> Ngasih ID ke layout utama, yaitu main. Bisa dipanggil lewat kode Kotlin/Java.
  - android:layout_width="match_parent" --> Lebarnya mengikuti ukuran layar penuh (parent).
  - android:layout_height="match_parent" --> Tingginya juga mengikuti layar penuh.
  - tools:context=".iniSplash" --> Untuk preview di Android Studio, menunjukkan layout ini dipakai di file iniSplash.kt.
  - android:background="#FFFFFF" --> Warna background layout-nya putih (#FFFFFF).

2. ImageView
  - android:id="@+id/logoImage"	Ngasih ID ke gambar ini, namanya logoImage. Supaya bisa dipanggil di Kotlin/Java pakai findViewById(R.id.logoImage).
  - android:layout_width="200dp"	Lebar gambar ditentukan 200dp (satuan ukuran di Android).
  - android:layout_height="200dp"	Tinggi gambar juga 200dp.
  - android:src="@drawable/logosmk"	Gambar yang ditampilkan berasal dari file logosmk.png atau .jpg yang ada di folder res/drawable.
  - android:contentDescription="Logo SMK"	Deskripsi untuk aksesibilitas. Ini dibaca oleh pembaca layar untuk tunanetra.
  - app:layout_constraintTop_toTopOf="parent"	Posisi atas gambar dikaitkan ke atas parent (layout utama).
  - app:layout_constraintBottom_toBottomOf="parent"	Posisi bawah gambar dikaitkan ke bawah parent (biar di tengah).
  - app:layout_constraintStart_toStartOf="parent"	Sisi kiri gambar dikaitkan ke sisi kiri parent.
  - app:layout_constraintEnd_toEndOf="parent"	Sisi kanan gambar dikaitkan ke sisi kanan parent.
    
📸 Screenshot

Hasil Tampilan

<img width="132" height="240" alt="image" src="https://github.com/user-attachments/assets/f6f4a8b1-5276-4d63-9e50-e3216da89a97" />

<img width="169" height="484" alt="Screenshot 2025-07-30 155649" src="https://github.com/user-attachments/assets/cd0f82d2-5952-44ec-aa2c-7c83e32c5e15" />

activity_main.xml
- Header Layout XML di Android
  
  <img width="644" height="322" alt="Screenshot 2025-07-30 150330" src="https://github.com/user-attachments/assets/9f8ca077-4735-4658-a5cb-a22b3c2bc690" />

- LinierLayout
  
  <img width="644" height="322" alt="Screenshot 2025-07-30 150759" src="https://github.com/user-attachments/assets/c407c9b1-dbb4-4560-ae33-f4e93d5c1118" />

- TextView
  
  <img width="644" height="322" alt="Screenshot 2025-07-30 151434" src="https://github.com/user-attachments/assets/ba9d6678-d78a-458f-b4a7-fa2119f44cbf" />

- EditText
  
  <img width="644" height="322" alt="Screenshot 2025-07-30 151830" src="https://github.com/user-attachments/assets/ca04c128-9353-473d-a83b-b2f288441d36" />

- EditText
  
  <img width="644" height="322" alt="Screenshot 2025-07-30 152111" src="https://github.com/user-attachments/assets/70523a75-e3f7-4833-8f99-9e1c3584e63e" />

- Button
  
  <img width="644" height="322" alt="Screenshot 2025-07-30 152317" src="https://github.com/user-attachments/assets/e38b9078-64f8-4533-9a3a-6cd19ea75ad2" />

- TextView
  
  <img width="644" height="322" alt="Screenshot 2025-07-30 152605" src="https://github.com/user-attachments/assets/9d4fae81-eb02-41a7-a2ed-8b0d4451c85e" />

activity_ini_splash.xml
- Header Layout XML di Android

  <img width="644" height="322" alt="Screenshot 2025-07-30 181903" src="https://github.com/user-attachments/assets/7ca3be20-d9df-4ddb-b6fb-fd20dc4c82bd" />

- ImageView

  <img width="644" height="322" alt="Screenshot 2025-07-30 182110" src="https://github.com/user-attachments/assets/2a5468bc-a477-4f0a-b064-9fc350b25145" />






  

