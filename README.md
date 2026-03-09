# Multi-Service API Hub

A unified backend platform built with **FastAPI** that integrates multiple external public APIs into a single service.
This project demonstrates API integration, modular backend architecture, caching strategies, and REST API design.

The platform aggregates several services such as **weather information, movie search, GitHub repository analytics, news headlines, cryptocurrency prices, currency conversion, holiday calendars, quotes, and IP geolocation**.

---

# 🚀 Features

* Modular FastAPI backend architecture
* Integration with multiple public APIs
* Automatic API documentation with Swagger
* Caching for performance optimization
* Clean service layer separation
* RESTful API design
* Easy to extend with new services

---

# 🏗 Project Architecture

The project follows a **layered architecture** separating routing logic from business logic.

```
Client
  ↓
Routes (API Endpoints)
  ↓
Service Layer (Business Logic)
  ↓
External APIs
```

---

# 📁 Project Structure

```
app/
│
├── main.py
│
├── routes/
│   ├── weather.py
│   ├── github.py
│   ├── movies.py
│   ├── news.py
│   ├── currency.py
│   ├── holidays.py
│   ├── crypto.py
│   ├── quotes.py
│   └── geo.py
│
└── services/
    ├── weather_service.py
    ├── github_service.py
    ├── movie_service.py
    ├── news_service.py
    ├── currency_service.py
    ├── holiday_service.py
    ├── crypto_service.py
    ├── quote_service.py
    └── geo_service.py
```

---

# 📡 API Endpoints

| Endpoint                     | Description                           |
| ---------------------------- | ------------------------------------- |
| `/weather/{city}`            | Get weather information for a city    |
| `/movies`                    | Search movies using OMDb API          |
| `/github/{owner}/{repo}`     | Get GitHub repository statistics      |
| `/news`                      | Fetch latest news headlines           |
| `/currency`                  | Convert currency values               |
| `/holidays/{country}/{year}` | Get public holidays                   |
| `/crypto`                    | Get cryptocurrency prices             |
| `/quotes`                    | Fetch quote of the day                |
| `/geo/{ip}`                  | Get location details of an IP address |

---

# 🔧 Installation

Clone the repository

```
git clone https://github.com/PranitBijave27/multi-service-api-hub.git
cd multi-service-api-hub
```

Create virtual environment

```
python -m venv venv
```

Activate environment

Mac/Linux:

```
source venv/bin/activate
```

Windows:

```
venv\Scripts\activate
```

Install dependencies

```
pip install -r requirements.txt
```

---

# ▶ Running the Server

Start the FastAPI server using:

```
uvicorn app.main:app --reload
```

Server will start at:

```
http://127.0.0.1:8000
```

---

# 📖 API Documentation

FastAPI automatically generates API documentation.

Swagger UI:

```
http://127.0.0.1:8000/docs
```

ReDoc Documentation:

```
http://127.0.0.1:8000/redoc
```

These interfaces allow interactive testing of all API endpoints.

---

# ⚡ Technologies Used

* Python
* FastAPI
* Uvicorn
* Requests
* CacheTools

---

# 🌐 External APIs Used

This project integrates several public APIs:

* OpenWeatherMap (Weather Data)
* OMDb API (Movie Database)
* GitHub REST API (Repository Analytics)
* NewsAPI (Latest News Headlines)
* ExchangeRate API (Currency Conversion)
* Nager.Date API (Public Holidays)
* CoinGecko API (Cryptocurrency Prices)
* ZenQuotes API (Daily Quotes)
* ip-api (IP Geolocation)

---

# 📊 Example Root Endpoint

Request:

```
GET /
```

Response:

```json
{
  "status": "Online",
  "message": "Welcome to the Multi-Service API Hub",
  "total_services": 9,
  "endpoints": [
    "/weather",
    "/movies",
    "/github",
    "/news",
    "/currency",
    "/holidays",
    "/crypto",
    "/quotes",
    "/geo"
  ]
}
```
# 👨‍💻 Author

Pranit
Engineering Student | Backend Developer
