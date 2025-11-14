<h1 align="center"> Grade Sorter | 8086 | Assembly Language</h1>

<p align="center">
  <img width="285" height="197" alt="image" src="https://github.com/user-attachments/assets/9c94c02d-fa8e-403d-95ac-d0300711b16a" />
</p>

This is a **console-based Grade Sorting Program** developed in **8086 Assembly Language** using **EMU8086**.

It was created as part of my **Computer Organization & Assembly Language** coursework.
The program allows users to enter student IDs and marks, validates the inputs, and then sorts the data using the Bubble Sort Algorithm, finally displaying a clean, formatted table of sorted results.

---

##  Program Summary

The user enters the number of students (1–1000). For each student, the program collects:
* **ID** (0–255)
* **Marks** (0–100)

All inputs are validated. The **Bubble Sort** algorithm is applied to arrange data **ascending by marks**.

The sorted output prints:
* ✅ **Student ID**
* ✅ **Corresponding Marks**

Errors trigger a message prompting for correct input.

## Features

| Feature | Description |
| :--- | :--- |
|  **User Input** | Handling for IDs, marks, and student count |
|  **Validation** | System for ensuring inputs are within correct ranges (0-255 for ID, 0-100 for Marks) |
|  **Sorting** | Bubble Sort Algorithm implemented in pure 8086 Assembly |
|  **Memory-Efficient** | Storage using byte (DB) and word (DW) arrays |
|  **Formatted Output** | Clean, structured Command Line Interface (CLI) display of sorted results |
|  **Error Handling** | Display of specific error messages for invalid entries |
|  **Scalability** | Supports datasets up to 1000 students |

##  Example Data

| Input | |
| :--- | :--- |
| **Number of students:** | 3 |
| **IDs:** | 12, 5, 8 |
| **Marks:** | 85, 90, 70 |

**After sorting (ascending by marks):**

---

## 📁 Project Structure

GradeSorter8086/ ├── code.asm └── README.md

## ⚙️ How to Run

1.  **Install EMU8086**
    Download and install EMU8086 from its official website.

2.  **Load the Program**
    Open the `code.asm` file inside EMU8086.

3.  **Compile & Run**
    Follow these steps in the EMU8086 IDE:
    > Compile → Emulate → Run
    
    The program will begin with input prompts and guide you through the process.

##  Skills Demonstrated

* **Low-level programming** (8086 Assembly Language)
* Effective use of registers: AX, CX, DX, SI
* Understanding of **Memory Segmentation** (DS, CS)
* Byte/array handling and indexing using offsets
* Implementation of **Conditional Jumps** and **Loop Control**
* **Bubble Sort implementation** at the machine level
* Direct I/O using EMU8086 library functions (`scan_num`, `print_num_uns`)
* Data validation and structured CLI output

---

##  How It Works

### Core Components

| Component | Description |
| :--- | :--- |
| `SCAN_NUM` | Reads integer input from the user |
| `PRINT_STRING` | Displays text messages on the console |
| `PRINT_NUM_UNS` | Prints unsigned decimal numbers |
| **Bubble Sort** | Sorts marks and swaps corresponding IDs to maintain data integrity |
| **Arrays** | `MARKS[1000]` and `ID[1000]` store student data in the Data Segment |

### 🔍 Program Logic

1.  Prompt for the number of students.
2.  Collect **IDs** and **marks** one by one.
3.  **Validate** all entries against their respective ranges.
4.  Use **Bubble Sort** to arrange marks in ascending order, swapping corresponding IDs along with the marks.
5.  Print the sorted list in a clean, structured format.
6.  Display detailed error messages for any invalid inputs.

##  Tools and Libraries Used

| Tool / Library | Purpose |
| :--- | :--- |
| **EMU8086** | Primary tool for writing, assembling, and testing 8086 assembly programs |
| `include 'emu8086.inc'` | Enables use of helpful input/output macros (scan_num, print_num_uns) |
| **8086 Registers** | Used for data manipulation, comparison, and address indexing during sorting |
| **Arrays in Data Segment** | Store collected IDs and marks |

---

## 🏁 Conclusion

The **Grade Sorter in Assembly Language** showcases precise control over CPU registers, memory, and algorithmic logic at a low level.

By manually implementing sorting, memory indexing, and input/output management, this project solidifies understanding of the **8086 microprocessor**, low-level computation, and fundamental data handling techniques. It stands as a foundational project representing both analytical thinking and technical depth in assembly programming.

---

## 👤 Author

* **Ahmed Hussain**
* **Instructor:** Miss Tahmina Khan
