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



==============================================================================================================================================================================

# using request.args and request.form

from flask import Flask, request

app = Flask(__name__)

@app.route('/greet')
def greet():
    name = request.args.get('name', 'Guest')                #req.args
    return f"Hello {name}!"

@app.route('/login', methods=['POST'])
def login():
    username = request.form.get('username')                #req.form
    password = request.form.get('password')
    return f"Received login for user: {username}"

if __name__ == '__main__':
    app.run(debug=True)




















