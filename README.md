

# 📚 **K-8 AI Homework Companion — Multi-Agent Learning Assistant**

*A personalized, multi-agent AI system for homework analysis, tutoring, feedback, and practice.*

---

## 🚨 Problem Statement

K–8 students often struggle with homework because most tools provide answers instead of real guidance. Without step-by-step explanations, hints, or encouragement, students get frustrated and lose confidence. Parents are busy, teachers can’t offer one-on-one help every day, and existing apps rarely adapt to a child’s learning style.

This project aims to create a supportive and interactive homework companion that teaches—not just solves.

---

## 🤖 Why Agents?

Homework support is not a single action. It involves:

* Understanding the assignment
* Planning steps
* Explaining concepts
* Answering questions
* Evaluating work
* Providing practice

A single LLM cannot reliably perform all these tasks in a structured sequence.
A **multi-agent system** allows specialization: one agent analyzes, one tutors, one grades, one generates practice, and one orchestrates the flow. The result is a more natural, adaptive, and educational experience that mirrors a real tutor.

---

## 🏗️ What I Built (Architecture Overview)

This solution uses a **sequential multi-agent workflow**, powered by Gemini and the Google ADK:

### **1. Orchestrator Agent**

Receives homework, initializes the session, and coordinates all other agents.

### **2. Analyzer Agent**

Identifies subject, grade level, concepts, and creates a structured homework plan.
Uses the **Google Search Tool** when needed.

### **3. Tutor Agent**

Guides students step-by-step, gives hints, and adapts tone based on memory.
Uses a long-term **Student Memory System**.

### **4. Grader Agent**

Evaluates student answers using a **custom grading tool**, then generates personalized feedback with Gemini.

### **5. Practice Agent**

Creates new practice questions using a **custom practice generator**.

### **6. Student Memory**

Tracks learning style, confidence, struggle areas, and performance history.

---

## 🎮 Demo

The included Kaggle Notebook demonstrates a full workflow:

1. Orchestrator receives a 4th-grade math assignment
2. Analyzer breaks it into concepts and steps
3. Tutor guides the student through each step
4. Student asks for hints
5. Grader evaluates submitted answers
6. Practice Agent generates new problems

The demo clearly shows tool calls, memory updates, and agent interactions.

---

## 🛠️ The Build (Tools & Tech)

* **Google Agent Development Kit (ADK)**
* **Gemini AI (gemini-2.5-flash)** for analysis, tutoring, feedback
* **Google Search Tool** for the Analyzer Agent
* **Custom Tools:**

  * `calculate_grade()` — scoring & feedback
  * `generate_practice_problem()` — practice generation
* **Long-Term Memory System** for personalization
* **Kaggle Notebook** runtime for execution
* **Sequential Multi-Agent Workflow** following ADK best practices

---

## 🚀 If I Had More Time

* Add OCR support for handwritten homework
* Voice-based tutoring mode

---

## 📄 License

Created for the **Google ADK Capstone Project — Agents for Good (Education Track)**.
Built with Google ADK, Gemini Pro, and custom Python tools.
