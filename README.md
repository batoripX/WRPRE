# WRPRE: Windows Research Project Reverse Engineering

Welcome to the **Windows Research Project Reverse Engineering (WRPRE)** repository. This project is dedicated to statically mapping, analyzing, and documenting the physical format layouts, export tables, and structural constraints of core Windows system binaries. 

The primary goal of this repository is to provide clean, verifiable architectural data structures to assist alternative toolchains, compilers (such as upstream LLVM and `llvm-mingw`), and interoperability platforms in understanding modern native system interfaces.

## ⚠️ Legal Disclaimer & Notice

* **Unofficial Project:** This repository is an entirely **unofficial, independent research initiative**. It is not affiliated with, authorized, sponsored, endorsed, or in any way officially connected to Microsoft Corporation or any of its subsidiaries or affiliates. 
* **Maintainer:** This project is solely developed, maintained, and curated by a solo independent developer.
* **Scope of Content:** The logs and data files hosted here are the result of purely **static analysis** and structural extraction via open-source tools (such as `llvm-objdump`). No proprietary source code is contained within this repository. This documentation maps public interfaces, export ordinals, calling conventions, and byte alignments solely for the purpose of interoperability, which is legally protected under copyright principles governing functional interfaces.
* **Trademarks:** "Windows", "Microsoft", and related system binary names are registered trademarks of Microsoft Corporation.

## 📁 Repository Contents

* `logs/kernel32_structure.log`: A comprehensive mapping of the physical layout headers, PE32+ security traits (ASLR, High Entropy VA, Control Flow Guard), and the Import/Export Address Tables tracking API Set virtualization layers (`api-ms-win-core-*`).
* `logs/kernel32_disassembly.log`: A clean static disassembly tracking function padding alignments (`int3`), x64 ABI calling convention frame structures, and RIP-relative addressing patterns.

## 📜 License

This project, its documentation, and extracted structural data maps are licensed under the **GNU General Public License v3.0 (GPLv3)**. 

This program and its data are distributed in the hope that they will be useful for alternative toolchain development and educational research, but **WITHOUT ANY WARRANTY**; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the `LICENSE` file for more details.
