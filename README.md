# Flask-


from flask import Flask

app = Flask(__name__)  # Create Flask application

# Route for homepage
@app.route('/')
def home():
    return "Welcome to the Home Page!"

# Route for about page
@app.route('/about')
def about():
    return "This is the About Page."

# Run the app
if __name__ == '__main__':
    app.run(debug=True)
