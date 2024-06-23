# Investigate Hotel Business using Data Visualization

## Business Understanding 

### Problem Statement

Manajemen kinerja bisnis merupakan metrik yang berguna untuk menilai kemajuan bisnis secara keseluruhan dalam mencapai suatu tujuan. Kinerja bisnis berkaitan dengan efektivitas penjualan atau pemasaran. Hal tersebut dipengaruhi oleh kemampuanan perusahaan dalam menyusun dan menetapkan strategi penjualan produk/jasa sehingga dapat memenuhi harapan pelanggan.

Dalam bisnis bidang perhotelan pastinya berkaitan erat dengan pelanggan. Semakin banyak pelanggan yang melakukan pemesanan maka semakin meningkat pendapatan perusahaan. Oleh karena itu, analisis terhadap perilaku pelanggan sangatlah diperlukan. Baik analisa terhadap perilaku pelanggan dalam memesan hotel mapaun analisa terhadap tingkat pembatalan pesanan perlu kita lakukan untuk mengetahui kinerja suatu bisnis dalam konteks ini berarti kinerja bisnis bidang perhotelan. Karena jika terdapat banyak pelanggan yang membatalkan pesanannya maka dapat berdampak buruk pada kinerja bisnis hotel.

Tujuan dari proyek ini yaitu menganalisis perilaku pelanggan dalam bisnis bidang perhotelan sehingga dapat memberikan _insight_ mengenai kinerja dari bisnis perhotelan ini.Untuk mendapatkan _Insight_ tersebut kita perlu melakukan eskplorasi data, seperti menganalisis bagaimana perilaku pelanggan dalam melakukan pemesanan hotel ataupun mencari faktor apa saja yang dapat mempengaruhi pelanggan sehingga melakukan pembatalan pemesanan hotel. Selanjutnya untuk memudahkan _audience_ dalam memahami data dan mendapatkan _insight_ maka diperlukan visualisasi dan juga perlu adanya _data storytelling_ untuk menjelaskan kepada _audience_ dengan bahasa yang sesuai dengan karakter _audience_.

### **Goals**

Perusahaan ingin meningkatkan kinerja bisnis dengan menganalisis bagaimana perilaku pelanggan dalam melakukan pemesanan hotel dan menemukan faktor apa saja yang dapat mempengaruhi pelanggan sehingga melakukan pembatalan pemesanan hotel.

### **Objectives**

Membuat laporanan atas _insight_ yang diperoleh sehingga dapat memberikan _inisght_ kepada _stakeholder_ terkait kinerja dari bisnisnya dengan menggunakan visualisasi data dan _data storytelling_.

## Work Environment

- **Tools**

<img src="https://github.com/MukhlishHaq/Investigate_Hotel_Business_using_Data_Visualization/blob/master/Assets/jupyter%20logo.png" height="100"/>

- **Programming Language**

<img src="https://github.com/MukhlishHaq/Investigate_Hotel_Business_using_Data_Visualization/blob/master/Assets/Python.png" height="100"/>

- **Data Preprocessing & Cleaning Library**

<img src="https://github.com/MukhlishHaq/Investigate_Hotel_Business_using_Data_Visualization/blob/master/Assets/pandas%20logo.png" height="100"/>

- **Data Visualization Library**

<img src="https://github.com/MukhlishHaq/Investigate_Hotel_Business_using_Data_Visualization/blob/master/Assets/logo%20matplotlib.png" height="100"/>

- **Dataset**

