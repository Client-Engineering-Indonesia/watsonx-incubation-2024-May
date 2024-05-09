# watson Discovery Set-Up Process

## Introduction
_Watson Discovery is an award-winning AI-powered intelligent search and text-analytics platform that eliminates data silos and retrieves information buried inside enterprise data. It uses innovative, market-leading natural language processing (NLP) to uncover meaningful business insights from documents, webpages, and big data. Watson Discovery makes it possible to rapidly build cognitive, cloud-based exploration applications that unlock actionable insights hidden in unstructured data including your own proprietary data, as well as public and third-party data._

## Uploading Document Process
### 1. Launch Watson Discovery
Klik _"Launch Watson Discovery"_ untuk mulai membuat projek

<img width="521" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/8d2865ec-a29e-444f-a105-7de3e45d2257">

_Notes:_

_API key and URL information:_ _Credentials_ digunakan untuk menghubungkan Watson Discovery ke service atau aplikasi lain. 

_Plan of Watson Discovery:_ Terdapat paket _Plus, Enterprise, Premium Plan_. Informsi lebih lanjut dapat ditemukan pada [Pricing Watson Discovery](https://www.ibm.com/products/watson-discovery/pricing)

### 2. Build your First Project
Terdapat Project dan Collections pada Watson Discovery yang dapat digunakan untuk mengatur utilisasi Dokumen yang kita miliki. Untuk memulai proses anda dapat klik "New Project"

<img width="570" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/32fa4387-3bb6-4a02-818a-66e0f47f5e49">

_Notes:_

_Sample Project_: Project ini telah otomatis dibuat oleh sistem dan dapat digunakan untuk melakukan ekplorasi kapabilitas watson Discovery

### 3. Creating a new project
Setelah Klik New Project anda akan diminta untuk mengisikan nama projek dan tipe projek anda dalam menggunakan watson discovery 

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/9fd0da8b-9be8-4a65-9064-331203c79e82">


### 4. Create a new collectionto Upload Document
A. Untuk memulai proses upload data, anda akan diminta untuk membuat _collection_ baru.

B. Berikan _collection name_ dan pilih bahasa yang akan digunakan

C. Upload file yang akan digunakan dengan sesederhana _drag and drop file_

D. Klik Finish

<img width="172" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/943966d4-a5bf-44b3-aa02-23d179a8da8b">

E. Selain _upload file via local_ terdapat beberapa opsi untuk _upload file_. Klik _here_ pada _Need to connect to data source_. Selain itu terdapat beberapa opsi _data preprocessing_ lain seperti OCR dan Stemming

<img width="184" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/0bb7d185-8091-4e98-af0a-0a85d94c0e5e">

<img width="275" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/e4307f7e-ae11-4367-99e6-8e72b3f605b5">

### 5. Click on Improve and customize
Jika anda memilih opsi _conversation search_ sebagai _project type_, watson discovery akan memprovide chatbot internal untuk melakukan tanya jawab dari dokumen. 

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/5b393765-8e71-4570-ac45-3e90219e7af5">

_Notes:_

_Improvement tools_: Tools ini dapat digunakan untuk meningkatkan result dari watson discovery. Buka link [berikut](https://cloud.ibm.com/docs/discovery-data?topic=discovery-data-improvements) untuk mempelajari lebih lanjut. 

### 6. Manage collections

Apabila anda berpindah ke _navigation menu_. Anda dapat memilih _manage colletion_ untuk melihat daftar _collection_ yang sebelumnya telah dibuat. 

<img width="123" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/908fa328-cd33-4f08-b065-91a32bb05332">
<img width="401" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/f446b996-3267-42bf-aa3e-ba1f5245fdef">

Klik _preview data_ maka anda dapat melihat dokumen yang telah diupload

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/c2f9ff71-732c-4e17-8a36-faef8d12b278">

### 7. Add More Collection

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/b209a233-16c7-4f0c-93d0-74b1d4441786">

Anda dapat menggunakan dokumen berikut ini untuk anda upload, ikutin proses yang sama seperti sebelumnya. 

## Additional Feature of watson Discovery
### OCR 

Selain dapat mengambil informasi dari PDF atau Docx file, watson discovery juga memiliki kapabilitas untuk mengupload file text yang berupa image dan dapat di OCR kan langsung.
#### 1. Buat Collection Baru dan Upload Document Anda

Pastikan untuk menyalakan fitur OCR ketika anda akan mengupload document anda

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/1901d1ea-46a3-4259-bd4d-bdebabb0a1e4">

#### 2. Klik Finisih lalu pergi ke Manage and Collection

Tunggu saat hingga Document Processing selesai.

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/0168ade6-4be0-47f9-8be3-0b8e55077a89">

Klik Preview data sesuai dengan nama project yang telah dibuat, dan bisa terlihat hasilnya. Anda akan melihat bahwa hasilnya telah menjadi text yang bisa anda preprocess lebih lanjut.

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/ca8aa53b-0e93-40e7-b65f-f4d8b63237ef">

### Webcrawling

Salah satu fitur lain yang dimiliki oleh watson Discovery adalah crawling data dari website tertentu.
#### 1. Buat Collection baru

Isi kan nama collection anda, lalu klik "Need to connect to a data source? Click here."

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/74fc041b-8568-4fa9-8006-5df848a08e1a">

#### 2. Pilih Web Crawl

Terdapat beberapa opsi yang disediakan oleh watson Discovery, untuk saat ini kita akan gunakan opsi webcrawl.

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/1b8237e3-3bab-4f91-978d-a319cac34a5a">

#### 3. Fill in the information needed

Anda perlu untuk menspesifikasi intensitas crawling serta website yang anda akan jadikan source crawling

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/1b462097-1f59-4771-bc13-81bac0fdf354">

Selain itu, anda dapat melakukan crawling ke lebih dari satu website

<img width="467" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/e246ce0e-59c2-4272-bacd-82659dea0986">

Terakhir Klik Finisih dan tunggu proses selesai. 

### Smart Document Understanding

Dalam proses untuk memahami dokumen, terkadang di setiap halamannya akan terdapat beberapa field, seperti header, sub header, text, dan halaman. Tetapi ketika kita coba membaca dokumen langsung dari pdf informasi tersebut tidak dapat kita ekstrak. Dengan menggunakan SDU kita dapat melakukan pendefinisian field pada beberapa halaman yang selanjutnya secara otomatis akan terefleksikan pada seluruh halaman yang ada.


<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/954408ec-417a-4c4c-91fc-c0efea0bf3bb">

Pilih use your trained model

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/bcd02238-a861-4878-81c8-bcdd9516ae76">

<img width="1728" alt="image" src="https://github.com/Client-Engineering-Indonesia/watsonx-incubation-2/assets/105551267/e6179a80-3d54-438f-88dd-775ed563fe49">

Lalu anda dapat melihat tampilan berikut, pilih field labels yang berada pada toggle paling kanan. Pilih field tertentu lalu tandai field tersebut pada dokumen anda, klik submit page. Lakukan pengulan proses tersebut pada beberapa lembar file. Lalu diakhir anda akan melihat bahwa semua halaman telah teridentifikasi.




























