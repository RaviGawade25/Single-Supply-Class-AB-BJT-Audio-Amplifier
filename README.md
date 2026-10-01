# Single-Supply Class-AB BJT Audio Amplifier

A discrete BJT-based audio amplifier designed and implemented using a **Class-A pre-amplifier** followed by a **Class-AB complementary push-pull power amplifier**. The system operates from a single **+12 V DC supply** and is designed to drive an **8 Ω speaker**.

## Project Overview

The amplifier consists of two main stages:

1. **Class-A Pre-Amplifier**
   - 2N3904 NPN transistor
   - Common-emitter configuration
   - Provides voltage amplification
   - Voltage-divider biasing

2. **Class-AB Power Amplifier**
   - TIP31 NPN transistor
   - TIP32 PNP transistor
   - Complementary push-pull configuration
   - Diode-based biasing using 1N4148
   - Provides current and power amplification
   - Reduces crossover distortion

## Key Specifications

| Parameter | Specification |
|---|---|
| Supply | +12 V DC |
| Input | ~300–400 mV peak-to-peak |
| Pre-Amplifier | Class-A BJT |
| Power Stage | Class-AB push-pull |
| Pre-Amplifier Transistor | 2N3904 |
| Output Transistors | TIP31 / TIP32 |
| Biasing | Voltage divider + diode bias |
| Load | 8 Ω speaker |
| Audio Range | 20 Hz–20 kHz |
| Coupling | Capacitor coupled |

## Circuit Architecture

```text
Audio Input
    │
    ▼
Input Coupling Capacitor
    │
    ▼
Class-A Pre-Amplifier
(2N3904 Common Emitter)
    │
    ▼
Inter-Stage Coupling
    │
    ▼
Class-AB Push-Pull Stage
(TIP31 + TIP32)
    │
    ▼
Output Coupling Capacitor
    │
    ▼
8 Ω Speaker
```

## Design Highlights

- Designed a complete discrete BJT audio amplification chain.
- Implemented Class-A voltage amplification followed by Class-AB power amplification.
- Used complementary TIP31/TIP32 transistors for the push-pull output stage.
- Implemented diode biasing to reduce crossover distortion.
- Used input, inter-stage, and output capacitors for AC coupling and DC blocking.
- Designed the system for single-supply +12 V operation.
- Analysed BJT biasing, voltage gain, current gain, power output, and efficiency.
- Verified the design using circuit simulation before hardware implementation.

## Simulation and Hardware Validation

The circuit was simulated using **Proteus** with a low-level audio/sine-wave input. The simulated amplifier demonstrated stable biasing, voltage amplification, smooth output waveform behaviour, and the ability to drive an 8 Ω load.

The design was subsequently implemented on a breadboard and tested with real audio input. Hardware observations showed behaviour consistent with the simulation, with reduced crossover distortion and stable operation at moderate output levels.

## Results

| Parameter | Theoretical | Simulation | Hardware |
|---|---:|---:|---:|
| Pre-Amplifier Gain | -4.56 | ~-4.5 | ~-4.4 |
| Overall Gain | 13.34 dB | ~13.3 dB | ~13.2 dB |
| Crossover Distortion | Reduced | Reduced | Reduced |
| Output Stability | Stable | Stable | Stable |

## Components

- 2N3904 NPN transistor
- TIP31 NPN power transistor
- TIP32 PNP power transistor
- 1N4148 diodes
- Resistors
- Coupling capacitors
- +12 V DC supply
- 8 Ω speaker

## Tools

- Proteus
- Analog circuit analysis
- BJT biasing
- Oscilloscope/waveform analysis
- Breadboard prototyping

## Project Structure

```text
Single-Supply-Class-AB-BJT-Audio-Amplifier/
│
├── README.md
├── Simulation/
│   ├── circuit/
│   └── waveforms/
│
├── Hardware/
│   ├── breadboard/
│   └── pcb/
│
├── Documentation/
│   └── Project_Report.pdf
│
└── Results/
    ├── input_waveform/
    ├── output_waveform/
    └── measurements/
```

## Applications

- Low-power audio systems
- Portable audio devices
- Educational analog electronics platforms
- Laboratory demonstrations
- Embedded audio applications
- Small speaker systems

## Future Improvements

- Replace diode biasing with a VBE multiplier for improved thermal stability.
- Add negative feedback for improved gain stability and lower distortion.
- Add heat sinking for higher-power operation.
- Integrate volume and tone control.
- Investigate a MOSFET-based output stage.

## Authors

**Ravi A Gawade**  
**Mail : ravigawade2005@gmail.com**

Department of Electronics and Communication Engineering  
KLE Technological University, Hubballi  
Academic Year: 2025–26
