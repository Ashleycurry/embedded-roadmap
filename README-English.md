<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F172A,45:1E3A8A,100:0EA5E9&height=210&section=header&text=Embedded%20Systems%20Roadmap&fontSize=44&fontColor=FFFFFF&fontAlignY=38&animation=fadeIn&desc=From%20Circuit%20Theory%20to%20RTOS%20and%20Linux&descAlignY=64&descSize=17" alt="Embedded Systems Roadmap" />

# Embedded Systems Roadmap

**From Ohm's law to task scheduling, from register bit-fields to system calls.**

<p>
  <a href="https://github.com/Ashleycurry?tab=repositories"><img src="https://img.shields.io/badge/Repositories-9-0EA5E9?style=flat-square&logo=github&logoColor=white" alt="Repositories" /></a>
  <img src="https://img.shields.io/badge/Course_Docs-16-0284C7?style=flat-square" alt="Course documents" />
  <img src="https://img.shields.io/badge/Language-中文%20%7C%20English-BAE6FD?style=flat-square" alt="Bilingual" />
  <img src="https://img.shields.io/badge/License-MIT-0369A1?style=flat-square" alt="MIT" />
</p>

[中文](README.md) | [English](README-English.md)

<p>
  <img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black" alt="C" />
  <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white" alt="C++" />
  <img src="https://img.shields.io/badge/ARM_Cortex--M-0091BD?style=flat-square&logo=arm&logoColor=white" alt="ARM Cortex-M" />
  <img src="https://img.shields.io/badge/STM32-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white" alt="STM32" />
  <img src="https://img.shields.io/badge/FreeRTOS-2C3E50?style=flat-square" alt="FreeRTOS" />
  <img src="https://img.shields.io/badge/EasyEDA-0EA5E9?style=flat-square" alt="EasyEDA" />
  <br />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux" />
  <img src="https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white" alt="Bash" />
  <img src="https://img.shields.io/badge/GCC-A42E2B?style=flat-square&logo=gnu&logoColor=white" alt="GCC" />
  <img src="https://img.shields.io/badge/Makefile-6D00CC?style=flat-square" alt="Makefile" />
  <img src="https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white" alt="CMake" />
  <img src="https://img.shields.io/badge/Keil_MDK-394049?style=flat-square" alt="Keil MDK" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git" />
</p>

</div>

---

## What This Is

This is an **index repository**. It does not store the course material itself.

It strings the embedded systems notes scattered across 9 independent repositories into a single reading path, running from language fundamentals through to system development. Each repository covers exactly one knowledge domain, and can be cloned and studied on its own or followed in numerical order.

```text
> power on ...
[BOOT] loading embedded-roadmap v1.0.0
[ OK ] 01-02  language & algorithms  · c / data structures
[ OK ] 03-05  circuits & hardware    · analog / digital / pcb
[ OK ] 06-09  chips & systems        · stm32 / freertos / linux
[INFO] recommended entry : c-systems-programming-handbook
[INFO] target            : read a datasheet, bring up a chip, ship a firmware
```

## System Overview

```mermaid
flowchart TB
    subgraph P1["Foundations"]
        direction LR
        N1["01<br/>C Language"]
        N2["02<br/>Data Structures"]
        N1 --> N2
    end

    subgraph P2["Hardware"]
        direction LR
        N3["03<br/>Analog Circuits"]
        N4["04<br/>Digital Logic"]
        N5["05<br/>Schematic and PCB"]
        N3 --> N4 --> N5
    end

    subgraph P3["Systems"]
        direction LR
        N6["06<br/>STM32 MCU"]
        N7["07<br/>FreeRTOS"]
        N8["08<br/>Linux and Shell"]
        N9["09<br/>Linux Applications"]
        N6 --> N7 --> N8 --> N9
    end

    P1 --> P2 --> P3

    classDef c1 fill:#0F172A,stroke:#38BDF8,color:#BAE6FD,stroke-width:1px
    classDef c2 fill:#1E3A8A,stroke:#7DD3FC,color:#E0F2FE,stroke-width:1px
    classDef c3 fill:#0EA5E9,stroke:#BAE6FD,color:#F8FAFC,stroke-width:1px
    class N1,N2 c1
    class N3,N4,N5 c2
    class N6,N7,N8,N9 c3
```

## Repository Index

Listed in recommended reading order, from language fundamentals through to system development.

| Repository | Description |
| :--- | :--- |
| `01` [**c-systems-programming-handbook**](https://github.com/Ashleycurry/c-systems-programming-handbook) | C core syntax, pointers, preprocessor, custom types, dynamic memory, and file I/O |
| `02` [**data-structures-and-algorithms**](https://github.com/Ashleycurry/data-structures-and-algorithms) | Arrays, linked lists, stacks, queues, searching and sorting with complexity analysis |
| `03` [**analog-circuits-and-components**](https://github.com/Ashleycurry/analog-circuits-and-components) | Electrical fundamentals, RLC components, diodes, BJTs, MOSFETs, and practical circuits |
| `04` [**digital-logic-and-computer-organization**](https://github.com/Ashleycurry/digital-logic-and-computer-organization) | Logic gates, flip-flops, Von Neumann model, instruction sets, buses, and boot flow |
| `05` [**schematic-and-pcb-design**](https://github.com/Ashleycurry/schematic-and-pcb-design) | EasyEDA schematic capture, PCB layout and routing, footprint design, and soldering |
| `06` [**stm32-mcu-development-notes**](https://github.com/Ashleycurry/stm32-mcu-development-notes) | GPIO, interrupts, timers, DMA, ADC, SPI, CAN, Ethernet, and low-power management |
| `07` [**freertos-learning-notes**](https://github.com/Ashleycurry/freertos-learning-notes) | Task scheduling, kernel porting, queues, semaphores, event groups, and memory management |
| `08` [**linux-shell-regex-notes**](https://github.com/Ashleycurry/linux-shell-regex-notes) | Ubuntu system administration, shell scripting, and regular expression text processing |
| `09` [**linux-application-development-notes**](https://github.com/Ashleycurry/linux-application-development-notes) | GCC toolchain, file I/O, processes and threads, IPC, sockets, and epoll |

## Repository Conventions

Every indexed repository follows the same layout, so they can be read and searched as a set:

```text
repository/
├── README.md            Chinese index and content overview
├── README-English.md    English index
└── docs/
    ├── <title>.pdf      Course document (read-only, easy to preview)
    └── <title>.docx     Editable version
```

- The `README` serves as an index and study guide only — **full definitions, diagrams, and examples live in the `docs/` documents**.
- Each document ships in both PDF and DOCX: PDF for online reading, DOCX for annotation and excerpting.
- Every repository ends with a `关键词` (keywords) section listing the technical terms it covers, for easier search.
- Scope follows the source course material; no untested conclusions are stated.

## Links

- **Profile**: [github.com/Ashleycurry](https://github.com/Ashleycurry)
- **Blog**: [xiaogao-code.space](https://xiaogao-code.space)

## License

[MIT](LICENSE) © 2026 xiaogao-code

---

<div align="center">

<sub>Build close to the machine. Bring intelligence to the edge.</sub>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0EA5E9,55:1E3A8A,100:0F172A&height=110&section=footer&animation=fadeIn" alt="footer" />

</div>
