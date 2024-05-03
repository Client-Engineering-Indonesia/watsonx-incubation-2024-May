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


























