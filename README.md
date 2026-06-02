FortiGate Firewall Initial Configuration Guide (FortiOS 7.x)**

This guide outlines the essential steps for the "out-of-the-box" setup of a **FortiGate 60F** firewall, covering connectivity, initial security, and dashboard optimization.

## **1. Physical Connectivity & Initial Access**
*   **Management Ports:** Entry-level models (e.g., 60 series) typically lack a dedicated Management Port; use any **LAN interface (Port 1)** for GUI access or the **Console Port** (RJ45/USB serial) for CLI [1, 2].
*   **Default Credentials:** 
    *   **IP Address:** `https://192.168.1.199` [2].
    *   **Username:** `admin`
    *   **Password:** (Leave blank) [3].
*   **Workstation Setup:** Configure the connecting PC to **DHCP** (FortiGate has a default DHCP server) or assign a static IP such as `192.168.1.100/24` [3].
*   **First-Time Login:** The system requires an immediate **password change** upon the first successful login [3, 4].

## **2. Essential System Settings**
To ensure accurate logging and an efficient workflow, configure these settings under **System > Settings**:
*   **Hostname:** Change from the default model name to a specific identifier (e.g., `Company-FW-01`) [5, 6].
*   **System Time:** Set the correct **Time Zone** (e.g., GMT +8) to ensure logs are accurate for troubleshooting [7].
*   **Idle Timeout:** Increase the default 5-minute timeout to **30 minutes** to prevent frequent disconnections during configuration [6, 7].
*   **Firmware:** Verify you are running a stable version (e.g., **v7.2.4**) before proceeding with deep configuration [4].

## **3. Dashboard & Monitoring Setup**
FortiOS 6.4 and above requires manual addition of certain monitoring widgets [8].
*   **Standard Widgets:** Monitor real-time **CPU, Memory, and Sessions** [9, 10].
*   **Advanced Monitoring:** Manually add the **Routing Monitor** (Network category) and **Device Inventory** (User & Authentication category) to the dashboard for better visibility [11].
*   **Interface Bandwidth:** Add widgets to monitor specific ports, such as **WAN1**, to track live traffic flow [10].

## **4. Administration & Maintenance**
*   **CLI Console:** Accessible directly from the GUI top-right header for advanced command-line configuration [8].
*   **Configuration Management:** The **Configuration** menu allows for **Backup, Restore, and Revisions** [8].
*   **System Operations:** Options for **Reboot** and **Shutdown** are located under the User/System menu [8].
