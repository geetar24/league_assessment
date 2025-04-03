Matrix Processor App
Spring Boot (Java 17) + React (Node.js 16+)
Perform matrix operations (Echo, Invert, Flatten, Sum, Multiply) via CSV uploads.

🛠️ Installation Guide
1. Install Prerequisites
Java 17 (Backend)
Windows:
Download from Oracle JDK 17 → Run installer → Set JAVA_HOME.

macOS/Linux:
brew install openjdk@17  # macOS
sudo apt install openjdk-17-jdk  # Linux
Verify:

bash
 
java -version  # Expected: "17.x.x"
Node.js 16+ & npm (Frontend)
Download from Node.js → Run installer.
Verify:

bash
 
node -v  # Expected: "v16.x.x" or higher
npm -v   # Expected: "8.x.x" or higher
Maven (Backend Build)
Windows: Download Maven → Unzip → Set MAVEN_HOME.

macOS/Linux:

bash
brew install maven  # macOS
sudo apt install maven  # Linux
Verify:

bash
mvn -v  # Expected: "Apache Maven 3.8.x"
🚀 Running the Application
1. Clone the Repository
bash
 
git clone https://github.com/your-username/your-repo.git
cd your-repo
2. Start Spring Boot Backend
bash 
cd matrix-backend
mvn clean install  # Build dependencies
mvn spring-boot:run  # Start server
✅ Expected Output:

 
Tomcat started on port(s): 8081
Started MatrixApplication in 2.305 seconds
Test Backend:

bash 
curl http://localhost:8081/api/hello
# Expected: "Backend is running!"
3. Start React Frontend
bash
cd ../frontend
npm install  # Install dependencies
npm start   # Launch development server
✅ Expected Output:

Automatically opens http://localhost:3000 in browser.

Console shows:
 
Compiled successfully!
🖥️ Using the Application
1. Prepare a CSV File
Create matrix.csv:

 
1,2,3
4,5,6
7,8,9
2. Perform Operations
Upload matrix.csv via the React interface.

Select Operation:
Echo
Expected Output: 
1,2,3
4,5,6
7,8,9
Invert
Expected Output: 
1,4,7
2,5,8
3,6,9
Sum
Expected Output: 45

3. Command-Line Testing (Optional)
bash
 
# Echo
curl -X POST -F "file=@matrix.csv" http://localhost:8081/api/echo

# Sum
curl -X POST -F "file=@matrix.csv" http://localhost:8081/api/sum

🐛 Troubleshooting
Issue	Solution
Port conflicts	Change ports in:
matrix-backend/src/main/resources/application.properties (Backend)
frontend/.env (Frontend)
npm install fails	Delete node_modules/ and re-run
Maven build errors	Run mvn clean install -U

📦 Production Build
Backend (JAR)
bash 
cd matrix-backend
mvn clean package
java -jar target/matrix-backend-0.0.1-SNAPSHOT.jar
Frontend (Optimized Build)
bash 
cd frontend
npm run build  # Outputs to /build
