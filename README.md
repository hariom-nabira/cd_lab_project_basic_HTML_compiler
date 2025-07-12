# HTML Compiler Project

A Python-based HTML compiler that can parse, validate, and correct HTML code with error detection and automatic correction capabilities.

## 📋 Project Information

- **Batch**: B2
- **Semester**: 6th
- **Branch**: CSE (Computer Science Engineering)
- **Course**: Compiler Design Lab

### Team Members
- **Member 1**: Hariom Nabira (Roll No: 34)
- **Member 2**: Harsh Tiwari (Roll No: 37)

## 🎯 Problem Statement

Create an HTML compiler in Python or Java to convert HTML code and generate appropriate output based on the tags. Also perform error correction.

## ✨ Features

### Core Functionality
- **HTML Tokenization**: Breaks down HTML code into individual tokens (tags and text content)
- **Syntax Validation**: Detects various types of HTML syntax errors
- **Error Correction**: Automatically fixes common HTML structure issues
- **Tag Nesting Validation**: Ensures proper parent-child tag relationships
- **Self-closing Tag Support**: Handles tags like `<br>`, `<img>`, `<input>`, etc.

### Error Detection
- Unmatched closing tags
- Mismatched tag pairs
- Unclosed tags
- Invalid tag nesting
- Missing closing tags

### Error Correction
- Automatically adds missing closing tags
- Corrects tag order and nesting
- Generates valid HTML structure
- Adds proper DOCTYPE declaration

## 🛠️ Technical Implementation

### Key Components

1. **`read_file(file_path)`**: Reads HTML content from a text file
2. **`tokenize_html(html)`**: Converts HTML string into tokens
3. **`parse_html(tokens)`**: Validates HTML structure and detects errors
4. **`correct_html(tokens)`**: Automatically corrects HTML errors
5. **`save_and_open_html(corrected_tokens)`**: Saves corrected HTML and opens in browser

### Supported HTML Tags

The compiler supports a comprehensive set of HTML tags with proper nesting rules:

- **Document Structure**: `html`, `head`, `body`
- **Text Elements**: `h1`, `h2`, `h3`, `h4`, `h5`, `h6`, `p`, `span`, `div`
- **Lists**: `ul`, `ol`, `li`
- **Tables**: `table`, `tr`, `td`, `th`
- **Links and Media**: `a`, `img`, `br`
- **Forms**: `form`, `input`, `select`, `textarea`, `button`, `label`
- **Semantic Elements**: `header`, `footer`, `nav`, `section`, `article`, `aside`, `main`

### Self-closing Tags
- `br`, `img`, `meta`, `link`, `input`, `hr`, `base`, `area`, `col`, `source`, `track`, `wbr`

## 🚀 Installation and Usage

### Prerequisites
- Python 3.x
- No additional dependencies required (uses only built-in Python libraries)

### Running the Project

1. **Clone or download the project**
2. **Open the Jupyter notebook**:
   ```bash
   jupyter notebook B2_34&37_CD_Project.ipynb
   ```

3. **Run the main function**:
   ```python
   main()
   ```

4. **Enter the path to your HTML text file** when prompted
   - Example: `C:\Users\username\testHtml.txt`

### Input Format
Create a text file (`.txt`) containing your HTML code:
```html
<html>
<head>
<title>My Page</title>
</head>
<body>
<h1>Welcome</h1>
<p>This is a test</p>
</body>
</html>
```

### Output
- **Console Output**: Displays detected errors and corrected HTML
- **File Output**: Saves corrected HTML as `corrected_output.html`
- **Browser**: Automatically opens the corrected HTML file in your default browser

## 📁 Project Structure

```
cd_lab_project_basic_HTML_compiler/
├── B2_34&37_CD_Project.ipynb    # Main Jupyter notebook with implementation
├── .git/                         # Git repository
└── README.md                     # This file
```

## 🔍 Example Usage

### Input HTML (with errors):
```html
<html>
<head>
<title>Test Page
<body>
<h1>Hello World
<p>This is a paragraph
</html>
```

### Detected Errors:
- Unclosed `<title>` tag
- Unclosed `<h1>` tag  
- Unclosed `<p>` tag
- Missing `</head>` tag

### Corrected Output:
```html
<!DOCTYPE html>
<html>
<head>
<title>Test Page</title>
</head>
<body>
<h1>Hello World</h1>
<p>This is a paragraph</p>
</body>
</html>
```

## 🧪 Testing

The compiler can handle various HTML scenarios:
- ✅ Valid HTML (no errors)
- ✅ Missing closing tags
- ✅ Mismatched tag pairs
- ✅ Invalid nesting
- ✅ Self-closing tags
- ✅ Complex nested structures

## 🔧 Technical Details

### Algorithm Overview
1. **Tokenization**: Parse HTML into individual tokens
2. **Validation**: Check syntax and structure using stack-based parsing
3. **Error Detection**: Identify syntax errors and structural issues
4. **Correction**: Apply fixes to generate valid HTML
5. **Output**: Save and display corrected HTML

### Error Handling
- File not found errors
- Invalid HTML syntax
- Malformed tag structures
- Graceful error reporting
