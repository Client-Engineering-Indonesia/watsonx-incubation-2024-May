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
Authentication: Basic Auth
Username: apikey
Password: <your_api_key> 
Server: <discovery_URL without https://>

Anda dapat memilih API dari watson Discovery pada step pertama.

<img width="245" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/8ce8eaac-99c7-4ed5-8e3f-a2e6b7b85d78">

### 6. Click Finish to complete the Custom Extension creation and Do the same process for watsonx.AI's extension

<img width="245" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/c3085466-c847-4877-b4cd-ef8e6ec185e9">

Gunakan Informasi yang ada dibawah ini untuk membuat _extension_ watsonx.AI 
A. Extension name: Generation WX

B. Authentication type: Oauth 2.0

C. Grant type: Custon apikey

D. Apikey: <IAM_APIKEY>

E. Client Authentication: Send as Body

F. Header prefix: Bearer

G. Servers: <your_wx.ai_region>

<img width="241" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/e93ea81a-b8e1-47f5-a0a7-2d35ac64c4bb">

Terakhir Klik Finish

<img width="254" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/db72587a-7858-4c1d-a166-183c9817fe68">

Untuk mendapatkan IAM_APIKEY anda dapat mengikuti step berikut:
A._IBM Cloud and Select Manage_
B. _Access IAM_
C. _API Keys and click ”Create”._
D. _Download or Copy your API Keys_

### 7. Re-create the action flow. 

Setelah selesai membuat _extension_ buka kembali action dan pilih flow yang sebelumnya telah dibuat. Apabila sebelumnya kita menggunakan _search extension_ kali ini kita akan menggunakan _Retrieval WD_ dan _Generation WX_. Saat memilih _User Response_ pilih _Use an Extension_.
<img width="177" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/04d9f9e0-a1f1-47e8-87cf-7fc0a3a15862">




























