# Interactive Quiz Loader (HTML/JS)

This is a single-file, client-side web application designed to help you study for exams by turning raw, structured question text files into an interactive, trackable quiz experience.

It features a permanent score tracker, answer reveal/hide functionality, and the ability to export a personalized study guide containing only the questions you marked as incorrect.

## 🖼️ Screenshots

### 1. The Interactive Quiz Interface

A view of the quiz page showing the fixed score tracker, a loaded question, the buttons, and a revealed correct answer (highlighted in green).

<img width="1919" height="906" alt="image" src="https://github.com/user-attachments/assets/bec50c42-bac9-4301-a509-f52727dc25aa" />


### 2. The Exported Study Guide

A screenshot of the generated `quiz_study_guide_YYYY-MM-DD.txt` file, showing the detailed summary and the content of an incorrectly answered question.

<img width="1919" height="824" alt="image" src="https://github.com/user-attachments/assets/83d7f2a4-d644-4a07-84c2-ad864f52f349" />


***

## ✨ Features

* **Single-File:** The entire application is contained within one self-sufficient HTML file (`index.html`). No server, dependencies, or external libraries are required.
* **Drag-and-Drop Loading:** Easily load one or more plain text files (`.txt`) containing your question bank.
* **Robust Parsing:** Uses a highly specific Regular Expression to correctly parse complex question structures, including:
    * Questions with 4 to 7 options (A through G).
    * Questions with single-letter answers (e.g., `Answer: C`).
    * **Multiple-Answer Questions** (e.g., `Answer: DE` or `Answer: ABF`).
* **Score Tracking:** A fixed header displays your progress, correct/wrong count, and a performance percentage that updates in real-time.
* **Study Guide Export:** Click "Export Results" to generate a `.txt` study guide containing only the questions you marked as **Wrong**, along with their correct answers and explanations.

## 🚀 How to Use

1.  **Save the File:** Save the provided HTML code (e.g., the last complete code block you received) as `index.html`.
2.  **Prepare Your Data:** Ensure your question bank is in the required text format (see below).
3.  **Open in Browser:** Double-click `index.html` to open it in any modern web browser (Chrome, Firefox, Edge, etc.).
4.  **Load Files:** Click the **"Select all question files"** button and select your prepared `.txt` files.
5.  **Start Quiz:** Click **"Load and Process Questions"**. The questions will appear below, ready for testing!

## 📝 Required Question Format

Your plain text files must strictly adhere to the following structure for the parser to work correctly.

**Key Requirements:**
* Start each question with `NEW QUESTION`
* Separate the question body, options, answer, and explanation with their respective labels, each on a new line or with minimal whitespace.

```text
NEW QUESTION 1
Which layer 3 device is used to connect two different subnetworks?

A. Layer 2 switch
B. Access point
C. Router
D. Media converter

Answer: C
Explanation: Routers operate at Layer 3 (Network Layer) and are required to forward traffic between different IP networks (subnets).

NEW QUESTION 2
Which of the following are characteristics of a firewall? (Select TWO)

A. Blocks unauthorized access
B. Filters network traffic based on rules
C. Operates only at Layer 2
D. Does not use access control lists (ACLs)
E. Cannot handle multiple interfaces

Answer: AB
Explanation: Firewalls are designed to block unauthorized access and filter network traffic based on predefined rules, often using ACLs.
