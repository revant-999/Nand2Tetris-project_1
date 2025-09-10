# Nand2Tetris Project 1: Boolean Logic

This project implements a complete set of elementary logic gates, 16-bit variants, and multi-way variants using only **NAND gates** as the primitive.  
It is the foundation for building a full computer from first principles (Nand2Tetris course).  

---

## 🔧 Implemented Components
### Elementary Gates
- Not, And, Or, Xor  
- Mux, DMux  

### 16-bit Variants
- Not16, And16, Or16  
- Mux16  

### Multi-way Variants
- Or8Way  
- Mux4Way16, Mux8Way16  
- DMux4Way, DMux8Way  

---

## 🧠 Key Idea
All gates are derived from the **NAND gate**:
- `NOT(A) = NAND(A, A)`  
- `AND(A, B) = NOT(NAND(A, B))`  
- `OR(A, B) = NAND(NOT(A), NOT(B))`  
- `XOR(A, B) = OR(AND(A, NOT(B)), AND(NOT(A), B))`  

Higher-level gates (Mux, DMux, Multiway) are built using combinations of these.  

---

## 📂 File Organization
- `ElementaryGates/` → Basic gates  
- `Variants16/` → 16-bit wide gates  
- `MultiwayVariants/` → Multi-input/output gates  
- `tests/` → Pre-written test scripts to validate correctness  

---

## ✅ Testing
All gates were tested using the **Hardware Simulator** provided in Nand2Tetris.  
Example:  
```bash
HardwareSimulator.sh tests/And.tst
