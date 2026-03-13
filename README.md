# 🧮 Sum of Distinct Elements

## 📝 Description
This project solves a common array challenge: finding the **sum of all distinct elements** from two different sets. 

**The Goal:** If an element exists in one set but is missing from the other, we add it to our total sum. If an element appears in both sets, we ignore it.

### 💡 Example
* **Set 1:** `[3, 1, 7, 9]`
* **Set 2:** `[2, 4, 1, 9, 3]`
* **Distinct Elements:** `7, 2, 4`
* **Result:** `13` (7 + 2 + 4)

---

## 🛠️ Logic & Algorithm
The solution uses a **Nested Loop** approach (a loop inside a loop) to compare the arrays.

1.  **Phase 1:** Iterate through `Set 1`. For each element, search through all of `Set 2`. If it’s not found, add it to `sum`.
2.  **Phase 2:** Iterate through `Set 2`. For each element, search through all of `Set 1`. If it’s not found, add it to `sum`.

---

🚀 Key Features
Array Manipulation: Demonstrates how to traverse and compare arrays.

Nested Loops: Efficiently handles cross-referencing between data sets.

Flag Logic: Uses a Boolean found flag to track the existence of elements across searches.

---

📂 Project Structure

ds.algo: The main algorithm file.

README.md: Project documentation.


### 📊 Step-by-Step Execution Trace
Here is how the algorithm processes the sets: `Set 1: [3, 1, 7, 9]` and `Set 2: [2, 4, 1, 9, 3]`.

| Step | Number Checked | Found in other Set? | Action | Current Sum |
| :--- | :--- | :--- | :--- | :--- |
| **Check Set 1** | **3** | Yes (in Set 2) | Ignore | 0 |
| | **1** | Yes (in Set 2) | Ignore | 0 |
| | **7** | **No** | **Add to Sum** | **7** |
| | **9** | Yes (in Set 2) | Ignore | 7 |
| **Check Set 2** | **2** | **No** | **Add to Sum** | **9** |
| | **4** | **No** | **Add to Sum** | **13** |
| | **1** | Yes (in Set 1) | Ignore | 13 |
| | **9** | Yes (in Set 1) | Ignore | 13 |
| | **3** | Yes (in Set 1) | Ignore | 13 |

**Final Result:** The distinct elements are **7, 2, and 4**, giving a total sum of **13**.