[Kaggle](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand) atau [lihat disini](https://github.com/MukhlishHaq/Investigate_Hotel_Business_using_Data_Visualization/blob/master/Dataset/hotel_bookings_data.csv) 

## Data Description 

**About Dataset:**

Data ini berisi informasi pemesanan untuk City Hotel dan Resort Hotel. Serta mencakup informasi seperti waktu pemesanan, lama menginap, jumlah orang dewasa, anak-anak, dan/atau bayi, dan jumlah tempat parkir yang tersedia.

Semua informasi pribadi sudah dihapus dari data sehingga tidak terdapat privasi.

Dataset ini berisi `119,390 samples` dan `29 features` :

- `hotel` - Hotel (H1 = Resort Hotel or H2 = City Hotel)
    
    - `City Hotel` adalah jenis hotel yang terletak di pusat kota dan biasanya ditemukan di kota besar.

    - `Resort Hotel` adalah jenis penginapan yang biasanya dibangun di pesisir pantai atau di dataran tinggi, yang menawarkan pemandangan alam yang indah.

- `is_canceled` - Nilai yang menunjukkan apakah pemesanan dibatalkan (1) atau tidak (0)

- `lead_time` - Jumlah hari antara tanggal masuknya pemesanan ke dalam Property Manajemen System dan tanggal kedatangan

- `arrival_date_year` - Tahun kedatangan

- `arrival_date_month`- Bulan kedatangan

- `arrival_date_week_number` - Minggu kedatangan

- `arrival_date_day_of_month` - Hari kedatangan

- `stays_in_weekend_nights` - Jumlah tamu yang menginap di akhir pekan (sabtu atau minggu)

- `stays_in_weekdays_nights` - Jumlah tamu yang menginap di hari kerja (senin - jumat)

- `adults` - Jumlah orang dewasa

- `children` - Jumlah anak-anak

- `babies` - Jumlah bayi

- `meal` - Jenis makanan yang dipesan. Kategori berdasarkan jenis paket makanan yang biasa disaikan : 
    - Undefined/SC – tidak ada paket
    - BB – Tempat tidur & sarapan
    - HB – Setengah paket (sarapan dan sekali makan – biasanya makan malam) 
    - FB – Paket lengkap (sarapan, makan siang, dan makan malam)

- `city` - Nama kota

- `market_segment` - Segmen pasar. Istilah “TA” berarti “Travel Agents” dan “TO” berarti “Tour Operators”

- `distribution_channel` - Channel pemesanan. Istilah “TA” berarti “Travel Agents” dan “TO” berarti “Tour Operators”

- `is_repeated_guest` - Nilai yang menunjukkan apakah pemesanan dari tamu yang melakukan pemesanan berulang (1) or not (0)

- `previous_cancellations` - Jumlah pemesanan sebelumnya yang dibatalkan oleh pelanggan sebelum pemesanan saat ini

- `previous_bookings_not_canceled` - Jumlah pemesanan sebelumnya yang tidak dibatalkan oleh pelanggan sebelum pemesanan saat ini

- `booking_changes` - Jumlah perubahan yang dilakukan pada pemesanan dari saat pemesanan dimasukkan pada Property Management System

- `deposit_type` - Menunjukkan deposit dari pelanggan untuk menjamin pemesanan. Terdiri dari 3 kategori: 
    - No Deposit – tidak ada deposit
    - Non Refund – deposit sebesar total biaya menginap
    - Refundable – deposit sebesar dibawah total biaya menginap

    Note : Deposit adalah uang jaminan yang akan dibayarkan Kembali kepada pelanggan. Dengan syarat tidak ada fasilitas yang disrusak dan tidak menggunakan fasilitas hotel berbayar lainnya. Jika memenuhi syarat maka deposit akan dikembalikan 100% kepada pelanggan.

- `agent` - ID dari agen perjalanan yang melakukan pemesanan

- `company` - ID perusahaan yang melakukan pemesanan atau bertanggung jawab untuk membayar pemesanan. ID ditampilkan sebagai pengganti nama.

- `days_in_waiting_list` - Jumlah hari pemesanan berada dalam daftar tunggu sebelum dikonfirmasi kepada pelanggan

- `customer_type` - Tipe pemesanan berdasarkan 4 kategori: 
    - Contract - Ketika terkait dengan kontrak atau perjanjian; 
    - Group – Ketika pemesanan berkaitan dengan group; 
    - Transient – Ketika pemesanan bukan bagian dari kontrak atau grup, dan tidak terkait dengan pemesanan lainnya; 
    - Transient-party – Ketika pemesanan bersifat sementara

- `adr`- Rata-rata tarif harian yang ditentukan dengan membagi jumlah semua transaksi penginapan dengan jumlah lama menginap

- `required_car_parking_spaces` - Jumlah ruang parkir yang dibutuhkan oleh pelanggan

- `total_of_special_requests` - Jumlah permintaan khusus dari pelanggan (misal twin bed atau memilih kamar dilantai berapa)

- `reservation_status` - Status akhir pemesanan, berdasarkan 3 kategori: 
    - Canceled – Pemesanan yang dibatalkan oleh pelanggan; 
    - Check-Out – Pelanggan yang sudah selesai menginap; 
    - No-Show – Pelanggan yang tidak melakukan check in dan menginformasikan alasannya ke pihak hotel


# Data Cleaning/Preprocessing

### Handling Missing Value

- Terdapat beberapa kolom dengan missing values:
    - `company` dengan total 94% null values atau sebanyak `112,593 baris`.
    
        Isi dengan nilai nol pada kolom 'company' yang tidak berkaitan.
        
    - `agent` dengan total 13% null values atau sebanyak `16,340 baris`.
    
        Isi dengan nilai nol pada kolom 'agent' yang tidak berkaitan.
        
    - `city` dengan total 0.4% null values atau sebanyak `488 rows`.
    
        Isi dengan 'unknown' kota yang tidak tersedia.
        
    - `children` dengan total 0.003% null values atau sebanyak `4 baris`.
    
        Isi dengan nilai nol untuk anak-anak atau pelanggan yang tidak mempunyai anak.

### Handling Duplicate Rows

- Dataset ini mempunyai banyak data yang double, dengan total 33,261 baris.
- Sebelum melakukan penghapusan data yang double, dataset ini memiliki 119,390 baris.
- Setelah dilakukan penghapusan data, dataset ini berkurang menjadi 86,129 rows.

### Data Types Information

Dilakukan perubahan tipe data `float64` yang sebelumnya terdapat null value, `children`, `agent`, and `company` menjadi tipe data `int64`

###Handling Invalid Values

Mengganti nilai yang salah pada kolom 'meal'. Nilai ini diubah menjadi 'No Meal' dengan asumsi pelanggan tidak melakukan pemesanan makanan

### Drop Unnecessary Data

Dari data yang ada dapat dilihat bahwa kondisi pelanggan sangat berpengaruh. Jadi perlu memastikan jumlah pelanggan dalam tiap pemesanan

- Jumlah pelanggan / Tamu
- Total durasi dalam sehari

Jadi, kita memfilternya dengan :

- Total Tamu (Jumlah Pelanggan / Tamu) <= 0, atau tidak ada tamu.
- Total durasi dalam sehari <= 0, atau tidak ada data durasi menginap.
- Jika ada satu data for adr (Average Daily Rate), itu mungkin karena ada kesalahan perhitungan. Jika hanya ada 1 baris, akan dihapus untuk menghidari kesalahan dalam analisis.


# Statistical Summary

![image](https://github.com/MukhlishHaq/Investigate_Hotel_Business_using_Data_Visualization/blob/master/Assets/Screenshot%202024-06-08%20194920.png)

![image](https://github.com/MukhlishHaq/Investigate_Hotel_Business_using_Data_Visualization/blob/master/Assets/Screenshot%202024-06-08%20194935.png)

# Exploring Business Insights

###Monthly Hotel Booking Analysis Based on Hotel Type

Dalam industri perhotelan, perilaku pelanggan dalam pemesanan hotel memainkan peran penting karena berdampak pada pendapatan perusahaan. Menganalisis perilaku pelanggan saat dalam memesan hotel sangatlah penting. Sehingga, kita dapat mengidentifikasi jenis hotel mana yang paling populer di kalangan pelanggan dan menghubungkannya dengan kondisi musiman saat terjadinya transaksi pemesanan hotel tersebut. 

Oleh karena itu, perlu untuk membandingkan jumlah pemesanan hotel setiap bulannya berdasarkan jenis hotel dan menganalisis kapan terjadi peningkatan atau penurunan pemesanan hotel pada bulan atau musim tertentu.

![image](https://github.com/MukhlishHaq/Investigate_Hotel_Business_using_Data_Visualization/blob/master/Assets/Screenshot%202024-06-08%20195014.png)

Interpretation:

- Kedua hotel mengalami tren peningkatan yang sama dalam jumlah rata-rata pemesanan hotel. Namun, puncak tertinggi terdapat pada City Hotel.

- Pemesanan hotel menunjukkan peningkatan yang signifikan selama musim liburan. Kenaikan tertinggi terjadi pada bulan Juni - Agustus untuk City Hotel dan Resort Hotel, hal itu dikarenakan sedang liburan sekolah di Indonesia.

- Selain itu, terdapat peningkatan yang tinggi juga pada bulan November dan Desember, namun memiliki durasi yang lebih pendek dibandingkan dengan pada bulan Juni dan Juli, hal itu kemungkinan besar disebabkan karena adanya libur Tahun Baru dan berakhirnya jatah cuti tahunan. Untuk mengoptimalkan pemesanan kamar hotel, dapat menerapkan promosi Tahun Baru untuk menarik lebih banyak pengunjung.

- Rendahnya pemesanan terjadi sepanjang Januari - Maret dan juga pada bulan Agustus - September, terutama di City Hotel, di mana terjadi penurunan pemesanan yang signifikan. Penurunan ini dapat dikaitkan dengan dimulainya musim sekolah dan awal masuk kerja setelah berakhirnya libur. Untuk menanggulangi hal ini, hotel dapat menawarkan diskon atau voucher untuk menarik pelanggan agar tetap mengunjungi hotel.


## Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates

In addition to analyzing customer behavior in booking hotels, the success of a hotel business can be measured by the booking cancellation rate. If many customers cancel their reservations, it can negatively impact the hotel's performance. Therefore, it is essential to explore the factors influencing booking cancellations. In this phase, we will investigate how the duration of stay can affect the hotel booking cancellation rate.

To analyze the correlation between the duration of stay and the hotel booking cancellation rate.

![image](https://github.com/MukhlishHaq/Investigate_Hotel_Business_using_Data_Visualization/blob/master/Assets/Screenshot%202024-06-08%20195038.png)

Interpretation : 
- The City Hotel experiences the highest number of cancellations with a significant increasing trend, while the Resort Hotel also shows an increasing trend, but not as steady.

- There is a positive correlation between Stay Duration and Cancellation Ratio, indicating that the longer customers stay, both in City and Resort Hotels, the higher the cancellation rate.

- The City Hotel's highest cancellation rate is observed for stays above 4 weeks, whereas for the Resort Hotel, the highest cancellation rate occurs for stays of 3 weeks.

- To address this issue, the hotel company can pay closer attention to the causes of booking cancellations and implement stricter cancellation policies. Additionally, offering special promotions may be effective in mitigating cancellations.

## Impact Analysis of Lead Time on Hotel Bookings Cancellation Rate

Tujuannya untuk menganalisis korelasi antara waktu tunggu pemesanan hotel dan tingkat pembatalan pemesanan hotel. Dalam industri perhotelan, pelanggan biasanya diizinkan untuk memesan hotel sebelum tanggal kedatangan mereka, dan waktu tunggu dapat bervariasi dari beberapa hari hingga beberapa bulan. 

Dengan demikian perlu untuk memeriksa apakah waktu tunggu antara pemesanan hotel dan tanggal kedatangan mempengaruhi tingkat pembatalan pemesanan hotel.

![image](https://github.com/MukhlishHaq/Investigate_Hotel_Business_using_Data_Visualization/blob/master/Assets/Screenshot%202024-06-08%20195106.png)

Interpretation :
- Semakin lama waktu tunggu, semakin tinggi kemungkinan pembatalan pemesanan. Waktu tunggu mengacu pada jumlah hari antara terjadinya pemesanan ke dalam Sistem Manajemen Properti (PMS) dan tanggal kedatangan, di mana waktu tunggu yang lebih lama berkaitan dengan tingkat pembatalan yang lebih tinggi.

- Kedua jenis hotel memiliki tingkat pembatalan terendah untuk waktu tunggu <= 1 bulan, dengan City Hotel sebesar 22,47% dan Resort Hotel sebesar 13,11%.

- Kedua tipe hotel ini memiliki tingkat pembatalan tertinggi untuk pemesanan yang dilakukan dengan waktu tunggu 11-12 bulan, dengan City Hotel sebesar 77,41% dan Resort Hotel sebesar 43,5%.

- Baik Resort maupun City Hotel mengalami tingkat pembatalan tertinggi di sekitar waktu tunggu 1 tahun. Hal ini dapat disebabkan oleh rencana liburan pelanggan yang dibatalkan atau lupa untuk reservasi hotel mereka jika waktu tunggu terlalu lama. Hotel dapat memberikan pengingat kepada pelanggan untuk mengurangi pembatalan dan menerapkan kebijakan pembatalan yang lebih ketat untuk setiap pemesanan untuk mencegah kejadian tersebut.

# Summary

- Keduanya menunjukkan tren peningkatan pemesanan yang mirip, dengan City Hotel mengalami puncak tertinggi. Pemesanan hotel meningkat secara signifikan selama musim liburan, terutama pada bulan Juni - Agustus dan November - Desember. City Hotel juga mengalami penurunan pemesanan yang signifikan pada bulan Januari - Maret dan Agustus - September. Untuk mengoptimalkan pemesanan, meningkatkan promosi dan memberikan diskon dapat menjadi strategi yang efektif untuk kedua hotel.

- City Hotel memiliki pembatalan tertinggi dengan tren peningkatan yang signifikan. Terdapat korelasi positif antara stay duration dan cancellation ratio untuk kedua hotel. Tingkat pembatalan tertinggi di City Hotel adalah untuk pemesanan dengan masa inap di atas 4 minggu, sedangkan tingkat tertinggi di Resort Hotel adalah untuk pemesanan dengan masa inap 3 minggu. Dengan menerapkan kebijakan pembatalan yang lebih ketat dan memberikan tawaran promosi khusus dapat membantu meminimalisir pembatalan.

- Waktu tunggu yang lebih lama memiliki korelasi dengan tingkat pembatalan yang lebih tinggi untuk City and Resort Hotel. Tingkat pembatalan terendah terjadi pada kategori waktu tunggu <= 1 bulan, sedangkan tingkat pembatalan tertinggi terjadi pada kategori waktu tunggu 11-12 bulan. Baik Resort dan City Hotel mengalami tingkat pembatalan tertinggi pada waktu tunggu 1 tahun. Menerapkan pengingat dan kebijakan pembatalan yang lebih ketat dapat membantu meminimalisir pembatalan dan meningkatkan efisiensi pemesanan secara keseluruhan.
