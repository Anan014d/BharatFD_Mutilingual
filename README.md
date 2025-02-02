# 🚀 Multilingual FAQ System

A **Django-based** FAQ system with **multilingual support, WYSIWYG editor, caching, and Dockerized deployment**. Supports **English, Hindi, and Bengali** with automatic translations via **Google Translate API**.

---

## 🌟 Features

✅ **Multilingual FAQs** (English, Hindi, Bengali)  
✅ **WYSIWYG Editor** for rich-text FAQ answers  
✅ **REST API** with language selection support  
✅ **Redis Caching** for optimized performance  
✅ **Google Translate API** for automated translations  
✅ **Dockerized Deployment** with PostgreSQL & Redis  
✅ **JWT Authentication** for secure API access  
✅ **Admin Dashboard** for easy FAQ management  
✅ **Swagger API Documentation** for better usability

---

## 🛠 Installation & Setup

### 📌 1. Clone the Repository

```bash
git clone https://github.com/AnandKasudhan/MultilingualFAQ
cd MultilingualFAQ
```

### 📌 2. Run the Project Using Docker

#### Option 1️⃣: Using docker-compose (Recommended)

```bash
docker-compose up --build
```

#### Option 2️⃣: Pull & Run Pre-Built Docker Image

```bash
docker pull anandkasudhan/faq-project:latest
docker run -p 8000:8000 anandkasudhan/faq-project
```

### 📌 3. Access the Application

#### API Endpoints

- **API Endpoint:** http://127.0.0.1:8000/api/faqs/
- **Django Admin Panel:** http://127.0.0.1:8000/admin/
- **Swagger API Docs:** http://127.0.0.1:8000/api/docs/

---

### 🔧 Usage

#### Add FAQs via Django Admin

1. Open: [Django Admin](http://127.0.0.1:8000/admin/)
2. Log in using admin credentials:
   - **Username:** admin
   - **Password:** admin123
3. Navigate to **FAQ Management** and add FAQs.

#### Access FAQs via API

➤ Fetch FAQs (Default: English)

```bash
curl http://127.0.0.1:8000/api/faqs/
```

➤ Fetch FAQs in Hindi

```bash
curl http://127.0.0.1:8000/api/faqs/?lang=hi
```

➤ Fetch FAQs in Bengali

```bash
curl http://127.0.0.1:8000/api/faqs/?lang=bn
```

---

### 🐳 Running with Docker

1️⃣ Ensure Docker and Docker Compose are installed.
2️⃣ Navigate to the project directory:

```bash
cd MultilingualFAQ
```

3️⃣ Build & start the containers:

```bash
docker-compose up --build -d
```

4️⃣ Apply database migrations:

```bash
docker-compose exec web python manage.py migrate
```

5️⃣ Create a superuser:

```bash
docker-compose exec web python manage.py createsuperuser
```

6️⃣ Check the logs if needed:

```bash
docker-compose logs -f
```

---

### 🧪 Running Tests

```bash
docker exec -it faq-app python manage.py test
```

---

## 👨‍💻 Author

Developed with ❤️ by **Anand Kasudhan**  
📧 Email: kasaudhananand2003@gmail.com  
🔗 LinkedIn: [Anand Kasudhan](https://www.linkedin.com/in/anandkasudhan/)
