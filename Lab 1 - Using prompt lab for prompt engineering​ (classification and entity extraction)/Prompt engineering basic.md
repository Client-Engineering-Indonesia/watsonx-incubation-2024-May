# Prompt engineering

**Note:** Gambar berikut menunjukkan hasil dari watsonx.ai. Teks berwarna abu-abu adalah contoh input yang dapat berikan untuk model. Teks yang di-highlight biru adalah respons dari model.

1.0 LLM Foundations
Sebelum kita mulai mengeksplorasi kemampuan watsonx.ai, pertama-tama kita perlu mengetahui tentang cara kerja Model Bahasa Besar (LLM), dan bagaimana kita dapat menyesuaikan model dan parameter untuk mengubah output yang dihasilkan. Mengetahui hal tersebut dapat membantu kita untuk lebih efisien menggunakan LLM model.


<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2024/assets/20800128/5dd09fbd-2158-495f-bdde-2be596d0742e">


Saat Anda membuka watsonx.ai, ini adalah tampilan yang akan ditunjukkan kepada Anda. Area teks tengah yang besar disebut Prompt Lab, atau Prompt Builder jika Anda memilih tampilan lebih lanjut dengan mengklik kotak centang di kiri atas. Di sisi kanan adalah parameter dari model yang dapat Anda gunakan untuk memilih guna mengoptimalkan respons model terhadap permintaan atau prompt Anda. Dan di kiri bawah, terdapat ringkasan jumlah token yang digunakan oleh prompt Anda selama eksekusi.

### 1.1 Tokens
Each time you enter a prompt, your “input tokens” and “generated tokens” will update. Tokens are an important concept to understand as they constrain the performance of your model plus determine the cost of using models. As you will learn throughout the Labs, tokens are not a 1:1 match with words in natural language, but on average, one token is equal to 4 characters. Before sending your prompt to the model, the prompt's text is Tokenized or broken into smaller subsets of characters better understood by a model.

It is important to monitor your token usage to know how much information you are feeding into the model with each prompt, as well as how much text is generated for you. Depending on the model selected in Prompt Builder, you will see a max of 2048 or 4096 tokens. Keep in mind that the more expressive you are with your prompt instructions, the less room the model has to respond back to you.

Setiap kali Anda melakukan prompting, “input tokens” dan “generated tokens” akan diperbarui. Token adalah konsep penting untuk dipahami karena membatasi performa model Anda dan menentukan biaya penggunaan model. Seperti yang akan Anda pelajari di melalui Lab, tokens bukanlah 1:1 dengan kata-kata yang ada dalam sebuah kalimat, namun rata-rata, satu token sama dengan 4 karakter. Sebelum mengirimkan perintah Anda ke model, teks perintah tersebut di-Tokenized atau dipecah menjadi subkumpulan karakter yang lebih kecil yang lebih mudah dipahami oleh model.

Penting untuk memantau penggunaan token Anda untuk mengetahui berapa banyak informasi yang Anda masukkan ke dalam model dalam setiap perintah, serta berapa banyak teks yang dihasilkan untuk Anda. Bergantung pada model yang dipilih di Prompt Builder, Anda akan melihat maks 2048 atau 4096 token. Ingatlah bahwa semakin ekspresif Anda dalam memberikan instruksi, semakin sedikit "ruang" yang dimiliki model untuk merespons Anda.

### 1.2 Everything is text completion
watsonx.ai bukan chatbot interface, terkadang hasil prompt tidak memberikan apa yang diharapkan, tapi kita dapat memberikan instruksi ke LLM model untuk melakukan sejumlah hal dengan cara yang lebih tepat. Misalnya, bagaimana jika kita meminta Watsonx.ai untuk: Sebutkan langkah-langkah memulai bisnis online

<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2024/assets/20800128/7e70cb01-9e2f-42ff-9a7f-eef7dd573fb5">

Jawaban di atas bukanlah apa yang kita harapkan.

### 1.3 Provide an example as guidance (or Single Shot Prompting)
Untuk mendapatkan respons dengan kualitas yang lebih baik, berikan contoh jenis respons yang Anda inginkan. Dalam istilah teknis, ini disebut Single Shot Prompting.

<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2024/assets/20800128/6d04e30f-b04b-4a0c-89b1-c199183b4b49">

Seperti yang Anda lihat, memberikan satu contoh sebelum memberikan perintah ke LLM disebut dengan Single Shot Prompting, namun menambahkan lebih banyak contoh ke dalam prompt juga lumrah untuk dilakukan. Umumnya, memberikan contoh dalam jumlah yang lebih dari satu disebut sebagai “Few Shot Prompting” dan merupakan cara yang ampuh untuk memastikan Anda mendapatkan hasil yang spesifik.

Gunakan teks berikut ini, untuk mencoba Prompt Builder:

```
Sebutkan langkah-langkah memulai bisnis online
1. Pilih produk atau jasa yang akan Anda jual.
2. Lakukan riset pasar.
3. Buat rencana bisnis.
4. Dapatkan izin dan sertifikasi yang diperlukan.
5. Buat situs web atau toko online.
6. Promosikan bisnis Anda.
7. Layanan pelanggan yang baik.

Sebutkan langkah-langkah memulai bisnis kuliner
```
