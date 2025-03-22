# EX01 Developing a Simple Webserver
## Date: 18.03.2025
## Reg No: 212224040111

## AIM:  
To create a structured HTML table to display data using HTML tags.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<table>
  <tr>
    <td>Emil</td>
    <td>Tobias</td>
    <td>Linus</td>
  </tr>
  <tr>
    <td>16</td>
    <td>14</td>
    <td>10</td>
  </tr>
</table>
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

## OUTPUT:

![web py - fwd-ex1 - Visual Studio Code 18-03-2025 11_00_51](https://github.com/user-attachments/assets/20316092-7626-4127-ab0c-6ce9dd6c15e1)

![localhost - Google Chrome 18-03-2025 11_00_20](https://github.com/user-attachments/assets/e19fe0bf-0600-4b58-85ff-78531b83f1ba)


## RESULT:
The program for implementing simple webserver is executed successfully.

