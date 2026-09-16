# LimbX

### Closing the loop between movement and touch.

LimbX is an ongoing project exploring tactile sensing and sensory feedback for prosthetic and wearable robotic systems.

The current prototype combines a sensorized glove, a real-time software interface, and a wearable vibrotactile band. The glove captures where contact occurs and how much force or pressure is applied, the software represents this interaction on a digital hand model, and the haptic band communicates the detected sensation back to the user through vibration patterns.

---

## Overview

A robotic or prosthetic hand can physically interact with objects, but the user does not naturally receive the same tactile information as they would from a biological hand.

LimbX explores a closed-loop sensory system that can detect physical interaction, represent it digitally, and communicate the information back to the user through haptic feedback.

The current prototype uses a glove as the sensing platform. The same sensing and feedback architecture is intended to be integrated directly into a prosthetic or robotic hand in future iterations.

---

## Current Prototype

The current system consists of three main parts:

### 1. Sensorized Glove

The glove contains multiple pressure and force sensors distributed across different regions of the hand.

When an object or surface comes into contact with the glove, the sensors detect the interaction.

The system captures information such as:

- Location of contact
- Hand/finger region involved
- Applied force
- Applied pressure
- Relative contact intensity
- Spatial distribution of the interaction

The glove acts as a prototype sensing platform for the tactile system.

In the intended prosthetic implementation, these sensors would be integrated into the corresponding regions of the prosthetic hand rather than the glove.

---

### 2. Real-Time Touch Simulation

Sensor data from the glove is sent to a local software interface that represents the physical interaction on a digital hand model.

The software provides a real-time visualization of:

- Which part of the hand is being touched
- The approximate contact location
- The region or area where contact is occurring
- Force applied to the contacted region
- Pressure applied to the contacted region
- Changes in interaction intensity

For example, when the upper region of the thumb is touched on the physical glove, the corresponding region of the digital hand is highlighted or represented in the software along with the measured force and pressure.

This creates a digital representation of the tactile interaction occurring on the physical hand.

---

### 3. Vibrotactile Feedback Band

A separate wearable band provides tactile feedback to the user through vibration.

The vibration response changes according to the information detected by the glove.

Different sensations and interaction conditions can be represented using different vibration patterns.

The feedback can encode information such as:

- Where the contact occurred
- The intensity of the interaction
- Changes in applied force or pressure
- Different detected touch conditions

The goal is to allow the user to learn the relationship between the vibration patterns and the corresponding physical sensations.

---

## System Flow

```text
          PHYSICAL CONTACT
                 ↓
          SENSORIZED GLOVE
                 ↓
       Force / Pressure Data
                 ↓
          DATA PROCESSING
                 ↓
       REAL-TIME SOFTWARE
                 ↓
       DIGITAL HAND MODEL
                 ↓
        HAPTIC INTERPRETATION
                 ↓
       VIBROTACTILE BAND
                 ↓
               USER
