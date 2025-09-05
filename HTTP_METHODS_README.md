# HTTP Methods, Data Formats, and APIs
---

## 🔹 HTTP Methods

### 1. GET
- **What**: Retrieve data from a server.  
- **Why**: To fetch resources (like user profiles, product lists).  
- **When**: Use when you only need to read data.  
- **Where**: Example → `/users/1` returns user info.  
- **Who**: Used by client apps (mobile, web).  

---

### 2. POST
- **What**: Send data to the server (create something new).  
- **Why**: To insert/create resources.  
- **When**: Use when adding data that doesn’t exist yet.  
- **Where**: Example → `POST /users` with JSON `{ "name": "John" }`.  
- **Who**: Client sends → server processes.  

---

### 3. PUT
- **What**: Update or replace an existing resource.  
- **Why**: To overwrite a record completely.  
- **When**: Use when updating the full object.  
- **Where**: Example → `PUT /users/1` with `{ "name": "John", "age": 25 }`.  
- **Who**: Client updates → server saves new version.  


---

### 4. PATCH
- **What**: Partially update a resource.  
- **Why**: More efficient than PUT if only 1-2 fields change.  
- **When**: Use when modifying part of a record.  
- **Where**: Example → `PATCH /users/1` with `{ "age": 26 }`.  
- **Who**: Client requests → server modifies only given fields.  

---

### 5. DELETE
- **What**: Remove a resource.  
- **Why**: To delete unwanted or outdated data.  
- **When**: Use when you want to remove something permanently.  
- **Where**: Example → `DELETE /users/1`.  
- **Who**: Client requests deletion → server removes record.  

---

## 🔹 Data Formats

### 6. JSON (JavaScript Object Notation)
- **What**: Lightweight data format using key–value pairs.  
- **Why**: Easy to read/write for humans and machines.  
- **When**: Use for APIs, config files, data exchange.  
- **Where**: Everywhere (mobile apps, web APIs, databases).  
- **Who**: Developers and systems exchanging data.  

**Example (JSON User Object):**
```json
{
  "id": 1,
  "name": "John",
  "age": 25
}
```

---

### 7. XML (Extensible Markup Language)
- **What**: A markup language using tags to structure data.  
- **Why**: Standardized, supports metadata and validation.  
- **When**: Used in older systems, SOAP APIs, configs.  
- **Where**: Banking systems, enterprise apps.  
- **Who**: Developers needing structured data.  

**Example (XML User Object):**
```xml
<user>
  <id>1</id>
  <name>John</name>
  <age>25</age>
</user>
```

---

## 🔹 API (Application Programming Interface)
- **What**: A set of rules that lets two systems communicate.  
- **Why**: To allow apps/services to talk without knowing each other’s code.  
- **When**: Use whenever one system needs data or functionality from another.  
- **Where**: REST APIs, GraphQL APIs, OS APIs, SDKs.  
- **Who**: Developers (client) call API → providers (server) respond.  

**Example (API Flow):**
```
Client (App) ---> API Request ---> Server
Client (App) <--- API Response <--- Server
```

---

✅ Summary:
- **GET** → fetch data  
- **POST** → create data  
- **PUT/PATCH** → update data  
- **DELETE** → remove data  
- **JSON/XML** → formats for exchange  
- **API** → the communication bridge  
