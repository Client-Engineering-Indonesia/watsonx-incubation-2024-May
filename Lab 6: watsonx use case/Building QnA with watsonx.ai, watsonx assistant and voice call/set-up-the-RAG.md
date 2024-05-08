# Connect Watson Discovery, watsonx Assistant and watsonx.ai to create a RAG application.

## Introduction
Now, let’s combine all of the 3: Watson Discovery, watsonx assistant, dan watsonx.ai This will give you full functionality of RAG. The answer will be engaging enough crafted by LLM model with information provided by Watson Discovery.

<img width="486" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/f2a7ce0f-2075-4e05-931a-5818f47b6b38">

## Setup the RAG
### 1. Setup the integration
Buka kembali laman utama dari watsonx assistant dan pilih integrations

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/c95d75bd-aac1-4af1-ad7e-d833cf13c497">

Pilih _Build custom extension_

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/9593fac6-517d-4383-9e5b-e90653065f18">

Klik _Next_

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/04320d65-b30b-4b1e-9ff1-c8cdd38e6267">

Isi _Basic Information_ yang dibutuhkan

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/c095073b-b46d-447c-b050-40f808dc05a5">

### 2. Prepare the OAS (Open API Specification)

OAS yang akan digunakan telah kami berikan pada folder "Lab - Enterprise RAG with watsonx Platform" terdapat OAS dengan nama _wx_oas.json_ dan _watson-discovery-query-openapi.json_

_OAS defines a standard, language-agnostic interface to HTTP APIs which allows both humans and computers to discover and understand the capabilities of the service without access to source code, documentation, or through network traffic inspection. You need to provide OAS as a JSON file format. This will describe the API structure you have and help the Watson assistant to send a request and represent the received response._

<img width="1166" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/bba0df1f-5af7-4b64-a476-864745175c27">

### 3. Create watsonx.AI dan Discovery Extension

Kita akan membuat dua ekstension, proses akan dilakukan secara iteratif. Pertama isikan nama _Retrieval WD_. Lalu, _Drag and Drop watson-discovery-query-openapi.json_.

<img width="234" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/66d367c7-9d59-469b-8c4d-d0eb49715a93">

<img width="232" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/230286af-e291-4b48-aced-04d888506dca">

Review ekstension yang telah dibuat

<img width="261" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/b409e967-b1e8-484c-b5bb-e2278350b112">

### 4. Add the created extension

<img width="96" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/b9d2ba00-2e6c-4f55-8e3c-6dc36c2883a7">
<img width="169" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/04b4cd76-7acb-496c-ac85-27843c92215f">

### 5. Setup the extension

Atur Authenthication setelah klik _Next_ dari _Get Started_
```
Authentication: Basic Auth
Username: apikey
Password: <your_api_key> 
Server: <discovery_URL without https://>
```

Anda dapat memilih API dari watson Discovery pada step pertama.

<img width="245" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/8ce8eaac-99c7-4ed5-8e3f-a2e6b7b85d78">

### 6. Click Finish to complete the Custom Extension creation and Do the same process for watsonx.AI's extension

<img width="245" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/c3085466-c847-4877-b4cd-ef8e6ec185e9">

Gunakan Informasi yang ada dibawah ini untuk membuat _extension_ watsonx.AI

```
A. Extension name: Generation WX
B. Authentication type: Oauth 2.0
C. Grant type: Custon apikey
D. Apikey: <IAM_APIKEY>
E. Client Authentication: Send as Body
F. Header prefix: Bearer
G. Servers: <your_wx.ai_region>
```

<img width="241" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/e93ea81a-b8e1-47f5-a0a7-2d35ac64c4bb">

Terakhir Klik Finish

<img width="254" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/db72587a-7858-4c1d-a166-183c9817fe68">

Untuk mendapatkan IAM_APIKEY anda dapat mengikuti step berikut:

```
A._IBM Cloud and Select Manage_
B. _Access IAM_
C. _API Keys and click ”Create”._
D. _Download or Copy your API Keys_
```

### 7. Re-create the action flow. 

Setelah selesai membuat _extension_ buka kembali action dan pilih flow yang sebelumnya telah dibuat. Apabila sebelumnya kita menggunakan _search extension_ kali ini kita akan menggunakan _Retrieval WD_ dan _Generation WX_. Saat memilih _User Response_ pilih _Use an Extension_.

<img width="177" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/04d9f9e0-a1f1-47e8-87cf-7fc0a3a15862">

### 8. _Use Retrieval WD Extension_

<img width="162" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/cfed900a-88fc-4939-91cd-69608606b99b">

Isikan informasi yang diminta untuk dapat menggunakan _extension_ Retrieval WD
```
project_id: <your-WD-project-id>
version: 2022-08-01
```

Buka kembali laman Watson Discovery dan klik _integrate and deploy_. Copy _Project ID_ yang anda temukan

<img width="239" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/ed12c7f6-e172-41f0-aa57-0f380f40e3b4">

Isikan informasi yang anda dapatkan ke _field_ berikut:

<img width="239" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/eae9fc69-5710-4423-a7ea-1a48920058cb">

Selain parameter utama, terdapat beberapa parameter tambahan yang bisa anda gunakan untuk meningkatkan performa dari _searching method_ yang kita gunakan:

```
count: 3
return: ["title","metadata.source.url"]
similar.fields: ["text"]
passages.enabled: True
passages.characters: 500
passages.find_answers: True
table_results.enabled: False
natural_language_query: $user_question
```

<img width="180" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/7535c541-32a6-4296-8417-f7efa1cdfa76">

