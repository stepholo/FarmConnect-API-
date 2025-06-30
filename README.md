# 🌱 FarmConnect API + Climate Insights

A scalable backend platform built to empower smallholder farmers with climate-smart tools, local marketplace access, and crop decision support.

This project was developed as part of the **ALX ProDev Back-End Software Engineering Programme**, and integrates real-time weather insights with agriculture and commerce APIs to support rural and remote communities.

---

## 🚀 Features

### 👤 User Management
- JWT-based authentication
- Role-based access: Farmer, Agronomist, Admin
- Profile update and account management

### 🌾 Farmer Module
- Farm profile creation (name, size, location)
- Crop selection & tracking
- Geolocation-based support

### 🌦 Climate Insights
- Real-time & 7-day forecasts (OpenWeatherMap)
- Historical data (NASA POWER)
- Crop-specific climate recommendations
- Risk scoring (e.g., drought alerts)

### 🛒 Marketplace
- List produce with price, harvest date, quantity
- Browse or search for available products
- Admin approval system for listings

### 🔔 Notifications
- SMS/Email alerts using Celery + Redis
- Custom alerts for weather changes, planting times, and crop sales

---

## 🛠️ Tech Stack

| Area            | Tool                          |
|-----------------|-------------------------------|
| Language        | Python 3.x                    |
| Framework       | Django, Django REST Framework |
| Database        | PostgreSQL                    |
| Auth            | JWT (SimpleJWT)               |
| APIs            | OpenWeatherMap, NASA POWER    |
| Background Jobs | Celery + Redis                |
| Docs            | Swagger (drf-yasg)            |
| DevOps          | Docker, .env, GitHub Actions  |

---

## 📁 Project Structure

```bash
farmconnect/
├── climate/ # Weather data integration
├── core/ # Shared utils and settings
├── farmers/ # Farmer profiles & crop tracking
├── marketplace/ # Produce listings
├── notifications/ # Alerts & background tasks
├── users/ # Registration, login, profiles
├── farmconnect/ # Django project settings
├── .env # Environment variables
├── requirements.txt # Dependencies
├── Dockerfile # Docker config
├── manage.py
└── README.md
```
---

## 📦 Installation & Setup

```bash
# Clone the repo
git clone https://github.com/stephelo/farmconnect-api.git
cd farmconnect-api

# Create and activate virtualenv
python3 -m venv env
source env/bin/activate

# Install dependencies
pip install -r requirements.txt

# Configure .env and run migrations
cp .env.example .env
python manage.py migrate

# Run the server
python manage.py runserver
```
---

## 🔐 Authentication

- All secure endpoints require a JWT token.
- Include Authorization: Bearer <token> in headers.
- Use:

```http
POST /api/login/
POST /api/register/
```
---

## 🧪 Testing

```bash
# Run tests
python manage.py test
```

## 📄 API Documentation
- Swagger UI available at /swagger/
- Postman collection coming soon
---

## 🌍 Deployment
- Planned deployment options:
    - Render
    - Railway
    - Docker support included
---

## 💡 Project Status
- 🔄 In development
- 👨‍💻 Solo developer
- 🎓 ALX ProDev Back-End Capstone Project
---

## 📧 Contact
- Built by Stephen Oloo
- Connect on [LinkedIn](www.linkedin.com/in/stepholo0)
- Email: [Stephen Oloo](oloobrian89@gmail.com)
---

## 🏁 License
- This project is licensed under the MIT License.