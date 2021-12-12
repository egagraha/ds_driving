# Deployment Model Clustering 

## Deskripsi singkat

Repository ini berisi file yang dibutuhkan untuk melakukan deployment model Driving behaviour Clustering dengan pendekatan K-Means. Adapun model yang digunakan merupakan model untuk mengelompokkan driving-style berdasarkan file input yang berisi data GPS pergerakan kendaraan dengan memperhatikan 
- Speed (kecepatan)
- Acceleration (percepatan)
- Jarak tempuh
- Durasi

#

## Sekilas mengenai input model

Agar dapat mempersiapkan data input, data input model harus mengikuti format XML sebagai berikut:
<GPS_points>
	<point>
		<time>0.295196</time>
		<lat>48.677994</lat>
		<lon>8.978952</lon>
	</point>
	<point>
		<time>120.314932</time>
		<lat>48.677994</lat>
		<lon>8.978952</lon>
	</point>
	<point>
		<time>240.334362</time>
		<lat>48.677994</lat>
		<lon>8.978952</lon>
	</point>
</GPS_points>

#

## Folder, file, dan kegunaannya

-   templates/
    -   index.html --> Berisi template website
-   app.py --> Berisi konfigurasi route untuk API
-   model.pkl --> Model Driving Clustering yang sudah di-training
-   request.py --> Berisi percobaan pemanggilan API dengan payload data JSON
-   requirements.txt --> Berisi daftar dependency/package Python yang diperlukan untuk menjalankan API dan model Regresi Linier

#

## Cara menjalankan API pada komputer Anda

### Menjalankan API

1. Pastikan Anda sudah menginstall Anaconda
1. Buka terminal/command prompt/power shell
1. Buat virtual environment dengan\
   `conda create -n <nama-environment> python=3.9`
1. Aktifkan virtual environment dengan\
   `conda activate <nama-environment>`
1. Install semua dependency/package Python dengan\
   `pip install -r requirements.txt`
1. Jalankan API menggunakan perintah\
   `python app.py`

### Akses melalui Website

Setelah API berjalan:

1. Anda akan diberikan URL untuk membuka website berupa `localhost:5000/` atau `127.0.0.1:5000/`
1. Buka URL dengan browser, upload file data yang ingin di prediksi

### Mencoba Akses API menggunakan payload JSON

Setelah API berjalan:

1. Buka terminal/comand prompt/power shell
1. Jalankan perintah `python request.py`
1. Setelah berhasil dieksekusi, Anda akan diberikan data response berupa JSON

