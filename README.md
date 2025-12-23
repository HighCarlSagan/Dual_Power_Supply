# Universal Power Supply Unit (PSU)

A compact dual-output power supply board providing regulated 3.3V and 5V rails, each capable of delivering up to 6A.

## Specifications

- **Input:** AC mains (via MEAN WELL IRM-60-12)
- **Output 1:** 3.3V @ 6A max
- **Output 2:** 5V @ 6A max
- **Total Power:** 60W maximum
- **Intermediate Rail:** 12V DC (from AC/DC converter)

## Key Components

- **AC/DC Converter:** MEAN WELL IRM-60-12 (60W, 12V output)
- **DC/DC Converter:** Texas Instruments TLVM14406RCHR (high-efficiency buck converter)

## Features

- Dual regulated outputs (3.3V and 5V)
- 6A current capability per rail
- Compact PCB design
- Integrated thermal management
- Complete with 3D models for mechanical integration

## Project Contents
```
universal-psu/
├── universal-psu.kicad_sch       # Main schematic (includes design calculations)
├── universal-psu.kicad_pcb       # PCB layout
├── Subsheets/                    # Hierarchical schematic sheets
│   ├── DC_DC_Converter_3v3.kicad_sch
│   └── DC_DC_Converter_5V.kicad_sch
├── libraries/
│   ├── symbols/                  # Custom KiCad symbols
│   │   ├── IRM-60-12.kicad_sym
│   │   └── TLVM14406RCHR.kicad_sym
│   ├── footprints/               # Custom footprints
│   │   ├── CONV_IRM-60-12.kicad_mod
│   │   └── CONV_TLVM14406RCHR.kicad_mod
│   └── 3dmodels/                 # 3D models for visualization
│       ├── IRM-60-12.step
│       └── RCH0028B.stp
└── README.md
```

## Design Notes

All component calculations and design mathematics are included directly in the schematic files. This includes:
- Buck converter component selection
- Output capacitor sizing
- Thermal considerations
- Load current distribution

## Opening the Project

1. Clone this repository:
```bash
   git clone git@github.com:HighCarlSagan/Dual_Power_Supply.git
   cd Dual_Power_Supply
```

2. Open `universal-psu.kicad_pro` in KiCad 7.0 or later

3. All custom symbols, footprints, and 3D models will load automatically from the `libraries/` folder

## Bill of Materials (BOM)

Key components:
- 1x MEAN WELL IRM-60-12 AC/DC Converter
- 2x TI TLVM14406RCHR Buck Converter IC
- Additional passives and connectors (see schematic for complete BOM)

## Applications

- Embedded system power supply
- Microcontroller projects requiring dual voltage rails
- IoT device power management
- Prototyping and development boards


## Author

Mayank S

## Version History

- **v1.0** - Initial design with 3.3V and 5V outputs
