
# Weather API Dockerized Project

This project is a full-stack Dockerized weather application featuring:
- A **Flask API backend** that retrieves weather data from OpenWeatherMap.
- A simple **frontend** served via a lightweight HTTP server.
- Managed via **Docker Compose** for easy deployment.

---

## 🌐 Features

- Retrieve weather information by city name.
- Environment-configurable OpenWeatherMap API key.
- Fully containerized for local development and production environments.

---

## 🗂️ Project Structure

```
weather_api_dockerized_final_fixed/
├── .env                      # Environment variables (API key, etc.)
├── docker-compose.yml        # Defines multi-container setup
├── flask_app/
│   ├── app.py                # Flask backend
│   ├── Dockerfile            # Dockerfile for Flask app
│   └── requirements.txt      # Python dependencies
└── frontend/
    ├── Dockerfile            # Dockerfile for frontend (basic HTTP server)
    └── index.html            # Static HTML interface
```

---

## ⚙️ Setup & Installation

### 1. Prerequisites

- [Docker](https://www.docker.com/products/docker-desktop) installed
- [Docker Compose](https://docs.docker.com/compose/) installed

### 2. Clone the repository

```bash
git clone <your-repo-url>
cd weather_api_dockerized_final_fixed
```

### 3. Configure environment variables

Edit the `.env` file to insert your OpenWeatherMap API key:

```
API_KEY=your_openweathermap_api_key
```

### 4. Build and run the application

```bash
docker-compose up --build
```

This will spin up two containers:
- `flask_app` on port `5000`
- `frontend` on port `80`

---

## 🚀 Usage

### Access the Frontend

Navigate to [http://localhost](http://localhost) in your browser.

### Use the API Directly

Endpoint: `http://localhost:5000/weather?city=London`

**Example Response:**
```json
{
  "city": "London",
  "temperature": "15°C",
  "description": "Cloudy"
}
```

---

## 🛠️ Development Tips

- Modify `flask_app/app.py` to enhance backend logic.
- Change `frontend/index.html` for UI customization.
- Use `docker-compose down` to stop services.

---

## 📦 Deployment

This stack is easily deployable on any Docker-compatible infrastructure such as:
- AWS ECS / Fargate
- DigitalOcean App Platform
- Heroku with Docker support

---

## 🧾 License

This project is licensed under the MIT License.

---

## 📬 Contact

For questions or contributions, please open an issue or submit a pull request.
