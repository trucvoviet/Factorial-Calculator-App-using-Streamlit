# Factorial Calculator App using Streamlit

This project is a simple **Streamlit web application** that calculates the **factorial of a number** entered by the user.

The application demonstrates:

* Basic **Python function implementation**
* **Recursive mathematical logic**
* Building an interactive **Streamlit UI**
* Deploying a Python app to the web using **Streamlit Cloud**

The deployed application is available here:

**Live App:**
[https://factorialcalculator-vtruc.streamlit.app/](https://factorialcalculator-vtruc.streamlit.app/)

**GitHub Repository:**
[https://github.com/trucvoviet/Factorial-Calculator-App-using-Streamlit](https://github.com/trucvoviet/Factorial-Calculator-App-using-Streamlit)

---

# What is Factorial?

The **factorial** of a number ( n ) is the product of all positive integers from **1 to n**.

[
n! = 1 \times 2 \times 3 \times ... \times n
]

A factorial can also be defined using **recursion**:

[
n! = n \times (n-1)!
]

with the base case:

[
0! = 1
]

---

# Examples

### Example 1: 3!

```
3! = 3 × 2 × 1
   = 6
```

### Example 2: 5!

```
5! = 5 × 4 × 3 × 2 × 1
   = 120
```

---

# Project Structure

```
Factorial-Calculator-App-using-Streamlit
│
├── app.py
├── factorial.py
├── requirements.txt
├── README.md
│
└── imgs
    └── factapp.png
```

* **app.py** → Streamlit user interface
* **factorial.py** → factorial calculation logic
* **requirements.txt** → project dependencies
* **imgs/** → application screenshot

---

# Step 1 — Create Project Folder

Create a folder for the project.

```
Factorial Calculation App
```

Open the folder in **VSCode** using Git Bash:

```bash
code .
```

---

# Step 2 — Open Terminal

In VSCode:

```
Ctrl + ~
```

Then open **Command Prompt (cmd)** inside the terminal.

---

# Step 3 — Check Python Version

Verify that Python is installed.

```bash
python --version
```

or

```bash
python -V
```

---

# Step 4 — Create a Virtual Environment

Create a new **conda environment** for the project.

```bash
conda create --name fact_env python=3.11.7
```

Activate the environment:

```bash
conda activate fact_env
```

---

# Step 5 — Install Required Libraries

Install the required dependencies from `requirements.txt`.

```bash
pip install -r requirements.txt
```

The most important dependency is:

```
streamlit
```

---

# Step 6 — Create the Factorial Function

Create a file named:

```
factorial.py
```

Add the factorial function inside it.

```python
# factorial.py

# Function to calculate factorial
def fact(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * fact(n - 1)
```

This function uses **recursion** to compute the factorial.

---

# Step 7 — Build the Streamlit Interface

Create a file named:

```
app.py
```

Add the following code to build the Streamlit interface.

```python
# app.py

# Import Streamlit library
import streamlit as st

# Import factorial function from factorial.py
from factorial import fact


def main():

    # Application title
    st.title("Factorial Calculator")

    # User input
    number = st.number_input(
        "Enter a number:",
        min_value=0,
        max_value=999
    )

    # Button to trigger calculation
    if st.button("Calculate"):

        # Calculate factorial
        result = fact(number)

        # Display result
        st.write(f"The factorial of {number} is {result}.")

        # Streamlit animation
        st.balloons()


if __name__ == "__main__":
    main()
```

---

# Note: Fix Streamlit Import Error in VSCode

If you see a red underline under `streamlit`, it means VSCode is not using the correct environment.

Fix it by:

```
Ctrl + Shift + P
```

Then choose:

```
Python: Select Interpreter
```

Select the environment:

```
fact_env
```

---

# Step 8 — Run the Application Locally

Run the Streamlit app:

```bash
streamlit run app.py
```

The application will open automatically in your browser.

---

# Step 9 — Deploy the App to Streamlit Cloud

To share the app publicly, deploy it using **Streamlit Cloud**.

Go to:

[https://streamlit.io](https://streamlit.io)

Click:

```
New App
```

Fill in the deployment information:

```
Repository:
trucvoviet/Factorial-Calculator-App-using-Streamlit

Branch:
main

Main file path:
app.py

App URL (optional):
factorialcalculator-vtruc.streamlit.app
```

Then click:

```
Deploy
```

---

# Web App Result

Below is the deployed application interface.

![factorial calculator app](imgs/factapp.png)


---

# Technologies Used

* Python
* Streamlit
* Conda Environment
* GitHub
* Streamlit Cloud

---
