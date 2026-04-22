# Locally-Hosted-GoLang-WebServer-
A lightweight web server built in Go using the net/http package. It supports routing, serves static files, and handles form submissions via HTTP requests. This project demonstrates core backend concepts like request handling, response writing, and building efficient web apps without external frameworks.
🚀 Go Web Server

A simple and lightweight web server built using Go’s standard net/http package. This project demonstrates core backend concepts like routing, serving static files, and handling form submissions without using any external frameworks.

✨ Features
🌐 HTTP server running on port 8080
📄 Serves static files (HTML, CSS, JS)
🔀 Custom routing (/hello, /form)
📝 Form handling (POST requests)
⚡ Fast and minimal (pure Go)
📂 Project Structure
.
├── main.go
└── static/
    ├── index.html
    └── style.css
⚙️ How It Works
1. Static File Server

Serves files from the static/ directory.

http://localhost:8080/ → loads index.html
All frontend assets are served automatically
2. /hello Endpoint
Method: GET
URL: /hello

Response:

Hello!
Returns 404 if path is incorrect
Only allows GET requests
3. /form Endpoint
Method: POST
URL: /form

Expected Form Fields:

name
address

Response Example:

POST request successful
Name = John
Address = India
▶️ Getting Started
Prerequisites
Go installed (version 1.18 or higher)
Run the Server
go run main.go

Server will start at:

http://localhost:8080
🧪 Sample HTML Form

Create this inside static/index.html:

<!DOCTYPE html>
<html>
<head>
  <title>Go Form</title>
</head>
<body>
  <h2>Submit Form</h2>
  <form action="/form" method="POST">
    <input type="text" name="name" placeholder="Enter Name" />
    <br><br>
    <input type="text" name="address" placeholder="Enter Address" />
    <br><br>
    <button type="submit">Submit</button>
  </form>
</body>
</html>
🔍 Key Concepts Covered
HTTP servers in Go
Routing with http.HandleFunc
Serving static files
Parsing form data (r.ParseForm)
Handling GET and POST requests
⚠️ Limitations
No database integration
No authentication system
No input validation
Basic error handling only
🛠 Possible Improvements
Add input validation & sanitization
Use templates (html/template)
Add REST API structure
Integrate database (MySQL/PostgreSQL)
Add logging middleware
Implement authentication
