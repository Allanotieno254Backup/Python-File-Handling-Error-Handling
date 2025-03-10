# Python File Handling & Error Handling Project

## 📌 Overview
This project focuses on **reading and modifying files in Python** while incorporating **error handling** for robustness. It allows users to:

- Read a file's contents.
- Modify the content (convert text to uppercase in this example).
- Save the modified content to a new file.
- Handle errors such as file not found or permission issues.

---

## 📂 Project Structure
```
📦 Python-File-Handling-Error-Handling
├── 📄 main.py  # Contains the Python code for reading, modifying, and handling errors
├── 📄 sample.txt  # Sample file for testing
├── 📄 modified_sample.txt  # File created after modification
└── 📄 README.md  # Project documentation
```

---

## 📝 Code Implementation

```python
# Python program for File Read, Write & Error Handling

def modify_file(input_filename, output_filename):
    try:
        with open(input_filename, "r") as infile:
            content = infile.read()  # Read original content

        # Modify content (convert to uppercase)
        modified_content = content.upper()

        with open(output_filename, "w") as outfile:
            outfile.write(modified_content)  # Write modified content

        print(f"✅ Successfully modified and saved to {output_filename}")

    except FileNotFoundError:
        print("❌ Error: The file does not exist. Please check the filename.")
    except IOError:
        print("❌ Error: Unable to read/write the file.")

# Ask user for input and output filenames
input_file = input("Enter the name of the file to read: ")
output_file = "modified_" + input_file  # Create new modified file

modify_file(input_file, output_file)
```

---

## 🏆 Expected Outputs

### **✅ Case 1: File Exists & Successfully Modified**
**Input:**
```
Enter the name of the file to read: sample.txt
```

**Original `sample.txt` content:**
```
Hello, this is a sample file.
File handling in Python is powerful!
```

**Output in `modified_sample.txt`**
```
HELLO, THIS IS A SAMPLE FILE.
FILE HANDLING IN PYTHON IS POWERFUL!
```

**Terminal Output:**
```
✅ Successfully modified and saved to modified_sample.txt
```

---

### **❌ Case 2: File Not Found**
**Input:**
```
Enter the name of the file to read: non_existent.txt
```
**Terminal Output:**
```
❌ Error: The file does not exist. Please check the filename.
```

---

### **❌ Case 3: Permission Error (Read-Only File System)**
**Input:**
```
Enter the name of the file to read: protected_file.txt
```
**Terminal Output:**
```
❌ Error: Unable to read/write the file.
```

---

## 🚀 Features & Learnings
- ✅ **File Handling** (`open()`, `read()`, `write()`, `close()`)
- ✅ **Error Handling** (`try-except` blocks for `FileNotFoundError` & `IOError`)
- ✅ **User Input Handling** (Reading filenames dynamically)
- ✅ **Content Modification** (Processing text in files)

---

## 🔧 How to Run the Program
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/Python-File-Handling-Error-Handling.git
   ```
2. Navigate into the project folder:
   ```bash
   cd Python-File-Handling-Error-Handling
   ```
3. Run the script:
   ```bash
   python main.py
   ```
4. Follow the prompts and enter the filename.

---

## 📌 Additional Notes
- Ensure the input file **exists** in the same directory as the script.
- Modify the `modify_file()` function to apply different transformations.
- Extend the script to handle different file formats (`.csv`, `.json`, etc.).

---

## 📜 License
This project is licensed under the MIT License.

---

## 🤝 Contributing
If you'd like to contribute, feel free to fork the repository and submit a pull request! 😊

---

## 📧 Contact
For any questions, reach out via:
- **GitHub**: [yourusername](https://github.com/yourusername)
- **Email**: your.email@example.com

Happy coding! 🚀


