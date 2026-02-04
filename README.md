# AI-Powered Customer Support Chatbot (Java + JSP)

## 📌 Project Overview

The AI Customer Support Chatbot provides **24/7 automated assistance** to users by:
- Answering common FAQs using a structured knowledge base
- Falling back to **Google Gemini AI** for complex or unseen queries
- Maintaining chat history for session-based context
- Offering a modern, responsive chat UI

---

## 🎯 Objectives

- Build an intelligent chatbot for automated customer support
- Combine rule-based pattern matching with AI-generated responses
- Store and retrieve conversation history securely
- Deliver a clean, responsive, and user-friendly web interface

---

## 🛠️ Technology Stack

### Frontend
- HTML5, CSS3
- JavaScript (ES6)
- Font Awesome

### Backend
- Java (JDK 24)
- JSP & Servlets
- Apache Tomcat 9

### Database
- PostgreSQL 16
- pgAdmin 4

### External API
- Google Gemini AI API (fallback response generation)

---

## 📸 Screenshots

### Chatbot Interface
![Chatbot UI](images/chatbot_ui.png)

---

## 📂 Project Structure

```text
CustomerSupportChatbot/
├── Source Packages/
│   ├── com.chatbot.controller/
│   │   └── ChatServlet.java
│   ├── com.chatbot.dao/
│   │   ├── ChatHistoryDAO.java
│   │   └── KnowledgeBaseDAO.java
│   ├── com.chatbot.model/
│   │   ├── Message.java
│   │   ├── KnowledgeBaseEntry.java
│   │   └── PatternMatcher.java
│   └── com.chatbot.util/
│       └── DBConnection.java
├── Web Pages/
│   ├── css/style.css
│   ├── js/chat.js
│   ├── index.jsp
│   └── test.jsp
├── pom.xml
└── Database (PostgreSQL)
---
## System Architecture

1. **User Input** is captured through the JSP-based frontend.
2. **ChatServlet** processes incoming user requests.
3. The system performs a **Knowledge Base lookup** using predefined FAQs and patterns.
4. If no match is found, the query is forwarded to **Google Gemini AI** as a fallback.
5. **Chat history** is stored securely in the PostgreSQL database.
6. The generated response is returned and displayed on the UI.

---
## Database Design

### Table: `knowledge_base`
- Stores predefined FAQs
- Contains keywords and regex patterns for rule-based matching

### Table: `chat_history`
- Stores session-wise conversation logs
- Enables context retention and chat history tracking

---

## How to Run the Project

### Prerequisites
- Java JDK 24
- Apache Tomcat 9
- PostgreSQL 16
- Apache NetBeans IDE
- Google Gemini API Key

### Steps
1. Clone the GitHub repository.
2. Create and configure the PostgreSQL database (`chatbot_db`).
3. Update database credentials in `DBConnection.java`.
4. Add your Google Gemini API key in `ChatServlet.java`.
5. Clean and build the project in NetBeans.
6. Deploy and run the application on Apache Tomcat.

---

## ✨ Key Features

- Hybrid **Knowledge Base + AI-powered** chatbot
- Session-based chat history storage
- Real-time **Google Gemini AI** integration
- Responsive and user-friendly interface
- Secure JDBC-based database connectivity
