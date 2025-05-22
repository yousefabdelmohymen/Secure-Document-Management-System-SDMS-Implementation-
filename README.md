# 🔐 Secure Document Management System

A **Flask-based secure document management system** featuring end-to-end encryption, access control, and file integrity verification — built with security-first principles.

---

## ✨ Features

* 🔒 **Secure File Storage** – AES encryption before storing files
* 🧾 **File Integrity** – RSA digital signatures to validate file authenticity
* 🌐 **HTTPS Support** – Encrypted communication via SSL/TLS
* 👤 **User Authentication** – Password hashing and login system
* 🗂️ **Access Control** – Role-based file visibility and actions
* 📜 **Audit Logging** – Logs user activity and file operations

---

## 🛡️ Security Highlights

| Feature                | Description                             |
| ---------------------- | --------------------------------------- |
| AES Encryption         | Encrypts files before storage           |
| RSA Digital Signatures | SHA256-based integrity checks           |
| HTTPS (SSL/TLS)        | Secures all network communication       |
| Bcrypt                 | Hashes user passwords securely          |
| Flask-Session          | Manages sessions with secure cookies    |
| File Verification      | Checks signatures before file downloads |

---

## ⚙️ Prerequisites

* Python 3.x
* `pip` (Python package manager)
* OpenSSL (for generating HTTPS certificates)

---

## 📦 Required Packages

```bash
pip install flask flask-bcrypt flask-sqlalchemy flask-session \
            flask-migrate flask-login pyotp pycryptodome
```

---

## 🛠️ Installation Guide

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/secure-docs.git
   cd secure-docs
   ```

2. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Setup SSL and RSA certificates**
   Place the following files in the root directory:

   * `cert.pem` – SSL certificate
   * `key.pem` – SSL private key
   * `public_key.pem` – RSA public key
   * `private_key.pem` – RSA private key

---

## 📁 Project Structure

```
secure-docs/
├── app/
│   ├── __init__.py          # App initialization
│   ├── models.py            # Database models
│   ├── routes.py            # API and web routes
│   ├── utils.py             # Helper functions
│   ├── static/              # Static assets
│   └── templates/           # HTML templates
├── uploaded_files/          # Original user files
├── uploaded_files_encrypted/ # Encrypted file storage
├── config.py                # Configuration settings
├── run.py                   # Application entry point
└── README.md                # Project documentation
```

---

## ▶️ Running the Application

1. Verify SSL certs and required packages are in place
2. Start the Flask server

   ```bash
   python run.py
   ```
3. Open your browser and go to:
   `https://localhost:5000`

---

## 🔐 Usage Workflow

1. Register an account
2. Log in to your dashboard
3. Upload a file (automatically encrypted)
4. Download to decrypt and verify
5. Click **"Check Integrity"** to verify any file
6. Admins can view system audit logs

---

## 📂 File Operations

| Operation       | Description                           |
| --------------- | ------------------------------------- |
| Upload          | AES-encrypts and signs files          |
| Download        | Verifies signature, decrypts if valid |
| Integrity Check | Validates digital signatures          |
| Delete          | Removes file securely with signature  |

---

## 🧠 Security Tips

* Keep all SSL and RSA keys **private**
* Back up your **encrypted files regularly**
* Audit logs should be **reviewed periodically**
* Run `pip list --outdated` to keep dependencies updated
* Never share your **private RSA key**

---

## 📄 License

This project is licensed under the **MIT License** – use it freely and contribute!


