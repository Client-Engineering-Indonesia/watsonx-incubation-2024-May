# Prompt Engineering Exercise (Bahasa Indonesia)
***

Gunakan Prompt Lab atau prompt Builder dari watsonx.ai untuk mengerjakan latihan berikut ini

__Latihan__

| __Exercise__ | __Goal__ |
| --- | --- |
| 1. Generate | Buatlah 3 kalimat mengenai Candi Prambanan|
| 2. Rewrite | Mengubah markdown menjadi HTML |
| 3. Summarize | Merangkum cerita pendek |
| 4. Summary points | Buat daftar topik dari _meeting transcript_ |
| 5. Study questions | Mengantisipasi pertanyaan yang mungkin ditanyakan _customer_ |
| 6. Text extraction | Ekstrak kata kerja yang ditemukan dalam kalimat |
| 7. Compare | Identifikasi kesamaan yang ditemukan dalam sejumlah paragraf |
| 8. Text search | Temukan halaman yang mengandung kata yang dicari |
| 9. Classify | Deteksi keinginan atau tujuan dari pengguna chatbot |
| 10. Anomaly detection | Temukan entri yang aneh |
| 11. Math question | Ada berapa menit dalam satu hari? |
| 12. Writing with persona | Menulis ulang kalimat dalam gaya yang berbeda |


## 1. Generate
***

__`Goal: Buatlah 3 kalimat mengenai Candi Prambanan`__


contoh:

```
3 kalimat mengenai Monas:
- Monas adalah monumen peringatan kemerdekaan Indonesia yang terletak di Jakarta.
- Monas memiliki tinggi 132 meter dan dimahkotai lidah api yang dilapisi emas.
- Monas merupakan salah satu landmark paling terkenal di Indonesia.

3 kalimat mengenai Jam Gadang:
- Jam Gadang adalah menara jam bersejarah yang terletak di Bukittinggi, Sumatra Barat.
- Jam Gadang dibangun pada tahun 1926 oleh pemerintah Hindia Belanda.
- Jam Gadang merupakan simbol kota Bukittinggi dan budaya Minangkabau.
```

_hint: copy paste contoh, dan berikan instruksi untuk membuat 3 kalimat mengenai Candi Prambanan, hal ini dimaksudkan agar model mendapat konteks lebih mengenai instruksi yang diberikan_

**Exercise**
```
Tulis 3 kalimat mengenai topik yang diberikan. Kalimat harus diawali dengan angka. kalimat yang dihasilkan harus berbeda dari kalimat sebelumnya.
Output harus terdiri dari 3 kalimat. Output harus memiliki struktur seperti contoh 1 dan 2.

3 kalimat mengenai Monas:
1. Monas adalah monumen peringatan kemerdekaan Indonesia yang terletak di Jakarta.
2. Monas memiliki tinggi 132 meter dan dimahkotai lidah api yang dilapisi emas.
3. Monas merupakan salah satu landmark paling terkenal di Indonesia.

3 kalimat mengenai Jam Gadang:
1. Jam Gadang adalah menara jam bersejarah yang terletak di Bukittinggi, Sumatra Barat.
2. Jam Gadang dibangun pada tahun 1926 oleh pemerintah Hindia Belanda.
3. Jam Gadang merupakan simbol kota Bukittinggi dan budaya Minangkabau.

3 kalimat mengenai Candi Prambanan:
```

Gunakan berbagai model yang tersedia untuk mendapatkan hasil yang berbeda. Atur maximum token menjadi __200__.

`meta-llama/llama-3-70b-instruct`
```
3 kalimat tentang Candi Prambanan:
1. Candi Prambanan adalah kompleks candi Hindu terbesar di Indonesia yang terletak di Yogyakarta.
2. Candi Prambanan dibangun pada abad ke-9 dan terdiri dari 240 candi.
3. Candi Prambanan dianggap sebagai salah satu warisan budaya dunia oleh UNESCO.
```

