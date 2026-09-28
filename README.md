# 🚢 NIST Cyber Risk Assessment CyberShip

A comprehensive cybersecurity risk assessment of a modern vessel ("CyberShip") using the **NIST SP 800-30** framework. This report was produced as a group project for the MSc course [**02277 Cyber Risk Management and Incident Response**](https://kurser.dtu.dk/course/02277) at the **Technical University of Denmark (DTU)**.

---

## 📄 Report

👉 [`Cyber_Risk_Assesment_NIST_Cybership.pdf`](Cyber_Risk_Assesment_NIST_Cybership.pdf)

---

## 📌 About

The shipping industry carries ~90 % of world trade, and modern vessels increasingly rely on interconnected cyber-physical systems for navigation, propulsion, cargo handling, and communication. This connectivity improves operational efficiency but also expands the attack surface.

This report applies the four step **NIST SP 800-30** risk management process *Prepare → Conduct → Communicate → Maintain* to systematically identify, analyze, and evaluate cybersecurity risks aboard the CyberShip.

---

## 🔍 Scope & Systems Analyzed

The assessment covers **12 critical shipboard assets** grouped into four categories:

| Category | Systems |
|---|---|
| **Navigation** | ECDIS · AIS · Radar · GNSS/GPS · Integrated Bridge System (IBS) · Voyage Data Recorder (VDR) |
| **Operational / Control** | Engine Control System · Ballast System · Ballast Water Management System · Cargo Management System |
| **Communication & IT** | Satellite Communication (SATCOM) · GMDSS |
| **Infrastructure** | Shipboard Network / LAN (VLAN-segmented IT/OT backbone) |

---

## ⚠️ Key Findings

- **High system interconnectivity** allows attacks on a single component (e.g., GNSS/GPS spoofing) to propagate across navigation, bridge, and control systems.
- **Shipboard LAN** was rated the highest risk (*Critical*) due to the diversity of endpoints and the potential for ransomware lateral movement from IT to OT networks.
- **ECDIS, GNSS/GPS, IBS, and Engine Control** all carry *High* initial risk scores driven by threats such as signal spoofing, USB-borne malware, and unauthorized remote access.
- **GMDSS** threats have catastrophic safety impact (SOLAS "Safety of Life at Sea") even with lower likelihood.
- Many shipboard OT systems run on **legacy operating systems** (e.g., Windows XP) that no longer receive security patches.

---

## 🛡️ Proposed Mitigations

| Component | Primary Threat | Key Control |
|---|---|---|
| Shipboard LAN | Lateral Movement / Ransomware | Zero Trust architecture, strict VLAN segmentation |
| ECDIS & IBS | USB Malware | Disable physical USB ports, enforce clean-ship policies |
| GNSS/GPS & AIS | Signal Spoofing / Jamming | Anti-spoofing antennas, cross-sensor validation |
| SATCOM | Credential Theft | Multi-Factor Authentication, firmware hardening |
| Engine Control | Unauthorized Access | Encrypted VPN remote diagnostics, anomaly monitoring |
| Cargo Management | Ransomware / Data Breach | Network isolation, immutable offline backups |
| Ballast Systems | Sensor Manipulation | Sensor validation algorithms, physical draft cross-checks |

With the proposed controls applied, all component risk levels are reduced to **Medium or below**.

---

## 🧭 Methodology

The assessment follows **NIST SP 800-30 Rev. 1** and is supplemented by:

- **IMO MSC-FAL.1/Circ.3** Guidelines on Maritime Cyber Risk Management
- **BIMCO** Guidelines on Cyber Security Onboard Ships (v5)
- **IACS UR E26** Cyber Resilience of Ships
- **ISO/IEC 27005:2022** Information Security Risk Management Guidance
- **ENISA** Port Cybersecurity & Maritime Sector Reports

Each component is evaluated through a five-step process: *Purpose → Threats & Vulnerabilities → Impact Analysis (CIA) → Risk Estimation → Risk Evaluation*.

---

## 👥 Authors

| Name | Responsibilities |
|---|---|
| **Pinac Joshi** | Communication & IT Systems (SATCOM, GMDSS, LAN); Risk Treatment & Communication; CyberShip Diagram |
| **Birkir Freyr Konráðsson** | Attacks & Threat Analysis; Navigation Systems (ECDIS, AIS, Radar, GNSS/GPS) |
| **Brynja Eyfjörð Jónsdóttir** | Bridge & Monitoring Systems (IBS, VDR); Introduction; Risk Management Process; Discussion |
| **Hanna Margrét Pétursdóttir** | Operational & Control Systems (Engine, Ballast, BWMS, Cargo); Conclusion |

---

## 🎓 Course

| | |
|---|---|
| **Course** | [02277 Cyber Risk Management and Incident Response](https://kurser.dtu.dk/course/02277) |
| **University** | Technical University of Denmark (DTU) |
| **Program** | MSc in Computer Science |
| **Date** | April 2026 |

---

## 📜 License

This project is an academic report. Please cite appropriately if referencing this work.
