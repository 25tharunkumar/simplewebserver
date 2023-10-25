# EX01 Developing a Simple Webserver
## Date:

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """

<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
<style>
    body{

        background-image:url('img.jpg');
    }
</style>
</head>
<body>
<h1 align="center"><b>Top 5 webdevelopment framework</b></h1><br>
    <table align="center" border="15" cellpadding="15" cellspacing="3">
        <tr>
            <th>Company name</th>
            <th>Location</th>
            <th>Yearly turn over</th>
        </tr>
        <tr>
            <td><ul>
                <li>Django</li>
                <br>
                <li>MEAN stack</li>
                <br>
                <li>MEAN stack</li>
                <br>
                <li>ASP.NET core</li>
                <br>
                <li>spring</li>
            </ul></td>
            <td>
                <ul>
                    <li>chennai</li>
                    <br>
                    <li>chennai</li>
                    <br>
                    <li>chennai</li>
                    <br>
                    <li>chennai</li>
                    <br>
                    <li>chennai</li>
                </ul>
            </td>
            <td>
                <ul>
                    <li>123162</li>
                    <br>
                    <li>12335402</li>
                    <br>
                    <li>41655262</li>
                    <br>
                    <li>4523122</li>
                    <br>
                    <li>74562162</li>
                </ul>
            </td>
        </tr>
    </table>
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',80)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```
## Top Five Web Application Development Frameworks
```
1.Django
2.MEAN stack
3.MEAN stack
4.ASP.NET core
5.spring
```
## OUTPUT:
![image](https://github.com/25tharunkumar/simplewebserver/assets/123470785/7d866625-d82e-4b4a-8629-d1da2b0ee3c3)


## RESULT:
The program for implementing simple webserver is executed successfully.
