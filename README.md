# 🤖 UiPath AI Agent - Resume Screener Automation

## 📌 Overview
This project is a UiPath-based AI automation agent that automatically processes incoming emails, extracts resume attachments, analyzes them using an AI Resume Screener agent deployed in UiPath Orchestrator, and sends back results via email.

It demonstrates end-to-end automation combining:
- Gmail integration
- Email attachment handling
- PDF text extraction
- AI Agent invocation (Resume Screener)
- Conditional logic and reporting

## ⚙️ Workflow Architecture

### 1. Trigger
- **Manual Trigger**
- Workflow starts execution manually

### 2. Email Processing (Gmail Integration)
- Connects to Gmail account:
- Reads emails from:
- Folder: **Inbox**
- Applies optional filters (if configured)

### 3. Download Email Attachments
- Downloads attachments from incoming emails
- Filters supported:
- File type (PDF resumes)
- Extracts attachments for processing

### 4. Loop Through Attachments
- Uses:
- Iterates over all downloaded resume files

### 5. PDF Text Extraction
- Extracts text content from resume PDFs
- Converts unstructured resume data into machine-readable format

### 6. Variable Assignment
- Stores extracted resume text into variables for further processing

### 7. AI Agent Execution (Resume Screener)
- Invokes UiPath Orchestrator AI Process:
- **Process Name:** Resume Screener  
- **Folder Path:** Shared/Agent  

- Input:
- Resume text extracted from PDF

- Output:
- Candidate evaluation / screening result

### 8. Logging
- Logs execution status using:
- Log Level: **Info**
- Helps track workflow execution and debugging

### 9. Decision Making (If Condition)
- Based on AI agent output:
- Determines next action (shortlisted / rejected / etc.)

### 10. Email Response
- Sends result back via Gmail:
- **Draft or Send Email**
- Includes:
- Subject (based on screening result)
- Body (AI evaluation summary)
- Optional attachments

## 🧠 Key Features
- Fully automated resume screening pipeline
- Gmail-based email ingestion
- AI-powered decision making using UiPath Agent
- PDF parsing and text extraction
- Scalable Orchestrator-based architecture

## 🛠️ Tech Stack
- UiPath Studio / Studio Web
- UiPath Orchestrator
- Gmail API integration
- PDF Text Extraction activities
- AI Agent (Resume Screener)
- RPA Workflow Design

## 📂 Project Structure
-entry-points.json
-Main.xaml
-project.json
-project.uiproj

## 🚀 How It Works (Simple Flow)
Incoming Email
↓
Fetch Gmail Inbox
↓
Download Attachments (PDF)
↓
Extract Resume Text
↓
Send to AI Resume Screener Agent
↓
Get Evaluation Result
↓
Send Email Response

## 📌 Use Case
This automation can be used in:
- HR recruitment automation
- Resume screening pipelines
- Talent acquisition systems
- AI-powered email processing systems

## 👩‍💻 Author
Aashi  
B.Tech CSE | KIIT University  
Interests: AI/ML, GenAI, RPA, Full Stack Development

## 📎 Future Improvements
- Add database storage for resumes
- Improve AI scoring model
- Add dashboard for HR analytics
- Integrate multiple email providers


