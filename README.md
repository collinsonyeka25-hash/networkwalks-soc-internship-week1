# networkwalks-soc-internship-week1

Documentation, lab configuration, and threat analysis findings for **Week 1** of the Cybersecurity SOC Analyst Internship with Networkwalks.

---

## 🛠️ Part 1: Testing Lab Environment Setup (TASK WK1-PM1)

Configured a secure local testing and virtualization environment with the following specifications:
* **Hypervisor:** Oracle VirtualBox (Latest Version)
* **Attacking Machine:** Kali Linux
* **Network Architecture:** NATNetwork configured in the `10.0.0.0/24` subnet with full internet access.
* **Kali IP Address:** `10.0.0.2/24`
* **Usability Settings:** Bidirectional clipboard and drag-and-drop file sharing enabled.
* **Shared Folders:** Host `/downloads` folder shared with the virtual machine.

### Setup Evidence:
* **VirtualBox Configuration:** Allocated VM specs, storage (`Kali Linux.vdi`), and network adapters.
* **Interface Verification:** Inspected network configuration using `ip addr` in the Kali Linux terminal.
* **User Management:** Configured administrative user accounts (`sudo adduser`) for secure lab execution.

---

## 🦈 Part 2: Wireshark SOC Analysis Labs

Investigated browser-based network capture labs to build core Security Operations Center (SOC) packet analysis skills:

1. **Identify the Attacker’s IP:** Detected port-scanning activity (`192.168.10.66` probing target web server `192.168.10.20`) using SYN packet filters (`tcp.flags.syn == 1`). Open ports responded with `[SYN, ACK]` while closed ports responded with `[RST, ACK]`.
2. **Follow TCP Stream 1 & 2:** Rebuilt network conversation sessions to read transmitted data.
3. **HTTP Plain Text Credentials:** Uncovered unencrypted authentication details traversing the network.
4. **Catch the Brute Force Attacker:** Identified repeated failed login attempts and automated attack patterns.
5. **Catch the Call Scammer:** Analyzed VoIP/telephony session traffic indicators.

---

## 📂 Documentation & Evidence
All verification screenshots, terminal logs (`ip addr`, user creation), and Wireshark capture analysis views are organized and stored in this repository.
