# 🪂 HARP-X: High Altitude Release Point Calculation APP

> An advanced aerial delivery calculation tool designed to compute precise aircraft release point coordinates for High Altitude High Opening (**HAHO**) and High Altitude Low Opening (**HALO**) cargo and heavy equipment operations.

---
🚀 **Live Demo:** *URL will be posted here pretty soon!*

---

## 🛠️ Tech Stack & Specifications

| Category | Details |
| :--- | :--- |
| **Language** | Python 🐍 |
| **Framework** | Streamlit 🎈 |
| **Security** | Custom Session Authentication via `hashlib` 🔒 |
| **Standard / Manual** | U.S. Air Force **AFI / AFM 11-231** (CARP Procedures) 📖 |
| **Domain** | Military Aviation, Flight Planning & Ballistic Calculations ✈️ |

---

## 💡 Key Features & Operational Workflow

### 1. 🔐 Authentication & Session Security
- Built-in lightweight user verification mechanism.
- Session tokens dynamically generated using Python's `hashlib` library.

### 2. 📥 Multi-Parametric Data Ingestion
The application collects real-time operational and environmental inputs:
- **Aircraft & Payload Specs:** Aircraft type, parachute type/quantity, total load, Indicated Airspeed (IAS), Magnetic Course (MC).
- **Altitudes & Dropping Dynamics:** Operation mode (HAHO vs. HALO), drop pressure altitude, activation altitude, drop indicated true altitude, Point of Impact (PI) elevation.
- **Meteorological Parameters:** Dropzone (DZ) pressure, Outside Air Temperature (OAT) at drop altitude, wind metrics at both drop altitude and DZ level, DZ geographic coordinates.

### 3. ⚙️ Background Physics & Ballistic Engine
Upon data ingestion, the core engine automatically resolves complex atmospheric and flight vector equations:
- **Atmospheric Corrections:** Dropzone altimeter setting, Pressure Altitude Variation (PAV), International Standard Atmosphere (ISA) temperature offset, $D$-value, and actual drop altitude.
- **Kinematic & Fall Dynamics:** Forward travel time/distance, high-velocity and low-velocity time of fall.
- **Navigation Vectoring:** True Airspeed (TAS), Magnetic Heading (MH), Groundspeed (GS) corrected for wind drift, and total payload drift offset.

### 4. 🎯 Precision Output
- Calculates and delivers the exact **Release Point Geographic Coordinates** formatted in:
  - **Decimal Degrees (DD)**
  - **Degrees, Minutes, Seconds (DMS)**

---

> ⚠️ **Notice on Source Code Access**  
> Due to particular ballistic calculation models, parameters, and flight algorithms, the source code for this project is maintained in a **private repository**.  
>  
> *For technical inquiries, system architecture discussions, or a live presentation of the application, feel free to reach out directly.*
