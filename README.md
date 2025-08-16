# Eth-Storage-Ceremony-v1

Bilkul Hii 👀 — maine us repo ka quick guide check kiya. Agar tum apne repo me ye instructions paste karna chahte ho, toh yeh raha ek clean, formatted version jo tum README ya kisi doc file me daal sakte ho:

---

## ⚡ EthStorage V1 Trusted Setup Ceremony – Quick Guide

### 🗓 Ceremony Duration: August 13 to 22

### 🧰 Requirements:
- **Local PC**: Ubuntu 22.04  
- **Or VPS**: 2 vCPU, 4GB RAM, 30GB+ SSD  
- **GitHub Account**:
  - Age ≥ 1 month  
  - At least 1 public repo  
  - Following ≥ 5 accounts  
  - At least 1 follower  


---

### 🛠 Setup Instructions:

# Update & install dependencies
sudo apt update && sudo apt upgrade -y
sudo apt install -y curl git build-essential

....

# Install Node.js
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs
sudo npm install -g npm@9.2

# Check versions
node -v
npm -v

# Create temp directory
mkdir ~/trusted-setup-tmp && cd ~/trusted-setup-tmp

# Install Phase2 CLI
sudo npm install -g @p0tion/phase2cli

# Verify CLI
phase2cli --version

# Authenticate with GitHub
phase2cli auth
# Visit https://github.com/login/device and enter the code
# Authorize ethstorage with Read & Write access to GitHub Gists

# Start screen session
screen -S ceremony

# Join the ceremony
phase2cli contribute -c ethstorage-v1-trusted-setup-ceremony
# Press Enter for random input or type your own
```

---

### 🧹 Cleanup & Logout

```bash
phase2cli clean
phase2cli logout
rm -rf ~/ceremonyeth
```

---

### 🖥 Screen Commands

| Action           | Command                        |
|------------------|--------------------------------|
| Detach           | `Ctrl + A + D`                 |
| Resume           | `screen -r ceremony`           |
| Delete screen    | `screen -XS ceremony quit`     |
| List sessions    | `screen -ls`                   |

---

### 🧯 Troubleshooting

- **npm EBADENGINE error**:  
  You're on Node 18 — switch to `npm@10`  
  ```bash
  npm install -g npm@10
  ```

- **Lost connection**:  
  Just re-run:  
  ```bash
  phase2cli contribute -c ethstorage-v1-trusted-setup-ceremony
  ```

---

🎉 You’ve successfully contributed to EthStorage’s decentralization!  
