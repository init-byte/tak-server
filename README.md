# TAK Server on Ubuntu Server 22.04 w/lightweight GUI
### System Requirements 
*   **Operating Systems**: Ubuntu Server 22.04 LTS and Raspberry Pi OS (Bookworm, 64-bit/ARM64) are fully supported.<br>⚠️ Avoid Debian Trixie OS on the Raspberry Pi, as it lacks the required Java 17 package dependencies.
*   **Required Software**: Java 17 (OpenJDK-17-jre) is a strict requirement. The TAK Server **will not start** on Java 11 or Java 21. This package is typically installed automatically via package dependencies.
*   **Recommended Hardware**: A Raspberry Pi 4 Model B (4GB RAM minimum) is required for a basic setup. **8GB RAM** is highly recommended if running a desktop environment or multitasking.
*   **Headless (CLI Only)**: A clean install of Ubuntu Server runs with no GUI, using only **200–300 MB of RAM** at idle.<br>ℹ️ This is the recommended configuration to maximize hardware resources for your database and active TAK connections.
*   **Lightweight GUI (XFCE)**: If a graphical desktop is strictly required, use **XFCE**.<br>ℹ️ It provides a low-bloat desktop environment with minimal overhead, consuming only **350–450 MB of RAM** at idle.
