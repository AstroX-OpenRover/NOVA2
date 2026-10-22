# NOVA2

**Rover CAD and bill of materials from AstroX at Georgia Tech.**

This repository contains the mechanical design files and bill of materials for NOVA2, a research rover developed in the **AstroX: Aerospace Stochastic Robotics and Exploration Lab** at the Georgia Institute of Technology. The files support inspection of the rover assembly, modification of its components, and hardware build planning.

The design files include the chassis, swerve modules, differential linkage, wheels, electronics enclosures, and sensor mounts. The bill of materials lists four drive gearmotors, four DYNAMIXEL servos, and the computing, sensing, and electrical components.

**Start here:** [Main rover assembly](Assembly/NOVA_V2_Assembly.SLDASM) · [Bill of materials](BOM.xlsx) · [All CAD files](Assembly/)

## Repository contents

| Location | Contents |
| --- | --- |
| [`Assembly/`](Assembly/) | SOLIDWORKS assemblies and parts, with STEP files for selected components. |
| [`Assembly/NOVA_V2_Assembly.SLDASM`](Assembly/NOVA_V2_Assembly.SLDASM) | Main NOVA2 rover assembly. |
| [`BOM.xlsx`](BOM.xlsx) | Component names, quantities, suppliers, and purchase links. |

### CAD assemblies

| Subsystem | Files |
| --- | --- |
| Rover | [`NOVA_V2_Assembly.SLDASM`](Assembly/NOVA_V2_Assembly.SLDASM) |
| Chassis | [`NOVA_Assembly_Chassis.SLDASM`](Assembly/NOVA_Assembly_Chassis.SLDASM), [`NOVA_Chassis_Assembly.SLDASM`](Assembly/NOVA_Chassis_Assembly.SLDASM) |
| Differential linkage | [`NOVA_Assembly_Diff_Bar.SLDASM`](Assembly/NOVA_Assembly_Diff_Bar.SLDASM), [`NOVA_Assembly_Diff_Bar_Connect.SLDASM`](Assembly/NOVA_Assembly_Diff_Bar_Connect.SLDASM) |
| Right drivetrain | [`NOVA_Assembly_Right_Drivetrain.SLDASM`](Assembly/NOVA_Assembly_Right_Drivetrain.SLDASM) |
| Swerve modules | [`SwereModuleV2.SLDASM`](Assembly/SwereModuleV2.SLDASM), [`SwereModuleDynamicsV2.SLDASM`](Assembly/SwereModuleDynamicsV2.SLDASM), and their component assemblies |

The links preserve the filenames used in the repository, including the `SwereModule` spelling.

## Getting started

### Download the files

Clone the repository:

```bash
git clone https://github.com/AstroX-OpenRover/NOVA2.git
cd NOVA2
```

Alternatively, select **Code → Download ZIP** on the repository page and extract the archive.

Download the entire repository and keep the folder structure and filenames intact. The SOLIDWORKS assemblies reference separate part and subassembly files.

### Open the rover assembly

1. Open `Assembly/NOVA_V2_Assembly.SLDASM` in a compatible version of **SOLIDWORKS**.
2. If SOLIDWORKS requests a referenced file, locate it in the downloaded `Assembly/` directory.
3. Check for unresolved references and rebuild errors before modifying or exporting the design.
4. Open the relevant subassembly or part to make a change, then check it in the rover assembly.

The required SOLIDWORKS release has not yet been documented. If a file cannot be opened, include your SOLIDWORKS version and the exact error when reporting the issue.

### File formats

| Extension | Use |
| --- | --- |
| `.SLDASM` | Native SOLIDWORKS assemblies and subassemblies. |
| `.SLDPRT` | Native SOLIDWORKS part models. |
| `.STEP`, `.step`, `.stp` | Neutral CAD files for selected components. |
| `.xlsx` | Bill of materials, viewable in Excel or another compatible spreadsheet application. |

The STEP files cover selected components. A complete rover STEP export and STL fabrication files are not currently included.

## Hardware overview

The following components are listed in [`BOM.xlsx`](BOM.xlsx). Use the workbook for the full list, quantities, suppliers, and purchase links.

| Function | Listed components |
| --- | --- |
| Drive | Four 100:1 metal gearmotors, 37D × 73 mm; Cytron MDD10A motor drivers. |
| Steering | Four DYNAMIXEL XL430-W250-T servos; ROBOTIS U2D2 and U2D2 Power Hub Board Set. |
| Onboard computing | NVIDIA Jetson Orin Nano Developer Kit. |
| Microcontroller | Raspberry Pi Pico 2 W. |
| Sensing | ZED 2i stereo camera and BNO055 IMU. |
| Power | 3S, 11.1 V, 10,000 mAh LiPo battery listing; Matek power distribution board and rocker switch. |
| Mechanical hardware | Bearings, timing belts and pulleys, aluminum tubes and shafts, couplers, fasteners, and heat-set inserts. |

CAD models of purchased components are included to support mechanical integration. Their presence does not establish firmware or software support.

## Using the bill of materials

The workbook groups components into motors, electrical hardware, connector cables, mechanical hardware, and miscellaneous supplies. Some quantities refer to retail packs rather than individual installed parts.

The following entries need confirmation before ordering:

- **Timing belt:** the BOM lists a 220 mm belt, while the CAD folder contains `200mm Belt.SLDPRT`. Confirm the intended belt length against the assembly.
- **Pulley bore:** the BOM's 6 mm shaft pulley entry has a link label describing a 5 mm bore. Check the selected product variant.
- **Heat-set inserts:** several purchase-link labels name a different thread size from the corresponding item. Confirm the M3, M4, and M5 selections.

## Build documentation

This repository currently provides CAD files and a bill of materials. Fabrication drawings, print settings, step-by-step assembly instructions, wiring diagrams, firmware, and rover control software are not included. The supported SOLIDWORKS version also remains to be documented.

## Contributing

Use [GitHub Issues](https://github.com/AstroX-OpenRover/NOVA2/issues) to report missing references, BOM discrepancies, or proposed design changes. Include the affected filename, software version, and a screenshot or description of the problem.

For CAD contributions:

- Describe the mechanical change and the reason for it.
- Include any modified parts and dependent assemblies.
- Preserve filenames where possible and update assembly references when renaming files.
- Update the BOM when a change affects purchased components or quantities.
- Include a neutral CAD export when practical, and state whether the change has been checked in CAD or tested on hardware.

## Lab

**AstroX: Aerospace Stochastic Robotics and Exploration Lab**  
Daniel Guggenheim School of Aerospace Engineering  
Georgia Institute of Technology

[Lab website](https://aerospaceroboticslab.ae.gatech.edu/) · [AstroX-OpenRover on GitHub](https://github.com/AstroX-OpenRover)

