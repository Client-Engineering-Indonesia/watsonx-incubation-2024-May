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


### 1. Generate
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
1. Candi Prambanan adalah kompleks candi Hindu yang terletak di Yogyakarta.
2. Candi Prambanan dibangun pada abad ke-9 dan merupakan salah satu candi Hindu terbesar di dunia.
3. Candi Prambanan memiliki 240 candi dan 18 tempat ibadah lainnya.
```

`ibm-mistralai/mixtral-8x7b-instruct-v01-q`
```
3 kalimat tentang Candi Prambanan:
1. Candi Prambanan adalah candi paling terkenal di Indonesia.
2. Candi Prambanan merupakan candi pertama yang dibangun di Indonesia.
3. Candi Prambanan terletak di Klaten, Jawa Barat.
```

### 2. Rewrite
***

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
# Contoh 2
Markdown:
# Ini adalah judul tingkat 1
## Ini adalah judul tingkat 2
### Ini adalah judul tingkat 3

Ini adalah paragraf teks.

* Ini adalah poin pertama
* Ini adalah poin kedua

Ini adalah tautan: [Google](https://www.google.com/)

HTML:
<h1>Ini adalah judul tingkat 1</h1>
<h2>Ini adalah judul tingkat 2</h2>
<h3>Ini adalah judul tingkat 3</h3>

<p>Ini adalah paragraf teks.</p>

<ul>
<li>Ini adalah poin pertama</li>
<li>Ini adalah poin kedua</li>
</ul>

<a href="https://www.google.com/">Google</a>
```




