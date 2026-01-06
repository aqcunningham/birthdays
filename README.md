# Birthdays

Small Flask web app to store and display birthdays using a SQLite database.  
Users can submit a name and date, and the app shows the full list of stored birthdays

<img width="1901" height="1061" alt="image" src="https://github.com/user-attachments/assets/b997ec1f-648e-446a-86aa-05cfa5167e7f" />
<img width="1904" height="1062" alt="image" src="https://github.com/user-attachments/assets/528455a5-7e31-4bbe-8e83-fa8eb51fd9cb" />
<img width="1905" height="830" alt="image" src="https://github.com/user-attachments/assets/31ecb1f9-c2c9-4eea-a47b-aa094ef52525" />
---

## 🌐 Live Demo

**Live Demo:** https://your-render-url-here.onrender.com

---

## Features

- Add birthdays via a simple HTML form
- Store data in a SQLite database (`birthdays.db`)
- Display all saved birthdays in a table
- Server-side rendering with Flask templates

---

## Tech Stack

- **Backend:** Flask (Python)
- **Database:** SQLite
- **Frontend:** HTML, CSS (served via Flask `templates/` and `static/`)
- **Deployment:** Render, gunicorn

---

## Getting Started (Local)

1. **Clone the repository**

   ```bash
   git clone https://github.com/<your-username>/birthdays-app.git
   cd birthdays-app
2. **Create and activate a virtual environment (optional but recommended)**

	python3 -m venv .venv
	source .venv/bin/activate   
	
3. **Install dependencies**
	
	pip install -r requirements.txt

4. **Run the app**
	
	flask run
or
	
	python app.py

6. **Open the URL printed in the terminal (usually http://127.0.0.1:5000/).**


		Project Structure
		birthdays/
		├── app.py
		├── birthdays.db
		├── requirements.txt
		├── README.md
		├── static/
		│   └── styles.css
		└── templates/
			└── index.html

		Implementation Details
		Defines a birthdays table:
				CREATE TABLE birthdays (
					id INTEGER PRIMARY KEY,
					name TEXT,
					month INTEGER,
					day INTEGER
				);

	On GET /:
		Queries all birthdays from the database
		Renders them in index.html

	On POST /:
		Reads name, month, and day from the submitted form
		Inserts a new row into the birthdays table
		Redirects back to the index page

What I Practiced:

	Building a small CRUD-style Flask app
	Working with SQLite from Python
	Using templates and static files in Flask
	Deploying a Python web app to Render
