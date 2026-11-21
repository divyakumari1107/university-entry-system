# University Gate Entry System 🏛️

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-success?style=for-the-badge&logo=github)](https://divyakumari1107.github.io/university-entry-system/)
[![Vercel Deployment](https://img.shields.io/badge/Deployed-Vercel-black.svg?logo=vercel)](https://university-entry-system.vercel.app/)
[![Java](https://img.shields.io/badge/Java-17-orange.svg)](pom.xml)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.3.4-brightgreen.svg)](pom.xml)
[![DevOps](https://img.shields.io/badge/DevOps-Docker%20%7C%20Kubernetes%20%7C%20Jenkins-blue.svg)](Jenkinsfile)
[![Database](https://img.shields.io/badge/Database-H2%20In--Memory-yellow.svg)](src/main/resources/application.properties)

A real-time QR-based university gate entry system built with Spring Boot, featuring a complete DevOps pipeline.

---

## 🌐 Live Production Deployments

This project includes a live interactive gate security dashboard and student mobile QR confirmation simulator:

| Resource | Live Link | Status |
| :--- | :--- | :--- |
| **University Gate Live Terminal (GitHub Pages)** | **[https://divyakumari1107.github.io/university-entry-system/](https://divyakumari1107.github.io/university-entry-system/)** | 🟢 **Live (24/7)** |
| **University Gate Live Mirror (Vercel)** | **[https://university-entry-system.vercel.app/](https://university-entry-system.vercel.app/)** | 🟢 **Production Ready** |

---

## 🚀 Features

- **Student Registration**: Register multiple students with name, registration number, and phone
- **QR Code Generation**: Automatic QR code generation for each student
- **Mobile Entry Confirmation**: Students scan QR on phone → Accept/Reject entry
- **Real-time Dashboard**: Security guard sees all entries with date, time, registration number
- **Database**: H2 in-memory database (persists during app runtime)

## 🛠️ Tech Stack

- **Backend**: Spring Boot 3.3.4, Java 17
- **Database**: H2 (in-memory)
- **Frontend**: Thymeleaf templates
- **DevOps**: Maven → Jenkins → Docker → Kubernetes

## 📦 Quick Start (Local)

```bash
# Clone repository
git clone <your-github-repo-url>
cd powerCA2

# Run application
mvn clean spring-boot:run

# Access application
# PC: http://localhost:9090/
# Students: http://localhost:9090/students
```

## 🌐 Free Deployment Options

### Option 1: Railway (Recommended - 100% Free)

1. Go to https://railway.app
2. Sign up with GitHub
3. Click **"New Project"** → **"Deploy from GitHub repo"**
4. Select your repository
5. Railway auto-detects Dockerfile and deploys
6. Get your URL: `https://your-app.railway.app`

**That's it!** Your app is live for free.

### Option 2: Render (Free Tier)

1. Go to https://render.com
2. Sign up with GitHub
3. Click **"New"** → **"Web Service"**
4. Connect your GitHub repo
5. Set **Environment**: `Docker`
6. Click **"Deploy"**

### Option 3: Fly.io (Free Tier)

```bash
# Install flyctl
# Then:
fly launch
fly deploy
```

## 🔧 DevOps Pipeline

This project demonstrates:
- ✅ **Git** - Source code version control
- ✅ **Maven** - Build automation (`pom.xml`)
- ✅ **Jenkins** - CI/CD pipeline (`Jenkinsfile`)
- ✅ **Docker** - Containerization (`Dockerfile`)
- ✅ **Kubernetes** - Orchestration (`k8s/`)

See `DEPLOYMENT.md` for detailed pipeline setup.

## 📱 How to Use

1. **Register Students** (PC):
   - Go to `http://localhost:9090/students`
   - Fill form: Name, Registration Number, Phone
   - Click "Save Student"
   - QR code appears automatically

2. **Scan QR** (Student's Phone):
   - Student scans QR code
   - Phone shows Accept/Reject page
   - Tap **Accept** → Entry recorded

3. **View Entries** (Security PC):
   - Go to `http://localhost:9090/`
   - See all entries with:
     - Student name
     - Registration number
     - Phone number
     - Entry date & time

## 📁 Project Structure

```
powerCA2/
├── src/main/java/com/university/gate/
│   ├── controller/     # Web controllers
│   ├── model/          # Entity classes
│   ├── repository/     # Data repositories
│   └── service/        # Business logic
├── src/main/resources/
│   ├── templates/      # Thymeleaf HTML pages
│   └── application.properties
├── Dockerfile          # Docker configuration
├── Jenkinsfile         # Jenkins pipeline
├── k8s/                # Kubernetes manifests
└── pom.xml             # Maven dependencies
```

## 🔐 Environment Variables

For production deployment, set:
- `PORT` - Server port (auto-detected on Railway/Render)
- `SPRING_PROFILES_ACTIVE=prod` (optional)

## 📝 License

This project is for educational purposes (DevOps pipeline demonstration).

## 🤝 Contributing

This is a university project demonstrating DevOps practices.

---

**Made with ❤️ for DevOps Pipeline Demonstration**
