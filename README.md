# Robots Dungeon 3D

[![Unity Version](https://img.shields.io/badge/Unity-2022.3%2B-blue.svg?style=flat-square&logo=unity)](https://unity.com/)
[![Platform](https://img.shields.io/badge/Platform-WebGL%20%7C%20PC-orange.svg?style=flat-square)](https://github.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)

An action-packed 3D top-down dungeon crawler built in Unity. Battle tactical AI robots, survive hazardous arenas, manage active spell mechanics like damage orbs, and escape the mechanical dungeon.

---

## 📌 Table of Contents
* [About the Project](#about-the-project)
* [Built With](#built-with)
* [Core Features](#core-features)
* [Project Architecture](#project-architecture)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Gameplay Controls](#gameplay-controls)
* [CI/CD & Deployment](#cicd--deployment)

---

## 📖 About the Project

**Robots Dungeon 3D** is a modularly designed action game showcasing scalable architecture patterns in Unity. It cleanly decouples input systems, combat logic, AI behavior profiles, and UI state managers, serving as a robust foundation for a fast-paced hack-and-slash dynamic gameplay loop.

---

## 🛠️ Built With

* **Game Engine:** Unity (3D Object Core)
* **Scripting Language:** C# (.NET / Assembly-CSharp)
* **Camera System:** Unity Cinemachine (Procedural Noise Profiles)
* **Input System:** Unity Input Framework

---

## 🚀 Core Features

* **Advanced Combat Mechanics:** Implements hitboxes, raycasting, tracking orbs (`DamageOrb.cs`), and dynamic tracking frameworks (`DamageCaster.cs`).
* **Stateful Entity Health System:** Uniform, reusable health components (`Health.cs`) tracking damage instances, execution loops, and death states across players and enemies alike.
* **Intelligent AI Logic:** Custom script handlers controlling ranged combat strategies (`Enemy02_shoot.cs`) coupled with dynamic visual destruction engines (`EnemyVFXManager.cs`).
* **Game Feel Enhancements:** Implements a central Cinemachine-driven singleton (`CameraShake.cs`) to trigger runtime impulse adjustments during high-impact interactions.

---

## 📂 Project Architecture

The core codebase is organized within `Assets/Scripts/` to maintain strict single-responsibility principles:

| Script Name | System Category | Description |
| :--- | :--- | :--- |
| **`GameManager.cs`** | Core Engine | Tracks structural progression, level criteria, win/loss configurations. |
| **`PlayerInput.cs`** | Input | Captures and bridges user input states to physical interaction mechanics. |
| **`Character.cs`** | Actor Profile | Acts as the foundational data and animation hub for characters. |
| **`Health.cs`** | Combat Systems | Manages computational health bounds, scaling damage, and live tracking. |
| **`DamageOrb.cs`** | Projectiles | Handles structural logic for ranged area-of-effect dynamic spells. |
| **`Enemy02_shoot.cs`**| AI Controller | Commands combat loops, distance tracking, and intervals for ranged enemies. |
| **`CameraShake.cs`** | Visual FX | Leverages a Cinemachine Virtual Camera framework to handle screen impacts. |
| **`GameUI_Manager.cs`**| Canvas UI | Handles operational interface updating, dashboard status, and HUD values. |

---

## 🏁 Getting Started

Follow these instructions to set up the development environment and run the project locally.

### Prerequisites
* **Unity Hub** installed.
* **Unity Editor** (Recommended: 2022.3 LTS or newer).
* **Visual Studio Code** or alternative C# IDE with Omnisharp/Unity extensions configured.

### Installation

# 1. Clone the repository using the HTTPS link
git clone https://github.com/ramamangtani26/Robots_Dungeon_3D.git

# 2. Move into the newly created project directory
cd Robots-Dungeon_3D