# UiPath Unit 2 Notes 
This document covers **Unit 2 topics** of UiPath: workflow automation, control flow, sequencing, loops, and data manipulation. Questions can be asked in any format, including mix and match.

---

## 1. Sequence, Flowchart, and Control Flow Activities in UiPath

### **1.1 Sequence**

* **Definition:** Linear execution of activities; executes one after the other.
* **Use Case:** Simple processes with minimal branching.
* **Example:** Read an Excel file → Process data → Write output to another file.

### **1.2 Flowchart**

* **Definition:** Graphical representation allowing branching, loops, and multiple decision points.
* **Use Case:** Complex processes with multiple conditions.
* **Example:** If invoice amount > 1000, send for approval; else, process automatically.

### **1.3 Control Flow Activities**

* **Definition:** Activities that control the execution path of workflows using decisions and loops.
* **Types:**

  1. **If Activity** – Decision making.
  2. **Switch Activity** – Multi-branch decision.
  3. **While Loop** – Repeats until a condition is false.
  4. **Do While Loop** – Repeats until a condition is false, executes at least once.
  5. **For Each Loop** – Iterates over collections.
  6. **Break & Continue** – Exit or skip iterations in loops.

### **Example of Control Flow**

```
For Each row in DataTable
    If row("Amount") > 1000
        SendApprovalEmail()
    Else
        ProcessInvoice()
Next
```

* Demonstrates decision-making with `If` and looping with `For Each`.

---

## 2. Sequencing in Workflow Automation

* **Definition:** Arranging activities in a logical order to achieve a task.
* **Sequence vs Flowchart:**

  * Sequence: Linear, simple tasks.
  * Flowchart: Complex, multiple branching.

**Example:**

1. Open Excel file.
2. Read data.
3. Loop through rows.
4. Perform calculations.
5. Save and close Excel file.

---

## 3. Loops and Decision-Making in Control Flow

### **Types of Loops**

1. **While Loop** – Repeats as long as the condition is true.
2. **Do While Loop** – Executes at least once and repeats while condition is true.
3. **For Each** – Iterates over arrays, collections, or DataTables.
4. **For Each Row** – Iterates specifically over DataTable rows.

### **Decision-Making Techniques**

* **If Activity:** Executes one path if condition is true, another if false.
* **Switch Activity:** Executes a branch based on multiple possible values.
* **Example:**

```
If Age > 18
    Print "Adult"
Else
    Print "Minor"
```

---

## 4. Data Manipulation in UiPath

### **4.1 Variables**

* Store data temporarily during workflow execution.
* Types: String, Int32, Boolean, Array, DataTable.
* **Scope:** Defines where the variable can be accessed (e.g., Sequence, Flowchart, Global).

### **4.2 Arguments**

* Used to **pass data between workflows**.
* Types:

  1. **In** – Input to the workflow.
  2. **Out** – Output from the workflow.
  3. **In/Out** – Both input and output.

### **4.3 Data Tables**

* Used to store structured data in rows and columns.
* Can be created manually or imported from CSV/Excel.
* Operations:

  * Add Data Row / Add Data Column.
  * Filter Data Table.
  * Sort Data Table.
  * Remove Duplicate Rows.

---

## 5. Data Table Operations with CSV/Excel

### **5.1 Import CSV/Excel to DataTable**

* **Steps:**

  1. Use `Read CSV` or `Read Range` activity.
  2. Output stored in a DataTable variable.

**Example:**

```
dtInvoices = ReadRange("InvoiceData.xlsx")
```

### **5.2 Manipulate DataTable**

* Loop through rows using `For Each Row`.
* Apply conditions using `If`.
* Modify cell values:

```
row("Status") = "Processed"
```

### **5.3 Export DataTable to CSV/Excel**

* **Steps:**

  1. Use `Write CSV` or `Write Range` activity.
  2. Specify DataTable and file path.

**Example:**

```
WriteRange("ProcessedInvoices.xlsx", dtInvoices)
```

### **5.4 Converting CSV/Excel to DataTable and Vice Versa**

* **CSV/Excel → DataTable:** Read data using `Read CSV` or `Read Range`. Store in DataTable variable.
* **DataTable → CSV/Excel:** Use `Write CSV` or `Write Range` to save the modified DataTable.
* **Step-by-Step Example:**

```
1. Read Excel: dt = ReadRange("Input.xlsx")
2. For Each Row in dt
       If row("Amount") > 1000
           row("Status") = "High"
       Else
           row("Status") = "Low"
3. WriteRange("Output.xlsx", dt)
```

---

**Tips for Exams:**

* Focus on **examples using For Each, If, Switch, While loops**.
* Remember **variable scope** for passing data between workflows.
* Know **how to import/export CSV/Excel** and manipulate DataTables.
* Mix and match **Sequences, Flowcharts, and Control Flow activities** based on question format.