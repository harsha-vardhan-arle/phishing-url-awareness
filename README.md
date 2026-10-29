# EWB Phishing URL Awareness Checker

## 1. Project Overview

The **Phishing URL Awareness Checker** is a beginner-friendly Python project that checks URL text for selected warning signs commonly associated with suspicious links.

The purpose of this project is to improve awareness of phishing risks and help users examine URLs more carefully before trusting them.

**Important:** This program only inspects the text of a URL. It does not open websites or send network requests.

## 2. Features

The program checks for six warning signs:

1. **`@` symbol:** Identifies URLs containing an at sign.
2. **Long URL:** Flags URLs longer than 100 characters.
3. **IP address:** Identifies an IPv4-style address used as the hostname.
4. **Many hostname segments:** Flags hostnames containing five or more dot-separated segments.
5. **Punycode marker:** Detects the `xn--` marker in a hostname.
6. **HTTP scheme:** Warns when a URL uses HTTP instead of HTTPS.

The program displays the detected warning signs and reminds users to be cautious.

## 3. Technologies Used

- Python 3.10 or newer
- Visual Studio Code
- Python standard-library modules:
  - `re`
  - `urllib.parse`

No additional Python packages are required.

## 4. Project Structure

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

## 5. How to Run the Program

### Requirements

- Python 3.10 or newer
- A Windows computer or another system with Python installed

### Instructions

1. Download or clone this repository.
2. Open the project folder in Visual Studio Code.
3. Open the integrated terminal.
4. Run the following command:

```bash
py phishing_checker.py
```

5. Enter a sample URL when prompted.
6. Review the warning signs displayed.
7. Type `quit` to exit the program.

## 6. Example Usage

Sample input:

```text
http://192.0.2.10/account
```

Expected warning signs include:

```text
- Uses an IP address instead of a familiar domain.
- Uses HTTP. HTTPS alone does not prove trust.
```

The exact output may also include the program's review reminder.

## 7. Testing

The program is tested using the five sample URLs provided in the EWB project workbook.

| Test case | Expected result |
|---|---|
| `https://www.example.com/login` | No listed warning signs; safety is not guaranteed |
| `http://192.0.2.10/account` | IP-style hostname and HTTP warnings |
| `http://example.com@sample.invalid/login` | `@` symbol and HTTP warnings |
| `https://a.b.c.d.e.example.invalid/path` | Many hostname segments warning |
| `https://xn--example.invalid/` | Punycode warning |

Actual results and pass/fail status are recorded in `tests/test_samples.md`.

## 8. Improvements

The project includes the following improvements:

- Allows users to inspect multiple URLs in one session.
- Provides a review reminder when warning signs are detected.
- Handles URL parsing errors with a `try/except` block.
- Displays individual warning messages for easier understanding.

## 9. Limitations

- The program checks only selected warning signs.
- It does not verify a website's reputation or ownership.
- It does not visit websites or perform network requests.
- Some phishing URLs may not trigger any of the implemented checks.
- A URL using HTTPS is not necessarily trustworthy.
- A result with no listed warning signs does not prove that a URL is safe.

## 10. Ethical Use and Safety

This project is intended for educational purposes and cybersecurity awareness.

Use the provided sample URLs for testing. Do not enter passwords or other sensitive information into websites reached through unexpected links. Always verify a website independently before trusting it.

## 11. Author

**Name:** Harsha Vardhan Arle  
**Project:** EWB Phishing URL Awareness Checker  
**Language:** Python
