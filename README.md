# 🏥 Hospital Management System

A Django-based hospital management web application connected to a Microsoft SQL Server (MSSQL) database. The system supports three user roles — Patient, Doctor, and Admin — and provides core features such as appointment booking, patient registration, and doctor listing.

---

## 🚀 About

This project is a web-based hospital management system built with Django. It allows patients to register, log in, and book appointments with doctors. Doctors can manage their schedules, and admins have full control over the system through the Django admin panel. The application uses Microsoft SQL Server as its database backend.

---

## 🛠️ Tech Stack

| Technology | Description |
|------------|-------------|
| **Python** | Backend language  |
| **Django** | Web framework |
| **HTML/CSS** | Frontend templates  |
| **MSSQL** | Microsoft SQL Server database |
| **django-mssql-backend** | Django connector for MSSQL |

---

## 👥 User Roles

### 🧑‍⚕️ Patient
- Register and log in to the system
- View available doctors
- Book appointments with doctors

### 👨‍⚕️ Doctor
- View assigned appointments
- Manage their schedule

### 🛡️ Admin
- Full control via Django admin panel
- Manage patients, doctors, and appointments
- Add or remove users and records

---

## ✨ Features

- 🔐 User registration and login (patient & doctor)
- 📅 Appointment booking system
- 🩺 Doctor listing and profile view
- 🗄️ MSSQL database integration
- 🖥️ Django admin panel for full system management

---

## 📁 Project Structure

```
hastane_sistem/
├── mysite/            # Main Django project directory (settings, URLs)
├── templates/         # HTML templates for all pages
├── .gitignore
├── dosya              # Config/notes file
└── README.md
```

---

## ⚙️ Getting Started

### Prerequisites

- Python 3.8+
- Microsoft SQL Server (local or remote)
- ODBC Driver for SQL Server

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/BerraCevik/hastane_sistem.git
   cd hastane_sistem
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate        # Linux/macOS
   venv\Scripts\activate           # Windows
   ```

3. **Install dependencies:**
   ```bash
   pip install django mssql-django
   ```

4. **Configure the database in `mysite/settings.py`:**
   ```python
   DATABASES = {
       'default': {
           'ENGINE': 'mssql',
           'NAME': 'your_database_name',
           'USER': 'your_username',
           'PASSWORD': 'your_password',
           'HOST': 'your_server',
           'PORT': '1433',
           'OPTIONS': {
               'driver': 'ODBC Driver 17 for SQL Server',
           },
       }
   }
   ```

5. **Apply database migrations:**
   ```bash
   python manage.py migrate
   ```

6. **Create a superuser (Admin):**
   ```bash
   python manage.py createsuperuser
   ```

7. **Start the development server:**
   ```bash
   python manage.py runserver
   ```

8. Open your browser and navigate to `http://127.0.0.1:8000`.

---

## 🔑 Admin Panel

Log in at `http://127.0.0.1:8000/admin` to manage all patients, doctors, and appointments.

---

## 🤝 Contributing

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add new feature'`
4. Push the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 📄 License

This project is open source and developed for educational purposes.

---

*Developer: [BerraCevik](https://github.com/BerraCevik)*
