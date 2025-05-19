# Flask Job Application Web App

This is a simple job application web application built with Flask. It allows users to submit their job application details, stores the data in a SQLite database, and sends a confirmation email to the applicant.

## Features

- Collects applicant's first name, last name, email, available date, and occupation.
- Stores submissions in a SQLite database.
- Sends a confirmation email to the applicant upon successful submission.
- Displays a success message after form submission.
- Uses Bootstrap for responsive UI.

## Screenshot

![App Screenshot](static/screenshot.png)

*Example: Job Application Form UI*

## Requirements

- Python 3.x
- Flask
- Flask-SQLAlchemy
- Flask-Mail

## Setup

1. **Clone the repository**  
   ```
   git clone <your-repo-url>
   cd application_webapp_flask
   ```

2. **Create a virtual environment and activate it**  
   ```
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**  
   ```
   pip install Flask Flask-SQLAlchemy Flask-Mail
   ```

4. **Configure Email**  
   - The app uses Gmail SMTP. Update `MAIL_USERNAME` and `MAIL_PASSWORD` in [`app.py`](app.py) with your credentials or use environment variables for security.

5. **Run the application**  
   ```
   python app.py
   ```

6. **Access the app**  
   Open your browser and go to [http://localhost:5500](http://localhost:5500)

## File Structure

```
.gitignore
app.py
instance/
    data.db
static/
    screenshot.png
templates/
    index.html
```

- [`app.py`](app.py): Main Flask application.
- [`templates/index.html`](templates/index.html): HTML template for the form.

## Notes

- Make sure to allow "Less secure app access" or use an App Password for Gmail if 2FA is enabled.
- For production, never commit sensitive information (like email passwords) to your repository.

## License

This project is licensed under the MIT License.