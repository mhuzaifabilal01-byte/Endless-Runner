# 🏃‍♂️ Endless Runner Game (Unity 3D)

A fully-featured, ready-to-play 3D Endless Runner game template built with Unity and Universal Render Pipeline (URP). This project serves as a comprehensive reference implementation for building mobile-optimized endless runner games (similar to Subway Surfers or Temple Run).

<p align="center">
  <video src="https://github.com/mhuzaifabilal01-byte/Endless-Runner/raw/main/Assets/Demo/demo.mp4" width="100%" height="auto" controls autoplay loop muted></video>
</p>

---

## ✨ Features

*   **🎮 Responsive Multi-Platform Controls:** Built-in `SwipeManager` supporting touch gestures (swipes left/right/up/down) for mobile devices, and Keyboard inputs (A/D/Space/S) for desktop play.
*   **🛣️ Dynamic Infinite Tile Spawning:** Memory-efficient `TileManager` and custom `ObjectPool` system that dynamically spawns, recycles, and positions road tiles as the player advances.
*   **🌌 Floating Origin System:** Solve vertex jittering and precision issues with `FloatingOrigin.cs`, which resets the scene's spatial origin dynamically as the player travels extreme distances.
*   **🛒 In-Game Shop & Skins:** Unlockable character skins/models purchased with collected gems. Local data persistence is managed seamlessly through `PlayerPrefs`.
*   **💵 Mobile Monetization Ready:** Integrated Google Mobile Ads SDK with configurations for Banner, Interstitial, and Rewarded Ads (`AdManager.cs`).
*   **🔊 Audio & UI Systems:** Centrally managed background music, sound effects, high score tracker, custom fonts, and main/game-over menus.

---

## 🛠️ Tech Stack & Architecture

*   **Engine:** Unity (URP - Universal Render Pipeline)
*   **Language:** C#
*   **Architecture Pattern:** Component-based with Managers (e.g., `PlayerManager`, `TileManager`, `AdManager`, `ShopManager`).
*   **Optimization:** Custom object pooling to avoid runtime garbage collection hiccups from continuous spawning/destroying.

---

## 📁 Project Structure

```bash
Assets/
├── Scripts/
│   ├── Game/          # AdManager, AudioManager, SwipeManager, LevelEvents, etc.
│   ├── Player/        # PlayerController, CameraController, PlayerManager
│   ├── Store/         # ShopManager, ShopElement
│   └── Tiles/         # TileManager, ObjectPool, Gem, FloatingOrigin
├── Prefabs/           # Pre-configured tiles, obstacles, and gems
├── Scenes/            # Main Menu and Gameplay Scenes
├── GrassRoadRace/     # Materials, textures, and models for the environment
└── Settings/          # URP Quality Settings
```

---

## 🚀 Getting Started

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/mhuzaifabilal01-byte/Endless-Runner.git
   ```
2. **Open in Unity:**
   * Open the project folder using **Unity Hub** (designed with modern Unity versions using URP).
3. **Open the Scene:**
   * Navigate to `Assets/Scenes/` and load either `Menu` or `MainScene` to run the game.
4. **Google Mobile Ads Configuration:**
   * Go to `Assets/Scripts/Game/AdManager.cs` to configure your App and Ad Unit IDs for production.

---

## 🕹️ Controls (Desktop)

*   **Move Left / Right:** `A` / `D` or `Left Arrow` / `Right Arrow`
*   **Jump:** `Space` or `Up Arrow`
*   **Slide:** `S` or `Down Arrow`
