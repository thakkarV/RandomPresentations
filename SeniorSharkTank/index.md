name: title-layout
layout: true
class: center, middle, title
---
name: basic-layout
layout: true
class: left, top
???
These two slides are the templates to be used for the rest of the presentation

---
name: title
template: title-layout
# SharTank: Senior Thesis Presentation
.footnote[Vijay Thakkar, Prof. Rich West]
???

---
name: thesis-statement
template: title-layout
#### Design a proof of concept system that allows for Android OS to be emulated on x86 hardware to serve as a host for low criticality (infotainment) processing in the presence of a high criticality sister guest. 
???
- Infrastructure for heterogenous mixed criticality compute for the cars of the future

---
name: modern-needs
template: basic-layout
## Modern Cars, Modern Needs
- Many more sensors
- High bandwidth datapaths (USB, PCIe)
- Large screen based dash/HUD (Android Auto)
- Self driving modules (Drive-AGX)
- Need to Consolidate CAN and USB into central processing

---
name: consolidation-issues
template: basic-layout
## Issue With Consolidation
- Still need CAN/USB for control and infotainment
- But cannot do low criticality processing on RTOS

---
name: solution
tempalte: basic-layout
## Proposed Consolidated Platform
- Single x86 multicore processor
- Quest-V Hypervisor for partitioning hardware
- Quest RTOS for real time processing of CAN and USB
- Shared memory buffer between Quest and Android/Linux
- Low criticality driver in Quest to copy CAN to shared memory
- Device driver in Android to access shared buffer

---
name: thesis-controbution
tempalte: basic-layout
## Thesis Contribution
- Modfications for mapping physical mapping in Quest-V
- Device driver in Quest RTOS for accesssing and writing to shared memory
- Device driver in Android to read from shared buffer and provide a 
- Ensuring and demonstrating preservation of RTOS timing gurantees
