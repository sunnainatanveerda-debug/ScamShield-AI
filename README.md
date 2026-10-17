# 🛡️ ScamShield AI
### AI-Powered Scam Message and Suspicious Link Analyzer

ScamShield AI is a Python-based application that helps users identify potential scams in suspicious messages, job offers, SMS texts, emails, and links. It combines a local rule-based detection system with an optional Google Gemini AI assessment to explain warning signs and recommend safer actions.

**The goal:** Help people recognize common scam indicators, think critically before responding, and make safer online decisions.

> **Disclaimer:** ScamShield AI is a decision-support tool, not a guarantee of fraud detection. Its indicator score is not a probability of fraud, and a low score does not mean a message is safe.

## ✨ Features

- **Rule-Based Scam Detection:** Identifies suspicious patterns using predefined warning rules.
- **Gemini AI Assessment:** Provides an additional AI-generated assessment, explanations, and safety recommendations when requested.
- **Multiple Message Types:** Supports job offers, SMS/text messages, emails, suspicious links, and other messages.
- **Indicator Scoring:** Assigns 25 points per matched rule, capped at 100.
- **Warning Explanations:** Shows the specific rules triggered by the analyzed message.
- **Safety Recommendations:** Offers practical guidance based on detected warning signs.
- **Message-Type Safety Checklists:** Displays relevant safety steps for different message categories.
- **Privacy Notice:** Explains when messages are analyzed locally and when they are sent to Google's Gemini API.
- **User-Friendly Error Handling:** Displays readable messages when the Gemini service cannot connect.
#### Screenshots
Main Interface, Rule-Based Detection Results, and Gemini AI Assessment.

## 🧠 How It Works

ScamShield AI uses two complementary analysis methods.

### 1. Rule-Based Analysis

The application checks the submitted text against predefined patterns. Examples of warning indicators include:

- Upfront payment requests
- Urgent pressure
- Password or OTP requests
- Prize or reward claims
- Suspicious account messages
- URL shorteners
- URLs using IP addresses
- Unusually high salary claims

Each matched rule adds 25 points, up to a maximum of 100.

**Important:** This is an indicator score, not a probability or confidence percentage. Rules may produce false positives or miss sophisticated scams.

### 2. Gemini AI Assessment

Users can request an additional assessment using Google's Gemini API. The AI can explain suspicious elements, identify potential risks, and recommend safety precautions.

The Gemini assessment is separate from the rule-based score. AI-generated conclusions can be incorrect and should be independently verified.

### 3. Safety Guidance

Based on the selected message type and detected indicators, the application provides recommendations such as avoiding unexpected payments, protecting verification codes, checking official websites, and verifying job offers independently.

## 🛠️ Technology Stack

- **Python** — Application logic and rule-based detection
- **Streamlit** — Interactive web application interface
- **Regular Expressions (`re`)** — Pattern matching for warning indicators
- **Google Gemini API** — Optional AI-powered assessment
- **Google Gen AI SDK (`google-genai`)** — Gemini API integration

## 🚀 Getting Started

### Prerequisites

Install the following before running the application:

- Python 3.10 or newer, compatible with the dependencies
- pip
- An internet connection for Gemini AI assessment
- A Google Gemini API key if you want to use the AI feature

### 1. Clone the Repository

Replace the repository URL below if your GitHub repository uses a different address.

```bash
git clone https://github.com/sunnainatanveerda-debug/ScamShield-AI.git
cd ScamShield-AI
```

### 2. Create a Virtual Environment

**Windows PowerShell:**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

If PowerShell blocks activation, you can run the application using `.venv`'s Python executable directly instead.

### 3. Install Dependencies

If the project contains a `requirements.txt` file:

```bash
python -m pip install -r requirements.txt
```

If the file is missing, install the packages used by the application:

```bash
python -m pip install streamlit google-genai
```

### 4. Configure the Gemini API Key

Create a file named `.streamlit/secrets.toml` in the project directory.

Add your own API key:

```toml
GEMINI_API_KEY =  "YOUR_GEMINI_API_KEY"
```

Replace the placeholder with your actual key. Never publish the real key in your repository, README, screenshots, or demo video.

If you do not configure the Gemini API, rule-based analysis may still be available, depending on your application's configuration.

### 5. Run the Application

From the project directory, run:

```bash
streamlit run app.py
```

Streamlit will provide a local address that you can open in your web browser.

## 📖 How to Use

1. Launch ScamShield AI.
2. Select the relevant message type.
3. Paste the suspicious message or link into the input field.
4. Click **Analyze Message**.
5. Review the rule-based indicator score and matched warning rules.
6. Read the recommended safety actions and checklist.
7. Optionally request a Gemini AI assessment.
8. Verify suspicious claims through official channels before taking action.

## 🔐 Privacy and Security

- Rule-based analysis is performed locally by the application.
- When a user requests Gemini AI assessment, the submitted message and selected message type are sent to Google's Gemini API.
- Do not submit passwords, OTPs, bank credentials, private documents, or other sensitive information.
- The application should not be assumed to provide guaranteed storage-free processing or complete anonymity.
- Keep API keys in local secrets or environment variables, not in source code.
- Exclude `.streamlit/secrets.toml` and other secret files from Git using `.gitignore`.
- Review repository contents before publishing to ensure credentials and private data are not committed.

## 🧪 Testing and Validation

The application has been tested with sample messages covering:

- Suspicious job offers involving upfront fees
- Legitimate job announcements
- Bank-related SMS messages requesting verification codes
- Prize and reward messages requiring processing fees
- Links containing IP addresses
- Shortened URLs
- Normal messages with no obvious warning indicators
- Gemini AI assessments and connection errors

These are manual functional tests using sample inputs, not a formal security audit or a comprehensive benchmark. Results can vary with message wording and the detection rules.

## ⚠️ Limitations

- Rule-based detection depends on predefined patterns and may miss new or sophisticated scams.
- Legitimate messages may occasionally trigger warnings.
- Gemini AI can produce inaccurate or incomplete assessments.
- The indicator score is not a probability of fraud.
- URL pattern detection does not establish whether a website is malicious.
- ScamShield AI does not replace professional cybersecurity tools or independent verification.

## 🔮 Future Improvements

Potential improvements include:

- More comprehensive testing against false positives and false negatives
- Additional scam patterns and multilingual detection
- Safer URL reputation checks through trusted security services
- Improved explanations and reporting
- Expanded test automation
- Further accessibility and interface improvements

## 🎯 Project Purpose

ScamShield AI explores how rule-based programming and generative AI can work together to help users recognize suspicious digital communications. It is designed as an educational and practical safety-support application.

## 👩‍💻 Author

**Sunnaina Tanveer**

Built with Python, Streamlit, and Google's Gemini API.

## 📄 License

No license has been specified yet. Add a `LICENSE` file if you want to publish the project under an open-source license.

---

**Stay alert. Verify independently. Think before you click.**
