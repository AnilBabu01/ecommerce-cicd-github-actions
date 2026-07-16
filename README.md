# 🏏 Cricket Application - Full Stack DevOps Deployment

A production-ready Full Stack Cricket Application consisting of **Cricket-Frontend**, **Cricket-Admin**, and **Cricket-Backend** deployed on **AWS EC2** using **GitHub Actions CI/CD**, **PostgreSQL**, **PM2**, **Nginx**, **Route53**, and **Let's Encrypt SSL**.

---

# 📌 Project Overview

This project demonstrates a complete DevOps implementation for deploying a production-ready MERN/Node.js application using AWS cloud services and CI/CD best practices.

### Features

- Cricket Frontend (React)
- Cricket Admin Panel (React)
- Cricket Backend (Node.js + Express)
- PostgreSQL Database
- GitHub Actions CI/CD
- AWS EC2 Deployment
- PM2 Process Manager
- Nginx Reverse Proxy
- Route53 DNS Configuration
- SSL using Let's Encrypt
- Zero manual deployment after Git Push

---

# 📂 Repository Structure

```
cricket-app/
│
├── cricket-admin/
│
├── cricket-backend/
│
├── cricket-frontend/
│
├── .github/
│   └── workflows/
│       └── deploy.yml
│
└── README.md
```

---

# 🛠 Technology Stack

| Category | Technology |
|----------|------------|
| Frontend | React.js |
| Admin | React.js |
| Backend | Node.js, Express |
| Database | PostgreSQL |
| CI/CD | GitHub Actions |
| Cloud | AWS EC2 |
| DNS | Route53 |
| Reverse Proxy | Nginx |
| Process Manager | PM2 |
| SSL | Let's Encrypt |
| Version Control | Git & GitHub |

---

# 🌐 Production URLs

| Service | URL |
|----------|------|
| Frontend | https://ffindiano1.xyz |
| Admin | https://admin.ffindiano1.xyz |
| Backend API | https://api.ffindiano1.xyz |

---

# 🏗 Architecture

```
                    Git Push
                       │
                       ▼
                 GitHub Repository
                       │
                       ▼
               GitHub Actions CI/CD
                       │
                       ▼
                 AWS EC2 Ubuntu
                       │
        ┌──────────────┼──────────────┐
        │              │              │
        ▼              ▼              ▼
 Frontend         Backend          Admin
  React            Node            React
  PM2              PM2             PM2
        │              │              │
        └──────────────┼──────────────┘
                       ▼
                     Nginx
                       │
               Route53 + SSL
                       │
                       ▼
                  Internet Users

Backend
      │
      ▼
 PostgreSQL Database
```

---

# ☁ AWS Infrastructure

Server Configuration

```
Ubuntu 24.04 LTS

t3.medium

30 GB Storage
```

Security Group

```
22 SSH

80 HTTP

443 HTTPS

3000 Frontend

3001 Backend

3002 Admin
```

---

# 🚀 Deployment Workflow

```
Developer

↓

Git Push

↓

GitHub Repository

↓

GitHub Actions

↓

SSH into EC2

↓

Git Pull

↓

Install Dependencies

↓

Build React Applications

↓

Restart PM2

↓

Application Live
```

---

# 📦 Backend Setup

Navigate

```bash
cd cricket-backend
```

Install packages

```bash
npm install
```

Run locally

```bash
npm run dev
```

Production

```bash
npm start
```

Package.json

```json
{
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js"
  }
}
```

---

# 🗄 PostgreSQL Setup

Install PostgreSQL

```bash
sudo apt install postgresql postgresql-contrib -y
```

Create Database

```sql
CREATE DATABASE cricketdb;
```

Create User

```sql
CREATE USER cricketuser
WITH PASSWORD 'StrongPassword123';
```

Grant Permissions

```sql
GRANT ALL PRIVILEGES
ON DATABASE cricketdb
TO cricketuser;
```

---

# 🔐 Environment Variables

Backend

```
PORT=3001

DB_HOST=localhost

DB_PORT=5432

DB_NAME=cricketdb

DB_USER=cricketuser

DB_PASSWORD=StrongPassword123
```

---

# ⚙ PM2 Configuration

