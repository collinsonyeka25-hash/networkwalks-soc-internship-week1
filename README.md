# networkwalks-soc-internship-week1

Documentation and lab findings for Week 1 of the Networkwalks Cybersecurity SOC Analyst Internship (VirtualBox Lab Setup & Wireshark Traffic Analysis).

---

## 🛠️ Part 1: Testing Lab Environment Setup (TASK WK1-PM1)

Configured a secure local testing and virtualization environment with the following specifications[cite: 21]:
* **Hypervisor:** Oracle VirtualBox (Latest Version)[cite: 21, 22]
* **Attacking Machine:** Kali Linux[cite: 21, 22]
* **Network Architecture:** NATNetwork configured in the `10.0.0.0/24` subnet with full internet access[cite: 21, 22].
* **Kali IP Address:** `10.0.0.2/24`[cite: 21]
* **Usability Settings:** Bidirectional clipboard and drag-and-drop file sharing enabled[cite: 21].
* **Shared Folders:** Host `/downloads` folder shared with the virtual machine[cite: 21].

---

## 🦈 Part 2: Wireshark SOC Analysis Labs

Investigated browser-based network capture labs to build core Security Operations Center (SOC) packet analysis skills[cite: 19, 20]:

1. **Identify the Attacker’s IP:** Detected port-scanning activity (`192.168.10.66` probing target `192.168.10.20`) using SYN packet filters (`tcp.flags.syn == 1`)[cite: 1, 19, 20].
2. **Follow TCP Stream 1 & 2:** Rebuilt network conversation sessions to read transmitted data[cite: 19, 20].
3. **HTTP Plain Text Credentials:** Uncovered unencrypted authentication details traversing the network[cite: 19, 20].
4. **Catch the Brute Force Attacker:** Identified repeated failed login attempts and automated attack patterns[cite: 19, 20].
5. **Catch the Call Scammer:** Analyzed VoIP/telephony session traffic indicators[cite: 19, 20].

---

## 📂 Documentation & Evidence
* Setup and terminal verification screenshots (`ip addr`, user creation, VirtualBox configuration) are stored in the repository.
