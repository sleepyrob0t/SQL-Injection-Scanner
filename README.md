# SQL-Injection-Scanner

This script scans web applications for SQL injection vulnerabilities by testing input fields and URLs for common SQL errors.

What is SQL Injection?

SQL injection is a web security vulnerability that allows attackers to interfere with the queries an application makes to its database. It can enable an attacker to:

View sensitive data they shouldn't have access to

Modify or delete database records

Perform administrative operations on the database

Bypass authentication and gain unauthorized access

SQL injection occurs when user inputs are improperly handled, allowing malicious SQL queries to be executed by the database.

Requirements

Python 3

Requests library

BeautifulSoup4

Install Dependencies

pip install requests beautifulsoup4

Usage

Run the script with the target URL:

python sql_injection_scanner.py http://example.com

How It Works

It scans the target URL for input forms.

It injects common SQL payloads to test for vulnerabilities.

It checks the server's response for SQL error messages.

If an error message is detected, it flags the vulnerability.

Example Output

[!] Trying http://example.com'
[+] SQL Injection vulnerability detected, link: http://example.com'
[+] Form:
{'action': '/login', 'method': 'post', 'inputs': [{'type': 'text', 'name': 'username'}, {'type': 'password', 'name': 'password'}, {'type': 'submit', 'name': 'submit'}]}

Notes

Run this script responsibly and only on websites you have permission to test.

The scanner looks for error-based SQL injection but may not detect more sophisticated attacks.

Disclaimer

This script is for educational purposes only. Unauthorized testing of websites is illegal and unethical.
