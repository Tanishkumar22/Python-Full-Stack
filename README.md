# 🛍️ Shop Nest — E-Commerce Web App

A full-featured e-commerce web application built with **Flask** and **Firebase Firestore**, featuring user authentication, product management, a shopping cart, and a dark/light mode toggle.

---

## ✨ Features

- 🔐 **User Authentication** — Register, login, and session management
- 👤 **Role-Based Access** — Separate admin and customer roles
- 🛒 **Shopping Cart** — Add, remove, and manage cart items
- 📦 **Product Management** — Admin can add/edit/delete products
- 🌗 **Dark / Light Mode** — User-preferred theme toggle
- 🔥 **Firebase Firestore** — Cloud NoSQL database backend
- 🛡️ **CSRF Protection** — Secure forms with WTForms

---

## 🗂️ Project Structure

```
Shop-Nest-Ecommerce/
├── app.py                        # Main Flask application
├── config.py                     # App configuration (uses env vars)
├── create_admin.py               # Script to seed an admin user
├── seed_products.py              # Script to seed sample products
├── requirements.txt              # Python dependencies
├── static/
│   ├── css/style.css             # Stylesheet
│   └── js/main.js                # Frontend JavaScript
└── templates/
    ├── base.html                 # Base layout template
    ├── index.html                # Home / product listing page
    ├── login.html                # Login page
    ├── register.html             # Registration page
    ├── cart.html                 # Shopping cart page
    └── admin_dashboard.html      # Admin panel
```

---

## ⚙️ Setup & Installation

### 1. Clone the repository
```bash
git clone https://github.com/PachaMadhu/Shop-Nest-Ecommerce.git
cd Shop-Nest-Ecommerce
```

### 2. Create a virtual environment
```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Set up Firebase credentials
- Go to [Firebase Console](https://console.firebase.google.com/) → Project Settings → Service Accounts
- Click **"Generate new private key"** and download the JSON file
- Rename it to `firebase_config.json` and place it in the project root

> ⚠️ **Never commit `firebase_config.json` to version control!** It is listed in `.gitignore`.

### 5. Configure environment variables (optional)
Create a `.env` file in the root directory:
```env
SECRET_KEY=your-very-secret-key
FIREBASE_CREDENTIALS=firebase_config.json
```

### 6. Seed the database
```bash
# Add an admin user
python create_admin.py

# Add sample products
python seed_products.py
```

### 7. Run the app
```bash
python app.py
```

Visit: **http://localhost:5000**

---

## 🔐 Security Notes

- `firebase_config.json` is excluded from git via `.gitignore`
- All secrets are loaded from environment variables via `config.py`
- CSRF protection is enabled on all forms

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Python, Flask |
| Database | Firebase Firestore |
| Auth | Firebase Admin SDK |
| Frontend | HTML5, CSS3, Vanilla JS |
| Forms | Flask-WTF (CSRF) |

---

## 📄 License

This project is for educational purposes.

---

> Built with ❤️ by [PachaMadhu](https://github.com/PachaMadhu)
