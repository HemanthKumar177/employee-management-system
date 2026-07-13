# 🚀 Employee Management System

A production-ready **Employee Management System** built using **React.js**, **Spring Boot**, and **MySQL**, containerized with **Docker** and deployed on **AWS EC2** using an automated **Jenkins CI/CD Pipeline**.

---

## ✨ Features

### 🎨 Frontend
- 📋 Employee Dashboard
- ➕ Add New Employee
- ✏️ Update Employee Details
- ❌ Delete Employee
- 🔍 View Employee Information
- 📱 Responsive User Interface
- 🔗 Axios Integration with Backend APIs

### ⚙️ Backend
- 🌐 RESTful Spring Boot APIs
- 📝 Complete CRUD Operations
- 🗄️ MySQL Database Integration
- 🔄 Spring Data JPA & Hibernate
- ⚡ Layered Architecture (Controller → Service → Repository)

### ☁️ DevOps
- 🐳 Docker Containerization
- 🏗️ Multi-stage Docker Builds
- 🌐 Custom Docker Network
- 🤖 Jenkins CI/CD Pipeline
- 🔀 Nginx Reverse Proxy
- ☁️ AWS EC2 Deployment
- ⚖️ AWS Application Load Balancer (ALB)
- 🌍 Amazon Route 53 Integration

---

# 🛠️ Tech Stack

| Category | Technologies |
|-----------|--------------|
| 🎨 Frontend | React.js, Vite, Axios |
| ⚙️ Backend | Spring Boot, Java 21 |
| 🗄️ Database | MySQL 8 |
| 🌐 Web Server | Nginx |
| 🐳 Containerization | Docker |
| 🤖 CI/CD | Jenkins |
| ☁️ Cloud | AWS EC2 |
| ⚖️ Load Balancer | AWS ALB |
| 🌍 DNS | Amazon Route 53 |
| 📦 Build Tool | Maven |
| 🔧 Version Control | Git & GitHub |

---

# 📡 REST API Endpoints

| Endpoint |                | Method    | Description |
|:---------|:------:|:------------|
| `/api/v1/employees`      | **GET**    | Retrieve all employees      |
| `/api/v1/employees/{id}` | **GET**    | Retrieve employee by ID     |
| `/api/v1/employees/add`  | **POST**   | Create a new employee       |
| `/api/v1/employees/{id}` | **PUT**    | Update an existing employee |
| `/api/v1/employees/{id}` | **DELETE** | Delete an employee          |

---

# 🏗️ Project Architecture

> *(Add your architecture diagram here)*

---

# 📂 Project Structure

```text
employee-management-system/
│
├── backend/
│   ├── src/
│   ├── Dockerfile
│   ├── pom.xml
│   └── application.properties
│
├── frontend/
│   ├── src/
│   ├── nginx/
│   │   └── default.conf
│   ├── Dockerfile
│   └── package.json
│
├── README.md
└── LICENSE
```

---

# 🚀 Getting Started

## 📥 Clone Repository

```bash
git clone https://github.com/HemanthKumar177/employee-management-system.git
cd employee-management-system
```

---

## ⚙️ Backend Setup

```bash
cd backend
./mvnw clean package
```

Run the application:

```bash
java -jar target/*.jar
```

---

## 🎨 Frontend Setup

```bash
cd frontend
npm install
npm run build
```

---

# 🐳 Docker Deployment

### Build Backend Image

```bash
cd backend
docker build -t emp-backend .
```

### Build Frontend Image

```bash
cd ../frontend
docker build -t emp-frontend .
```

### Create Docker Network

```bash
docker network create emp-network
```

### Run MySQL Container

```bash
docker run -d \
--name mysql \
--network emp-network \
-e MYSQL_ROOT_PASSWORD=root \
-e MYSQL_DATABASE=employee_db \
mysql:8
```

### Run Backend Container

```bash
docker run -d \
--name emp-backend \
--network emp-network \
-p 8081:8080 \
emp-backend
```

### Run Frontend Container

```bash
docker run -d \
--name emp-frontend \
--network emp-network \
-p 3000:80 \
emp-frontend
```

---

# 🔄 CI/CD Pipeline

The Jenkins Pipeline automates the deployment process by performing the following stages:

- ✅ Checkout Source Code
- 🏗️ Build Backend Docker Image
- 🏗️ Build Frontend Docker Image
- 🛑 Stop Existing Containers
- 🗑️ Remove Old Containers
- 🚀 Deploy Updated Containers
- ✔️ Verify Successful Deployment

---

# 📸 Screenshots

| Feature | Preview |
|----------|---------|
| 🏠 Home Page | *(Add Screenshot)* |
| 📋 Employee List | *(Add Screenshot)* |
| ➕ Add Employee | *(Add Screenshot)* |
| ✏️ Update Employee | *(Add Screenshot)* |
| 🤖 Jenkins Pipeline | *(Add Screenshot)* |
| 🐳 Docker Containers | *(Add Screenshot)* |
| ☁️ AWS Deployment | *(Add Screenshot)* |

---

# 🚀 Future Enhancements

- 🔐 JWT Authentication
- 👥 Role-Based Access Control
- 🔍 Search & Pagination
- 📄 Export Employee Data
- 🧪 Unit & Integration Testing
- ☸️ Kubernetes Deployment
- 📊 Prometheus & Grafana Monitoring

---

# 👨‍💻 Author

**Hemanth Kumar HV**

⭐ If you found this project useful, consider giving it a **Star** on GitHub!
