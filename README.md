# ancient-message-validator

# Ancient Message Validator 📜

A Python and Jupyter Notebook implementation using the **Stack (LIFO)** data structure to parse and validate nested bracket sequences from an ancient text messaging system.

---

## 📌 Project Overview
An ancient civilization stored their historical data using highly nested structures. Before decoding these files, we must verify if the messages are corrupted. 

This project implements a linear-time (`O(n)`) validation engine that ensures every opening bracket has a corresponding, properly nested closing bracket using an in-memory stack.

### 💼 Real-World Impact
The underlying mechanics of this project reflect the core parsing engines used in:
* **Compilers & Interpreters:** Matching syntax brackets, parentheses, and braces.
* **HTML/XML Validators:** Ensuring tags close in the exact reverse order they opened.
* **IDEs:** Providing real-time syntax highlighting and red-underline errors for unbalanced code blocks.

---

## ⚙️ Stack Behavior & Logic
The algorithm relies on the **Last-In, First-Out (LIFO)** structural design:

1. **Push (`O(1)`):** When an opening bracket (`(`, `{`, `[`) is encountered, it is pushed onto the top of the stack.
2. **Peek & Pop (`O(1)`):** When a closing bracket (`)`, `}`, `]`) is encountered, the algorithm checks the top element of the stack. If it matches the closing pair, the opening bracket is popped off.
3. **Early Failure Conditions:**
   * A closing bracket appears but the stack is empty (e.g., `())`).
   * A closing bracket does not match the type of the bracket on top of the stack (e.g., `[(])`).
4. **Final Integrity Check:** Once the entire string is read, the stack must be completely **empty**. If any elements remain, the string contains orphaned opening brackets (e.g., `{[(`) and is flagged as invalid.

---

## 📁 Repository Structure
```text
ancient-message-validator/
├── README.md                          # Project documentation
└── ancient_message_validator.ipynb    # Main interactive Jupyter Notebook
```

---

## 🚀 How to Run the Notebook

### Prerequisites
Ensure you have Python 3 and Jupyter installed:
```bash
pip install jupyter
```

### Execution Steps
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com
   ```
2. Navigate into the project directory:
   ```bash
   cd ancient-message-validator
   ```
3. Launch the Jupyter environment:
   ```bash
   jupyter notebook
   ```
4. Open `ancient_message_validator.ipynb` and run the cells sequentially using **Shift + Enter**.
