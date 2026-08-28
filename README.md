<div align="center">

# 🔐 Cybersecurity & Ethical Hacking — Practical Project Modules

### 👩‍💻 by Arshiya Sharma

![Cybersecurity](https://img.shields.io/badge/Domain-Cybersecurity-critical?style=for-the-badge&logo=hackaday&logoColor=white)
![Kali Linux](https://img.shields.io/badge/OS-Kali%20Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white)
![Python](https://img.shields.io/badge/Language-Python%203-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Claude Desktop](https://img.shields.io/badge/AI-Claude%20Desktop-D97757?style=for-the-badge&logo=anthropic&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

*A hands-on documentation of my cybersecurity learning journey — from password hashing to AI‑assisted security automation.*

</div>

---

## 📌 Overview

This repository documents my hands-on learning journey through practical **Cybersecurity & Ethical Hacking Project Modules**, provided by **Networkwalks Academy**.

The modules focused on moving beyond theory into real, practical exposure to:

- 🔑 Password security & hashing
- 🧠 Wordlist-based password cracking
- 🐧 Linux security environments
- 🤖 AI-assisted security tooling
- 🔗 MCP-based security automation

> ⚠️ All work was performed in a **controlled lab/learning environment**, strictly for educational and cybersecurity training purposes.

---

## 🗂️ Table of Contents

- [🧪 Module 1 — Cybersecurity Practical Tasks](#-module-1--cybersecurity-practical-tasks)
- [🤖 Module 2 — Setting Up HexStrike MCP with Claude](#-module-2--setting-up-hexstrike-mcp-with-claude)
- [🧠 Overall Learning](#-overall-learning)
- [🛠️ Technologies & Tools](#️-technologies--tools)
- [📈 Learning Journey](#-learning-journey)
- [🏁 Conclusion](#-conclusion)
- [🙏 Acknowledgement](#-acknowledgement)
- [⚠️ Disclaimer](#️-disclaimer)

---

## 🧪 Module 1 — Cybersecurity Practical Tasks

### 🎯 Objective

Gain practical exposure to fundamental cybersecurity concepts through hands-on security challenges, including password security, hashing, wordlists, and CTF-style problem solving.

**Skills covered:**

| 🧩 Area | 📖 Focus |
|---|---|
| Cybersecurity Fundamentals | Core concepts & terminology |
| Security Testing Methodology | Structured problem solving |
| Password Security | Weak vs. strong passwords |
| Hashing Concepts | One-way transformations |
| Wordlists | Dictionary-based attacks |
| Password Cracking | Practical recovery workflow |
| CTF Challenges | Flag-based validation |

### 🔑 Password Security & Hashing

Passwords aren't usually stored directly — instead, systems rely on **cryptographic hashes**, a one-way transformation producing a fixed-format representation of the original input.

**Practical workflow:**

```
Protected File
     ↓
Hash Extraction
     ↓
Hash Identification
     ↓
Password Cracking
     ↓
Password Recovery
     ↓
Access to Protected File
```

### 🧰 Networkwalks Password Cracker

Practiced against a lab file: `My Locked PDF1.pdf`

**Steps followed:**

1. 📥 Download the encrypted lab PDF
2. 🧮 Open the Networkwalks Hash Calculator
3. 📤 Upload the protected PDF
4. 🔍 Extract the PDF hash
5. 📋 Copy the hash (starting with `$pdf$`)
6. 🖥️ Open the Networkwalks Password Cracker
7. 📝 Provide the extracted hash
8. ▶️ Start the cracking process
9. ⏳ Wait for password recovery
10. 🔓 Use the recovered password to open the PDF

### 🧠 Wordlists & Password Cracking

Password-cracking effectiveness depends on:

- 📏 Password length
- 🔀 Password complexity
- 🎯 Password predictability
- 📚 Wordlist quality
- 🔡 Character combinations
- 🌐 Search space
- ⚡ Available computing resources

> 💡 **Key takeaway:** Weak and predictable passwords are significantly easier to recover than strong, unique ones.

### 🚩 Captured Flags

```
🏁 nw[networkwalks_flag_260821_1]
🏁 nw[networkwalks_persistence_jtr_270521]
🏁 nw[cybersecurity_flag_captured_2608]
```

### 📚 Key Learning Outcomes

- ✅ Password security fundamentals
- ✅ Hashing concepts
- ✅ Password recovery techniques
- ✅ Wordlist-based attacks
- ✅ Practical cybersecurity investigation
- ✅ Capture-the-Flag methodology
- ✅ Understanding weak-password risks

---

## 🤖 Module 2 — Setting Up HexStrike MCP with Claude

### 🎯 Objective

Set up the **HexStrike MCP Server** with **Claude Desktop** inside a **Kali Linux** environment, exploring how an MCP-based architecture connects an AI assistant with locally running security tooling.

### 🖥️ Environment

| Component | Detail |
|---|---|
| **OS** | Kali Linux |
| **AI Assistant** | Claude Desktop |
| **Security Platform** | HexStrike AI |
| **Protocol** | MCP |
| **Server** | Localhost |
| **Port** | `8888` |

### 🐉 HexStrike AI

Configured as the local security-tool server, providing an MCP-based interface to multiple security tools.

### 🖥️ Step 1 — Claude Desktop Setup

- 🔑 Added the required GPG key
- 📦 Added the Claude Desktop repository
- 🔄 Updated package repositories
- ⬇️ Installed Claude Desktop
- 🚀 Launched and signed in

### 📥 Step 2 — Downloading HexStrike AI

```bash
git clone <hexstrike-ai-repo>
# Project directory: /home/arshiya/hexstrike-ai
```

### 🐍 Step 3 — Python Virtual Environment

```bash
python3 -m venv hexstrike-env
source hexstrike-env/bin/activate
```

### 📦 Step 4 — Installing Dependencies

```bash
pip3 install -r requirements.txt
```

### 🚀 Step 5 — Starting the HexStrike Server

```bash
cd ~/hexstrike-ai
source hexstrike-env/bin/activate
python3 hexstrike_server.py
```

**Output confirmed:**
```
[INFO] Server starting on 127.0.0.1:8888
Running on http://127.0.0.1:8888
```

### ⚙️ Step 6 — MCP Configuration

```
Claude Desktop
      │
      │ MCP
      ▼
hexstrike_mcp.py
      │
      ▼
localhost:8888
      │
      ▼
HexStrike AI Server
```

### 🔗 Step 7 — HexStrike MCP Connection

```
hexstrike-env/bin/python
        ↓
hexstrike_mcp.py
        ↓
--server
        ↓
http://localhost:8888
```

### ✅ Step 8 — Server Verification

```
Serving Flask app 'hexstrike_server'
Debug mode: off
Running on all addresses (0.0.0.0)
Running on: http://127.0.0.1:8888
```

### 🧩 Architecture

```
                    ┌──────────────────┐
                    │  Claude Desktop  │
                    └────────┬─────────┘
                             │ MCP
                             ▼
                    ┌──────────────────┐
                    │ hexstrike_mcp.py │
                    └────────┬─────────┘
                             │ HTTP
                             ▼
                    ┌──────────────────┐
                    │ HexStrike Server │
                    │   Port: 8888     │
                    └────────┬─────────┘
                             ▼
                    ┌──────────────────┐
                    │ Security Tools   │
                    │ & Analysis       │
                    └──────────────────┘
```

### 🔍 What I Learned

- ✅ MCP architecture
- ✅ AI-to-tool integration
- ✅ Local security-tool infrastructure
- ✅ Python virtual environments
- ✅ Dependency management
- ✅ Linux-based security environments
- ✅ Flask-based server execution
- ✅ Connecting AI assistants with local tooling

---

## 🧠 Overall Learning

<table>
<tr>
<th>🧪 Module 1</th>
<th>🤖 Module 2</th>
</tr>
<tr>
<td>

```
Security Concepts
      ↓
Hashing
      ↓
Password Security
      ↓
Password Cracking
      ↓
CTF / Flag Capture
```

</td>
<td>

```
Linux Environment
      ↓
Python Environment
      ↓
Security Tool Server
      ↓
MCP
      ↓
Claude Desktop
      ↓
AI-Assisted Workflow
```

</td>
</tr>
</table>

---

## 🛠️ Technologies & Tools

<div align="center">

![Kali Linux](https://img.shields.io/badge/-Kali%20Linux-557C94?style=flat-square&logo=kalilinux&logoColor=white)
![Python](https://img.shields.io/badge/-Python%203-3776AB?style=flat-square&logo=python&logoColor=white)
![Claude](https://img.shields.io/badge/-Claude%20Desktop-D97757?style=flat-square&logo=anthropic&logoColor=white)
![Flask](https://img.shields.io/badge/-Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Git](https://img.shields.io/badge/-Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/-GitHub-181717?style=flat-square&logo=github&logoColor=white)
![MCP](https://img.shields.io/badge/-MCP-6C63FF?style=flat-square)
![HexStrike AI](https://img.shields.io/badge/-HexStrike%20AI-FF4B4B?style=flat-square)

</div>

- 🐧 Kali Linux
- 🐍 Python 3
- 🖥️ Claude Desktop
- 🔗 MCP
- 🐉 HexStrike AI
- ⚗️ Flask
- 🧮 Networkwalks Hash Calculator
- 🔓 Networkwalks Password Cracker
- 📚 Wordlists
- 🌱 Git & GitHub

---

## 📈 Learning Journey

```
Cybersecurity Fundamentals
          ↓
Password Security
          ↓
Hashing
          ↓
Password Cracking
          ↓
Wordlists
          ↓
Capture The Flag
          ↓
Linux Security Environment
          ↓
Python Virtual Environment
          ↓
HexStrike AI
          ↓
MCP
          ↓
Claude Desktop
          ↓
AI-Assisted Cybersecurity 🔐🤖
```

> From understanding attacks → to understanding tools → to connecting AI with security tooling.

---

## 🏁 Conclusion

These practical modules were a significant part of my cybersecurity learning journey. From understanding how password hashes can be extracted and tested in controlled environments, to setting up an MCP-based security environment with **Claude Desktop** and **HexStrike AI**, the exercises provided valuable hands-on exposure to modern cybersecurity workflows.

More importantly, this experience reinforced the value of **learning by doing** — understanding the underlying technology and continuously developing a practical security mindset.

---

## 🙏 Acknowledgement

<div align="center">

### 🌟 Special Thanks 🌟

A heartfelt thank you to my instructor **Waqas Karim (CCIE)** for his invaluable guidance, mentorship, and support throughout this learning journey.

And to **Networkwalks Academy** for providing a structured, practical cybersecurity learning environment with hands-on challenges that made these concepts much easier to understand through real implementation.

</div>

---

## ⚠️ Disclaimer

> All activities documented in this repository were performed as part of **authorized cybersecurity training** and **controlled laboratory exercises**.
>
> The techniques and tools discussed should only be used on systems, files, networks, and environments where **explicit authorization** has been provided.

---

<div align="center">

### 🔐 Made with dedication by **Arshiya Sharma** 🤖

⭐ *If you found this useful, consider giving this repo a star!* ⭐

</div>
