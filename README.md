# 📬 Postfix Mail Server Setup (Linux)

This project demonstrates installing and configuring a local SMTP mail server using Postfix on Linux.

---

## 🚀 Tech Stack
- Linux
- Postfix (SMTP server)
- Mailutils
- Shell commands
- Git

---

## 📦 Features
✔ Install Postfix  
✔ Configure SMTP  
✔ Create local users  
✔ Setup mailbox (mbox format)  
✔ Send & receive emails via terminal  
✔ Debug using mail logs  

---

## 🛠 Installation Steps

### Install packages
sudo apt update
sudo apt install postfix mailutils -y

### Start postfix
postfix start

### Create user
sudo adduser ben

### Create mailbox
sudo mkdir -p /var/mail
sudo touch /var/mail/ben
sudo chown ben:mail /var/mail/ben
sudo chmod 660 /var/mail/ben

---

## ✉ Send Test Mail
echo "Hello" | mail -s "Test" ben@localhost

---

## 📥 Read Mail
su - ben
mail

---

## 📁 Important Files
/etc/postfix/main.cf → configuration  
/var/mail/ben → mailbox  
/var/log/mail.log → logs  

---

## 🧠 Skills Learned
- Linux system administration
- Mail server setup
- SMTP basics
- Log troubleshooting
- CLI tools

---

## ✅ Result
Successfully configured a working local mail server with Postfix.
