[![arXiv](https://img.shields.io/badge/arXiv-2504.05293-<COLOR>.svg)](https://arxiv.org/abs/2504.05293)

**Project Title:** BLE & UWB Beacon-Assisted Framework for Multiuser AR Synchronization

[📄 Extended Abstract](https://github.com/ARBeacon/Docs/blob/main/Extended%20Abstract.pdf) | [📚 Reports](https://github.com/ARBeacon/Docs/tree/main/Reports) | [🖼️ Slides](https://github.com/ARBeacon/Docs/blob/main/Keynote.pdf) | [📇 Poster](https://github.com/ARBeacon/Docs/blob/main/Poster.pdf) | [📹 Demo](https://share.descript.com/view/GvDXv3NAZu4)

<img src="https://github.com/user-attachments/assets/ae1eee5b-6c5e-4e58-9d83-81537c3d57ab" width="30%">

## 📖 Project Overview
This project develops a framework to synchronize Augmented Reality (AR) experiences across multiple devices in shared environments using Bluetooth Low Energy (BLE) and Ultra-Wideband (UWB) beacon technologies. The system addresses scalability and reliability challenges in traditional vision-based AR synchronization by leveraging beacon-assisted spatial referencing.

### ✨ Key Features
**BLE-Assist AR Synchronization:**
![Frame 7 (1)](https://github.com/user-attachments/assets/fc92a98c-68a6-44a6-aec2-a6e084903e83)
- Room-based ARWorldMap segmentation for scalable localization.
- Cloud Anchor synchronization with dynamic room context.

**UWB-Assist AR Synchronization:**
![Frame 9 (1)](https://github.com/user-attachments/assets/b2cc12c3-d198-43ce-92d7-1c3c771b265d)
- Centimeter-precise UWB ranging and magnetic heading fusion.
- Homogeneous transformation for persistent anchor resolution.

## 📂 Repositories
### 📱 Client (AR Apps)
1. **BLE-Assist AR Synchronization:** Uses iBeacon for room context recognition and integrates with ARKit [ARWorldMap](https://developer.apple.com/documentation/arkit/arworldmap) and ARCore [Cloud Anchors](https://developers.google.com/ar/develop/cloud-anchors). 

| Repository   | Description |
| ------------- | ------------- |
| [BeaconScanner](https://github.com/ARBeacon/BeaconScanner) | iOS app for detecting and monitoring iBeacon signals. |
| [BeaconSyncAR-iBeacon-ARKit](https://github.com/ARBeacon/BeaconSyncAR-UWB-ARKit) | BLE-assisted AR synchronization using Apple ARKit's ARWorldMap. |
| [BeaconSyncAR-iBeacon-ARCore](https://github.com/ARBeacon/BeaconSyncAR-UWB-ARKit) | BLE-assisted AR synchronization using Google ARCore's Cloud Anchors. |

2. **UWB-Assist AR Synchronization:** Utilizes UWB's precise ranging and magnetic heading to establish fixed spatial references for persistent AR anchoring. 

| Repository   | Description |
| ------------- | ------------- |
| [UWBScanner](https://github.com/ARBeacon/UWBScanner) | iOS app for UWB beacon ranging and stabilization using Apple Nearby Interaction. |
| [BeaconSyncAR-UWB-ARKit](https://github.com/ARBeacon/BeaconSyncAR-UWB-ARKit) | UWB-assisted AR synchronization with ARKit, enabling persistent spatial references. |

### 🛰️ Server
| Repository   | Description |
| ------------- | ------------- |
| [BeaconSyncAR-api](https://github.com/ARBeacon/BeaconSyncAR-api) | Backend service (Swift Vapor) for managing rooms, beacons, ARWorldMaps, and anchors. |
| [BeaconSyncAR-namespace-functions](https://github.com/ARBeacon/BeaconSyncAR-namespace-functions) | Serverless functions for generating ARCore API OAuth2 tokens to authorize backend requests. |

### 📈 Evaluation
| Repository   | Description |
| ------------- | ------------- |
| [ARBeaconEvaluation](https://github.com/ARBeacon/ARBeaconEvaluation) | Evaluation scripts and logs for accuracy, latency, robustness, and power consumption tests. |

## 🛠 Technologies
**BLE-Assist AR Synchronization:**
- **Hardware:** ESP32 (BLE Beacon), iPhone
- **Software:** Swift, ARKit, ARCore, SwiftUI, PostgreSQL, Digital Ocean Spaces (S3-compatible)
- **Protocols:** [iBeacon](https://developer.apple.com/ibeacon/)
  
**UWB-Assist AR Synchronization:**
- **Hardware:** [DWM3001CDK](https://www.qorvo.com/products/p/DWM3001CDK) (UWB Beacon), iPhone (UWB-enabled)
- **Software:** Swift, ARKit, SwiftUI, PostgreSQL
- **Protocols:** [FiRa](https://www.firaconsortium.org/) (UWB), Nearby Interaction (Apple)

## 🚀 Getting Started
#### 1. **Backend Deployment** 
Follow instructions in [BeaconSyncAR-api](https://github.com/ARBeacon/BeaconSyncAR-api) to set up database and server.

#### 2. **Client AR Apps**
Follow instructions in each approach's repository to set up the AR app.

**BLE-Assist AR Synchronization:**
- [BeaconSyncAR-iBeacon-ARKit (BLE-Assst ARWorldMap)](https://github.com/ARBeacon/BeaconSyncAR-UWB-ARKit)
- [BeaconSyncAR-iBeacon-ARCore (BLE-Assst Cloud Anchors)](https://github.com/ARBeacon/BeaconSyncAR-UWB-ARKit)
**BLE-Assist AR Synchronization:**
- [BeaconSyncAR-UWB-ARKit (UWB-Assist)](https://github.com/ARBeacon/BeaconSyncAR-UWB-ARKit)

## 📄 License
This project is licensed under the [MIT License](LICENSE).

_Note: This README.md was refined with the assistance of [DeepSeek](https://www.deepseek.com)_
