# mapping_project

Tugas 1: Geocoding (Alamat dari Koordinat)
Saat ini kita hanya menampilkan Lat/Lng. Buatlah agar aplikasi menampilkan alamat
(nama jalan, kota, dll) dari koordinat yang didapat.
Petunjuk:
1. Anda sudah menambahkan paket geocoding di pubspec.yaml.
<img width="909" height="456" alt="image" src="https://github.com/user-attachments/assets/7f671a14-2ba2-4f17-9da8-0d3cfdeeb4e2" />

2. Import paketnya: import ’package:geocoding/geocoding.dart’;
<img width="945" height="190" alt="image" src="https://github.com/user-attachments/assets/8fc53435-2707-48ad-96d0-9c1981e37155" />

3.  Buat variabel String? currentAddress; di MyHomePageState.
variabel ini digunakan untuk menyimpan hasil convert koordinat menjadi alamat lengkap, supaya setiap kali aplikasi mendapatkan lokasi terbaru, alamat tersebut bisa langsung ditampilkan ke pengguna sebagai informasi yang lebih mudah dipahami
   <img width="668" height="121" alt="image" src="https://github.com/user-attachments/assets/e5429906-3e40-4110-8e05-f9e2647ff8d6" />

4. Buat fungsi baru getAddressFromLatLng(Position position).
  mengambil koordinat latitude dan longitude, lalu mengubahnya menjadi alamat lengkap dan menyimpannya ke variabel, untuk menampilka di aplikasi
<img width="790" height="351" alt="image" src="https://github.com/user-attachments/assets/1a4e0de9-009f-480e-b53e-d5f53fe92887" />

5.  Panggil fungsi getAddressFromLatLng( currentPosition!) di dalam getLocation dan startTracking (di dalam .listen()) setelah setState untuk currentPosition.
Pemanggilan fungsi getAddressFromLatLng terdapat setelah setState di getLocation dan di dalam .listen() milik startTracking, yang berfungsi untuk mengubah koordinat terbaru menjadi alamat dan langsung menampilkannya
   * Pemanggilan di getLocation
<img width="576" height="103" alt="image" src="https://github.com/user-attachments/assets/49559665-3307-4dd5-99c1-273b8e238fe1" />

  * Pemanggilan di startTracking
<img width="683" height="174" alt="image" src="https://github.com/user-attachments/assets/58313e32-7c5f-481c-9344-1c1b1d0f3475" />

6. Tampilkan currentAddress di UI Anda, di bawah Lat/Lng.
berfungsi untuk menampilkan isi variabel _currentAddress tepat di bawah teks Lat/Lng, sehingga setiap kali alamat berhasil didapat dari koordinat, aplikasi langsung menampilkan alamat lengkap kepada pengguna sebagai informasi tambahan setelah koordinat ditampilkan.
<img width="652" height="341" alt="image" src="https://github.com/user-attachments/assets/276a4496-95a0-4dd3-90e0-ba95cf9f7490" />

HASIL
![WhatsApp Image 2025-11-10 at 17 49 07_877370b4](https://github.com/user-attachments/assets/98d4344d-f57d-40c8-955d-b3867df2f875)


# TUGAS 2
*Tugas 2*: Jarak Real-time ke Titik Tetap
Manfaatkan fungsi Geolocator.distanceBetween dari Langkah 4.
1. Buat variabel String? distanceToPNB; di MyHomePageState.
untuk menyimpan hasil perhitungan jarak antara dua titik koordinat, Lokasi pengguna (latitude & longitude yang didapat dari GPS), Lokasi tujuannya
<img width="1366" height="241" alt="image" src="https://github.com/user-attachments/assets/95c65df7-4df0-4ba1-ac67-26c1458b6bf8" />

2. Di dalam startTracking (di dalam .listen()), panggil fungsi untuk menghitung jarak:
Menghitung jarak antara lokasi pengguna dan tujuan yang berfungsi memantau perubahan lokasi pengguna secara real-time
<img width="802" height="134" alt="image" src="https://github.com/user-attachments/assets/72f3bf21-1b63-4233-969c-62834c43e49f" />

3. Simpan hasilnya di distanceToPNB menggunakan setState
Setelah jarak dihitung, nilainya disimpan ke variabel _distanceToPNB, setelah itu memperbarui UI, sehingga setiap kali lokasi pengguna berubah, tampilan aplikasi ikut berubah secara otomatis
<img width="851" height="143" alt="image" src="https://github.com/user-attachments/assets/bf1c4bf1-e813-4bb5-802c-4dfedcab4395" />

4. Tampilkan distanceToPNB di UI agar jaraknya ter-update secara real-time saat Anda bergerak
<img width="965" height="305" alt="image" src="https://github.com/user-attachments/assets/e62948a8-fa4f-4312-9085-ab9db2c60622" />

*Hasil sebelum dikasih jarak
![WhatsApp Image 2025-11-11 at 18 44 10_0acca244](https://github.com/user-attachments/assets/b95bcf29-b251-4c4e-8120-8816fbadd434)

*Hasil
![WhatsApp Image 2025-11-11 at 18 21 55_b9ec0639](https://github.com/user-attachments/assets/71eaa991-275b-44d6-95e3-bb39ba7b5556)



   
