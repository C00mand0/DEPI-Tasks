# Users Management System (API + OOP)

## 📌 Overview

This project is a simple **Users Management System** built with Python. It demonstrates clean software design by applying **Object-Oriented Programming (OOP)** principles while consuming a public REST API.

The application fetches users from an external API, converts them into Python objects, and prints user information in a clean and structured way.

---

## 🎯 Objectives

* Consume a public API using HTTP GET
* Parse JSON data
* Apply OOP principles:

  * Abstraction
  * Encapsulation
  * Inheritance
  * Polymorphism
* Handle errors using `try / except`
* Maintain clean code structure and separation of concerns

---

## 🌐 Data Source

The application uses the following public API:

```
https://jsonplaceholder.typicode.com/users
```

---

## 🧱 Project Structure

```
project/
│
├── models/
│   └── user.py
│
├── datasource/
│   ├── user_data_source.py
│   └── user_api.py
│
├── services/
│   └── printer.py
│
└── main.py
```

---

## 🧩 OOP Design

### 1️⃣ Abstraction

* `UserDataSource` is an abstract base class
* Defines a contract (`get_users`) for any data source

### 2️⃣ Encapsulation

* `User` class hides internal data (`city`, `company`)
* Access is allowed only through getter methods

### 3️⃣ Inheritance

* `UserAPI` inherits from `UserDataSource`
* Implements the `get_users` method using an API

### 4️⃣ Polymorphism

* `print_users` function works with any `UserDataSource`
* Does not depend on API, file, or database implementation

---

## ⚠️ Error Handling

* Network and API errors are handled using:

  ```python
  requests.exceptions.RequestException
  ```
* Unexpected runtime errors are also safely handled

---

## ▶️ How to Run

1. Install dependencies:

   ```bash
   pip install requests
   ```

2. Run the application:

   ```bash
   python main.py
   ```

---

## ✅ Sample Output

```
Name: Leanne Graham
City: Gwenborough
Company: Romaguera-Crona
------------------------------
```

---

## 🏆 Key Learnings

* Clean separation between data source and business logic
* Proper use of OOP concepts in a real-world scenario
* Writing maintainable and extensible Python code

---

## 👤 Author

**Fares Ahmed**

---

## 🚀 Future Improvements

* Add file or database data sources
* Filter or group users
* Add unit t
