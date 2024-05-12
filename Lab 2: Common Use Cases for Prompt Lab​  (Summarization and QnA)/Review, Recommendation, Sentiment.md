## Review, Recommendation, Sentiment
In this demonstration, your objective is to get sentiment **review, recommendation, or sentiment** based on the information from the passage text based on your specific requirements. Feel free to use zero-shot, one-shot, or few-shot learning, and adjust your model parameter and instruction of the prompt.

***

### Product Review:
Your task is to review the information based on the product perspective.

**Instruction:** Anda adalah asisten yang bertugas untuk menganalisis konteks dalam ulasan produk. Temukan informasi seperti sentimen pengguna (positif/netral/negatif) dan alasannya, apakah terdapat konteks yang mencerminkan kekecewaan atau kepuasan, nama produk yang diulas, dan berikan informasi tentang perusahaan yang bersangkutan. Sebagai asisten dalam ulasan produk, tugas Anda adalah menganalisis dan mengumpulkan informasi yang relevan dari ulasan yang tersedia. Jawablah pertanyaan dalam bahasa Indonesia dan susun dalam format JSON tanpa informasi tambahan atau tanggapan.

**Example:** 
- Kebetulan lagi perlu lampu untuk ruang tidur saya, dan ternyata lampu tidur LightPro ini punya battery cadangan juga, dan dari segi harga juga cukup terjangkau, jadi saya memutuskan langsung membelinya. Walau kabelnya rusak selama pengiriman, penjual mau menggantinya. Dan ternyata ada bagian yang kurang lengkap juga, dan saya langsung memberi tahu penjual. Barang yang kurang lengkap dikirim bersamaan dengan kabel yang baru! menurut saya Lumina adalah perusahaan yang peduli dengan pelanggannya, dan bertanggung jawab dengan produk mereka!!

  
<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/36d4f65f-bd3e-4585-a3cb-63fbe29279ef">


**Exercise:**
- Saya sedang mencari earphone yang nyaman dan memiliki kualitas suara yang bagus untuk mendengarkan musik saat bepergian. Saya menemukan produk dari SoundWave yang memiliki ulasan bagus dan harganya juga cukup terjangkau. Setelah saya membelinya, saya menyadari bahwa kualitas suaranya memang luar biasa, namun sayangnya salah satu earphone-nya tidak berfungsi dengan baik setelah beberapa hari penggunaan. Saya menghubungi layanan pelanggan SoundWave, dan mereka dengan cepat mengirimkan penggantian earphone baru tanpa biaya tambahan. Selain itu, mereka juga memberikan saya bonus diskon untuk pembelian berikutnya sebagai kompensasi atas ketidaknyamanan yang saya alami. Saya sangat menghargai respons cepat dan pelayanan yang ramah dari SoundWave, sehingga saya merasa yakin untuk merekomendasikan produk-produk mereka kepada teman-teman saya.


***


Review merupakan kalimat diantara 3 tanda kutip diatas.
Buatlah rangkuman yang menjelaskan tentang apa yang diulas dalam Review diatas.
Rangkuman terdiri dari maksimum 2 kalimat.
Rangkuman:

Review merupakan kalimat diantara 3 tanda kutip diatas.
Berdasarkan review diatas, buatlah rangkuman yang berhubungan dengan pengiriman.
Seperti pesanan tiba tepat waktu atau tidak, paket yang diterima rusak atau tidak.
Rangkuman terdiri dari maksimum 2 kalimat.
Rangkuman:

Review merupakan kalimat diantara 3 tanda kutip diatas.
Berdasarkan review diatas, buatlah rangkuman dari sisi harga dan nilai produk yang dibeli.
Seperti harga terlalu mahal untuk kualitas barang atau tidak.
Rangkuman terdiri dari maksimum 2 kalimat.
Rangkuman:

Saya baru saja mencoba burger rendang di Burger Champs melalui applikasi mereka dan saya sangat menyukainya. 
Burger ini memiliki roti yang lembut dan empuk, daging yang juicy dan gurih, dan keju yang meleleh sempurna.
Saus burgernya juga sangat lezat, dengan rasa yang pas dan tidak terlalu berlebihan. Sayurannya juga segar dan renyah.
Harga yang cukup terjangkau untuk kualitas daging yang digunakan. Selain itu, burger ini tiba tepat waktu dan dalam keadaan yang masih hangat. Saya sangat puas dengan layanan pengantarannya. Pengemudi yang mengantarkan pesanan saya juga sangat ramah dan sopan. Dia juga sangat sigap dan mengantarkan pesanan saya dengan cepat. Secara keseluruhan, burger rendang di Burger Champs adalah salah satu burger terbaik yang pernah saya coba. 
Saya sangat merekomendasikannya kepada Anda yang mencari burger yang lezat dan menggugah selera, serta layanan pengantaran yang cepat dan profesional.




