# 🧮 Matrix Processor Application  
**Spring Boot Backend + HTML Frontend**  

Perform matrix operations (Echo, Invert, Flatten, Sum, Multiply) via CSV uploads. Includes a sample `matrix.csv` for testing.  

---

## 📦 What's Included  
- 📂 **matrix-backend/** → Spring Boot application (Port: 8081)  
- 📄 **matrix-backend/src/main/resources/static/index.html** → Ready-to-use frontend  
- 📜 **matrix.csv** → Sample test file (in root folder)  

---

### 📑 Sample CSV Contents:  
`csv 
1,2,3  
4,5,6  
7,8,9`

## 🚀 Quick Start

### 1️⃣ Install JDK 17  
🔗 [Download JDK 17](https://adoptopenjdk.net/)

### 2️⃣ Run the Backend:  
`bash
cd matrix-backend  
mvn spring-boot:run  # Starts at http://localhost:8081`

### 3️⃣ Open the Frontend:
📂 **Double-click:** `matrix-backend/src/main/resources/static/index.html`

### 4️⃣ Test with the Included CSV:
📌 Click **"Choose File"** → Select `matrix.csv`  
📌 Choose an **operation** → Click **Submit**

---

## 🛠️ Usage Guide

### 🔹 Using the Included Sample File  
The provided **matrix.csv** contains:  
`csv
1,2,3  
4,5,6  
7,8,9  `


### 📊 Expected Outputs

#### 1️⃣ Echo
`csv
1,2,3
4,5,6
7,8,9`

### 2️⃣ Invert  
`csv
1,4,7  
2,5,8  
3,6,9  `

### 3️⃣ Flatten  
`text
1,2,3,4,5,6,7,8,9  `

### 4️⃣ Sum 
`text
45  `

### 5️⃣ Multiply  
`text
362880  `