`ibm-mistralai/mixtral-8x7b-instruct-v01-q`
```
3 kalimat tentang Candi Prambanan:
1. Candi Prambanan adalah kompleks candi Hindu yang terletak di Klaten, Jawa Tengah.
2. Candi Prambanan terdiri dari 240 candi, dengan candi utama yang tinggi 47 meter.
3. Candi Prambanan merupakan patungan antara keindahan seni bina dan keagungan rupa.

```

## 2. Rewrite

__`Goal: Mengubah markdown menjadi HTML`__

```
# Contoh 1
Markdown:
## Selamat datang di website saya!!! 
Saya sangat senang bisa berbagi keseharian dan kegiatan saya dengan anda. Disini saya akan membahas berbagai topic seperti teknologi, travel, dan personal growth. Ikuti terus jika ingin terus mendapat update terbaru!

HTML:
<h2>Selamat datang di website saya!!!</h2> <p>Saya sangat senang bisa berbagi keseharian dan kegiatan saya dengan anda. Disini saya akan membahas berbagai topic seperti teknologi, travel, dan personal growth. Ikuti terus jika ingin terus mendapat update terbaru!</p>
```

```

**Exercise**
```
Markdown:
# Judul Artikel
Menggunakan LLMs merupakan hal yang cukup mudah: Berikan perintah terhadap model menggunakan teks (contoh: "Saya mengajak hewan peliharaan saya") dan modelnya menghasilkan teks yang melanjutkan kata-kata tersebut (contoh: "berjalan-jalan di taman")

HTML:
```

```
Markdown: 
### Hall of shame: Ketika LLMs melakukan kesalahan, Bahkan pembuatnya tidak bisa menjelaskan jawaban yang dihasilkan secara menyeluruh: [Pembuat ChatGPT tidak mengetahui mengapa model enggan membicarakan Trump](https://www.semafor.com/
article/02/03/2023/how-chatgpt-inadvertently-learned-to-avoid-talking-about-trump)

HTML:
```

## 3. Summarize

__`Goal: Merangkum cerita pendek`__

`Cerita Pendek 1`
```
Di sebuah rumah sakit, ada seorang dokter bernama dr. Andi. dr. Andi adalah seorang dokter yang berdedikasi tinggi. Ia ingin memberikan pelayanan kesehatan yang terbaik bagi pasien-pasiennya. Namun, dr. Andi menghadapi tantangan karena banyaknya data medis yang harus dianalisis. Suatu hari, dr. Andi mendapatkan bantuan dari sebuah perusahaan teknologi. Perusahaan tersebut memberikan dr. Andi alat bantu berupa sistem kecerdasan buatan (AI) yang dapat membantunya untuk menganalisis data medis. dr. Andi pun sangat senang. Ia dapat mendiagnosis penyakit pasiennya dengan lebih cepat dan akurat.

Rangkuman: Data medis dan AI membantu dr. Andi mendiagnosis penyakit pasiennya dengan lebih cepat dan akurat.
```

`Cerita Pendek 2`
```
Di sebuah desa, ada seorang petani bernama Pak Budi. Pak Budi adalah seorang petani yang ulet dan gigih. Ia ingin meningkatkan produktivitas pertaniannya. Suatu hari, Pak Budi mendapatkan bantuan dari sebuah perusahaan teknologi. Perusahaan tersebut memberikan Pak Budi alat bantu berupa sistem AI yang dapat membantunya untuk mengelola pertaniannya. Pak Budi pun sangat senang. Ia dapat meningkatkan produktivitas pertaniannya dengan lebih mudah dan efisien.

Rangkuman: AI membantu Pak Budi meningkatkan produktivitas pertaniannya dengan lebih mudah dan efisien.
```

**Exercise**

`Cerita Pendek 3`
```
Di sebuah kota, ada seorang pemerintah daerah bernama Pak Dimas. Pak Dimas adalah seorang pemerintah daerah yang peduli terhadap masyarakatnya. 
Ia ingin meningkatkan pelayanan publik di kotanya. Suatu hari, Pak Dimas mendapatkan bantuan dari sebuah perusahaan teknologi. 
Perusahaan tersebut memberikan Pak Dimas alat bantu berupa sistem data yang dapat membantunya untuk mengelola pelayanan publik. 
Pak Dimas pun sangat senang. Ia dapat meningkatkan pelayanan publik di kotanya dengan lebih efektif dan efisien.

