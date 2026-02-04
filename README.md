# ssh-bruteforce-demo


# ssh-bruteforce-demo

This repository demonstrates a simulated SSH brute-force attack scenario between a victim Ubuntu machine and an attacker Kali machine. It includes real-time logs, service status, IP configurations, and brute-force traces captured during the experiment.

---

## 🧱 Victim Machine (Ubuntu)

- **SSH Service Status:**  
  Verified using `systemctl status ssh`, confirming the SSH daemon is active and listening.  
  ![SSH Status](<img width="1603" height="684" alt="docsvictim-ubuntussh-status png" src="https://github.com/user-attachments/assets/d843e8d3-022b-4cb8-a30e-0a2003c020d3" />)

- **IP Address Configuration:**  
  Output from `ip addr show`, showing loopback and global IP bindings.  
  ![IP Addr](<img width="1753" height="347" alt="docsvictim-ubuntuip-addr png" src="https://github.com/user-attachments/assets/d37c47d9-04c2-4f65-b965-f306110be135" />)

- **Authentication Log Monitoring:**  
  Live output from `sudo tail -f /var/log/auth.log`, capturing multiple failed login attempts from 127.0.0.1 targeting user `vs979`.  
  ![Auth Log](<img width="2872" height="1695" alt="docsvictim-ubuntuauth-log png" src="https://github.com/user-attachments/assets/f0f8e29c-3d32-4b61-8afe-4ed3e8ea4c63" />)

---

## 🧨 Attacker Machine (Kali)

- **Nmap Port Scan:**  
  Scanned victim IP to identify open SSH port and service fingerprint.  
  ![Nmap Scan](<img width="1223" height="426" alt="docsattacker-kalinmap-scan png" src="https://github.com/user-attachments/assets/52bf5455-4c71-4113-8911-058fc586f20d" />)

- **Hydra Brute-force Execution:**  
  Used Hydra to launch dictionary-based SSH login attempts against the victim.  
  ![Hydra Run](<img width="2867" height="632" alt="docsattacker-kaliresult-output png" src="https://github.com/user-attachments/assets/3dc39a63-98d5-4ba8-a233-d307df39758d" />)

- **Result Output:**  
  Captured Hydra’s success/failure output, showing login attempts and response codes.  
  ![Result Output](<img width="2823" height="157" alt="docsattacker-kalihydra-run png" src="https://github.com/user-attachments/assets/5f28896c-3611-4f1e-9fff-e1ce4295b728" />)

---















