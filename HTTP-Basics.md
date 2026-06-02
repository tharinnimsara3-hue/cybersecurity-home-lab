# HTTP Basics Notes

## Introduction

HTTP (HyperText Transfer Protocol) is the protocol used for communication between web browsers and web servers. HTTPS is the secure version of HTTP that uses encryption.

---

## How a Web Application Works

Browser
↓
Web Server
↓
Application
↓
Database

When a user visits a website, the browser sends a request to the web server. The application processes the request and may interact with a database before sending a response back to the browser.

---

## HTTP

### Definition

HTTP is a communication protocol used to transfer data between clients and servers.

### Characteristics

* Data is transmitted in plain text
* No encryption
* Less secure

### Example

http://example.com

---

## HTTPS

### Definition

HTTPS is the secure version of HTTP that uses TLS encryption.

### Characteristics

* Data is encrypted
* Provides confidentiality
* Protects against eavesdropping

### Example

https://example.com

---

## GET Method

### Definition

Used to request data from a server.

### Example

GET /products

### Common Uses

* Viewing web pages
* Searching content
* Retrieving information

---

## POST Method

### Definition

Used to send data to a server.

### Example

POST /login

### Common Uses

* Login forms
* Registration forms
* Uploading information

---

## HTTP Status Codes

### 200 OK

Request completed successfully.

### 301 Moved Permanently

Resource has been redirected.

### 403 Forbidden

Access denied.

### 404 Not Found

Requested resource cannot be found.

### 500 Internal Server Error

A server-side error occurred.

---

## Cookies

### Definition

Small pieces of information stored in a user's browser.

### Uses

* User authentication
* Session management
* User preferences

### Example

PHPSESSID=abc123

---

## Sessions

### Definition

A session allows a server to remember a user after authentication.

### Process

User Login
↓
Session Created
↓
Session ID Stored in Cookie
↓
User Remains Logged In

### Benefits

* Maintains user authentication
* Improves user experience
* Reduces repeated logins

---

## HTTP Request and Response

### Request Components

* Method (GET, POST)
* URL
* Headers
* Body

### Response Components

* Status Code
* Headers
* Content

---

## Difference Between HTTP and HTTPS

| Feature     | HTTP | HTTPS |
| ----------- | ---- | ----- |
| Encryption  | No   | Yes   |
| Security    | Low  | High  |
| TLS Support | No   | Yes   |
| Recommended | No   | Yes   |

---

## Conclusion

Understanding HTTP, HTTPS, requests, responses, cookies, sessions, and status codes is fundamental for web application security testing and vulnerability assessment.
