# 🖥️ RISC-V Virtual Machine (C Implementation)

## 🚀 Overview
This project is a **C-based Virtual Machine (VM)** that interprets a **simplified RISC-V-like instruction set**. It emulates a small CPU by executing binary instructions, managing memory and registers, and handling I/O operations.

### **Key Features**
- **Memory Management:** Supports **instruction memory, data memory, and heap memory**.
- **Register Emulation:** Implements **32 CPU registers**.
- **Instruction Execution:** Supports arithmetic, logic, memory, and control flow operations.
- **I/O Handling:** Reads/writes **characters and integers**, supports **memory-mapped I/O**.
- **Heap Allocation:** Uses a **linked list-based allocator** for dynamic memory.
- **Basic Debugging Features:** Dumps registers and memory when requested.

📜 **Source Code:** [GitHub Repository](https://github.com/your-username/vm-riscv)

---

## 🔧 Installation & Setup

### **1️⃣ Clone the Repository**
```sh
git clone https://github.com/your-username/vm-riscv.git
cd vm-riscv
```

### **2️⃣ Compile the Virtual Machine**
```sh
gcc -g -o vm_riskxvii vm_riskxvii.c
```

### **3️⃣ Run the Virtual Machine with a Program**
```sh
./vm_riskxvii program.bin
```
Where `program.bin` is a binary file containing RISC-V-like machine instructions.

---

## 🏗️ Virtual Machine Components

### **📌 Memory Layout**
| Memory Section | Size | Description |
|--------------|------|-------------|
| **Instruction Memory** | 1024 bytes | Stores program instructions |
| **Data Memory** | 1024 bytes | Stores variables and temporary data |
| **Heap Memory** | 64-byte blocks | Managed via linked list for dynamic allocation |
| **Registers (`regs[32]`)** | 32 registers | CPU register emulation |

### **🔹 Supported Instructions**
- **Arithmetic & Logic:** `add`, `sub`, `xor`, `or`, `and`
- **Shift Operations:** `sll`, `srl`, `sra`
- **Memory Operations:** `lw`, `lh`, `lb`, `sw`, `sh`, `sb`
- **Branching:** `beq`, `bne`, `blt`, `bltu`, `bge`, `bgeu`
- **Jumping:** `jal`, `jalr`
- **Heap Management:** `malloc`, `free`
- **I/O Operations:** `printf`, `scanf` for console interactions

### **📌 Special Memory-Mapped Operations**
| Address | Operation |
|---------|-----------|
| `2048` | Console Write Character |
| `2052` | Console Write Signed Integer |
| `2056` | Console Write Unsigned Integer |
| `2060` | Halt CPU Execution |
| `2080` | Dump PC (Program Counter) |
| `2084` | Dump Registers |
| `2088` | Dump Memory Word |
| `2096` | `malloc` (Heap Allocation) |
| `2100` | `free` (Heap Deallocation) |

---

## 🛠️ How It Works
### **1️⃣ Initialization**
- Reads a **binary file** (`program.bin`) containing **machine instructions**.
- Initializes **memory banks** as a **linked list**.
- Sets up **registers** and **program counter** (`pc`).

### **2️⃣ Fetch-Decode-Execute Loop**
- **Fetch:** Reads a **32-bit instruction** from memory.
- **Decode:** Extracts the **opcode, registers, and immediates**.
- **Execute:** Performs the operation (arithmetic, memory access, branch, etc.).
- **Handles I/O and memory-mapped operations.**

### **3️⃣ System Calls & Debugging**
- Supports **HALT operation** to stop execution.
- Dumps **registers & memory** for debugging.
- Implements **heap allocation & deallocation**.

---

## 📜 Project Structure
```
vm-riscv/
│── src/
│   ├── vm_riskxvii.c     # Core VM implementation
│── programs/
│   ├── example.bin       # Example binary program
│── README.md
```

---

## 📜 License
This project is licensed under the MIT License.

---

## 🔗 Related Links
- 🔗 [GitHub Repository](https://github.com/your-username/vm-riscv)