Backend

```bash
pm2 start server.js --name cricket-backend
```

Frontend

```bash
pm2 serve build 3000 --name cricket-frontend
```

Admin

```bash
pm2 serve build 3002 --name cricket-admin
```

Save

```bash
pm2 save
```

Auto Start

```bash
pm2 startup
```

---

# 🌍 Route53 Configuration

Hosted Zone

```
ffindiano1.xyz
```

DNS Records

```
ffindiano1.xyz

↓

EC2 Public IP
```

```
admin.ffindiano1.xyz

↓

EC2 Public IP
```

```
api.ffindiano1.xyz

↓

EC2 Public IP
```

---

# 🌐 Nginx Reverse Proxy

Frontend

```
ffindiano1.xyz

↓

localhost:3000
```

Admin

```
admin.ffindiano1.xyz

↓

localhost:3002
```

Backend

```
api.ffindiano1.xyz

↓

localhost:3001
```

---

# 🔒 SSL Configuration

Install Certbot

```bash
sudo apt install certbot python3-certbot-nginx -y
```

Generate SSL

```bash
sudo certbot --nginx
```

Domains

```
ffindiano1.xyz

admin.ffindiano1.xyz

api.ffindiano1.xyz
```

---

# 🔄 GitHub Actions CI/CD

Workflow

```
Push Code

↓

Checkout Repository

↓

Install Dependencies

↓

Build React Apps

↓

SSH to EC2

↓

Git Pull

↓

Install Packages

↓

Restart PM2

↓

Deployment Completed
```

GitHub Secrets

```
EC2_HOST

EC2_USER

EC2_KEY
```

---

# 📊 PM2 Monitoring

Check running applications

```bash
pm2 list
```

Logs

```bash
pm2 logs
```

Status

```bash
pm2 status
```

Restart

```bash
pm2 restart all
```

---

# 📁 Useful Commands

Clone Repository

```bash
git clone <repository-url>
```

Install Dependencies

```bash
npm install
```

Build React

```bash
npm run build
```

Run Backend

```bash
npm start
```

Restart PM2

```bash
pm2 restart all
```

Restart Nginx

```bash
sudo systemctl restart nginx
```

Restart PostgreSQL

```bash
sudo systemctl restart postgresql
```

---

# 📈 CI/CD Flow

```
Developer

↓

Git Commit

↓

Git Push

↓

GitHub

↓

GitHub Actions

↓

SSH

↓

EC2

↓

Git Pull

↓

npm install

↓

npm run build

↓

pm2 restart

↓

Production
```

---

# 📋 Deployment Checklist

- AWS EC2 Created
- Ubuntu Configured
- Node.js Installed
- PostgreSQL Installed
- Database Created
- Repository Cloned
- Backend Configured
- Frontend Configured
- Admin Configured
- PM2 Installed
- Nginx Configured
- Route53 DNS Configured
- SSL Enabled
- GitHub Secrets Added
- GitHub Actions Configured
- CI/CD Pipeline Working
- Production Deployment Successful

---

# 🎯 Key DevOps Skills Demonstrated

- AWS EC2 Deployment
- Linux Server Administration
- PostgreSQL Database Management
- Git Version Control
- GitHub Actions CI/CD
- PM2 Process Management
- Nginx Reverse Proxy
- Route53 DNS Management
- SSL/TLS Configuration
- Environment Variable Management
- Production Deployment
- Zero-Downtime Application Deployment

---

# 👨‍💻 Author

**Anil Babu**

**Role:** Junior DevOps Engineer

### Skills

- AWS
- Linux
- Docker
- Kubernetes
- GitHub Actions
- Jenkins
- Terraform
- Ansible
- PostgreSQL
- Nginx
- PM2
- CI/CD
- DevOps

---

# ⭐ Project Highlights

✅ Full Stack Cricket Application

✅ Single GitHub Repository

✅ Production Ready Infrastructure

✅ Automated CI/CD Pipeline

✅ PostgreSQL Database

✅ AWS EC2 Deployment

✅ Route53 Domain Mapping

✅ Nginx Reverse Proxy

✅ HTTPS SSL Enabled

✅ PM2 Process Management

✅ Zero Manual Deployment

---