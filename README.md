# 🛡️ Aegis-IAM Dashboard

### Privilege Escalation Detection & IAM Risk Intelligence Platform

Aegis-IAM Dashboard is a production-ready IAM (Identity & Access
Management) risk analysis tool designed to detect privilege escalation
paths, over-privileged identities, and separation-of-duties conflicts
from real-world cloud exports.

------------------------------------------------------------------------

## 🚀 Features

### 🔹 Real-World JSON Ingestion

-   Starts in **Awaiting Data** mode (no auto demo)
-   Manual **Initialize Simulation** button
-   Supports:
    -   Simple IAM schema (users / roles / permissions / inherits)
    -   AWS IAM `get-account-authorization-details` JSON export
-   Handles nested policy structures and wildcards safely

------------------------------------------------------------------------

### 🔹 Privilege Escalation Detection

-   Graph-based escalation path discovery (NetworkX)
-   Detects assume-role abuse and wildcard permissions
-   Severity classification (Critical / High / Medium / Low)

------------------------------------------------------------------------

### 🔹 Dynamic Remediation Playbooks

For every detected risk: 1. Technical Root Cause\
2. Step-by-Step CLI Patch Commands\
3. Real-World Resolution Strategy

------------------------------------------------------------------------

### 🔹 Intelligence Report Generation

-   **Vector PDF Export (ReportLab)** -- Crisp, professional output\
-   **Client-Side PDF Export (html2pdf)** -- Quick browser export

------------------------------------------------------------------------

### 🔹 MITRE ATT&CK Mapping

Detected risky permissions are mapped to: - Technique ID - Tactic -
Description

------------------------------------------------------------------------

## 🏗️ Project Structure

    aegis-iam-dashboard/
    │
    ├── app.py
    ├── requirements.txt
    ├── mitre_map.json
    ├── README.md
    │
    ├── data/
    │   └── demo_aws_auth_details.json
    │
    ├── uploads/
    │
    ├── static/
    │   ├── css/
    │   │   └── hud.css
    │   └── js/
    │       └── hud.js
    │
    └── templates/
        ├── base.html
        ├── index.html
        ├── graph.html
        ├── playbook.html
        └── intel_lab.html

------------------------------------------------------------------------

## ⚙️ Installation

``` bash
python -m venv venv
# Windows:
venv\Scripts\activate
# Mac/Linux:
source venv/bin/activate

pip install -r requirements.txt
python app.py
```

Open: http://127.0.0.1:5000

------------------------------------------------------------------------

## ☁️ AWS IAM Export Example

``` bash
aws configure
aws iam get-account-authorization-details --output json > iam_auth.json
```

Upload `iam_auth.json` into the dashboard.

------------------------------------------------------------------------

## 🛡️ Security Notes

-   No use of eval or unsafe execution
-   Upload size limit enforced
-   OWASP-aligned security headers
-   Intended for authorized environments only

------------------------------------------------------------------------

## 👤 Author

Owned and Developed by\
**Nisarg Chasmawala (Shroff)**\
© 2026 All Rights Reserved.
