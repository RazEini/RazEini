# Hi, I'm Raz Eini 👋  
### Software Engineering Student | Security & Backend Focus

[![committers.top badge](https://user-badge.committers.top/israel/RazEini.svg)](https://committers.top/israel/RazEini)

[![XERJ Corpus Hub contributor](https://hub.xerj.org/contributors/RazEini/badge.svg)](https://hub.xerj.org/contributors/RazEini)


🎓 B.Sc. Software Engineering student at **Afeka College** (Academic Reserve – Atuda) <br><br>
🔐 Focused on network security, binary exploitation and systems programming <br><br>
💡 I build clean, practical, and maintainable software, and I test and benchmark what I build

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
  Linux ELF Binaries (32/64-bit), Memory Safety & Corruption (Buffer Overflows), Dynamic Debugging (`GDB` + `GEF`), Mitigation Analysis (`checksec`: Canary, NX, PIE), Static Analysis (`Ghidra`), Exploit Automation (`pwntools`, C, Python).

* **Networking & Security Observability:**
  OSI & TCP/IP (L2–L7), Deep Packet Inspection (DPI), Raw Sockets (`Scapy`), Traffic Analysis & Intrusion Detection (DoS, Port & Stealth Scans, DNS Tunneling), Active Defense (time-limited firewall blocks), Infrastructure-as-Code (`Grafana`, `Loki`, `Promtail`).

* **Cryptography & Vault Architecture:**
  Symmetric Encryption (AES-128-CBC / Fernet, HMAC-SHA256), Key Derivation (PBKDF2), Salting, Secure Vault Design.

* **Backend Systems & Concurrency:**
  Multi-threaded Architecture (Producer-Consumer Pipelines), Thread Synchronization (`threading.Lock`), C-FFI / Native Libraries (`ctypes`).

* **DevOps, Testing & Infrastructure:**
  CI/CD (`GitHub Actions`), Containerization (`Docker`), Automated Testing (`pytest`), Memory-Safety Fuzzing (`ASan` / `UBSan`), Infrastructure Automation & Scripting (`Bash`), PyPI Packaging.

---

## 🚀 Featured Projects

### 🕵️ [WireWarden – Hybrid Python/C NIDS & Observability Engine](https://github.com/RazEini/WireWarden) 
> **Real-Time Network Intrusion Detection & Prevention with Dual-Layer DPI & a Code-Managed Observability Stack**
* **Motivation:** Building a real-time NIDS/NIPS to monitor L3-L7 traffic, detect attacks, and respond through the OS firewall, while learning how network defense tools work internally.
* **The Challenge:** Scanning raw binary traffic quickly and safely: Python is slow per packet, the C engine must never read past a buffer (**Memory Safety**), and the system must avoid false positives (SYN-ACK replies, outbound traffic, encrypted payloads) and never block innocent hosts — including diagnosing and fixing a false-positive signature match against encrypted traffic during live testing.
* **Key Learning:** Implemented a dual-layer live DPI pipeline — an Aho-Corasick automaton for cleartext credentials alongside a **Native C DPI Engine (ctypes)** with 14 case-insensitive injection signatures and explicit bounds checks, scanning about **1M packets/s per call** (about 5x a naive Python loop, up to 1.5x Aho-Corasick on larger payloads). Profiling showed that Scapy dissection accounts for about 80% of per-packet time while all DPI is under 3%. Audited my own code and fixed 8 defects, each pinned by a regression test; **46 pytest tests**, C engine fuzzed under **ASan/UBSan**, GitHub Actions CI. Applied producer-consumer queues, thread safety (`threading.Lock`), time-limited firewall blocks, and **Dashboards-as-Code**.
* **Tech Stack:** Python, C (GCC/ctypes), Scapy, pytest, GitHub Actions, Multithreading, Docker Compose, Grafana, Loki, Promtail, JSON Structured Logging, IaC.
<p align="left">
  <a href="https://github.com/RazEini/WireWarden">
    <br>
    <img src="https://img.shields.io/badge/View_Code-GitHub-24292e?style=for-the-badge&logo=github" />
  </a>
</p>

---

### 🚩 [CTF Writeups & Binary Exploitation](https://github.com/RazEini/ctf-writeups) 
> **Personal security research repository with picoCTF binary-exploitation writeups, working exploit scripts, and mitigation analysis**

* **Motivation:** Deepening practical skills in low-level vulnerabilities, memory safety, and binary analysis, one documented challenge at a time.
* **The Challenge:** Analyzing compiled ELF binaries, identifying memory-corruption flaws (stack buffer overflows, function-pointer misuse, unchecked `gets()` / `strcpy()`), and crafting exploits that redirect execution flow or change program logic.
* **Key Learning:** Four solved challenges covering return-address overwrite on a 32-bit binary (offsets found with De Bruijn patterns in **GDB + GEF**), function-pointer redirection through symbol lookup, and targeted stack-variable overwrite. Read the decompiled code in **Ghidra** to understand each binary, did the exploit development itself in **GDB + GEF**, read `checksec` output to see which mitigations (Canary, NX, PIE) actually matter, and automated every exploit with **pwntools** against local and remote targets.
* **Status:** Ongoing. Next platform: ROP Emporium.
* **Tech Stack & Tools:** C, Python, pwntools, GDB (GEF), Ghidra, checksec, Linux (WSL2/Ubuntu), Bash.

<p align="left">
  <a href="https://github.com/RazEini/ctf-writeups">
    <br>
    <img src="https://img.shields.io/badge/View_Code-GitHub-24292e?style=for-the-badge&logo=github" />
  </a>
</p>

---

### 🔐 [Password Manager](https://github.com/RazEini/Password_Manager) 
> **Secure, modular CLI/TUI password manager published on PyPI with automated testing and releases**

* **Motivation:** Moving away from third-party managers to build a personal vault on vetted cryptographic primitives, and to learn end-to-end Python packaging and release automation.
* **The Challenge:** Correctly using **Fernet authenticated encryption** (AES-128-CBC & HMAC-SHA256) and **PBKDF2** key derivation (600,000 iterations, per OWASP guidance) with a per-vault salt, so the master password is never stored; plus storage that survives crashes and an interactive arrow-key TUI (`questionary`/`rich`).
* **Key Learning:** Auditing my own security tool and fixing what I found: atomic vault writes, owner-only file permissions, a self-clearing clipboard and an upgrade path for older vaults. Separated the cryptographic core from the CLI/TUI, covered it with **54 `pytest` tests (76% coverage)** running in CI on Python 3.10–3.13, and publish releases through **PyPI Trusted Publishing** (OIDC, signed attestations, approval-gated environment).
* **Tech Stack:** Python, Cryptography, Pyperclip, Rich, Questionary, Pytest, GitHub Actions (CI/CD, Trusted Publishing), PyPI.

<p align="left">
  <a href="https://pypi.org/project/razeini-password-manager/">
    <img src="https://img.shields.io/pypi/v/razeini-password-manager.svg?style=for-the-badge&logo=pypi&logoColor=white"/>
  </a>
  &nbsp;
  <a href="https://github.com/RazEini/Password_Manager">
    <img src="https://img.shields.io/badge/View_Code-GitHub-24292e?style=for-the-badge&logo=github"/>
  </a>
</p>

---

## 📊 My GitHub Metrics

<br>
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats-fast.vercel.app/api?username=RazEini&show_icons=true&theme=github_dark&hide_rank=true&cache_bust=4">
    <source media="(prefers-color-scheme: light)" srcset="https://github-readme-stats-fast.vercel.app/api?username=RazEini&show_icons=true&theme=default&hide_rank=true&cache_bust=4">
    <img src="https://github-readme-stats-fast.vercel.app/api?username=RazEini&show_icons=true&theme=default&hide_rank=true&hide_border=true&cache_bust=4" width="28%" alt="GitHub Stats" />
  </picture>
  &nbsp;
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats-fast.vercel.app/api/top-langs/?username=RazEini&layout=compact&theme=github_dark&hide=java%2Cjavascript%2Cjs%2Chtml%2Ccss&cache_bust=4">
    <source media="(prefers-color-scheme: light)" srcset="https://github-readme-stats-fast.vercel.app/api/top-langs/?username=RazEini&layout=compact&theme=default&hide=java%2Cjavascript%2Cjs%2Chtml%2Ccss&cache_bust=4">
    <img src="https://github-readme-stats-fast.vercel.app/api/top-langs/?username=RazEini&layout=compact&theme=default&hide=java%2Cjavascript%2Cjs%2Chtml%2Ccss&cache_bust=4&hide_border=true" width="32%" alt="Top Languages" />
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
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/raz-eini)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:razeini972@gmail.com)
[![Resume](https://img.shields.io/badge/Resume-PDF-2EA44F?style=for-the-badge&logoColor=white)](https://github.com/RazEini/RazEini/raw/main/Raz_Eini_Resume.pdf)
