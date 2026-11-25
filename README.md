Flask Blog

A multi-user personal blog built with Flask, HTML, CSS and JavaScript. Visitors can read posts, register, log in and comment, while the site admin writes and manages the posts.

Status: In progress. Core features work; more are on the way (see Roadmap).

Features
User registration and login, with passwords hashed before they are stored
Admin-only tools for creating and deleting posts
Rich text editing for posts and comments with CKEditor
Comments on every post, limited to logged-in users
Avatar images generated from each user's email via Gravatar
Relational database with linked tables for users, posts and comments
Responsive layout styled with Bootstrap
About and Contact pages
Tech stack
Area	Tools
Backend	Python, Flask, Flask-Login, Flask-SQLAlchemy, Werkzeug
Frontend	HTML, CSS, JavaScript, Jinja2 templates, Bootstrap 5
Editor	Flask-CKEditor
Config	python-dotenv
Getting started
1. Clone the repository
bash
git clone https://github.com/Just-UPI/flask-blog.git
cd flask-blog
2. Create and activate a virtual environment
bash
python -m venv venv
source venv/bin/activate      # on Windows: venv\Scripts\activate
3. Install dependencies
bash
pip install -r requirements.txt
4. Set up environment variables

Create a .env file in the project root:

FLASK_KEY=your-secret-key-here
DB_URI=sqlite:///posts.db
FLASK_KEY is the secret key Flask uses to secure sessions. Use any long, random string.
DB_URI is the database connection string. The example above uses a local SQLite file.

The .env file is listed in .gitignore, so your secrets are never committed.

5. Run the app
bash
python main.py

Then open http://127.0.0.1:5001 in your browser.

Admin account: the first user to register (user ID 1) is treated as the admin and can create and delete posts.

Roadmap
[ ] Working contact form that sends email
[ ] Deploy the blog online
[ ] Screenshots and a live demo link
What I learned
Building a full-stack app with Flask: routing, Jinja templates and forms
Modelling related data with SQLAlchemy (users, posts and comments)
Handling authentication with Flask-Login and password hashing
Restricting routes with custom decorators
Keeping secrets out of source code with environment variables
Credits

Built as a learning project while following the 100 Days of Code Python bootcamp by Angela Yu.

Author

Urhoboghara Ifeanyi — Computer Science student, University of Lagos GitHub: @Just-UPI
