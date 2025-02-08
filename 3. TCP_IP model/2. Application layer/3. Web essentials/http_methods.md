# HTTP Methods & Status Codes

## HTTP Methods

### 1. GET
- Used to retrieve data from a server.
- No request body.
- Safe and idempotent.

#### **Success Response:**
- **Status Code:** `200 OK` (if resource is found)
- **Response Body:** Requested resource

#### **Failure Response:**
- **Status Code:** `404 Not Found` (if resource is missing)
- **Status Code:** `403 Forbidden` (if access is restricted)

---

### 2. POST
- Used to create a new resource on the server.
- Sends data in the request body.

#### **Success Response:**
- **Status Code:** `201 Created` (if resource is successfully created)
- **Response Body:** Created resource or location of resource

#### **Failure Response:**
- **Status Code:** `400 Bad Request` (if request payload is invalid)
- **Status Code:** `409 Conflict` (if resource already exists)

---

### 3. PUT
- Used to update an existing resource or create one if it does not exist.
- Sends data in the request body.

#### **Success Response:**
- **Status Code:** `200 OK` (if resource is updated)
- **Status Code:** `201 Created` (if resource is created)

#### **Failure Response:**
- **Status Code:** `400 Bad Request` (if request payload is invalid)
- **Status Code:** `404 Not Found` (if resource does not exist)

---

### 4. PATCH
- Used to partially update an existing resource.
- Sends data in the request body.

#### **Success Response:**
- **Status Code:** `200 OK` (if resource is updated and response body contains the updated resource or relevant metadata.)
- **Status Code:** `204 OK` (If the request is successful but there is no response body (only headers).)

#### **Failure Response:**
- **Status Code:** `400 Bad Request` (if request payload is invalid)
- **Status Code:** `404 Not Found` (if resource does not exist)

---

### 5. DELETE
- Used to delete a resource from the server.

#### **Success Response:**
- **Status Code:** `200 OK` (if resource is deleted with response)
- **Status Code:** `204 No Content` (if resource is deleted without response)

#### **Failure Response:**
- **Status Code:** `404 Not Found` (if resource does not exist)
- **Status Code:** `403 Forbidden` (if deletion is not allowed)

---

## Common HTTP Status Codes

### **1xx - Informational**
- `100 Continue` - Server has received request headers, client should proceed.
- `101 Switching Protocols` - Server agrees to switch protocols.

### **2xx - Success**
- `200 OK` - Successful request.
- `201 Created` - Resource successfully created.
- `204 No Content` - Request successful but no response body.

### **3xx - Redirection**
- `301 Moved Permanently` - Resource permanently moved.
- `302 Found` - Temporary redirect.
- `304 Not Modified` - Cached resource unchanged.

### **4xx - Client Errors**
- `400 Bad Request` - Malformed request.
- `401 Unauthorized` - Authentication required.
- `403 Forbidden` - Request is valid but not allowed.
- `404 Not Found` - Resource does not exist.
- `409 Conflict` - Resource conflict.

### **5xx - Server Errors**
- `500 Internal Server Error` - General server error.
- `502 Bad Gateway` - Invalid response from upstream server.
- `503 Service Unavailable` - Server is overloaded or down.
- `504 Gateway Timeout` - Upstream server timeout.