### 9. Create Session Variable to store the result

<img width="170" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/c3b4cf41-0435-4c68-8b95-a4df017b8323">

Buat parameter baru dengan nama _"retrieval_result"_ dengan tipe data _"Any"_

<img width="433" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/158cf4fc-4374-4587-a7b2-e0a9e064903a">

Set nilai parameternya sebagai _$body.result[0].passage_text_ dengan menggunakan _expression_ tersebut. Kita dapat menggunakan hasil dari _searching_ yang dilakukan untuk proses selanjutnya.

### 10. Preview Result 

<img width="185" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/57bd514a-cca2-455e-8e4b-691aab6d2355">

Apabila anda telah mencapai tahap ini, seharusnya anda telah mampu melakukan query informasi dari watson discovery, anda dapat klik _preview result_. 

### 11. Applying watsonx.AI Extension

<img width="324" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/1e7cbfc0-d843-44c0-9f83-85e113760e30">

Klik _New Step_ dan pilih kembali _Use an Extension_ lalu pilih extension watsonx.AI. Terdapat beberapa parameter yang dapat diisikan sebagai berikut:
```
model_id: meta-llama/llama-2-70b-chat
project_id: <your-watsonx.ai-project-id>
parameters.max_new_tokens: 300
parameters.min_new_tokens: 1
version: 2023-05-29
```
<img width="201" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/06510687-a05d-4d2d-9dc2-aa42471ac5e0">

Informasi _Project ID_ dapat ditemukan pada _watsonx.ai project >> Manage >> General_

### 12. Fill in the input field.

<img width="410" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/fde7f57d-240a-44a0-8fd6-d7eada7da82b">

Dalam pendifinisiaan saat ini, kita mendefinisikan parameter _Input_ sebagai prompt yang akan digunakan untuk mendapatkan jawaban yang kita inginkan.
Terdapat tiga paramter yang perlu diperhatikan:
```
retrieval_result: hasil dari watson Discovery
user_question: pertanyaan yang diajukan user
Session History: Riwayat percakapan sebelumya pada session yang sama
```
<img width="410" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/f0713475-582c-4ad7-8154-3c8ab0c001b1">

selain itu terdapat parameter _input_ yang akan diisikan dengan prompt yang kita gunakan. Anda dapat menggunakan prompt berikut dan copy kedalam field _input_ yang anda gunakan.
```
("Anda adalah asisten yang membantu, sopan, dan jujur. Selalu jawab sebisa mungkin dengan cara yang membantu, sambil tetap aman. Jawaban Anda tidak boleh mengandung konten yang berbahaya, tidak etis, rasialis, seksis, beracun, berbahaya, atau ilegal. Pastikan bahwa respons Anda bersifat sosial tidak memihak dan positif. \nKonteks:").concat($retrieval_result).concat("\nPertanyaan:").concat($user_question).concat("\nChat history:").concat("$Session history").concat("\nHarap pahami konteksnya dan jawablah pertanyaan berdasarkan informasi yang diberikan. Identifikasi dan ekstrak URL yang disebutkan dalam konteks jika berkaitan dengan pertanyaan. Jangan sertakan URL yang tidak berhubungan dalam jawaban Anda. Berikan jawaban secara berurutan jika diperlukan atau berikan daftar yang jelas dan ringkas. Jika suatu pertanyaan tidak masuk akal atau tidak koheren secara faktual, jelaskan mengapa daripada menjawab sesuatu yang tidak benar. Jika Anda tidak tahu jawaban atas suatu pertanyaan, tolong jangan memberikan informasi palsu. Jika konteks atau history chat tidak ada hubungan dengan pertanyaan, jawab saja tidak tahu. \nJawaban:")
```

### 13. Generate the Watsonx.AI result

<img width="354" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/cfbe6893-7576-4f05-a456-f1f45d429e17">

Selanjutnya, klik _New Step_ dan buat _Session Variable_ baru dengan nama _generation_result_ dengan tipe data _Any_ 

<img width="392" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/58b8c1e8-f3d0-42f1-ad7b-94ee704a097c">

Definisikan variable tersebut menggunakan syntax berikut:
```
body.result[0].generated_text.
````

### 14. Compare the result

Klik _Preview_ dan tanyakan pertanyaan berikut: "”tata cara pembukaan digital branch?” Anda dapat membandingkan hasil yang didapatkan sebagai berikut:

<img width="148" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/0a99669f-0414-42dc-af69-a5f02a9bf5fd">

Pertanyaan yang diajukan

<img width="148" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/56ddf56e-4d6c-4893-96af-66e5f6341f2e">

Hasul dari watson Discovery

<img width="145" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/ddad374d-95e1-4a96-8459-59a9ed0dce0e">

Hasil dengan watsonx.AI

### 15. Remove Answer dari watson Discovery

<img width="401" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/47d48737-7fce-4b92-91ac-b8dbdb286845">

Apabila anda telah yakin bahwa hasil dari Discoery dan AI telah sama dan ter-generate. Anda dapat merapihkan output dari watsonx Assistant dengan menghapus hasil original dari watson discovery. Klik tombol delete (_Trash Bin_) yang terdapat pada _Action step_ yang ingin anda hapus.

### 16. Re-Ask Previous Step

<img width="209" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/95057c76-48e0-417b-b2cf-0cfecf1f1666">

Lakukan proses berikut agar setelah anda menanyakan pertanyaan dan watson assistant mengeluarkan hasil, kita dapat menanyakan pertanyaan lainnya. 

### 17. Preview Result. 
















































