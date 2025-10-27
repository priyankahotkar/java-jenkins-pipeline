# Java Jenkins Pipeline Project

This project demonstrates a **Jenkins CI/CD Pipeline** for building and running a simple Java application using Maven.

## 📘 Project Overview

- **Language:** Java (JDK 17)
- **Build Tool:** Maven
- **Pipeline Tool:** Jenkins
- **Author:** Priyanka Hotkar
- **Repository Name:** java-jenkins-pipeline

---

## 📁 Project Structure
```
java-jenkins-pipeline/
│
├── src/
│   └── main/
│       └── java/
│           └── HelloWorld.java
├── pom.xml
├── Jenkinsfile
└── README.md
```

---

## 🚀 How to Run

### Step 1: Clone Repository
```bash
git clone https://github.com/priyankahotkar/java-jenkins-pipeline.git
cd java-jenkins-pipeline
```

### Step 2: Build Using Maven
```bash
mvn clean package
```

### Step 3: Run Application
```bash
java -jar target/java-jenkins-pipeline-1.0-SNAPSHOT.jar
```

Output:
```
Hello from Priyanka’s Java Jenkins Pipeline!
```

---

## ⚙️ Jenkins Pipeline Setup

1. **Install Jenkins** and configure tools:
   - JDK 17 (named `Java17`)
   - Maven 3 (named `Maven3`)

2. **Create New Pipeline**
   - Go to Jenkins Dashboard → *New Item*
   - Enter name: `Java-Build-Pipeline`
   - Select **Pipeline** → OK
   - Under *Pipeline from SCM* → Choose **Git**
   - Enter Repo URL: `https://github.com/priyankahotkar/java-jenkins-pipeline.git`
   - Script Path: `Jenkinsfile`
   - Save

3. **Build the Pipeline**
   - Click **Build Now**.
   - Check console output — you should see `BUILD SUCCESS` and the Java app output.

---

## 🧱 Jenkinsfile Stages
1. **Checkout** → Pulls latest code
2. **Build** → Compiles Java source
3. **Test** → Runs unit tests (if present)
4. **Package** → Creates JAR file
5. **Run Application** → Executes the Java program

---

## 🧩 Output in Jenkins Console
```
[INFO] BUILD SUCCESS
Hello from Priyanka’s Java Jenkins Pipeline!
Pipeline execution completed.
```

---

### ✅ Author
**Priyanka Hotkar**
