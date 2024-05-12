## Summary
In this demonstration, your objective is to get a **Summarization** based on the information from the passage text based on your specific requirements. Feel free to use zero-shot, one-shot, or few-shot learning, and adjust your model parameter and instruction of the prompt.

***

### Meeting Summarization:
Your task is to summarize the information based on the information provided.

**Instruction:** 
Anda adalah asisten yang bertugas untuk menganalisis percakapan dalam rapat. Buatlah dalam bahasa Indonesia dengan format Minutes Of Meeting (MoM), mencakup topik, kapan meeting dilaksanakan, daftar peserta, ringkasan, poin penting dalam bentuk daftar, dan langkah-langkah selanjutnya yang diambil.

**Example:** 
```
00:00 [Agus] Selamat pagi, semuanya. Terima kasih sudah hadir dalam pertemuan online pada hari ini. Saya sangat senang cuaca hari ini baik karena kemarinl 7 Mei hujan terus.
00:05 [Agus] Kita akan memulai dengan membahas implementasi sistem baru untuk proses produksi yang menjadi fokus utama.
00:15 [Agus] Pak Budi, mohon penjelasan mendalam mengenai desain dan arsitektur sistem baru yang akan diterapkan.
00:30 [Budi] Tentu. Sistem baru yang kami rencanakan dirancang untuk memanfaatkan infrastruktur cloud computing yang canggih, dengan lapisan keamanan yang ditingkatkan dan mekanisme redundansi yang kuat untuk memastikan kehandalan operasional.
00:45 [Budi] Keuntungan utama dari implementasi ini adalah efisiensi yang ditingkatkan melalui penggunaan sumber daya yang terelastis dan skalabilitas yang dapat disesuaikan dengan kebutuhan produksi, serta integrasi yang lebih mulus dengan sistem yang ada.
01:05 [Agus] Terima kasih, Pak Budi, penjelasan yang sangat komprehensif.
01:10 [Agus] Apakah ada pertanyaan lebih lanjut seputar infrastruktur atau aspek teknis lainnya?
01:15 [Cici] Saya ingin memahami lebih dalam tentang strategi yang akan diterapkan dalam memitigasi risiko dan menangani potensi kendala selama proses migrasi.
01:30 [Budi] Tentu. Kami telah merancang rencana mitigasi risiko yang komprehensif, termasuk uji coba terperinci, pemulihan bencana, dan perencanaan kebalikan. Selain itu, kami juga memiliki tim respons yang siap tanggap untuk menangani kendala yang mungkin muncul secara proaktif.
01:45 [Agus] Pertanyaan yang sangat relevan, Cici. Terima kasih atas kecerdasan dalam mempertanyakan hal tersebut.
01:50 [Agus] Apakah ada pertimbangan tambahan atau pemikiran lain sebelum kita lanjut ke tahap selanjutnya?
01:55 [Dedi] Saya mendukung implementasi sistem baru ini, namun saya ingin menyarankan agar ada evaluasi rutin untuk memastikan bahwa performa sistem tetap optimal dan sesuai dengan harapan.
02:00 [Agus] Saya setuju dengan saran tersebut. Evaluasi rutin akan menjadi bagian penting dari siklus pengembangan dan perbaikan berkelanjutan.
02:05 [Agus] Baiklah, dengan dukungan dari semua pihak, saya rasa kita sudah cukup untuk tahap diskusi saat ini. Terima kasih atas kontribusi dan pemikiran yang sangat berharga dari masing-masing dari Anda.
02:10 [Agus] Pak Budi, saya harap Anda dapat mengoordinasikan dengan tim IT untuk memulai tahap migrasi data yang telah direncanakan dengan cermat.
```


<img width="1722" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/20800128/5d713ad5-cc02-43fe-95ea-7cd001bacbfb">


**Exercise:** 
```
10:00 [Rina] Selamat pagi, semuanya. Terima kasih telah bergabung dalam pertemuan strategis HR hari ini, tanggal 13 Mei 2024. Kita akan mulai dengan membahas rencana pengembangan karyawan untuk tahun ini.
10:05 [Rina] Pertama-tama, saya ingin menyampaikan bahwa target kita tahun ini adalah meningkatkan tingkat retensi karyawan sebesar 15% dari tahun sebelumnya.
10:10 [Rina] Untuk mencapai target tersebut, kami telah merancang program pelatihan dan pengembangan yang lebih terstruktur dan menyeluruh.
10:15 [Rina] Pak Joko, bisakah Anda memberikan gambaran singkat mengenai program pelatihan yang direncanakan?
10:20 [Joko] Tentu, Rina. Kami merencanakan program pelatihan yang terdiri dari serangkaian kursus online dan pelatihan langsung yang disesuaikan dengan kebutuhan karyawan di setiap departemen.
10:25 [Joko] Selain itu, kami juga akan mengadakan sesi mentoring dan coaching untuk membantu karyawan dalam pengembangan keterampilan spesifik dan pencapaian tujuan karir mereka.
10:30 [Rina] Terima kasih, Pak Joko, rencana tersebut terdengar sangat komprehensif.
10:35 [Rina] Ada pertanyaan atau saran lain terkait program pelatihan dan pengembangan?
10:40 [Santi] Saya ingin menyarankan agar ada mekanisme evaluasi yang jelas untuk mengukur efektivitas program pelatihan tersebut. Bagaimana rencana evaluasinya?
10:45 [Joko] Kami telah merencanakan survei kepuasan peserta setelah setiap sesi pelatihan, serta melakukan evaluasi kinerja sebelum dan sesudah pelatihan untuk mengukur peningkatan kinerja yang terkait.
10:50 [Rina] Pertimbangan yang bagus, Santi. Evaluasi akan menjadi kunci untuk memastikan program pelatihan kita berjalan dengan baik.
10:55 [Rina] Ada saran atau pertimbangan lain sebelum kita lanjut ke langkah berikutnya?
11:00 [Budi] Saya ingin menyarankan agar kita juga mempertimbangkan program penghargaan dan insentif untuk mengapresiasi partisipasi dan pencapaian karyawan dalam program pelatihan ini.
11:05 [Rina] Saya setuju dengan saran tersebut, Budi. Program penghargaan akan menjadi motivasi tambahan bagi karyawan untuk mengambil bagian aktif dalam pengembangan mereka.
11:10 [Rina] Dengan adanya dukungan dari semua pihak, saya rasa kita sudah siap untuk melangkah ke tahap implementasi. Terima kasih atas kontribusi dan ide-ide yang sangat berharga dari masing-masing dari Anda.
11:15 [Rina] Pak Joko, tolong koordinasikan dengan tim pelatihan untuk memulai implementasi program pengembangan karyawan sesuai dengan rencana yang telah disusun.
```
