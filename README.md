# Hi, I'm Raz Eini 👋  
### Software Engineering Student | Security & Backend Focus

🎓 B.Sc. Software Engineering student at **Afeka College** (Academic Reserve – Atuda) <br><br>
💡 I build clean, practical, and maintainable software for real-world problems <br><br>
🔍 Continuously learning new technologies and hands-on software development

---

## 🛠️ Tech Stack

**Languages**  

<p align="left">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=c,java,kotlin,python,bash,html,css,js" alt="Languages" />
  </a>
</p>

**Frameworks & Tools**  

<p align="left">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=androidstudio,firebase,flask,linux,docker,git,github" alt="Tools" />
  </a>
</p>

---

## 💻 Core Engineering Concepts

* **Low-Level Analysis & Reverse Engineering:** 
  x86_64 Architecture, CPU Registers (`rax`, `rbp`, `rsp`), Stack Frame Layouts, Memory Inspection (`gdb`), Disassembly Analysis, Memory Endianness, and Binary Exploitation Fundamentals.

* **Cybersecurity & Cryptography:** 
  Modern Symmetric Encryption (Fernet / AES-128-CBC & HMAC-SHA256), Key Derivation Functions (PBKDF2-HMAC-SHA256), Password Hashing & Salting, Vault Architecture, Security-First Workflows, Dynamic Threat Mitigation.

* **Networking & Security Observability:** 
  OSI Model & TCP/IP Stack (L2–L7), Deep Packet Inspection (DPI), Raw Sockets, Traffic Analysis, Real-Time Intrusion Detection (DoS/Port Scans), Infrastructure-as-Code (Grafana, Loki, Promtail, Structured JSON Logging).

* **Backend Systems, Concurrency & State Management:** 
  Multi-threaded Architectures (Producer-Consumer Pipelines), Thread Synchronization (`threading.Lock`), Custom In-Memory Cleanup Routines, Event-Driven File Monitoring (`watchdog`), State Persistence.

* **DevOps, Shell Scripting & Infrastructure Automation:** 
  Automated Infrastructure Deployment & Shell Scripting (`Bash`), Containerization & Orchestration (Docker, Docker Network, Multi-Volume Persistence), Automated CI/CD Pipelines (GitHub Actions), Backup & Recovery Workflows (`mysqldump`, Volume Management), Unit Testing (`pytest`).

* **Software Architecture & Full-Stack Engineering:** 
  OOP Principles (Polymorphism, Encapsulation), Custom Exception Flow, Clean Architecture & MVVM, Modern Mobile Stack (Android, Jetpack Compose, StateFlow), Web APIs & RESTful Services (Flask).

---

## 🚀 Featured Projects

### 🚩 [picoCTF Writeups & Low-Level Labs](https://github.com/RazEini/picoCTF-Writeups) 
> **Hands-on binary analysis, dynamic memory inspection, and reverse engineering**

* **Motivation:** Mastering low-level systems execution, assembly language, and debugging workflows from the ground up to prepare for advanced security analysis.
* **The Challenge:** Analyzing compiled ELF binaries, tracking stack/register states in GDB, and dynamically reconstructing memory without source code.
* **Key Learning:** Advanced GDB debugging, x86_64 calling conventions, stack inspection (`x/s`), memory endianness, and control flow analysis.
* **Tech Stack:** C / Assembly (x86_64), GDB, Linux (WSL2 / Ubuntu), GCC.

<p align="left">
  <a href="https://github.com/RazEini/picoCTF-Writeups">
    <br>
    <img src="https://img.shields.io/badge/View_Code-GitHub-24292e?style=for-the-badge&logo=github" />
  </a>
</p>

---

### 🔐 [Password Manager](https://github.com/RazEini/Password_Manager) 
> **Secure vault implementation using industry-standard encryption protocols**

* **Motivation:** Moving away from third-party managers to build a personal "vault" and fully understand encryption "under the hood."
* **The Challenge:** Correctly implementing **Fernet symmetric encryption** (AES-128-CBC & HMAC-SHA256) and **PBKDF2** key derivation while maintaining a clean, modular architecture.
* **Key Learning:** Masterclass in **Cybersecurity fundamentals**: Salting, Hashing, Key Derivation Functions (KDF), and secure local storage. Developed a "security-first" mindset and CI/CD automation.
* **Tech Stack:** Python, Cryptography (Fernet: AES-128-CBC + HMAC-SHA256), PBKDF2-HMAC-SHA256, Pytest, GitHub Actions (CI/CD).

<p align="left">
  <a href="https://github.com/RazEini/Password_Manager">
    <br>
    <img src="https://img.shields.io/badge/View_Code-GitHub-24292e?style=for-the-badge&logo=github" />
  </a>
</p>

---

### 🕵️ [NetGuard – Full-Stack NIDS & Observability Engine](https://github.com/RazEini/python_sniffer) 
> **Real-time Network Intrusion Detection System & Security Observability Stack**

