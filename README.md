# AI Study Planner & Learning Assistant Agent

A multi-agent AI system that generates personalized study plans, recommends resources, tracks progress, and sends motivational reminders. Built with Google Gemini for the Kaggle x Google 5-Day AI Agents Intensive Capstone Project.

---

## Table of Contents

- [Problem Statement](#problem-statement)
- [Solution](#solution)
- [Key Features](#key-features)
- [System Architecture](#system-architecture)
- [Technology Stack](#technology-stack)
- [Installation & Setup](#installation--setup)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Example Output](#example-output)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)
- [Credits](#credits)

---

## Problem Statement

Students preparing for exams face several challenges:

- Creating structured and realistic study schedules
- Identifying and prioritizing weak subjects
- Finding relevant learning resources quickly
- Maintaining consistency and motivation throughout preparation
- Tracking progress effectively

This project addresses these pain points through an intelligent multi-agent system.

---

## Solution

An AI-powered study planning system that:

1. Collects student information (subjects, weak areas, goals, available time)
2. Generates personalized multi-day study timetables
3. Recommends learning resources and search strategies
4. Evaluates plan quality and feasibility
5. Tracks daily progress with persistent memory
6. Sends motivational reminders to maintain momentum

---

## Key Features

- **Multi-Agent Architecture**: Specialized agents for different tasks working together
- **Personalized Plans**: Custom study schedules based on individual needs
- **Resource Discovery**: Curated YouTube search keywords and learning strategies
- **Progress Tracking**: Daily logging with JSON-based memory
- **Motivational Support**: AI-generated daily reminders
- **Gemini Integration**: Powered by Google's latest Gemini Flash model
- **Kaggle Native**: Runs entirely in Kaggle notebooks with secure API key handling

---

## System Architecture

The system uses six specialized agents coordinated by an orchestrator:

### Agents

| Agent | Role | Responsibilities |
|-------|------|-----------------|
| **Input Agent** | Data Collection | Gathers subjects, weak areas, goals, and study duration |
| **Planning Agent** | Schedule Generation | Creates detailed multi-day study timetables using Gemini |
| **Resource Agent** | Learning Materials | Suggests resource strategies and YouTube search queries |
| **Evaluation Agent** | Quality Assurance | Reviews plan quality, balance, and feasibility |
| **Progress Agent** | Tracking | Logs daily progress and updates persistent memory |
| **Reminder Agent** | Motivation | Generates personalized daily motivational messages |

### Orchestrator

Coordinates agent communication, manages workflow, and ensures smooth operation of the entire system.

---

## Technology Stack

| Component | Technology |
|-----------|-----------|
| **Language** | Python 3.10+ |
| **LLM** | Google Gemini (`models/gemini-flash-latest`) |
| **Runtime** | Kaggle Notebook |
| **Memory** | JSON persistent storage |
| **Logging** | Python logging framework |
| **API Integration** | `google-generativeai` SDK |
| **Secrets Management** | Kaggle Secrets |

---

## Installation & Setup

### Prerequisites

- Kaggle account
- Google API key for Gemini

### Steps

1. **Clone or download this repository**

2. **Open the Kaggle notebook**
   - Upload `study_planner_agent.ipynb` to Kaggle
   - Or use the direct Kaggle link: [Add your Kaggle notebook link]

3. **Add API Key to Kaggle Secrets**
   - Go to Kaggle Settings → Secrets
   - Add a new secret:
     - Name: `GOOGLE_API_KEY`
     - Value: Your Google API key

4. **Install dependencies** (auto-installed in notebook)
```python
   !pip install google-generativeai
```

5. **Run the notebook**
   - Execute all cells in order
   - Follow the prompts to input your study details

---

## Usage

### Basic Workflow

1. **Run the notebook**

2. **Provide input when prompted**:
```
   Enter subjects (comma-separated): Physics, Chemistry, Math
   Enter weak areas (comma-separated): Thermodynamics, Organic Chemistry
   Enter your goal: Score 90% in board exams
   Enter study duration (days): 30
```

3. **Review generated study plan**
   - Daily timetable with time allocations
   - Subject prioritization
   - Break schedules

4. **Check resource recommendations**
   - YouTube search keywords
   - Learning strategies
   - Resource types (videos, practice problems, notes)

5. **Log daily progress**
   - Mark completed topics
   - Note challenges
   - Update memory

6. **Receive motivational reminders**
   - Daily personalized messages
   - Progress encouragement

### Memory Management

Progress is automatically saved to `study_memory.json`:
```json
{
  "subjects": ["Physics", "Chemistry", "Math"],
  "weak_areas": ["Thermodynamics", "Organic Chemistry"],
  "goal": "Score 90% in board exams",
  "duration": 30,
  "progress": {
    "day_1": {
      "completed": ["Basic Thermodynamics"],
      "notes": "Good progress on first day"
    }
  }
}
```

---

## Project Structure
```
ai-study-planner-agent/
│
├── study_planner_agent.ipynb    # Main implementation notebook
├── README.md                     # This file
├── LICENSE                       # Project license
```

---

## Example Output

### Generated Study Plan
```
Day 1:
09:00-10:30 - Physics: Thermodynamics basics
10:30-10:45 - Break
10:45-12:15 - Chemistry: Organic reactions intro
12:15-13:00 - Lunch break
13:00-14:30 - Math: Calculus review
14:30-14:45 - Break
14:45-16:00 - Physics: Practice problems
```

### Resource Recommendations
```
Subject: Physics - Thermodynamics
Recommended searches:
- "thermodynamics basics for beginners"
- "first law of thermodynamics explained"
- "thermodynamics problems and solutions"

Strategy: Watch concept videos first, then solve practice problems
```


---

## Future Enhancements

- **Google Calendar Integration**: Auto-sync study plans to calendar
- **Voice Assistant**: Voice-based interaction for hands-free planning
- **Adaptive Scheduling**: ML-based real-time plan adjustments based on progress
- **Mobile/Web UI**: Deploy as a web or mobile application
- **Quiz Generation**: Auto-generate practice quizzes using Gemini
- **Peer Collaboration**: Group study planning features
- **Analytics Dashboard**: Visual progress tracking and insights
- **Notification System**: Push notifications for study reminders
- **Multi-language Support**: Support for non-English speakers

---
### Areas for Contribution

- Additional agent types (Quiz Agent, Revision Agent)
- UI/UX improvements
- Integration with other APIs (Notion, Trello)
- Testing and documentation
- Bug fixes and performance optimization

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Credits

**Author**: Vidish Kumar

**Project**: Kaggle x Google 5-Day AI Agents Intensive Capstone Project

**Track**: Concierge Agents

**Special Thanks**:
- Kaggle team for hosting the AI Agents Intensive
- Google Gemini development team
- Open source community for inspiration and resources

---


## Acknowledgments

- Inspired by real challenges faced by students during exam preparation
- Built using Google's Gemini API
- Part of the Kaggle AI Agents learning path

---

**Made with dedication for students everywhere**
