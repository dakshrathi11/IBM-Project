# IBM-Project
🛡️ ThreatLens AI

AI-Assisted Website Intelligence & Malware Threat Classification

ThreatLens AI is an educational cybersecurity project designed to help users understand website content and investigate potential security threats using external threat-intelligence data.

Key Features

- 🌐 Website Intelligence: Extracts website titles, descriptions, headings, and visible text from accessible web pages.
- 🔍 Threat Intelligence: Retrieves existing reports from the VirusTotal API for URLs, domains, IPv4 addresses, and supported file hashes.
- 🦠 Malware Classification: Displays provider-reported threat labels, malware-family names, threat categories, and security-engine detections when available.
- 📊 Detection Statistics: Presents malicious, suspicious, harmless, and undetected counts.
- 📝 Investigation Reports: Supports saving investigation results as JSON files.

Technologies Used

- Python
- Jupyter Notebook
- Requests
- Beautiful Soup
- VirusTotal API v3

Project Purpose

The goal of ThreatLens AI is to make cybersecurity investigation more understandable by separating website-content analysis from threat-intelligence results.

Disclaimer: This is an educational prototype, not a replacement for professional malware analysis. Threat classifications depend on third-party reports and may contain false positives. An absence of detections does not guarantee that a website or file is safe.
