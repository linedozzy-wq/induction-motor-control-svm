# Induction Motor Scalar Control with S-Curve Profile

## Overview
Development of a scalar (V/f) control system for an induction motor featuring:
- S-curve acceleration/deceleration profiles
- Motor parameter identification
- Space Vector PWM implementation
- Real-time embedded control on TI DSP

## Features
- **S-Curve Acceleration**: Smooth start/stop with configurable jerk limits
- **Motor Parameter Identification**: Automated Rs, Ls, Lσ measurement
- **V/f Control with IR Compensation**: Voltage boost at low frequencies
- **Real-time Implementation**: 5kHz PWM on TMS320F28035
- **ADC Calibration**: Current and speed measurement processing

## Repository Structure
Induction-Motor-Scalar-Control/
│
├── README.md                 # Project overview
├── Documentation/
│   ├── Course_Project.pdf    # Your original document
│   ├── Technical_Report.md   # Summary in English
│   └── Schematics/           # Circuit diagrams
│
├── Simulation/
│   ├── SimInTech_Models/     # SimInTech simulation files
│   ├── Results/              # Simulation plots
│   └── README.md
│
├── Embedded_Code/
│   ├── src/
│   │   ├── main.c            # Main control loop
│   │   ├── ramp_generator.c  # S-curve algorithm
│   │   ├── svpwm.c           # Space Vector PWM
│   │   ├── motor_parameters.c
│   │   └── adc_processing.c
│   ├── inc/                  # Header files
│   ├── CCS_Project/          # Code Composer Studio project
│   └── README.md
│
├── Results/
│   ├── Oscilloscope_Captures/
│   ├── Performance_Data/
│   └── Comparisons/
│
└── .gitignore

## Results
- Successful motor start from 0 to 50 Hz in 1 second
- Reduced inrush current by 40% compared to linear acceleration
- Stable operation across full frequency range

## Technologies
- **Hardware**: TI TMS320F28035 DSP, IGBT inverter, induction motor
- **Software**: Code Composer Studio v10+, C language
- **Simulation**: SimInTech for system modeling
- **Control Theory**: Scalar control, SVPWM, discrete-time filtering