* **Motivation:** Building an enterprise-grade NIDS to perform real-time L2-L7 network monitoring, deep packet inspection (DPI), active defense, and dynamic threat mitigation.
* **The Challenge:** Handling high-throughput network traffic without memory leaks or packet loss using a multi-threaded Producer-Consumer pipeline, along with seamless observability integration.
* **Key Learning:** Deep mastery of **OSI/TCP-IP stacks**, real-time anomaly detection (DoS/Port Scans), thread-safety (`threading.Lock`), custom background garbage collection, and **Dashboards-as-Code**.
* **Tech Stack:** Python, Scapy, Multithreading, Docker Compose, Grafana, Loki, Promtail, JSON Structured Logging, IaC.

<p align="left">
  <a href="https://github.com/RazEini/python_sniffer">
    <br>
    <img src="https://img.shields.io/badge/View_Code-GitHub-24292e?style=for-the-badge&logo=github" />
  </a>
</p>

---

### 🛒 [E-Commerce Shop](https://github.com/RazEini/e_commerce_shop) 
> **Real-time data synchronization & complex state management**

* **Motivation:** Understanding how large-scale consumer apps maintain data consistency between thousands of users and an admin dashboard.
* **The Challenge:** Implementing a real-time shopping cart that syncs across multiple devices and handles instant inventory updates during checkout.
* **Key Learning:** Mastered **Firebase Realtime Database** and user authentication. Designed an Admin Panel that simplifies complex management tasks.
* **Tech Stack:** Android (Java), Firebase.

<p align="left">
  <a href="https://github.com/RazEini/e_commerce_shop">
    <br>
    <img src="https://img.shields.io/badge/View_Code-GitHub-24292e?style=for-the-badge&logo=github" />
  </a>
</p>

---

### 🧠 [Smart Task Flow](https://github.com/RazEini/Smart_Task_Flow) 
> **Automated prioritization logic & modern Android UI with Jetpack Compose**

* **Motivation:** Most task managers are just "to-do lists" that eventually become cluttered. I built a tool that actively helps with decision-making—telling me *what* to do next based on priority and urgency.
* **The Challenge:** Designing an automated prioritization logic that feels intuitive and doesn't overwhelm the user.
* **Key Learning:** Deep dive into **Jetpack Compose** and **MVVM** architecture. Managed complex UI states while keeping business logic clean and decoupled.
* **Tech Stack:** Kotlin, Firebase, Jetpack Compose.

<p align="left">
  <a href="https://github.com/RazEini/Smart_Task_Flow">
    <br>
    <img src="https://img.shields.io/badge/View_Code-GitHub-24292e?style=for-the-badge&logo=github" />
  </a>
</p>

---

### 📂 [Smart File Organizer](https://github.com/RazEini/SmartFileOrganizer) 
> **Intelligent desktop automation tool for efficient file system management**

* **Motivation:** Solving the "cluttered folders" problem by building a robust system that automates file categorization and monitoring in the background.
* **The Challenge:** Implementing a reliable **Undo/Redo** system based on operation history and managing real-time file system events without data loss.
* **Key Learning:** Gained deep experience in **Event-driven programming** using the Watchdog library and modern GUI development with `ttkbootstrap`.
* **Tech Stack:** Python, Watchdog, ttkbootstrap.

<p align="left">
  <a href="https://github.com/RazEini/SmartFileOrganizer">
    <br>
    <img src="https://img.shields.io/badge/View_Code-GitHub-24292e?style=for-the-badge&logo=github" />
  </a>
</p>

---

## 📊 My GitHub Metrics

<br>
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats-fast.vercel.app/api?username=RazEini&show_icons=true&theme=github_dark">
    <source media="(prefers-color-scheme: light)" srcset="https://github-readme-stats-fast.vercel.app/api?username=RazEini&show_icons=true&theme=default">
    <img src="https://github-readme-stats-fast.vercel.app/api?username=RazEini&show_icons=true&theme=default&hide_border=true" width="42.5%" alt="GitHub Stats" />
  </picture>
  &nbsp;
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats-fast.vercel.app/api/top-langs/?username=RazEini&layout=compact&theme=github_dark">
    <source media="(prefers-color-scheme: light)" srcset="https://github-readme-stats-fast.vercel.app/api/top-langs/?username=RazEini&layout=compact&theme=default">
    <img src="https://github-readme-stats-fast.vercel.app/api/top-langs/?username=RazEini&layout=compact&theme=default&hide_border=true" width="32%" alt="Top Languages" />
  </picture>
</p>

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/RazEini/RazEini/output/github-snake-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/RazEini/RazEini/output/github-snake.svg">
    <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/RazEini/RazEini/output/github-snake.svg">
  </picture>
</div>

---

## 📫 Contact

> 🤝 Let's Connect! Whether it's about a project or a potential opportunity, I'm just a message away.

<br>

[![GitHub](https://img.shields.io/badge/GitHub-24292e?style=for-the-badge&logo=github)](https://github.com/RazEini)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/raz-eini-9875a8394)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:razeini972@gmail.com)
[![Resume](https://img.shields.io/badge/Resume-PDF-2EA44F?style=for-the-badge&logoColor=white)](https://github.com/RazEini/RazEini/raw/main/Raz_Eini_Resume.pdf)
