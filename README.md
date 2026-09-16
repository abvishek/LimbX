# LimbX

### Closing the loop between movement and touch.

LimbX is an adaptive wearable robotic limb platform that explores how artificial limbs can sense, understand and communicate physical interaction.

The current prototype combines a sensorized glove, real-time touch simulation and a wearable vibrotactile band, while the mechanical platform is being developed around a lightweight, tendon-driven and highly adaptable CAD architecture.

---

# The Problem

### Imagine reaching out with a robotic hand, touching an object, and not knowing how it feels.

You can see the hand move. You can see the object being touched. But without tactile information, you may not know exactly where contact occurred, how much force was applied, or whether you are gripping too hard.

Prosthetic and wearable robotic hands can restore or extend movement, but the sensory connection between the user and the artificial limb is still limited.

LimbX explores a closed-loop approach that brings this missing connection back:

**Touch → Sense → Understand → Simulate → Feel**

The platform is designed not only for amputees, but also to assist people with paralysis or limited/non-functional limbs, while its wearable architecture can potentially be used by able-bodied users as an additional robotic **"third arm."**

---

# The LimbX Approach

LimbX brings together four core systems:

1. **Tactile Sensing**
2. **Real-Time Touch Simulation**
3. **Vibrotactile Feedback**
4. **Adaptive Mechanical & CAD Architecture**

Together, they form a complete physical-to-digital-to-human feedback loop.

---

# 1. Tactile Sensing — Sensorized Glove

The current prototype uses a glove containing multiple pressure and force sensors distributed across different regions of the hand.

When an object or surface touches the glove, the sensors detect the interaction and capture information such as:

- Contact location
- Finger/hand region
- Contact area
- Applied force
- Applied pressure
- Relative interaction intensity
- Changes in force and pressure over time

For example, if the upper region of the thumb is touched, the system identifies the corresponding region and sends its sensor information to the software.

The glove is currently used as the prototype sensing platform.

In the intended robotic implementation, the same sensing concept can be integrated directly into the corresponding regions of the prosthetic or robotic hand.

---

# 2. Real-Time Touch Simulation

The sensor data from the glove is sent to a local software interface that represents the physical interaction on a digital hand.

The software provides a real-time representation of:

- Where the hand was touched
- Which finger or region was involved
- The area of contact
- Applied force
- Applied pressure
- Interaction intensity
- Changes in the detected interaction

For example:

**Physical interaction:**

A surface touches the upper part of the thumb.

**Software representation:**

The corresponding region of the digital hand is highlighted/represented, along with the detected force and pressure.

This allows the physical tactile interaction to be visualized and analyzed in real time.

---

# 3. Vibrotactile Feedback Band

The detected tactile information is communicated back to the user through a separate wearable vibrotactile band.

The band uses vibration actuators to represent different sensations through different vibration patterns.

The feedback can encode:

**Location → Where the interaction occurred**

**Intensity → How strong the interaction was**

**Pattern → How the sensation is being represented**

This allows the user to learn a relationship between the vibration they feel and the physical interaction occurring at the robotic hand.

The band is a physical hardware component of the current prototype.

---

# 4. Adaptive CAD & Mechanical Architecture

The mechanical system is designed as a lightweight, tendon-driven and highly modular robotic limb rather than a fixed one-size-fits-all structure.

The CAD architecture focuses on adaptability at the level of the limb, joints, mounting interfaces and component placement.

### Key Mechanical Features

- Lightweight structural architecture
- Tendon-driven actuation
- Low distal mass through flexible actuator placement
- Modular finger and joint architecture
- Adjustable limb dimensions
- Flexible attachment interfaces
- Customizable mounting geometry
- Replaceable mechanical modules
- Adaptable actuator and tendon routing
- Reconfigurable mechanical components
- Designed around different limb configurations
- Integration points for tactile sensors
- Integration points for haptic/control electronics
- Geometry that can be modified for individual users

The attachment system is designed so that the robotic limb does not have to be restricted to a single anatomical configuration.

It can be adapted for:

- Above-elbow amputees
- Below-elbow amputees
- Different residual-limb configurations
- People with limited hand function
- People with paralysis
- People with non-functional limbs
- Assistive applications for disabilities
- Rehabilitation-oriented applications
- Able-bodied users

The same underlying platform can also be adapted as a wearable robotic **"third arm"**, allowing users who already have functioning hands to use the robotic limb as an additional physical extension.

The objective is therefore not simply to build one prosthetic hand, but to develop a **flexible robotic limb architecture that can be configured around different users and use cases.**

---

# System Architecture

```text
                    PHYSICAL CONTACT
                           ↓
                  ┌─────────────────┐
                  │ SENSORIZED GLOVE│
                  │                 │
                  │ Force / Pressure│
                  │ Touch / Location│
                  └────────┬────────┘
                           ↓
                  ┌─────────────────┐
                  │    ESP32-S3     │
                  │ DATA PROCESSING │
                  └────────┬────────┘
                           ↓
                  ┌─────────────────┐
                  │ REAL-TIME       │
                  │ SOFTWARE        │
                  │                 │
                  │ Touch Mapping   │
                  │ Contact Area    │
                  │ Force / Pressure│
                  └────────┬────────┘
                           ↓
                  ┌─────────────────┐
                  │ HAPTIC MAPPING │
                  └────────┬────────┘
                           ↓
                  ┌─────────────────┐
                  │ VIBROTACTILE    │
                  │ BAND            │
                  │                 │
                  │ Patterns        │
                  │ Intensity       │
                  └────────┬────────┘
                           ↓
                         USER
