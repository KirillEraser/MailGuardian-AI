![n8n](https://img.shields.io/badge/Built_with-n8n-orange)
![OpenAI](https://img.shields.io/badge/AI-OpenAI-blue)
![Status](https://img.shields.io/badge/status-active-success)

# InboxGuardian AI (n8n + Gmail + OpenAI)
🚀 **AI-powered system that automatically organizes your inbox by priority, relevance, and context.**

University and corporate inboxes are often overloaded with low-value emails, making it difficult to identify critical information.

**InboxGuardian AI** solves this by automatically analyzing incoming emails and applying intelligent labels, allowing you to instantly distinguish between urgent messages and background noise.

---

## 🎯 Overview
This project implements an automated email classification pipeline using **n8n**, **OpenAI**, and the **Gmail API**.

Each incoming email is processed, analyzed, and labeled based on:

* content and intent
* sender relationship
* historical interaction
* email metadata and headers

The result is a structured, prioritized inbox with minimal manual effort.

---

## ❓ Why?
As a student at Nazarbayev University, my inbox was _constantly_ flooded with dozens of emails every day—club announcements, newsletters, event invite, while the few emails **that actually mattered** (grades released, lecture changes, professor messages) were easy to miss. I built this because I got tired of **scanning through noise** just to find the **one critical email**.

---

## 🚀 Features

* 📬 Real-time Gmail monitoring (unread inbox)
* 🤖 AI-driven email classification
* 🧠 Context-aware analysis using email history
* 🔍 Detection of bulk, promotional, and irrelevant emails
* ⚡ Automatic Gmail label assignment
* 🎯 Prioritization of urgent and academic messages
* 🧾 Designed for high-noise environments (e.g., university inboxes)

---

## ⚙️ System Architecture

### 1. Gmail Trigger

* Polls inbox every minute
* Filters for unread messages

---

### 2. Email Retrieval

* Fetches full email data:

  * sender information
  * subject and body
  * headers
  * existing labels

---

### 3. Context Enrichment

The system queries:

* 📥 Previous emails from the sender
* 📤 Emails sent to the sender

This enables detection of:

* first-time (cold) emails
* ongoing conversations

---

### 4. AI Classification Engine

The OpenAI-powered agent evaluates:

* semantic meaning of the email
* urgency indicators
* relationship context
* metadata (unsubscribe links, bulk headers)

It outputs a structured label ID.

---

### 5. Automated Labeling

* Applies the predicted label in Gmail
* Organizes inbox automatically

---

## 🧠 Classification Logic

The system combines multiple signals:

* **Content analysis** (subject + body)
* **Sender relationship detection**
* **Header inspection**:

  * `List-Unsubscribe`
  * `Precedence: Bulk`
* **Academic relevance rules**

---

## 📌 Label System

| Label          | Description                                               |
| -------------- | --------------------------------------------------------- |
| 🔴 Urgent      | Requires immediate action (deadlines, exams, submissions) |
| 🟡 Grades      | Results, feedback, assessment updates                     |
| 🔵 Course Info | General course announcements                              |
| 🟢 Personal    | Direct communication with sender                          |
| 🏛 Admin       | Official institutional messages                           |
| ⚪ Likely Spam  | Events, newsletters, irrelevant content                   |

---

## 🧩 Tech Stack

* **n8n** – workflow orchestration and automation engine
* **Gmail API** – email ingestion and labeling
* **OpenAI (GPT-5-mini)** – natural language classification
* **LangChain (n8n nodes)** – structured AI execution

---

## 🛠️ Setup

### Requirements

* n8n instance (self-hosted recommended)
* Gmail OAuth credentials
* OpenAI API key

---

### Installation

1. Import the workflow JSON into n8n
2. Configure credentials:

   * Gmail
   * OpenAI
3. Create required Gmail labels
4. Activate the workflow

---

## 🎯 Use Cases

* Students managing high-volume academic inboxes
* Professionals dealing with noisy email environments
* AI-driven productivity systems
* Automated email prioritization pipelines

---

## 💡 Why This Matters

Email overload reduces productivity and increases the risk of missing critical information.

InboxGuardian AI transforms email from an unstructured stream into a prioritized system, enabling:

* faster decision-making
* reduced cognitive load
* improved information visibility

---

## 🔮 Future Improvements

* Priority scoring system
* Push notifications for urgent emails
* Web dashboard for analytics
* Multi-account support
* Fine-tuned classification models

---

## 🧑‍💻 Author

Built by Kirill — Robotics student & automation engineer.

---

## ⭐ Support

If you find this project useful, consider starring the repository.
