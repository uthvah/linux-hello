# 🔐 Linux Hello (Face Auth)

<div align="center">

![2025-10-11 21-31-45](https://github.com/user-attachments/assets/1c7b188f-02fe-4ca6-830b-9fc285153fa3)

![Face Auth Demo](https://img.shields.io/badge/Face%20Auth-Linux-blue?style=for-the-badge&logo=linux)
[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.x-red?style=for-the-badge&logo=opencv)](https://opencv.org/)

</div>

---

### Overview

Linux Hello brings secure, efficient facial recognition to the Linux ecosystem. Designed as an open-source alternative to proprietary biometric systems, it leverages deep learning to authenticate users via standard webcams.

### Core Features

*   **Precision Recognition:** Utilizes a ResNet-34 based model via dlib for high-accuracy face matching and identification.
*   **Active Liveness Detection:** To verify physical presence, the system utilizes randomized challenge-response protocols. During authentication, the user is prompted to perform a specific, randomly selected sequence of actions (such as blinking, nodding, or turning their head) which must be completed in real-time to pass verification.
*   **Encrypted Storage:** Facial templates are hashed and secured using AES-256 encryption, ensuring biometric profiles remain inaccessible to unauthorized users.
*   **Privacy-Centric:** Operates entirely offline. Video feeds are processed locally, and no biometric data is transmitted to external servers.

### Operational Logic

The application functions in two distinct modes:

1.  **Enrollment:** Upon the first execution, the system guides the user through a brief capture process to generate a secure facial profile.
2.  **Authentication:** On subsequent runs, the system compares the live camera feed against the encrypted profile. Simultaneously, it issues a randomized motion challenge. A successful match combined with a verified challenge response returns a success exit code, allowing for integration with authentication wrappers.

### License

This project is open source and available under the **MIT License**.
