## TAK Server 5.X on Ubuntu Server 22.04 w/lightweight GUI
### System Requirements 
*   **Operating Systems**: Ubuntu Server 22.04 LTS and Raspberry Pi OS (Bookworm, 64-bit/ARM64) are fully supported.
>⚠︎ WARNING: Avoid Debian Trixie OS on the Raspberry Pi because it lacks the required Java 17 dependencies.
*   **Required Software**: Java 17 (OpenJDK-17-jre) is a strict requirement. 
>⚠︎ WARNING: The TAK Server **will not start** on Java 11 or Java 21. This package is typically installed automatically via package dependencies.
*   **Recommended Hardware**: A Raspberry Pi 4 Model B (4GB RAM minimum) is required for a basic setup. 
>🛈 NOTE: **8GB RAM** is highly recommended if running a desktop environment or multitasking.
*   **Headless (CLI Only)**: A clean install of Ubuntu Server runs with no GUI, using only **200–300 MB of RAM** at idle.
>🛈 NOTE: This is the recommended configuration to maximize hardware resources for your database and active TAK connections.
*   **Lightweight GUI (XFCE)**: If a graphical desktop is strictly required, use **XFCE**.
>🛈 NOTE: It provides a low-bloat desktop environment with minimal overhead, consuming only **350–450 MB of RAM** at idle.

---

## Disclaimer & License

### Disclaimer
This repository is an independent installation guide and is not affiliated with, endorsed by, or connected to the Department of Defense, the TAK Product Center, or any official TAK development entity. The instructions provided are for educational and training purposes. **Use these instructions at your own risk.**

### License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
