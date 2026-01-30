# Cisco-Secure-Network-Lab
"A hands-on cybersecurity lab implementing network segmentation, management plane hardening, and VoIP security on physical Cisco hardware".
# Cisco Secure Network Lab: Infrastructure Hardening & Asset Management

## 🎯 Project Overview
This repository documents a hands-on cybersecurity lab designed to bridge the foundational security concepts of **CompTIA Security+ (SY0-701)** with the advanced analytical skills of **CompTIA CySA+ (CS0-003)**. By utilizing a "Analyze & Defend" strategy, I implement security controls on physical Cisco hardware while performing continuous vulnerability assessment and reporting.

## 🛠️ Hardware & Environment
- **Switch 1:** Cisco Catalyst 2960 (Core Access & Hardening)
- **Switch 2:** Cisco SF 100D-08P (PoE for VoIP endpoints)
- **Endpoint:** Cisco 7960 IP Phone
- **Management:** MacBook M4 (macOS Sequoia)
- **Power Distribution:** ADJ-PC-100A

## 🚀 Phase 1: Initial Access & Asset Discovery
The objective of this phase was to establish a secure management baseline and perform a comprehensive audit of existing infrastructure.

### **Technical Implementation**
- Established a serial console connection using the `screen` utility via macOS Terminal.
- **Asset Audit:** Performed `show version` and `show inventory` to document firmware levels and hardware serial numbers for the organization's asset register.

### **Troubleshooting Log: Modern-to-Legacy Compatibility**
- **Issue:** Received `$TERM too-long` error when connecting via MacBook M4.
- **Root Cause:** Modern terminal environment variables exceeded the buffer limits of legacy Cisco IOS.
- **Resolution:** Manually exported a standard environment variable (`export TERM=vt100`) to successfully initialize the CLI.

## 🛡️ Certification Objective Alignment
- **Security+ (SY0-701):** - **Objective 3.2:** Applying security principles to secure enterprise infrastructure.
  - **Objective 4.2:** Management of hardware, software, and data assets.
- **CySA+ (CS0-003):**
  - **Objective 1.1:** System and network architecture concepts in security operations.
  - **Objective 1.5:** Efficiency and process improvement through standardized documentation.

## 📊 Verification
[Image of Cisco Switch CLI showing 'show version' and 'show vlan brief' output]
- Firmware integrity verified against known CVEs.
- Management VLAN segmentation initialized.
