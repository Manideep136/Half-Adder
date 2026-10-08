# Half-Adder


## 📌 Project Overview

A **Half Adder** is a basic digital logic circuit used to perform the addition of two single-bit binary numbers. It produces two outputs:

* **Sum (S)**
* **Carry (C)**

The Half Adder is one of the fundamental building blocks used in digital electronics and forms the basic concept behind more complex arithmetic circuits such as **Full Adders, Binary Adders, and Arithmetic Logic Units (ALUs)**.

This project demonstrates the design and implementation of a Half Adder circuit using logic gates and a PCB designed using **KiCad**.

---

## 🎯 Objectives

* To understand the basic operation of binary addition.
* To design a Half Adder using digital logic gates.
* To implement the Sum and Carry logic.
* To create the circuit schematic using KiCad.
* To design a PCB layout for the circuit.
* To understand the relationship between logic gates and binary arithmetic.

---

## ⚙️ Working Principle

A Half Adder accepts two binary inputs:

* **A** – First input bit
* **B** – Second input bit

It produces:

* **Sum (S)** – Result of binary addition
* **Carry (C)** – Carry generated when both inputs are `1`

The Sum output is generated using an **XOR gate**, while the Carry output is generated using an **AND gate**.

### Boolean Expressions

```text
Sum = A XOR B

Carry = A AND B
```

Therefore, the circuit requires:

* 1 × XOR gate
* 1 × AND gate

---

## 🔢 Truth Table

| A | B | Sum | Carry |
| - | - | --- | ----- |
| 0 | 0 | 0   | 0     |
| 0 | 1 | 1   | 0     |
| 1 | 0 | 1   | 0     |
| 1 | 1 | 0   | 1     |

### Explanation

* **0 + 0 = 00** → Sum = 0, Carry = 0
* **0 + 1 = 01** → Sum = 1, Carry = 0
* **1 + 0 = 01** → Sum = 1, Carry = 0
* **1 + 1 = 10** → Sum = 0, Carry = 1

---

## 🧩 Components Required

| Component             |    Quantity | Purpose                 |
| --------------------- | ----------: | ----------------------- |
| XOR Gate IC           |           1 | Generates Sum           |
| AND Gate IC           |           1 | Generates Carry         |
| LED                   |           2 | Indicates Sum and Carry |
| Resistors             |           2 | Limits LED current      |
| Push Buttons/Switches |           2 | Provides inputs A and B |
| Breadboard/PCB        |           1 | Circuit implementation  |
| Connecting Wires      | As required | Electrical connections  |
| Power Supply          |           1 | Provides circuit power  |

### Example ICs

For a 74-series implementation, commonly used ICs include:

* **74LS86** – Quad 2-Input XOR Gate
* **74LS08** – Quad 2-Input AND Gate

---

## 🔌 Circuit Operation

The two input switches provide binary values **A** and **B**.

The inputs are connected simultaneously to the XOR and AND gates.

```text
             ┌─────────────┐
      A ─────┤             │
             │   XOR Gate  ├──── Sum
      B ─────┤             │
             └─────────────┘

             ┌─────────────┐
      A ─────┤             │
             │   AND Gate  ├──── Carry
      B ─────┤             │
             └─────────────┘
```

When the inputs are different, the XOR gate produces a `1`, so the **Sum LED turns ON**.

When both inputs are `1`, the AND gate produces a `1`, so the **Carry LED turns ON**.

---

## 🖥️ KiCad Design

The project can be designed using **KiCad** through the following stages:

1. Create a new KiCad project.
2. Draw the Half Adder schematic.
3. Add XOR and AND gate ICs.
4. Add input switches.
5. Add LEDs for Sum and Carry.
6. Add current-limiting resistors.
7. Connect the power supply and ground.
8. Assign appropriate footprints.
9. Create the PCB layout.
10. Run Electrical Rules Check (ERC).
11. Run Design Rules Check (DRC).
12. Generate the final PCB.

---

## 📐 PCB Design

The PCB contains the components required to implement the Half Adder circuit.

The board can include:

* Input terminals for **A and B**
* XOR gate IC
* AND gate IC
* Sum LED
* Carry LED
* Resistors
* Power and Ground terminals

Proper component placement and routing should be used to keep the PCB compact and easy to understand.

---

## 🧪 Testing

After assembling the PCB, the circuit can be tested by applying all possible combinations of the two inputs.

| Input A | Input B | Expected Sum | Expected Carry |
| ------- | ------- | ------------ | -------------- |
| OFF     | OFF     | OFF          | OFF            |
| OFF     | ON      | ON           | OFF            |
| ON      | OFF     | ON           | OFF            |
| ON      | ON      | OFF          | ON             |

The observed outputs should match the truth table.

---

## 📊 Applications

Half Adders are used as basic building blocks in:

* Binary arithmetic circuits
* Full Adders
* Arithmetic Logic Units (ALUs)
* Digital calculators
* Microprocessors
* Digital computers
* Counters and arithmetic circuits
* Digital signal processing systems

---

## ⚠️ Limitations

A Half Adder can add only **two single-bit binary numbers**. It does not have a **Carry-In** input.

Therefore, it cannot directly add multiple-bit binary numbers where a carry from a previous bit needs to be considered. For this purpose, a **Full Adder** is used.

---

## 🚀 Future Improvements

The project can be extended by:

* Designing a **Full Adder**.
* Combining multiple Full Adders to create a multi-bit binary adder.
* Adding switches for easier input control.
* Adding a 7-segment display for output.
* Designing a compact PCB.
* Simulating the circuit before hardware implementation.

---

## 🛠️ Tools Used

* **KiCad** – Schematic and PCB Design
* **74LS86** – XOR Gate IC
* **74LS08** – AND Gate IC
* LEDs
* Resistors
* Push Buttons/Switches
* DC Power Supply

---


---

## 👨‍💻 Author

**Manideep**

Electronics and Communication Engineering (ECE)

---

## 📜 Conclusion

The Half Adder is a fundamental digital logic circuit that demonstrates how binary addition can be implemented using basic logic gates. In this project, an XOR gate is used to generate the **Sum**, while an AND gate generates the **Carry**. The circuit provides a simple and practical introduction to digital arithmetic and PCB design.