Summary:
```

`Cerita Pendek 4`
```
Di sebuah perusahaan, ada seorang pebisnis bernama Pak Budi. Pak Budi adalah seorang pebisnis yang cerdas dan inovatif. 
Ia ingin meningkatkan penjualan perusahaannya. Suatu hari, Pak Budi mendapatkan bantuan dari sebuah perusahaan teknologi. 
Perusahaan tersebut memberikan Pak Budi alat bantu berupa sistem data yang dapat membantunya untuk menganalisis data penjualan. 
Pak Budi pun sangat terbantu karenanya. Ia dapat meningkatkan penjualan perusahaannya dengan lebih tepat sasaran.

Summary:
```

## 4. Summary points

__`Goal: Buat daftar topik dari meeting transcript`__

Contoh 1:
```
Transkrip:
00:00 [Mark] Halo, selamat pagi semuanya, terima kasih karena telah meluangkan waktu untuk mengikuti meeting hari ini.
00:05 [Mark] Hari ini mari kita berdiskusi mengenai peluncuran product yang akan datang.
00:10 [Mark] Tanggal peluncuran sudah di tetapkan menjadi bulan depan.
00:15 [Sarah] Kabar baik dong! tapi kita harus segera melakukan perancanaan marketing campaign.
00:20 [Sarah] Menurut saya, sebaiknya kita menggunakan social media dan influencers untuk memviralkan product ini.
00:30 [John] Saya setuju dengan sarah, kita juga harus menyiapakan video product yang menarik penonton.
00:35 [Mark] Ide yang sangat bagus, Sarah, John, ayo kita buat list apa saja yang harus dikerjakan dan juga timeline eksekusi dari task tersebut.

Summary:
- Peluncuran produk baru
- Tanggal peluncuran sudah diputuskan bulan depan
- Marketing campaign menggunakan sosial media
- Membuat video produk yang menarik
- Membuat timeline dari hal yang harus dieksekusi
```

__Rangkum transkrip percakapan dengan menggunakan poin-poin. Setiap poin haruslah merupakan baris baru. Setiap poin terdiri dari 2-5 kata-kata.__

`cobalah menggunakan beberapa model seperti: granite-13b-instruct-v2, flan-ul2-20b`

```
00:00   [ali]   Tujuan meeting kita hari ini adalah untuk memilih desain dari solusi kita.
00:12   [alex]  Menurut saya, pilihan pertama adalah pilihan yang tepat.
00:25   [ali]   Saya juga setuju.
00:40   [erin]  Tapi, kelebihan dari pilihan kedua adalah waktu yang dibutuhkan lebih cepat.
01:03   [alex]  Sebenernya itu juga harus dipertimbangkan sih.
01:30   [ali]   Jadi, gimana?
01:55   [alex]  Saya setuju juga kalo pilihan kedua.
02:20   [erin]  Saya juga.
02:45   [ali]   Oke, kita pakai pilihan kedua saja.
```

```
00:00   [alex]  Halo semua, ayo kita bikin rencana untuk pesta akhir tahun!
00:10   [ali]   Eh gimana kalo kita makan-makan di restaurant pas makan siang?
00:21   [sam]   Ide bagus sih.
00:47   [sam]   Kalo abis itu nonton gimana?
01:04   [alex]  kalau Golf?
01:15   [sam]   Gimana kalau, setiap orang bebas memilih nonton atau main golf sesuai keinginana mereka.
01:29   [alex]  Ide bagus.  Let's have a party!
```

## 5. Study questions

__`Goal: Mengantisipasi pertanyaan yang mungkin ditanyakan customer`__

Contoh 1:
```
Topic: overview AutoAI

