# Hybrid Facial Biometric Authentication System (Java)

## 🔐 Overview
This project implements a **secure hybrid facial biometric authentication system** using **Java and OpenCV**, designed with **security, privacy, and real-world deployment considerations** in mind.

The system follows a **hybrid architecture**, separating responsibilities between a **client application** and a **backend service** to reduce attack surface, protect biometric data, and demonstrate enterprise-grade authentication design.

This project is intended as a **cybersecurity and software engineering portfolio project**.

---

## 🎯 Project Goals
- Implement secure **biometric enrollment and authentication**
- Avoid storage of raw biometric images
- Protect biometric templates using **encryption**
- Demonstrate **liveness detection** and **anti-spoofing** concepts
- Apply **secure software architecture** principles
- Showcase real-world **IAM and Zero Trust design thinking**

---

## 🧠 Architecture Overview (Hybrid Model)

### Why Hybrid?
A hybrid architecture mirrors how **modern biometric authentication systems** are built in banking, healthcare, and enterprise environments.

### Key Design Decisions
- Facial images are processed **client-side**
- Only **feature vectors** are transmitted to the backend
- Biometric templates are **encrypted at rest**
- Communication is secured using **TLS**
- Clear trust boundaries between client and server

---

## 🏗️ High-Level Architecture

Client Application (Java)
├─ Webcam Capture
├─ Face Detection
├─ Liveness Detection
├─ Feature Extraction
└─ Secure API Client
↓ (TLS + Encrypted Payload)
Backend Service (Java)
├─ Enrollment Service
├─ Matching Engine
├─ Encrypted Template Store
└─ Authentication Decision

---

## 🔑 Authentication Workflows

### Enrollment Flow
1. User captures facial data via webcam
2. Face is detected and validated
3. Liveness checks are performed
4. Facial features are extracted
5. Feature vector is encrypted
6. Encrypted template is sent to backend
7. Template is stored securely

### Authentication Flow
1. User presents face for authentication
2. Liveness detection is performed
3. Facial features are extracted
4. Feature vector is encrypted
5. Backend compares against stored templates
6. Match score is calculated
7. Authentication decision is returned

---

## 🔒 Security Considerations

This project intentionally emphasizes **security-first design**:

- No raw facial images stored
- Encrypted biometric templates
- TLS-secured communication
- Replay attack mitigation
- Threshold-based matching logic
- Designed for MFA integration
- STRIDE threat modeling applied

---

## 🛠️ Technology Stack

| Layer | Technology |
|----|----|
| Programming Language | Java |
| Computer Vision | OpenCV (Java bindings) |
| Build Tool | Maven |
| Client UI | JavaFX or Swing |
| Backend | Java REST API |
| Encryption | AES, PBKDF2 |
| Data Storage | Encrypted file system or database |

---

## 📁 Planned Project Structure

hybrid-facial-biometric-authentication/
├─ client/
│ ├─ src/main/java/
│ ├─ src/main/resources/
│ └─ pom.xml
├─ server/
│ ├─ src/main/java/
│ ├─ src/main/resources/
│ └─ pom.xml
├─ diagrams/
│ ├─ uml/
│ ├─ sequence/
│ └─ dataflow/
└─ README.md

---

## 🗺️ Roadmap (High-Level)
- [ ] Project setup (Maven, folder structure)
- [ ] Webcam capture and face detection
- [ ] Feature extraction
- [ ] Secure enrollment workflow
- [ ] Matching and authentication logic
- [ ] Template encryption and storage
- [ ] Liveness detection
- [ ] UML, sequence, and data flow diagrams
- [ ] Security hardening and documentation

---

## 🚀 Future Enhancements
- Multi-user support
- MFA (Face + PIN / Password)
- Behavioral biometrics integration
- Audit logging and monitoring
- Database-backed storage
- Containerization (Docker)

---

## ⚠️ Disclaimer
This project is for **educational and portfolio purposes only**.  
It is **not intended for production use** without additional security hardening, testing, and compliance review.

---

## 👤 Author
**Patrick Barredo**  
Cybersecurity & Software Engineering Portfolio Project
