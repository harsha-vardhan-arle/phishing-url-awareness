# EWB Phishing URL Awareness Checker

## 1. Project Overview

The **Phishing URL Awareness Checker** is a beginner-friendly cybersecurity mini-project developed using Python. It examines the text of a URL for selected warning signs that may be associated with phishing links.

The main objective is to improve phishing awareness and help users recognize potentially suspicious URL patterns.

The program performs text-based checks only. It does not visit websites or send network requests.

## 2. Project Objectives

- Understand common warning signs found in suspicious URLs.
- Implement basic URL inspection using Python.
- Practice conditional statements, functions, loops, and exception handling.
- Test the program using sample URLs.
- Promote safe and responsible cybersecurity awareness.

## 3. Technologies Used

- **Programming language:** Python 3.10 or newer
- **Code editor:** Visual Studio Code
- **Python modules:** `re` and `urllib.parse`
- **Operating system:** Windows

No additional third-party Python packages are required.

## 4. Features

The program checks for six warning signs:

1. **`@` symbol:** Flags URLs containing an at sign.
2. **Unusually long URL:** Flags URLs longer than 100 characters.
3. **IP address hostname:** Identifies an IPv4-style address used as the hostname.
4. **Many hostname segments:** Flags hostnames containing five or more dot-separated segments.
5. **Punycode marker:** Detects `xn--` in the hostname.
6. **HTTP scheme:** Warns when the URL uses HTTP.

The program displays the detected warning signs and reminds users to be careful when following unexpected links.

## 5. Project Folder Structure

```text
phishing-url-awareness/
├── phishing_checker.py
├── README.md
├── requirements.txt
├── tests/
│   └── test_samples.md
└── screenshots/
    ├── sample_run.png
    └── test_results.png
```

## 6. Installation and Execution

### Prerequisites

- Python 3.10 or newer
- Visual Studio Code or another Python editor

### Steps to Run

1. Download or clone the project repository.
2. Open the project folder in Visual Studio Code.
3. Open the integrated terminal.
4. Run the following command:

```bash
py phishing_checker.py
```

5. Enter a sample URL when prompted.
6. Read the warning signs displayed by the program.
7. Type `quit` to exit the checker.

## 7. Sample Output

Example input:

```text
http://192.0.2.10/account
```

Expected warning messages include:

```text
- Uses an IP address instead of a familiar domain.
- Uses HTTP. HTTPS alone does not prove trust.
```

The program may also display a reminder to review the URL carefully.

## 8. Testing and Results

The following five sample URLs are used to test the program.

| Test | Sample URL | Expected result |
|---|---|---|
| 1 | `https://www.example.com/login` | No listed warning signs; this does not prove safety |
| 2 | `http://192.0.2.10/account` | IP-style hostname and HTTP warnings |
| 3 | `http://example.com@sample.invalid/login` | `@` symbol and HTTP warnings |
| 4 | `https://a.b.c.d.e.example.invalid/path` | Many hostname segments warning |
| 5 | `https://xn--example.invalid/` | Punycode warning |

The actual output and pass/fail status for each test are documented in `tests/test_samples.md`.

## 9. Improvements Implemented

The following improvements make the program easier to use and understand:

### Improvement 1: Repeat Checking Loop

The program allows users to inspect multiple URLs in one session without restarting it. Users can type `quit` to exit.

### Improvement 2: Review Reminder

When warning signs are detected, the program displays a reminder to review the URL carefully.

### Improvement 3: Error Handling

The program uses `try/except` to handle URL parsing errors and display a helpful message rather than terminating unexpectedly.

### Improvement 4: Clear Warning Messages

Each check produces an understandable message explaining the detected URL pattern.

### Improvement 5: Improved Output Formatting

The program separates the results from the input prompt and displays each warning on a separate line.

## 10. Limitations

- The checker examines only the warning signs implemented in the program.
- It does not determine whether a website is malicious or legitimate.
- It does not visit URLs or verify website content.
- Some phishing URLs may not trigger any of the implemented checks.
- HTTPS does not guarantee that a website is trustworthy.
- The hostname and IP-address checks are basic pattern checks, not complete URL validation.
- A result with no listed warning signs must not be treated as proof of safety.

## 11. Ethical Use and Safety

This project is intended for educational purposes and cybersecurity awareness.

- Use the workbook's sample URLs for testing.
- Do not enter passwords, banking information, or other sensitive data into websites reached through unexpected links.
- Verify a website independently before trusting it.
- Do not use this educational tool as a replacement for professional security software or security analysis.

## 12. Screenshots

The project includes screenshots demonstrating execution and testing.

- `screenshots/sample_run.png` — example program execution.
- `screenshots/test_results.png` — test cases and results.

These screenshots provide visual evidence of the project and its functionality.

## 13. Conclusion

The EWB Phishing URL Awareness Checker demonstrates how Python can be used to inspect URL text for selected phishing warning signs.

The project provides practical experience with string handling, regular expressions, URL parsing, functions, loops, and exception handling. It also reinforces an important cybersecurity lesson: suspicious patterns deserve attention, but the absence of warning signs does not establish that a URL is safe.

## 14. Author Information

**Author:** HARSHA VARDHAN ARLE

**Batch/Course:** Ewb AI POWERED CYBERSECURITY INTERNSHIP

**Project:** EWB Phishing URL Awareness Checker  
**Programming Language:** Python  
**Project Type:** Cybersecurity Awareness Mini-Project
