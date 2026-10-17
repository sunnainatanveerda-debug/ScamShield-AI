# 🛡️ ScamShield AI

### Your Assistant for Spotting Potential Scams

ScamShield AI is a bilingual, rule-based scam message detection prototype that helps users identify common warning signs in suspicious messages. It provides an indicator score, explains matched warning signs, and recommends practical safety actions in **English and Urdu**.

## 🎯 Project Overview

Online scams can use fake job offers, prize claims, urgent account alerts, and suspicious links to trick people into sharing money or sensitive information.

ScamShield AI helps users examine a message and recognize potential warning signs before taking action.

## ✨ Features

- **Bilingual interface:** English and Urdu support.
- **Multiple message types:** Job offers, SMS/text messages, emails, suspicious links, and other messages.
- **Rule-based detection:** Checks messages for predefined scam warning indicators.
- **Risk indicator score:** Assigns a score from 0 to 100 based on matched rules.
- **Safety recommendations:** Provides advice related to detected indicators.
- **Message-specific checklists:** Displays practical safety steps for different message types.
- **Privacy-conscious design:** The prototype is designed to analyze messages locally without sending them to an external AI service.

## 🔍 Warning Indicators

ScamShield AI currently checks for warning signs such as:

- Upfront payment requests
- Urgent pressure
- Password or OTP requests
- Prize or reward claims
- Suspicious account messages
- Shortened URLs
- URLs using IP addresses
- Unusually high salary claims

## 📊 Indicator Score

Each matched rule contributes 25 points, up to a maximum of 100.

| Score | Warning level |
|---|---|
| 0–24 | Low |
| 25–49 | Low |
| 50–74 | Medium |
| 75–100 | High |

**Important:** This is a rule-based indicator score, not a probability that a message is fraudulent. A low score or zero matches does not guarantee that a message is safe.

## 🧪 Testing

The following synthetic messages were tested during development.

### Test 1: Suspicious Bank SMS

**Expected indicators:**
- Urgent pressure
- Password or OTP request
- Suspicious account message
- URL shortener

**Observed result:** 4 indicators detected.

**Score:** 100/100 — High warning level.

### Test 2: Prize Scam

**Sample message:**

> Congratulations! You won $5,000. Pay a $50 processing fee today to claim your prize.

**Expected indicators:**
- Upfront payment
- Prize or reward claim

**Observed result:** 2 indicators detected.

**Score:** 50/100 — Medium warning level.

**Improvement opportunity:** The urgency rule did not detect the word “today” in this test.

### Test 3: Suspicious IP-Address Link

**Sample message:**

> Your account needs verification. Visit http://192.0.2.1/login immediately.

**Expected indicators:**
- Urgent pressure
- Suspicious account message
- URL using an IP address

**Observed result:** 3 indicators detected.

**Score:** 75/100 — High warning level.

The IP address used here is reserved for documentation and testing.

## 🛠️ Technology Stack

- Python
- Streamlit
- Regular expressions and predefined rules

## 🚀 Run Locally

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd ScamShield-AI
```

Replace `YOUR_GITHUB_REPOSITORY_URL` with your actual repository URL.

### 2. Install dependencies

```bash
pip install streamlit
```

If your project has a `requirements.txt` file, use:

```bash
pip install -r requirements.txt
```

### 3. Run the application

```bash
streamlit run app.py
```

The application should open in your browser.

## 🔒 Privacy and Safety

The prototype is designed to analyze messages using local rules rather than an external AI service. Avoid entering real passwords, OTPs, financial information, or private messages during testing.

Privacy claims should be verified against the actual code and deployment environment.

## ⚠️ Limitations

- The detector uses predefined rules and does not understand every scam pattern.
- Legitimate messages may trigger warnings, and scams may go undetected.
- URL patterns alone cannot establish whether a website is malicious.
- The indicator score is not a verified fraud probability.
- This prototype does not replace independent verification or professional security tools.

## 🔮 Future Improvements

- Improve urgency detection for more natural phrases.
- Expand testing with diverse synthetic messages.
- Reduce duplicate recommendations.
- Improve URL analysis.
- Evaluate false positives and missed scam indicators.
- Explore multilingual machine-learning methods in a future version.

## 👩‍💻 Project Status

ScamShield AI is a working prototype under development.

## 📄 Disclaimer

ScamShield AI is an educational safety tool. Always verify suspicious requests through official channels before sharing information, clicking links, or sending money.
