# Authentication Server

The following is a small authentication server using python built using Flask. The server serves the following endpoint

# Endpoints
-   /register: given an email address and a password as parameters, it creates a user record
-   /login: given an email and password, it returns a session token if successful, or 400 error
-   /resetpassword:: given an email, current password and new password.
-   /: an endpoint to see all registered users

The authentication server currently SQLite as db. 
Passwords are stored as hash values, and upon a successful login, a session token is generated using JWT and returned

# Running Unit tests
python -m pytest

# Running the server

docker build -t amal_test .

docker run -p 5000:5000 amal_test

![docker_run](https://github.com/amalsalimcode/elsa/blob/main/readme_images/docker_run.png)


![login](https://github.com/amalsalimcode/elsa/blob/main/readme_images/login.png)
