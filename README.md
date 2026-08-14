# AltiumLibrary
Component library for Altium Designer projects.
The library consists of the following files and directories:
- **pcb contains** component footprints stored in .PcbLib libraries;
- **sch** contains schematic symbols stored in .SchLib libraries;
- **Scripts** contains executable scripts;
- **Template of sheets** contains schematic drawing sheets;
- **Altium DataBase Library** contains components from the MOP component list and foreign-manufactured components;
- Component database in Excel format.

SCH library design convention for **.SchLib** files:
- TBD.

PCB library design convention for **.PcbLib** files:
1. Pattern name: package type (in case of the standard package), or manufacturer part number;
2. Description: taken from Digikey site with package type (package/case) and dimensions in format L X.XX mm x W X.XX mm;
3. Height: According to drawing from the component's datasheet;
4. Pads size: According to drawing from the component's datasheet;
5. Pads enumeration: According to drawing from the component's datasheet;
6. Pads location: According to drawing from the component's datasheet;
7. Pads Paste Mask Expansion for stencil fabrication and automated PCB assembly: Expansion value from rule;
8. Pads Solder Mask Expansion for PCB fabrication tolerances and reliable pad exposure: Expansion value from rule;
9. Mechanical 13:
- Replicates 3D model borders;
- Line width is 0.1 mm.
10. 3D model:
- Attached to the pattern;
- Type - Generic 3D model, realistic;
- Placed on Mechanical 13;
- Has pin 1 mark (if necessary);
- 3D model's Pins locations correspond to the component's pads locations;
- No standoff between the component and a PCB.
11. Top Overlay:
- The shape is similar to the component's bounds;
- Line width is 0.2 mm;
- Pin 1 is marked by a dot diameter 0.3 mm (if necessary);
- The line doesn't go over any pad.

> [!NOTE]
> To reduce assembly risks, remove the silkscreen lines and keep only the First Pin Mark Dot.

12. Mechanical 15:
- Line width is 0.05 mm;
- Cross at the geometric center of the component;
- Corresponds to the pattern's overall size.
13. Reference point: Located in the center of the pattern.
