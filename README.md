# 🕯️ TheLastPatient

A VR escape room experience built in Unity 2022.3.6f1, designed for the Meta Quest 3.  
Navigate through a dark, abandoned asylum using a flashlight, and find the Morgue to escape!

---

## 🚀 Project Setup

1. **Unity Version**:  
   - Unity 2022.3.6f1 (LTS)
   - 3D Core Project Template (not URP/HDRP)

2. **Required Unity Packages**:
   - XR Plugin Management
   - XR Interaction Toolkit
   - Oculus XR Plugin
   - TextMeshPro (for UI)

3. **Required External Assets**:
   - [Abandoned Asylum Environment Asset](#)

4. **XR Settings**:
   - XR Plugin Management → Oculus Provider (Standalone + Android)
   - OpenXR Runtime → Set to Oculus
   - XR Origin (Room-Scale) added for player control
   - Continuous Move Provider (Action-Based) for joystick movement

---

## 🎮 Gameplay Features

- **Joystick Movement**: Move using the left thumbstick.
- **Flashlight Mechanic**: Spot Light attached to head (Main Camera).
- **Victory Condition**: Reach the invisible trigger at the Morgue to win.
- **Victory UI**: World-space canvas displays "YOU ESCAPED!" on success.

---

## 🛠️ Development Instructions

1. **Movement**:
   - XR Origin has Character Controller and Continuous Move Provider.
   - Left-hand Move Action mapped to primary 2D Axis (left joystick).

2. **Flashlight**:
   - Spot Light parented to Main Camera.
   - Range: 20–30 units.
   - Spot Angle: ~45–60 degrees.

3. **Victory Trigger**:
   - Invisible Box Collider (IsTrigger enabled) near the Morgue entrance.
   - WinTrigger script detects player collision and activates Victory UI.

4. **Lighting Settings**:
   - Realtime lighting (no baked lightmaps).
   - Skybox ambient environment.

5. **Controls**:
   - Walk: Left Thumbstick (or W/A/S/D during editor simulation with keyboard script).
   - Look: Head rotation (via Main Camera).

---

## 📱 Testing & Deployment

- **In Editor**:  
  - Simulate movement using keyboard W/A/S/D or manual XR Origin dragging.
- **On Quest 3**:  
  - Connect via Meta Link.
  - Enter Play Mode for full VR walking and exploration.

---

## 📋 Future Improvements (Optional)

- Add sound effects (footsteps, ambient asylum noises).
- Add interactive doors and puzzles.
- Implement a flashlight battery mechanic (power draining over time).
- Add fade-out transition when escaping.
- Deploy full APK build to Quest 3 for untethered VR experience.

---

## 📄 License

This project uses free and purchased Unity assets.  
Abide by original asset licenses when distributing builds.

---

> **Built with passion for horror exploration and immersive storytelling. 🏚️🔦**
