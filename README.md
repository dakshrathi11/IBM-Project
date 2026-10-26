# ThreatLens AI --- Website Intelligence & Threat Classification

**Project:** IBM SkillsBuild Cyber Security BootCamp 2026\
**Author:** Daksh Rathi\
**Project type:** Educational Python/Jupyter Notebook prototype

## Overview

ThreatLens AI combines two separate workflows: 1. **Website
intelligence:** retrieves accessible HTML metadata, headings, and a
short visible-text excerpt to help users understand what a page
presents. 2. **Threat classification:** queries an existing VirusTotal
v3 report for a URL, domain, IPv4 address, or file hash and displays
provider-reported detection counts, suggested threat labels, categories,
and engine labels when available.

This project does not claim to confirm that a site is safe, execute or
detonate malware, or perform full forensic analysis.

## Technologies

-   Python 3
-   Jupyter Notebook
-   Requests
-   Beautiful Soup 4
-   VirusTotal API v3
-   IPython display

## Files

-   `DakshRathi_ThreatLensAI.ipynb` --- main runnable notebook
-   `requirements.txt` --- Python dependencies
-   `DakshRathi_ThreatLensAI_ProjectReport.docx` --- project report
-   `README.md` --- setup and project overview

## Setup

1.  Install Python 3.10+ and Jupyter Notebook.

2.  Download or clone this repository.

3.  In a terminal, run:

    ``` bash
    python -m venv .venv
    ```

    Activate the virtual environment:

    -   Windows: `.venv\\Scripts\\activate`
    -   macOS/Linux: `source .venv/bin/activate`

4.  Install packages:

    ``` bash
    pip install -r requirements.txt
    ```

5.  Configure a VirusTotal API key privately. Recommended: set the
    `VIRUSTOTAL_API_KEY` environment variable before starting Jupyter.
    Never commit keys to the repository. The notebook also offers a
    hidden prompt for a session-only key if the variable is not set.

6.  Launch Jupyter:

    ``` bash
    jupyter notebook
    ```

7.  Open `DakshRathi_ThreatLensAI.ipynb` and run the cells in order. The
    notebook's example calls are commented out; uncomment and edit the
    URL/indicator you are authorized to check.

## How to use

-   Website inspection: call `inspect_website("https://example.com")`.
-   Reputation lookup: call `report = lookup_virustotal("example.com")`,
    then `show_vt_report(report)`.
-   Combined flow: call
    `investigation = investigate_website("https://example.com")`.
-   Save a local JSON report: `save_report(investigation)`.

VirusTotal's public API has rate limits and access terms. This notebook
retrieves existing reports and does not upload files or request a forced
rescan.

## Data and dataset

This project does not require a separate downloaded training dataset. It
uses live public webpage content and existing VirusTotal report data
when the user supplies a valid API key and the provider returns a
report. VirusTotal is a third-party source; data availability and labels
may change.

## Security and ethical considerations

-   Only investigate systems you have permission to check.
-   Do not upload confidential or sensitive files to third-party
    scanning services.
-   Never commit API keys, tokens, private URLs, or sensitive report
    data.
-   Provider labels can disagree and may be false positives.
-   An absent report or zero detections is not proof of safety.
-   Webpage scraping can fail or be restricted by a website's terms.

## Current limitations

-   Page summaries are based on extracted HTML content; this notebook
    does not include an LLM-based summary endpoint.
-   Website checks are not a malware scan of files downloaded from that
    website.
-   No file is executed or detonated in a sandbox.
-   No model is trained as part of this prototype.
