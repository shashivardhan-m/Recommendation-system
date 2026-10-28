# Recommendation System using Generative AI

A Django-based web application that leverages Google Gemini AI to provide generative recommendations for recommender systems. The application supports tasks like synthetic data generation (GANs/VAEs), cold-start problem solving, diversity enhancement, and recommender system evaluation.

## Features

- **User Registration & Login** — Account creation with admin approval workflow
- **Admin Dashboard** — Manage users (activate, deactivate, delete)
- **Generative AI Recommender** — Gemini-powered interface with multiple task modes:
  - Generate synthetic user-item interaction data
  - Cold-start problem solutions
  - Recommendation diversity enhancement
  - Recommender system design evaluation
- **PDF Export** — Download GenAI outputs as PDF documents

## Tech Stack

| Component       | Technology                  |
|-----------------|-----------------------------|
| Framework       | Django 5.2                  |
| AI Model        | Google Gemini 1.5 Flash     |
| Database        | SQLite3                     |
| PDF Generation  | xhtml2pdf                   |
| Frontend        | HTML Templates + Bootstrap  |
| Environment     | python-dotenv               |

## Prerequisites

- Python 3.10+
- pip

## Installation

1. **Clone the repository**

   ```bash
   git clone <repo-url>
   cd Recommendation-system-main
   ```

2. **Create a virtual environment**

   ```bash
   python -m venv venv
   source venv/bin/activate  # macOS/Linux
   venv\Scripts\activate     # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install django google-generativeai xhtml2pdf python-dotenv
   ```

4. **Configure the API key**

   Create a `.env` file in `RecommendationSystems/`:

   ```env
   GOOGLE_API_KEY=your_gemini_api_key_here
   ```

5. **Run migrations**

   ```bash
   cd RecommendationSystems
   python manage.py migrate
   ```

6. **Start the development server**

   ```bash
   python manage.py runserver
   ```

   The application will be available at `http://127.0.0.1:8000/`.

## Project Structure

```
Recommendation-system-main/
├── BASEPAPER/                  # Reference research paper
├── RecommendationSystems/
│   ├── Recommendation_Systems/ # Django project config
│   │   ├── settings.py
│   │   ├── urls.py
│   │   ├── views.py
│   │   └── wsgi.py
│   ├── users/                  # User app (registration, login, GenAI)
│   │   ├── models.py
│   │   ├── views.py
│   │   └── forms.py
│   ├── admins/                 # Admin app (user management)
│   │   ├── models.py
│   │   └── views.py
│   ├── templates/              # HTML templates
│   └── manage.py
└── .gitignore
```

## Usage

1. Register a new user account via the registration page.
2. Admin approves/activates the account from the admin dashboard.
3. Log in and navigate to the **GenAI Recommender** page.
4. Select a task type, provide context, and generate recommendations.
5. Optionally export the output as a PDF.

## License

This project is for academic/research purposes.
