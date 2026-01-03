# Ansible Playbook-Based Automation Project

This repository contains a **playbook-based Ansible automation project** that demonstrates real-world infrastructure automation concepts with a strong focus on **security, structure, and best practices**.

The project was initially implemented as part of a technical assignment as **part of NTI Scholarship** and later refined to reflect production-style Ansible workflows commonly used in DevOps environments.

---

## 🚀 Project Overview

This Ansible playbook automates common system administration tasks, including:

- Creating multiple Linux users in an idempotent manner
- Updating package repositories
- Installing and managing system packages
- Managing services using handlers
- Modifying system configuration files
- Executing shell scripts and capturing their output
- Managing sensitive credentials securely using **Ansible Vault**

---

## 🔐 Security & Secrets Management

This project applies secure secret management practices using **Ansible Vault**:

- Sensitive variables are stored in an encrypted `vault.yml` file
- A local `.vault_pass` file is used to decrypt secrets at runtime
- Secret-related files are excluded from version control via `.gitignore`

This approach mirrors common security practices used in real production environments.

---

## 📁 Project Structure

```text
.
├── playbook.yml          # Main Ansible playbook
├── vault.yml             # Encrypted secrets (Ansible Vault)
├── group_vars/
│   └── all.yml           # Global variables
├── inventory.ini         # Local inventory (ignored in Git)
├── script.sh             # Helper shell script
├── script2.sh            # Helper shell script
├── .gitignore            # Git ignore rules
└── README.md             # Project documentation


## ▶️ How to Run the Playbook

### Prerequisites

- Linux system
- Ansible installed
- SSH access to target hosts
- Ansible Vault password available

### Run the Playbook

Using an interactive vault password prompt:

```bash
ansible-playbook playbook.yml --ask-vault-pass
```

Or, using a local vault password file:

```bash
ansible-playbook playbook.yml --vault-password-file .vault_pass
```

---

## 🧠 Key Concepts Demonstrated

- Playbook-based Ansible design
- Idempotent automation
- Handlers and service management
- Separation of configuration and secrets
- Secure authentication using SSH keys
- Version control best practices with Git & GitHub

---

## 🛠 Technologies Used

- Ansible
- Ansible Vault
- Bash scripting
- Git & GitHub
- Linux (Ubuntu)

---

## 📌 Notes

- The `inventory.ini` file is intentionally excluded from version control.
- The `.vault_pass` file is local-only and must never be committed.
- This project is intended for learning and demonstration as part of my **NTI 6-month intensive program**.

---

##  Author: **Mohammed Mourad**  
