# Core Systems

LimbX is built around four interconnected systems:

## 1. Sensorized Glove

The current prototype uses a glove containing multiple pressure and force sensors distributed across different regions of the hand.

When a surface or object touches the glove, the sensing layer captures:

- Contact location
- Hand/finger region
- Contact area
- Applied force
- Applied pressure
- Relative interaction intensity
- Changes in force and pressure over time

The glove currently acts as the prototype sensing platform. In the intended robotic/prosthetic implementation, the sensing elements will be integrated directly into the corresponding regions of the artificial hand.

---

## 2. Real-Time Software Simulation

The sensor data is processed and represented through a local real-time software interface.

The digital hand reproduces the physical interaction detected by the glove, including:

- Contact location
- Contact region
- Contact area
- Force
- Pressure
- Interaction intensity

For example, touching the upper region of the physical thumb results in the corresponding region of the digital hand being represented in the software along with the measured interaction.

The software provides the visualization and processing layer for developing and validating the tactile system.

---

## 3. Vibrotactile Feedback Band

A separate wearable band communicates the detected sensation back to the user through vibration.

The band uses multiple vibration actuators and different vibration patterns to represent different tactile conditions.

The feedback can encode:

**Location → Where the interaction occurred**

**Intensity → How strong the interaction is**

**Pattern → What type of sensation is being communicated**

This creates a learnable connection between the physical interaction detected by the sensing system and the sensation perceived by the user.

---

## 4. Modular CAD & Mechanical Architecture

LimbX is designed around a lightweight, tendon-driven and highly modular mechanical architecture.

The CAD system is designed to be adaptable rather than being restricted to a single fixed limb configuration.

### Mechanical Features

- Lightweight structural design
- Tendon-driven actuation
- Modular CAD architecture
- Flexible attachment interfaces
- Adjustable mounting geometry
- Adaptable limb configuration
- Customizable mechanical dimensions
- Replaceable/modular components
- Flexible actuator placement
- Reduced distal weight
- Designed for integration with different sensing configurations
- Designed to accommodate different residual-limb and attachment requirements

The modular design allows the same underlying platform to be adapted for different users and applications, including above-elbow and below-elbow amputees, below-elbow configurations, people with limited or impaired limb function, paralysis-related applications, disability and assistive applications, and potential wearable robotic augmentation.

The same architecture can also be explored as a wearable robotic extension or **"third arm"** for able-bodied users.

The CAD and mechanical architecture therefore forms the physical platform on which the sensing, software and haptic systems can eventually be integrated.
