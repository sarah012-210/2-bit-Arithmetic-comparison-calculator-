
# 2-Bit Arithmetic Comparison Calculator

## 📌 Objective

The aim of this project is to design and simulate a digital circuit capable of performing:

- **Addition** with overflow detection  
- **Subtraction** with overflow detection  
- **Absolute Value Comparison**  

This circuit is designed using basic logic gates and digital ICs and implemented on both simulation software (e.g., Logisim) and physical hardware.

---

## 🧩 Project Components

- Breadboard  
- 9V Battery with Regulator  
- Jumper Wires  
- Switches  
- LEDs  
- Resistors  
- IC 7430 – 8-input NAND  
- IC 7411 – 3-input AND  
- IC 7432 – 2-input OR  
- IC 7486 – 2-input XOR  
- IC 74154 – 4×16 Decoder  
- IC 7408 – 2-input AND  

---

## ⚙️ Design Explanation

### 🔘 Operation Selection
The circuit uses two selectors `s0` and `s1` to choose between different operations:

| s1 | s0 | Operation    |
|----|----|--------------|
| 0  | 0  | No Output    |
| 0  | 1  | Addition     |
| 1  | 0  | Subtraction  |
| 1  | 1  | Comparison   |

### ➕ 2-Bit Adder/Subtractor
- The selectors (`s0`, `s1`) are connected to XOR and AND gates to control when the adder/subtractor logic is enabled.
- `s1` is also connected to the carry-in (Cin) to toggle between addition and subtraction.
- The output is shown via LEDs.

### ⚠️ Overflow Detection
Overflow is detected by comparing the last two carry outputs (`c1`, `c0`):
- If `c1 ≠ c0`, overflow has occurred.
- Overflow output is sent through an XOR gate to an LED, which lights up if overflow happens.

### 🔍 Comparator
- Uses a 4x16 decoder.
- Enabled only when `s0 = 1` and `s1 = 1`.
- Decoder enable pin is connected to a NAND gate output of `s0` and `s1`.

---

## 🧪 Simulation

- The complete circuit is built in **Logisim** (or another simulation software).
- Different test cases were used to verify correctness:
  - Addition and subtraction with/without overflow.
  - Comparator function for absolute values.

---

## 🛠️ Hardware Implementation & Testing

- Implemented on a physical breadboard with the listed ICs.
- Verified outputs for each operation mode (addition, subtraction, comparator, and idle/off).

---

## 👤 Team Members

- Sarah Sameh Mohamed  
- Lyan Ahmed Mohsen  
- Mariam Sherif Mohamed  
- Ahmed Wael Ahmed Naem  
- Ahmed Wael Shenif  

---

## 👨‍🏫 Supervisor

- Eng. Muhammed Mostafa

---

## 📂 Project Files

- `2bit_comparator.circ` – Logisim circuit file  
- `README.md` – This documentation

> 💡 If you'd like to share the `.circ` file publicly, consider uploading it to a platform (e.g., GitHub, Google Drive) and update this README with the link.
