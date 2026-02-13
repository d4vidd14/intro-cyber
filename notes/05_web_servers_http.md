# Web Servers, CMS, HTTP Methods & Status Codes

## What is a web server?
A web server is software (and the machine running it) that receives HTTP/HTTPS requests from clients (browsers/apps) and returns responses (pages, APIs, files).

Common examples: Nginx, Apache, IIS.

## CMS (Content Management System)
A CMS lets non-technical users create/manage website content without coding everything manually.
Examples: WordPress, Joomla, Drupal.

Security note: CMS ecosystems are common targets because of plugins/themes and frequent misconfigurations, so patching and updates matter.

---

## HTTP Methods (client actions)

### Core methods
- **GET**: retrieve data (read-only). Parameters often appear in the URL/query string.
  - Security note: avoid sending sensitive data in URLs (can be logged, cached, shared).
- **POST**: submit data to the server (forms, login, creating resources).
  - Security note: if sensitive data is involved, use **HTTPS** (TLS). Never send credentials over plain HTTP.

### Other common methods
- **PUT**: create or replace a resource (idempotent).
- **DELETE**: remove a resource.
- **PATCH**: partial update of a resource.
- **OPTIONS**: asks the server what methods are allowed / used in CORS preflight.
- **HEAD**: like GET but without body (headers only).

---

## HTTP Status Codes (server responses)

### 1xx Informational
- **100 Continue**: request received, client can continue.

### 2xx Success
- **200 OK**: request successful.
- **201 Created**: resource created (common after POST/PUT).

### 3xx Redirection
- **301 Moved Permanently**
- **302 Found** (temporary redirect)
- **304 Not Modified** (cache-related)

### 4xx Client errors
- **400 Bad Request**: malformed request.
- **401 Unauthorized**: authentication required/failed.
- **403 Forbidden**: understood but not allowed.
- **404 Not Found**: resource not found.

### 5xx Server errors
- **500 Internal Server Error**: generic server failure.
- **502 Bad Gateway**: proxy/upstream error.
- **503 Service Unavailable**: overloaded/maintenance.

---

## Practical cybersecurity takeaways
- Always prefer **HTTPS** for authentication and any sensitive data.
- Avoid credentials or sensitive parameters in **GET** URLs.
- Understanding methods and status codes helps identify issues (auth failures, missing resources, server misconfigurations).
