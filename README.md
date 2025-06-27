# 🔥 Task 4: Firewall Configuration with UFW on Linux

## 🚀 Objective
Configure and test basic firewall rules to allow or block traffic using UFW on Linux.

---

## Prerequisites

### 1. Update Package Lists:
```bash
sudo apt update
```
### 2. Install UFW:
```bash
sudo apt install ufw
```
# Firewall Configuration Steps

1. Enable UFW:
```bash
sudo ufw enable
```

2. List Current Firewall Rules:
```bash
sudo ufw status numbered
```

4. Block Inbound Traffic on Port 23 (Telnet):
```bash
sudo ufw deny in 23
```

5. Verify the Block Rule is Applied:
```bash
sudo ufw status numbered
```

6.Allow SSH on Port 22:
```bash
sudo ufw allow in 22
```

7.Test Connection to Blocked Port 23
```bash
telnet localhost 23
```

# Remove the Test Block Rule to Restore Original State

1. First, get the rule number for port 23:
```bash
sudo ufw status numbered
```

2, Then,delete the rule by its number (replace 1 with the correct number shown in your output):
```bash
sudo ufw delete 1
```

3. Verify Firewall Rules After Deletion:
```bash
sudo ufw status numbered
```
