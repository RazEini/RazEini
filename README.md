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
    <img src="https://skillicons.dev/icons?i=androidstudio,firebase,flask,cmake,grafana,linux,docker,git,githubactions,github" alt="Tools" />
  </a>
</p>

---

## 💻 Core Technical Competencies

* **Low-Level, Binary Exploitation & Reverse Engineering:**
  Linux ELF Binaries, Memory Safety & Corruption (Buffer Overflows), Dynamic Debugging (`GDB` + `GEF`), Disassembly (`Ghidra`), Exploit Automation (`pwntools`, C, Python).

* **Networking & Security Observability:**
  OSI & TCP/IP (L2–L7), Deep Packet Inspection (DPI), Raw Sockets, Traffic Analysis & Intrusion Detection (DoS/Port Scans), Infrastructure-as-Code (`Grafana`, `Loki`, `Promtail`).

* **Cryptography & Vault Architecture:**
  Symmetric Encryption (AES-128-CBC / Fernet, HMAC-SHA256), Key Derivation (PBKDF2), Dynamic Threat Mitigation, Password Hashing & Salting.

* **Backend Systems & Concurrency:**
  Multi-threaded Architecture (Producer-Consumer Pipelines), Thread Synchronization (`threading.Lock`), C-FFI / Native Extensions (`ctypes`), Event-Driven Architecture (`watchdog`).

* **DevOps & Infrastructure:**
  CI/CD (`GitHub Actions`), Containerization (`Docker`), Infrastructure Automation & Scripting (`Bash`), PyPI Packaging, Automated Testing (`pytest`).

---

## 🚀 Featured Projects

### 🕵️ [NetGuard – Hybrid Python/C NIDS & Observability Engine](https://github.com/RazEini/NetGuard) 
> **High-Performance Network Intrusion Detection System with Dual-Layer DPI & Observability Stack**
* **Motivation:** Building an enterprise-grade NIDS to perform real-time L3-L7 network monitoring, multi-pattern payload scanning, active defense, and dynamic threat mitigation.
* **The Challenge:** Overcoming Python's FFI overhead and GIL bottlenecks during deep packet inspection (DPI) under heavy traffic while ensuring **Memory Safety** and preventing buffer over-reads on raw binary traffic — including diagnosing and fixing a false-positive signature match against encrypted traffic during live testing.
* **Key Learning:** Implemented a dual-layer live DPI pipeline — an Aho-Corasick automaton for keyword signatures alongside a **Native C DPI Engine (ctypes)** using bounds-checked memory operations (`memchr`/`memcmp`) for injection-pattern signatures, measured at an **8x throughput speedup in isolated benchmarking (~2.5M pkts/sec)** with zero crash risk on invalid network frames. Mastered Producer-Consumer queues, thread safety (`threading.Lock`), background GC routines, and **Dashboards-as-Code**.
* **Tech Stack:** Python, Native C Extension (GCC/ctypes), Scapy, Multithreading, Docker Compose, Grafana, Loki, Promtail, JSON Structured Logging, IaC.
<p align="left">
  <a href="https://github.com/RazEini/NetGuard">
    <br>
    <img src="https://img.shields.io/badge/View_Code-GitHub-24292e?style=for-the-badge&logo=github" />
  </a>
</p>

---

### 🚩 [CTF Writeups & Binary Exploitation](https://github.com/RazEini/ctf-writeups) 
> **Personal security research repository containing binary exploitation exploits, writeups, and reverse engineering analysis**

* **Motivation:** Deepening practical skills in low-level vulnerabilities, memory safety, binary analysis, and reverse engineering techniques.
* **The Challenge:** Analyzing unknown compiled ELF binaries, identifying memory corruption flaws (e.g., Buffer Overflows, format string bugs), and crafting reliable exploits to redirect execution flow.
* **Key Learning:** Advanced dynamic analysis with **GDB + GEF**, static analysis using **Ghidra**, shellcode execution, and automating exploit scripts via **pwntools**.
* **Tech Stack & Tools:** C, Python, Pwntools, GDB (GEF), Ghidra, Linux (WSL2/Ubuntu), Bash.

<p align="left">
  <a href="https://github.com/RazEini/ctf-writeups">
    <br>
    <img src="https://img.shields.io/badge/View_Code-GitHub-24292e?style=for-the-badge&logo=github" />
  </a>
</p>

---

### 🔐 [Password Manager](https://github.com/RazEini/Password_Manager) 
> **Secure, modular CLI/TUI password manager published on PyPI with automated CI/CD**

* **Motivation:** Moving away from third-party managers to build a production-ready personal vault, implement secure cryptography from scratch, and master end-to-end software packaging.
* **The Challenge:** Correctly implementing **Fernet symmetric encryption** (AES-128-CBC & HMAC-SHA256), **PBKDF2** key derivation, an interactive arrow-key TUI (`questionary`/`rich`), and a fully automated PyPI release pipeline via GitHub Actions.
* **Key Learning:** Masterclass in **Cybersecurity fundamentals**, software modularity, robust exception flows, and end-to-end DevOps automation from local testing to global package distribution.
* **Tech Stack:** Python, Cryptography, Pyperclip, Rich, Questionary, Pytest, GitHub Actions (CI/CD), PyPI.

<p align="left"><a href="https://pypi.org/project/razeini-password-manager/"><img src="https://img.shields.io/pypi/v/razeini-password-manager.svg?style=for-the-badge&logo=pypi&logoColor=white"/></a> &nbsp; <a href="https://github.com/RazEini/Password_Manager"><img src="https://img.shields.io/badge/View_Code-GitHub-24292e?style=for-the-badge&logo=github"/></a></p>

---

## 📊 My GitHub Metrics

<br>
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats-fast.vercel.app/api?username=RazEini&show_icons=true&theme=github_dark&hide_rank=true">
    <source media="(prefers-color-scheme: light)" srcset="https://github-readme-stats-fast.vercel.app/api?username=RazEini&show_icons=true&theme=default&hide_rank=true">
    <img src="https://github-readme-stats-fast.vercel.app/api?username=RazEini&show_icons=true&theme=default&hide_rank=true&hide_border=true" width="28%" alt="GitHub Stats" />
  </picture>
  &nbsp;
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats-fast.vercel.app/api/top-langs/?username=RazEini&layout=compact&theme=github_dark&hide=java%2Cjavascript%2Cjs%2Chtml%2Ccss&cache_bust=2">
    <source media="(prefers-color-scheme: light)" srcset="https://github-readme-stats-fast.vercel.app/api/top-langs/?username=RazEini&layout=compact&theme=default&hide=java%2Cjavascript%2Cjs%2Chtml%2Ccss&cache_bust=2">
    <img src="https://github-readme-stats-fast.vercel.app/api/top-langs/?username=RazEini&layout=compact&theme=default&hide=java%2Cjavascript%2Cjs%2Chtml%2Ccss&cache_bust=2&hide_border=true" width="32%" alt="Top Languages" />
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
