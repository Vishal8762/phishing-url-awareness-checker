EWB Phishing URL Awareness Checker

1. Project Overview

Phishing is a type of cyber attack in which attackers use fake links to steal personal information, passwords, or banking details.

The Phishing URL Awareness Checker is a Python-based command-line project that checks URL text for common phishing warning signs. It does not open or visit any website.

2. Features

This project checks for six common URL warning signs:

1. Presence of the "@" symbol.
2. URL length greater than 100 characters.
3. IP address used as the hostname.
4. Five or more hostname segments.
5. Punycode marker ("xn--") in the hostname.
6. Use of HTTP instead of HTTPS.

3. Requirements

- Python 3.10 or later.
- No external Python packages required.
- Uses built-in Python libraries.

4. How to Run

1. Open the project folder in VS Code.
2. Open the terminal.
3. Run the following command:

python phishing_checker.py

For Mac/Linux:

python3 phishing_checker.py

5. Example Output

Example input:

http://192.0.2.10/account

Expected warnings:

- Uses an IP address instead of a familiar domain.
- Uses HTTP. HTTPS alone does not prove trust.

6. Testing

Five sample URLs are tested. Their results are documented in "tests/test_samples.md".

No.| Test case| Expected result
1| Normal example URL| No listed warning signs
2| IP address URL| IP address and HTTP warnings
3| URL containing @| @ symbol and HTTP warnings
4| Multiple hostname segments| Many hostname segments warning
5| Punycode URL| Punycode warning

7. Screenshots

Sample Program Run

"Sample Run" (screenshots/sample_run.png)

Test Results

"Test Results" (screenshots/test_results.png)

8. Improvements

Two improvements have been added:

1. Repeated URL Checking: A loop allows users to check multiple URLs without restarting the program. Users can type "quit" to exit.
2. Invalid URL Handling: A try-except block handles malformed URL input without crashing the program.

9. Limitations

- This is an educational project.
- It checks only the visible URL text.
- It does not open or visit URLs.
- It does not scan websites for malware.
- It cannot guarantee that a URL is safe.
- No warning signs found does not mean that a URL is safe.

10. Ethical Use

- Use sample URLs for educational testing.
- Never enter passwords or personal information on suspicious websites.
- Do not use this tool to deceive others.
- Respect website owners and their permissions.

11. Author

Vishal Yadav
EWB Courses
