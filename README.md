# Flask User REST API

A simple REST API built using Flask that performs CRUD (Create, Read, Update, Delete) operations on user data stored in memory.

## 📌 Project Overview

This project demonstrates the fundamentals of REST API development using Flask. The API allows users to:

- Create new users
- Retrieve all users
- Retrieve a specific user by ID
- Update existing user details
- Delete users

The application uses an in-memory list to store user data, making it lightweight and easy to understand for beginners.

---

## 🚀 Technologies Used

- Python 3.x
- Flask
- Postman (for testing)
- JSON

---

## 📂 Project Structure

```text
flask-user-rest-api/
│
├── app.py
├── requirements.txt
├── README.md
└── screenshots/
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/flask-user-rest-api.git
cd flask-user-rest-api
```

### 2. Create Virtual Environment (Optional)

```bash
python -m venv venv
```

Activate Virtual Environment:

**Windows**

```bash
venv\Scripts\activate
```

**Linux/Mac**

```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Application

```bash
python app.py
```

Output:

```text
* Running on http://127.0.0.1:5000
```

Open your browser or Postman and access:

```text
http://127.0.0.1:5000
```

---

## 📡 API Endpoints

### 1. Home Route

**GET /**

Returns a welcome message.

#### Response

```json
{
  "message": "User Management REST API"
}
```

---

### 2. Get All Users

**GET /users**

#### Response

```json
[
  {
    "id": 1,
    "name": "Alice",
    "email": "alice@example.com"
  },
  {
    "id": 2,
    "name": "Bob",
    "email": "bob@example.com"
  }
]
```

---

### 3. Get User By ID

**GET /users/<id>**

Example:

```http
GET /users/1
```

#### Response

```json
{
  "id": 1,
  "name": "Alice",
  "email": "alice@example.com"
}
```

---

### 4. Create User

**POST /users**

#### Request Body

```json
{
  "name": "John",
  "email": "john@example.com"
}
```

#### Response

```json
{
  "id": 3,
  "name": "John",
  "email": "john@example.com"
}
```

---

### 5. Update User

**PUT /users/<id>**

Example:

```http
PUT /users/1
```

#### Request Body

```json
{
  "name": "Alice Smith",
  "email": "alice.smith@example.com"
}
```

#### Response

```json
{
  "id": 1,
  "name": "Alice Smith",
  "email": "alice.smith@example.com"
}
```

---

### 6. Delete User

**DELETE /users/<id>**

Example:

```http
DELETE /users/1
```

#### Response

```json
{
  "message": "User deleted successfully"
}
```

---

## 🧪 Testing with Postman

1. Open Postman.
2. Create requests for each endpoint.
3. Select the correct HTTP method:
   - GET
   - POST
   - PUT
   - DELETE
4. For POST and PUT requests:
   - Select **Body**
   - Choose **raw**
   - Select **JSON**
   - Enter request data.

---

## 📋 HTTP Status Codes Used

| Status Code | Meaning |
|------------|---------|
| 200 | Success |
| 201 | Resource Created |
| 404 | Resource Not Found |

---

## 🎯 Learning Outcomes

By completing this project, you will understand:

- REST API fundamentals
- Flask routing
- HTTP methods
- JSON data handling
- CRUD operations
- API testing using Postman

---

## 🔮 Future Improvements

- Connect to a database (SQLite/MySQL/PostgreSQL)
- Add user authentication
- Implement input validation
- Add Swagger API documentation
- Deploy on Render or Railway

---

## 👨‍💻 Author

Narem Venkata Vijay Kumar Reddy

---

## 📜 License

This project is for educational purposes.