<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/7eeb4c63-222a-4671-88e0-cc83bad36ef9">


**Exercise:**
- Pada sebuah acara kumpul-kumpul di kafe kota, saya berkenalan dengan seorang wanita bernama Emily Smith. Emily adalah seorang desainer grafis yang tinggal di sebuah apartemen kecil di pinggiran kota. Dia lahir di Chicago tetapi pindah ke San Francisco untuk mengejar karier di dunia desain. Emily adalah penggemar seni rupa dan sering menghabiskan waktu luangnya mengunjungi galeri seni lokal. Dia juga seorang penggemar berat musik indie dan suka menghadiri konser di akhir pekan. Emily bercerita bahwa dia memiliki kucing peliharaan bernama Luna yang selalu menemani di apartemennya. Selain itu, dia adalah anggota aktif dalam komunitas desainer lokal dan sering menghadiri pertemuan dan lokakarya untuk terus meningkatkan keterampilannya dalam desain grafis.

***

### Email Content:
Your task is to recreate the email content without the sensitive information provided

**Instruction:** Berdasarkan email di atas, lakukan hal berikut: buatlah ulang email dengan menghapus informasi pribadi yang sensitif seperti nama individu, alamat, nomor telepon, nomor HP, alamat email, nomor kartu kredit, dan informasi medis. Pastikan tidak menambah atau mengurangi konteks email yang diberikan.

**Example:**
```
Yth. Bapak Putra,

Semoga email ini menemukan Bapak dalam keadaan sehat. Perkenalkan, nama saya Surya Permana, saya adalah tenaga penjual di Cheap Dealz Auto, dealer mobil terpercaya di Surabaya.
Saya mengetahui bahwa Bapak baru saja membeli mobil baru. Saya ingin mengucapkan selamat atas pembelian mobil baru Bapak, dan juga ingin menawarkan penawaran khusus untuk mobil baru lainnya.
Saat ini, Cheap Dealz Auto sedang mengadakan promo besar-besaran untuk mobil baru. Kami menawarkan berbagai macam mobil baru dengan harga yang sangat menarik. 
Selain itu, kami juga memberikan berbagai macam bonus dan hadiah menarik untuk setiap pembelian mobil baru.

Jika Bapak tertarik untuk mengetahui lebih lanjut tentang promo kami, silakan hubungi saya melalui nomor telepon atau email di bawah ini. 
Saya akan dengan senang hati membantu Bapak memilih mobil baru yang sesuai dengan kebutuhan dan budget Bapak.

Terima kasih atas perhatian Bapak.

Hormat saya,

Surya Permana
Cheap Dealz Auto

Jl. Soekarno hatta No.125, Surabaya

No HP: (0812)12293456
Email: SuryaPermana@CDAuto"
```


<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/04bd2692-9d64-4788-90c6-ea01d1656b31">


**Exercise:**
```
Yth. Ibu Anisa,

Semoga pesan ini menemui Ibu dalam keadaan baik. Saya, Farhan Ardiansyah, mewakili tim pemasaran dari Gaya Furniture, ingin menyampaikan salam hangat kepada Ibu.
Kami ingin mengucapkan terima kasih atas pembelian lemari baru Ibu beberapa waktu lalu. Kami berharap lemari tersebut dapat memenuhi kebutuhan penyimpanan Ibu dengan baik.

Untuk memperluas penawaran kami, kami ingin menginformasikan bahwa saat ini Gaya Furniture sedang mengadakan promo spesial untuk koleksi furnitur kamar tidur. Kami menawarkan berbagai desain lemari pakaian, meja rias, dan tempat tidur dengan diskon menarik. Selain itu, kami juga memberikan paket bonus berupa lampu tidur dan kursi santai untuk setiap pembelian paket kamar tidur lengkap.

Jika Ibu tertarik untuk melihat lebih banyak pilihan atau memiliki pertanyaan tentang promo kami, jangan ragu untuk menghubungi saya melalui nomor telepon atau email di bawah ini. Kami siap membantu Ibu dengan penuh perhatian.

Terima kasih atas dukungan dan kepercayaan Ibu kepada Gaya Furniture.

Hormat kami,

Farhan Ardiansyah
Gaya Furniture

Jl. Jendral Sudirman No. 78, Jakarta

Telp: (021) 12345678
Email: Farhan@gayafurniture.com
```

***
