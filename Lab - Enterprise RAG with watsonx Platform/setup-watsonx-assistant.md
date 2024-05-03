# Setup watsonx Assistant

### 1. Log in ke halaman watsonx Assistant anda
Ketika membuka source watsonx assistant pertama kali. Anda akan diarahkan kepada laman berikut, isi nama bot sesuai dengan kebutuhan anda. Berikan deskripsi apabila diperlukan dan pilih Assistant language dengan _“Another Language”_
<img width="486" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/b67ee118-2614-495a-bef4-2fbfeab198dc">

### 2. Melakukan Konfigurasi kepada watsonx Assistant
Anda dapat mengonfigurasi pilihan opsi yang tersedia, mulai dari tempat assistant akan digunakan hingga kebutuhan anda dalam menggunakan watsonx assistant!

<img width="446" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/80d93982-fd75-4b3b-b633-e3efbbbcb9a8">

### 3. Melakukan Kostumasi Tampilan watsonx assistant
Anda juga dapat melakukan kostumisasi untuk tampilan watsonx assistant anda, seperti berikut ini, klik next dan klik create untuk membuat Watson assistant anda. 

<img width="521" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/97c4a595-193b-4a5e-835f-7998f69a185c">

**Untuk melanjutkan proses anda harus melakukan konfigurasi di watso discovery terlebih dahulu klik link berikut [Set Up Watson Discovery](https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/blob/main/Lab%20-%20Enterprise%20RAG%20with%20watsonx%20Platform/setup-watson-discovery.md)**

### 4. Set Up Conversation Flow pada watsonx Assistant
Apabila anda telah melakukan set up flow pada watson Discovery, anda dapat melanjutkan proses pada watson assistant anda.
Pilih menu _action_ sebagai _conversation flow_ yang akan dibuat untuk user anda. 

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/84a7798e-daf8-4240-90c9-6ea68f6a0d99">

### 5. Build your action from scratch!

Untuk membuat _conversation flow_ anda dapat memilih opsi _start from scratch or find existing_ template dari _Quick start with templates_

<img width="280" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/7d7b5981-9396-4c41-b6b6-d559a85e8c95">

### 6. Name your action!

Anda dapat menamakan _action_ berdasarkan topik pembicaraan atau berdasarkan frasa yang sering diungkapkan oleh user. Kata kata tidak perlu spesifik sama persis. Misalnya: bertanya, menanyakan, ingin tahun.

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/bb8b94f9-8f70-4e73-b296-f93d2c834ee4">

### 7. Add the response into “Assistant says”

Ketika user mengatakan: 
“Saya ingin bertanya” atau kalimat lainnya yang dibutuhkan.
Asisten lalu akan mengatakan : “apa yang ingin anda tanyakan?”

<img width="298" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/568abe42-9fcd-4383-99e2-21d206cf01d3">

### 8. Define the customer response.

Anda dapat mendefiniskan _customer response_ dalam beberapa tipe, salah satunya adalah _”free text”_

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/1ca590ba-a0e7-4765-b4cf-ece32ea007e8">

Click_ “Continue to next step”_

Lalu buat step percakapan baru dengan klik _“New step”_

<img width="66" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/1d8755a1-74b3-4b49-ac7c-18f56eafb2bc">


### 9. Create step 2

Tujuan dari tahap ini untuk menyimpan response yang telah diberikan oleh user sebagai _session variable_ yang nantinya dapat digunakan kembali. Klik _Set Variable values_ lalu klik _set new values_. Pada tombol drop down click _New session variable_

<img width="247" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/c327344f-aef2-4ecf-a4c6-c2ebae7ec9c9">

### 10. Create a new Session variable!

Pada opsi _session variable_. Tambahkan _user_question_ sebagai _variable name_ lalu set tipe data menjadi _Any_. Selanjutnya klik _apply_

<img width="188" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/d1b55ff6-a957-45c3-9f24-d60715cb7d43">

### 11. Set user_question values.

Set nilai _user_question_ menjadi _”Action step variable”_ dari (1. apa yang ingin anda tanyakan)”

<img width="210" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/39436bc9-b29b-4ec2-a317-1c4f77c1ea0f">

<img width="162" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/d0d4c9a2-ea4b-46e0-bbcd-6438d971faa8">

### 12. Set the response into _”Search for the Answer”_

Search for the answer untuk menghubungkan flow conversation dengan _searching capabilities_ seperti Watson Discovery dan Elastic Search. Klik dan Klik _edit settings_

<img width="315" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/90e40850-4518-40c8-b57d-da8811cfab9e">

### 13. Add user_query as input of the Search for the answer.

Pada _custom query part_ tambahkan tanda "$" dan pilih _user_question_. Hal ini berarti maka _user_question_ akan menjadi _keywords_ untuk mencari informasi dari _content storage_

<img width="210" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/b3a2f2f0-4c84-4f39-9f15-d7a2d3ad7fd5">

<img width="185" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/690c31e4-5b23-430b-948b-1f3e8824f5e4">

### 14. Add step 3

Klik kembali _new step_ dan pilih _Re-ask previous step(s)_ and pilih from step _1. Click Apply_

<img width="272" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/1aedc81e-8bb1-44ac-a0d4-1d38bc8a209d">
<img width="218" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/a4d81c11-c81f-47fd-80f9-216a897ce2d8">

Jangan lupa untuk selalu _clik save_ setiap selesai membuat flow atau melakukan pembaharuan atau sebelum berpindah flow.

<img width="100" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/d71ad2ea-2d4e-4309-8823-747e57cb9c0e">

### 15. Select the Environments

Select _Environments_ pastikan anda ada di model _draft_. Karena terdapat 2 _environment_ yakni _draft & live_

<img width="359" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/02d3e5ab-ba91-480e-bb25-1f283923efbc">

### 16. Add Search Extension

Untuk menambahkan _search capabilities_ ke Watson Assistant klik _“Add +”_

<img width="208" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/913ac9d7-9ca5-44b3-a84e-864ddc2d4422">

### 17. Select the Project

Setelah memilih watson discovery, pilih instance Discovery untuk dapat terhubung dengan watson discovery project yang telah kita buat sebelumnya.

<img width="472" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/6a196ad7-c3a2-49cf-9ba9-a9ba93046383">

### 18. Configure the Search Integration

Pilih Title dan Body dan sesuaikan result quantity ke angka 3. Lalu Save

<img width="419" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/fc2d5947-c73c-4860-9794-2cb3bf759ea5">

### 19. Re-visit the Action

Lalu tanyakan hal berikut ke bot anda

Bot: Welcome, how can I assist you?

User: Saya mau tanya

Bot: Apa yang ingin anda tanyakan?

User: perlindungan data pribadi

Bot: Berikut informasi yang saya temukan di content store …

<img width="157" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/a3f97ff8-13c9-4fbd-b95e-0523f996ae9c">















































