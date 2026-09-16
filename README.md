# LimbX

### Closing the loop between movement and touch.

LimbX is an ongoing project exploring tactile sensing and sensory feedback for prosthetic and wearable robotic systems.

The current prototype combines a sensorized glove, a real-time software interface, and a wearable vibrotactile band. The glove detects where contact occurs and how much force or pressure is applied, the software maps and visualizes the interaction on a digital hand, and the haptic band communicates the detected sensation back to the user through different vibration patterns.

Alongside the sensory system, LimbX is being developed around a lightweight, tendon-driven and highly modular CAD architecture with flexible attachment and adjustment interfaces for different users and applications.

---

## Overview

Robotic and prosthetic hands can perform movements and interact with objects, but users often lack direct sensory information about where contact occurs and how much force is being applied.

LimbX explores a closed-loop approach to this problem by:

1. Detecting physical contact and force
2. Mapping the interaction to a digital representation of the hand
3. Visualizing the location, area, pressure and force in real time
4. Converting the detected sensation into haptic feedback
5. Communicating the sensation back to the user through a wearable vibrotactile band

The current glove-based prototype provides a way to develop and validate this sensory architecture before integrating the sensing system directly into a robotic or prosthetic hand.

---

# Current Prototype

The current system consists of three primary components:

## 1. Sensorized Glove

The glove acts as the current tactile sensing platform.

It contains multiple pressure and force sensors distributed across different regions of the hand. When an object, surface or another force interacts with the glove, the sensors detect the resulting changes.

The system captures information including:

- Contact location
- Hand and finger region
- Applied force
- Applied pressure
- Contact intensity
- Contact area or region
- Changes in interaction over time

For example, if the upper region of the thumb is touched, the corresponding region of the digital hand is identified and represented in the software.

The glove is used as a prototype implementation of the sensing architecture. In the intended robotic/prosthetic implementation, these sensors would be integrated into the corresponding regions of the artificial hand.

---

# 2. Real-Time Touch Simulation

Sensor data from the glove is transmitted to a local software interface.

The software creates a real-time digital representation of the hand and maps the physical interaction detected by the glove onto the corresponding region of the digital hand.

The interface represents:

- Where the hand is being touched
- Which finger or region is involved
- The approximate location of contact
- The area or region of contact
- Applied force
- Applied pressure
- Relative interaction intensity
- Changes in the detected interaction

For example:

```text
Physical Interaction
        ↓
Thumb Sensor Activated
        ↓
Sensor Location Identified
        ↓
Digital Thumb Region Mapped
        ↓
Force / Pressure Displayed
