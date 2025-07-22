# Django Project Setup

## 1. Project Setup & Virtual Environment
- Create a new folder for your Django project.
- Open the folder in VS Code and open terminal.
- Create virtual environment:
  ```bash
  python -m venv virt
  ```
- Activate virtual environment:
  - **Windows:** `virt\Scripts\activate`
  - **Mac/Linux:** `source virt/bin/activate`

## 2. Create .gitignore File
Create a `.gitignore` file in the root folder and add:
```
virt/
media/
db.sqlite3
credentials.txt
__pycache__/
```

## 3. Install Required Packages
Install Django and Pillow:
```bash
pip install django
pip install pillow
```

## 4. Save Installed Packages
Freeze requirements:
```bash
pip freeze > requirements.txt
```

## 5. Start Django Project
Start your project :
```bash
django-admin startproject vshop
```

Folder structure will look like:
```
project-folder/
│
├── virt/
├── .gitignore
├── requirements.txt
├── README.md
│
└── vshop/
    ├── manage.py
    └── vshop/
```

## 6. Run Migrations
Navigate to the project folder:
```bash
cd vshop
python manage.py migrate
```

## 7. Run Development Server
```bash
python manage.py runserver
```
Open the link shown in terminal (e.g., http://127.0.0.1:8000).

## 8. Create Superuser for Admin Panel
```bash
python manage.py createsuperuser
```
Then go to `http://127.0.0.1:8000/admin` and log in with the credentials.



## ✅ Note
- Activate virtual environment every time before working:  
  - **Windows:** `virt\Scripts\activate`
  - **Mac/Linux:** `source virt/bin/activate`
- Run `pip freeze > requirements.txt` again if you install new packages.
- Use `Ctrl + C` to stop the development server in terminal.