Informasi:
"AutoAI merupakan alat dengan graphical interface pada Watson Studio yang dapat digunakan untuk menganalisa data dan menemukan data transformation, algoritma, dan parameter yang paling sesuai untuk predictive model anda,
AutoAI menampilkan hasil rekomendasi dengan menampilkan beberapa pipeline yang paling sesuai sebagai pilihan untuk anda."

Pertanyaan dari Informasi diatas:
1. Bagaimana cara AutoAI menganalisa data saya?
2. Bagaimana cara AutoAI menentukan algoritman terbaik?
3. Bagaimana cara AutoAI menentukan parameter yang terbaik?
4. Bagaimana cara AutoAI mengurutkan hasil rekomendasi terbaik?
```

```
Topic: Jupyter notebook

Informasi: Jupyter Notebook adalah aplikasi web yang memungkinkan pengguna untuk membuat dokumen interaktif yang menggabungkan kode, teks, dan visualisasi. 
Dokumen ini dapat digunakan untuk berbagai keperluan, seperti analisis data, pembelajaran mesin, dan pengembangan perangkat lunak. 
Jupyter Notebook adalah alat yang mudah digunakan dan fleksibel, serta mendukung berbagai bahasa pemrograman. 
Dokumen Jupyter Notebook dapat dibagikan dan dikolaborasikan dengan mudah.

Pertanyaan dari Informasi diatas:
1. Apakah Jupyter Notebook hanya untuk data scientist?
2. Apa saja bahasa pemrograman yang didukung oleh Jupyter Notebook?
3. Bagaimana cara menggunakan Jupyter Notebook?
4. Apa saja kelebihan Jupyter Notebook dibandingkan dengan IDE programming lainnya?
```

__Berikut informasi yang ditandi dengan petik dua, buat 4 pertanyaan yang berhubungan dengan informasi tersebut. pertanyaan harus berdasarkan informasi yang disediakan.Pertanyaan harus diberi angka (1, 2, 3, 4)__

`cobalah menggunakan beberapa model seperti: granite-13b-instruct-v1,  llama-2-70b-chat, mpt-7b-instruct2`

```
Topic: Docker Contaner

Informasi: "Docker container adalah sebuah lingkungan terisolasi yang dapat digunakan untuk menjalankan aplikasi. 
Container dapat digunakan untuk berbagai aplikasi, seperti web server, database, atau aplikasi seluler.
Untuk membuat Docker container, Anda perlu memiliki Docker image. Docker image adalah template yang digunakan untuk membuat container. 
Docker image dapat dibuat dari berbagai sumber, seperti Docker Hub, atau Anda dapat membuatnya sendiri."

Pertanyaan dari Informasi diatas:
```

## 6. Text extraction

__`Goal: Ekstrak kata kerja yang ditemukan dalam setiap kalimat `__

```
Contoh 1:
Paragraf: "Petani kopi di Desa Kopi, Jawa Tengah, memetik biji kopi yang matang dengan hati-hati agar tidak merusak buahnya. 
Biji kopi tersebut kemudian disortir berdasarkan ukuran dan kualitasnya. 
Biji kopi yang sudah tersortir kemudian disangrai dengan suhu dan waktu yang tepat agar menghasilkan aroma dan rasa yang khas. 
Biji kopi yang sudah sangrai kemudian digiling untuk menghasilkan bubuk kopi. Bubuk kopi tersebut kemudian dikemas dan dijual ke berbagai daerah di Indonesia dan mancanegara.

kata kerja yang ditemukan:
- memetik
- matang
- merusak
- sortir
- sangrai
- menghasilkan
- digiling
- kemas
- jual
```

```
Contoh 2:
Paragraf: "Seorang pemuda membuka kotak kardus baru yang berisi smartphone terbaru dari merek ternama. 
Pemuda itu dengan hati-hati mengeluarkan smartphone dari kotak dan menyalakannya. 
Smartphone tersebut langsung menampilkan layar yang cerah dan tajam. Pemuda itu tersenyum puas karena telah mendapatkan smartphone yang diinginkannya."

kata kerja yang ditemukan:
- membuka
- mengeluarkan
- menyalakan
- menampilkan
- tersenyum
```

