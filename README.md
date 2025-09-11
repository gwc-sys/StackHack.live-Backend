
# StackHack.live
## 🚀 Features  
- 🔑 **JWT Authentication** (via `djangorestframework-simplejwt`)  
- 🗄 **MySQL Database** integration  
- ☁️ **Cloudinary Storage** for media and static files  
- 🎵 **Audio Analysis & Processing** using `librosa`, `pydub`, and `scikit-learn`  
- 🔗 **RESTful APIs** built with DRF  
- 🌐 **CORS Support** for frontend integration (React/Next.js/Angular etc.)  
- ⚡ **ASGI Support** with `uvicorn` & `gunicorn`  

---

## 🛠 Tech Stack  
- **Backend Framework:** Django 5.2.4  
- **API Framework:** Django REST Framework 3.16.0  
- **Authentication:** JWT (SimpleJWT)  
- **Database:** MySQL   
- **Audio/ML:** librosa, scikit-learn, scipy, numpy  
- **Deployment:** Gunicorn, Uvicorn  

📂 Project Structure

StackHack.live-Backend/
│── backend/              # Django project core
│── api/                  # REST API apps
│── manage.py             # Django management script
│── requirements.txt      # Dependencies
│── .env.example          # Example environment variables


⸻

🔐 Authentication

This project uses JWT authentication.
	•	Obtain a token: POST /api/token/
	•	Refresh a token: POST /api/token/refresh/
	•	Use in headers:

Authorization: Bearer <your_token>

📡 Example API Endpoints

Auth

POST /api/token/            # Login and get JWT token
POST /api/token/refresh/    # Refresh JWT token

Users

POST /api/users/register/   # Register a new user
GET  /api/users/me/         # Get current user profile

Audio

POST /api/audio/upload/     # Upload an audio file
GET  /api/audio/analyze/    # Run audio analysis

🌍 Deployment

For production, use Gunicorn with Uvicorn workers:

gunicorn backend.asgi:application -k uvicorn.workers.UvicornWorker

🤝 Contributing

Contributions are welcome! Please fork this repo and submit a pull request.

📜 License

This project is licensed under the MIT License.

---

👉 Do you want me to also **generate a `.env.example` file** so contributors know exactly which environment variables to set up?
