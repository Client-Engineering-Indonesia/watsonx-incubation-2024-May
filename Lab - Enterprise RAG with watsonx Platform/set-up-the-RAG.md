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

OAS yang akan digunakan telah kami berikan pada folder "Lab - Enterprise RAG with watsonx Platform" terdapat OAS dengan nama _wx_oas.json_ dan _discovery.json_

_OAS defines a standard, language-agnostic interface to HTTP APIs which allows both humans and computers to discover and understand the capabilities of the service without access to source code, documentation, or through network traffic inspection. You need to provide OAS as a JSON file format. This will describe the API structure you have and help the Watson assistant to send a request and represent the received response._

<img width="1166" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/bba0df1f-5af7-4b64-a476-864745175c27">

### 3. Create watsonx.AI dan Discovery Extension

Kita akan membuat dua ekstension, proses akan dilakukan secara iteratif. Pertama isikan nama watsonxAI. Lalu, _Drag and Drop wx_oas.json_.

<img width="234" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/66d367c7-9d59-469b-8c4d-d0eb49715a93">

<img width="232" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/230286af-e291-4b48-aced-04d888506dca">

Review ekstension yang telah dibuat

<img width="261" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/b409e967-b1e8-484c-b5bb-e2278350b112">












