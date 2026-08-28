# 🏁 PodiumAI

## Multi-Agent AI Formula 1 Intelligence Platform

**PodiumAI** is an AI-powered Formula 1 intelligence platform that combines detailed F1 datasets, machine learning, multi-agent AI, and interactive visualizations into a single web application.

The platform allows users to **ask questions about Formula 1 in natural language**, explore races and drivers, analyze performance and strategy, and eventually run AI-powered what-if simulations.

> **Ask Formula 1 anything. Explore the data. Understand the race.**

---

# 🚦 Vision

Formula 1 produces enormous amounts of data across every race weekend — lap times, telemetry, tyre compounds, pit stops, weather, race events, driver performance, qualifying results, and championship standings.

Raw data alone, however, does not explain **why** something happened.

PodiumAI aims to turn this data into an intelligent system that can answer questions such as:

> **"Why did Vettel win the 2018 Bahrain Grand Prix?"**

> **"Why did this driver lose time during the second stint?"**

> **"Compare Hamilton and Vettel's race pace."**

> **"Which tyre strategy was most effective?"**

> **"How did the weather affect the race?"**

> **"What would have happened if the driver had pitted five laps earlier?"**

Instead of being a generic chatbot, PodiumAI will ground its answers in **actual Formula 1 data**.

---

# 🤖 Multi-Agent AI System

The core intelligence of PodiumAI will be a **multi-agent architecture**.

A central **Master Agent** will understand the user's question and determine which specialized agents need to work together.

```text
                         USER
                           │
                           ▼
                  ┌─────────────────┐
                  │   PODIUMAI WEB  │
                  │   AI Assistant  │
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │   MASTER AGENT  │
                  │  Orchestrator   │
                  └────────┬────────┘
                           │
       ┌───────────────────┼───────────────────┐
       │                   │                   │
       ▼                   ▼                   ▼
 ┌───────────┐       ┌───────────┐       ┌───────────┐
 │Race Data  │       │ Prediction│       │ Strategy  │
 │  Agent    │       │   Agent   │       │   Agent   │
 └───────────┘       └───────────┘       └───────────┘
       │                   │                   │
       ▼                   ▼                   ▼
 ┌───────────┐       ┌───────────┐       ┌───────────┐
 │  Weather  │       │Simulation │       │  Events   │
 │   Agent   │       │   Agent   │       │   Agent   │
 └───────────┘       └───────────┘       └───────────┘
       │                   │                   │
       └───────────────────┼───────────────────┘
                           ▼
                  ┌─────────────────┐
                  │ F1 Knowledge /  │
                  │   RAG Agent     │
                  └────────┬────────┘
                           ▼
                  ┌─────────────────┐
                  │ Explanation /   │
                  │ Response Agent  │
                  └────────┬────────┘
                           ▼
                          USER
```

---

# 🧠 Specialized Agents

## Master Agent

The central orchestrator.

Responsibilities:

* Understand user questions
* Determine which agents are required
* Route tasks to specialized agents
* Combine agent outputs
* Coordinate multi-step reasoning
* Return the final response

---

## 🏎️ Race Data Agent

Responsible for retrieving and analyzing structured Formula 1 data.

Potential responsibilities:

* Race results
* Driver information
* Constructor information
* Circuits
* Sessions
* Lap data
* Timing data
* Historical results

---

## 🔮 Prediction Agent

Responsible for machine-learning-based predictions.

Potential capabilities:

* Race performance prediction
* Qualifying performance prediction
* Driver performance analysis
* Finishing-position prediction
* Performance trends

---

## 🛞 Strategy Agent

Analyzes race strategy.

Potential capabilities:

* Tyre strategies
* Pit-stop timing
* Stint lengths
* Undercuts
* Overcuts
* Tyre degradation
* Strategy comparison

---

## 🌦️ Weather Agent

Analyzes the relationship between weather and race performance.

Potential capabilities:

* Temperature analysis
* Rain conditions
* Track conditions
* Humidity
* Wind
* Weather-performance relationships

---

## 🚨 Event Agent

Analyzes important race events.

Potential events include:

* Safety cars
* Virtual safety cars
* Red flags
* Pit stops
* Incidents
* Position changes
* Retirements
* Race control messages

---

## 🔬 Simulation Agent

Responsible for future what-if analysis.

Examples:

> "What if the driver had pitted five laps earlier?"

> "What if the driver had started on Medium tyres?"

> "What if there had been no safety car?"

The simulation system will only be introduced after sufficient historical data and reliable models are available.

---

## 📚 F1 Knowledge / RAG Agent

Handles broader Formula 1 knowledge that may not exist directly in structured race datasets.

Potential sources:

* F1 documentation
* Historical information
* Technical knowledge
* Driver/team information
* Regulations
* Curated F1 knowledge base

The RAG system will allow the AI to retrieve relevant information before generating an answer.

---

## 💡 Explanation Agent

Transforms technical analysis into an understandable response.

It will:

* Combine outputs from multiple agents
* Explain results clearly
* Provide supporting statistics
* Reference relevant race data
* Distinguish between data-driven conclusions and model predictions

The goal is to make complex F1 analysis understandable even to users who are not data scientists.

---

# 🌐 Website Experience

PodiumAI will be designed as a **modern F1 intelligence command center**.

The website will not simply be a chatbot.

It will combine:

* AI conversation
* Race exploration
* Driver dashboards
* Constructor analysis
* Circuit information
* Data visualizations
* Strategy analysis
* Predictions
* Future simulations

---

# 🏠 Home Page

The home page will immediately introduce the AI assistant.

```text
┌──────────────────────────────────────────────────────────────┐
│  PODIUMAI                         Races  Drivers  Analytics   │
│                                                              │
│                                                              │
│             YOUR AI FORMULA 1 ENGINE                         │
│                                                              │
│       Ask questions. Explore races. Understand F1.           │
│                                                              │
│   ┌──────────────────────────────────────────────────────┐   │
│   │ Ask PodiumAI anything about Formula 1...             │   │
│   │                                                      │   │
│   │                                   [ Ask → ]          │   │
│   └──────────────────────────────────────────────────────┘   │
│                                                              │
│  Try:                                                       │
│  "Why did Vettel lose time in Bahrain 2018?"                │
│  "Compare Hamilton and Vettel's race pace."                 │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

The primary action is:

> **Ask PodiumAI anything about Formula 1.**

---

# 💬 AI Assistant

The AI Assistant is the main interface of the platform.

A typical interaction could look like:

```text
┌──────────────────────────────────────────────────────────────┐
│ USER                                                          │
│ Why did Vettel win the 2018 Bahrain GP?                       │
│                                                              │
├──────────────────────────────────────────────────────────────┤
│ PODIUMAI                                                     │
│                                                              │
│ Vettel's victory was influenced by race pace, tyre strategy, │
│ and the way the race developed around the leading drivers.   │
│                                                              │
│ 🏎 Race Data Agent                                            │
│ ✓ Retrieved race results                                      │
│                                                              │
│ 🛞 Strategy Agent                                             │
│ ✓ Analyzed tyre strategy                                      │
│                                                              │
│ 🌦 Weather Agent                                              │
│ ✓ Checked race conditions                                     │
│                                                              │
│ 💡 Explanation Agent                                          │
│ ✓ Combined findings                                           │
│                                                              │
│ [Lap Chart]  [Tyre Strategy]  [Race Pace]                    │
└──────────────────────────────────────────────────────────────┘
```

The user does **not** need to manually select agents.

The Master Agent determines which agents are required.

---

# 🔍 Agent Activity

PodiumAI can expose the agent workflow through an expandable interface.

```text
┌──────────────────────────────┐
│ PODIUMAI AGENTS              │
│                              │
│ ● Master Agent       Active  │
│ ✓ Race Data Agent    Done    │
│ ✓ Strategy Agent     Done    │
│ ✓ Weather Agent      Done    │
│ ○ Prediction Agent   Idle    │
│ ○ Simulation Agent   Idle    │
└──────────────────────────────┘
```

For example:

```text
User Question
      │
      ▼
Master Agent
      │
      ├── Race Data Agent
      │
      ├── Strategy Agent
      │
      ├── Weather Agent
      │
      └── Explanation Agent
              │
              ▼
          Final Answer
```

---

# 🏁 Race Explorer

Users will be able to browse Formula 1 seasons and races.

Example:

```text
2018 SEASON

┌─────────────┬─────────────┬─────────────┐
│ 🇦🇺 Australia│ 🇧🇭 Bahrain │ 🇨🇳 China    │
│    GP        │    GP       │    GP       │
│             │             │             │
│   Vettel    │   Vettel    │  Ricciardo  │
└─────────────┴─────────────┴─────────────┘

                 [ Explore Race ]
```

Selecting a race opens its dedicated race dashboard.

---

# 📊 Race Dashboard

Example:

### 2018 Bahrain Grand Prix

```text
┌─────────────────────────────────────────────────────────────┐
│ BAHRAIN GRAND PRIX 2018                                     │
│ Sakhir • Round 2                                             │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│ 🥇 Vettel       🥈 Bottas       🥉 Hamilton                 │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│ Position Changes                                             │
│                                                             │
│          ╱╲                                                 │
│    ╲────╱  ╲──────                                         │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│ Tyre Strategy       Lap Pace          Pit Stops             │
│                                                             │
│ Soft                Vettel            1 stop                │
│ Medium              Bottas            1 stop                │
│ Soft                Hamilton          1 stop                │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│                 [ Ask AI About This Race ]                  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

# 👨‍🚀 Driver Dashboard

Each driver will eventually have a dedicated performance page.

Example:

```text
┌─────────────────────────────────────────────────────────────┐
│ SEBASTIAN VETTEL                                             │
│ Ferrari • 2018                                               │
│                                                             │
│ Wins             Podiums          Points                     │
│   5                12              320                       │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│ Race Performance                                             │
│                                                             │
│  █████████████████████                                      │
│                                                             │
│ Qualifying Pace    Race Pace    Consistency                 │
│                                                             │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│ 🤖 Ask PodiumAI                                              │
│                                                             │
│ "Why was Vettel stronger than Räikkönen in 2018?"            │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

# 🔮 What-If Simulator

One of PodiumAI's future flagship features will be an interactive race simulator.

Example:

```text
              WHAT-IF SIMULATOR

Race: Bahrain 2018

Driver: Sebastian Vettel

Current Strategy:
Soft → Medium

Alternative:
Pit 5 laps earlier

          [ RUN SIMULATION ]

                    ↓

┌─────────────────────────────────────────┐
│ SIMULATION RESULT                        │
│                                         │
│ Estimated finishing position             │
│                                         │
│ Current       → P1                      │
│ Alternative   → P2                      │
│                                         │
│ Confidence: 78%                         │
└─────────────────────────────────────────┘
```

These results will be generated using actual historical data and trained models rather than arbitrary AI-generated numbers.

---

# 📈 Data Visualization

PodiumAI will provide interactive visualizations for:

* Lap times
* Race pace
* Position changes
* Tyre strategies
* Stint lengths
* Pit stops
* Sector performance
* Telemetry
* Weather
* Driver comparisons
* Constructor performance
* Championship standings

---

# 🏎️ Data Foundation

PodiumAI will use two major F1 data sources.

## FastF1

FastF1 will provide detailed Formula 1 session information.

Potential data includes:

* Race results
* Practice sessions
* Qualifying
* Sprint sessions
* Lap timing
* Sector times
* Telemetry
* Tyres
* Tyre life
* Pit stops
* Weather
* Track status
* Race control messages
* Session information

FastF1 will be the primary source for detailed race analysis.

---

## Jolpica F1 API

Jolpica will provide structured historical Formula 1 information.

Potential data includes:

* Seasons
* Races
* Circuits
* Drivers
* Constructors
* Race results
* Driver standings
* Constructor standings
* Qualifying results
* Sprint results
* Pit stops

Jolpica will complement FastF1 where appropriate.

---

# 🗂️ Data Architecture

Data will be organized carefully rather than placing everything into a single dataset.

```text
data/
│
├── races/
│
├── drivers/
│
├── constructors/
│
├── circuits/
│
├── results/
│
├── laps/
│
├── telemetry/
│
├── pit_stops/
│
├── weather/
│
└── standings/
```

Each dataset will maintain separation between raw and processed data.

```text
dataset/
├── raw/
└── processed/
```

---

# 📅 Historical Data Strategy

The project will be developed **year-by-year**.

The first target is:

```text
2018
```

After 2018 has been:

* collected
* validated
* processed
* committed

the project will continue with:

```text
2019
2020
2021
2022
2023
2024
2025
2026
```

The project will prioritize **data accuracy and completeness over speed**.

---

# 🔗 Data Relationship

The long-term data model will connect information across multiple levels:

```text
Season
   │
   ▼
Race
   │
   ▼
Session
   │
   ▼
Driver
   │
   ▼
Lap
   │
   ▼
Telemetry
```

This relationship is essential for answering complex questions.

For example:

> "Why did Driver X lose three seconds during this part of the race?"

The system may need to connect:

```text
Race Result
      ↓
Lap Data
      ↓
Sector Data
      ↓
Telemetry
      ↓
Tyre Data
      ↓
Weather
      ↓
Race Events
      ↓
AI Explanation
```

---

# 🏗️ System Architecture

```text
                         USER
                           │
                           ▼
                  ┌─────────────────┐
                  │  React Web App  │
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │   FastAPI API   │
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │   Master Agent  │
                  └────────┬────────┘
                           │
          ┌────────────────┼────────────────┐
          │                │                │
          ▼                ▼                ▼
      Race Data        Strategy        Prediction
        Agent            Agent            Agent
          │                │                │
          └────────────────┼────────────────┘
                           │
          ┌────────────────┼────────────────┐
          │                │                │
          ▼                ▼                ▼
      Weather          Events          Simulation
        Agent            Agent            Agent
          │                │                │
          └────────────────┼────────────────┘
                           │
                           ▼
                    F1 Knowledge/RAG
                           │
                           ▼
                    Explanation Agent
                           │
                           ▼
                         USER
```

---

# 🛠️ Technology Stack

## Frontend

* React
* Vite
* TypeScript
* Tailwind CSS
* Headless UI
* Motion

## Backend

* Python
* FastAPI

## Data

* FastF1
* Jolpica F1 API
* Pandas
* NumPy

## Machine Learning

* Scikit-learn
* Future ML frameworks as required

## Visualization

* Plotly
* Recharts
* D3.js

## AI

* Large Language Models
* RAG
* Multi-Agent Architecture
* Tool-based AI workflows

## Development

* Git
* GitHub
* Jupyter Notebooks

---

# 📁 Planned Repository Structure

```text
PodiumAI/
│
├── data/
│
├── notebooks/
│
├── src/
│   ├── data/
│   ├── features/
│   ├── models/
│   ├── analysis/
│   └── agents/
│
├── backend/
│
├── frontend/
│
├── tests/
│
├── docs/
│
├── requirements.txt
├── .gitignore
└── README.md
```

---

# 🔬 Potential Analytics

PodiumAI can eventually investigate questions such as:

* How strongly does qualifying position influence race finishing position?
* Which drivers are most consistent?
* Which teams manage tyres most effectively?
* How does tyre degradation affect race pace?
* How does weather influence performance?
* Which circuits produce the largest performance differences?
* How effective are undercuts and overcuts?
* How do drivers perform against teammates?
* What factors contribute most to race wins?
* Can historical data predict race outcomes?

---

# 🎯 Development Roadmap

## Phase 1 — Project Foundation

* [ ] Create PodiumAI repository
* [ ] Set up project structure
* [ ] Set up Python environment
* [ ] Explore FastF1
* [ ] Explore Jolpica
* [ ] Define initial schemas

---

## Phase 2 — 2018 Data Foundation

* [ ] Collect 2018 race information
* [ ] Collect 2018 race results
* [ ] Validate all 2018 rounds
* [ ] Create raw dataset
* [ ] Create processed dataset
* [ ] Check duplicates
* [ ] Check missing values
* [ ] Commit 2018 data to `main`

---

## Phase 3 — Detailed 2018 FastF1 Data

After race results are stable:

* [ ] Add lap data
* [ ] Add sector data
* [ ] Add tyre data
* [ ] Add pit-stop information
* [ ] Add weather
* [ ] Add telemetry
* [ ] Add race events
* [ ] Connect datasets to 2018 races

---

## Phase 4 — Historical Expansion

Expand the same validated structure year-by-year:

```text
2018 → 2019 → 2020 → 2021 → 2022 → 2023 → 2024 → 2025 → 2026
```

---

## Phase 5 — Data Analysis

* [ ] Exploratory data analysis
* [ ] Driver comparisons
* [ ] Race pace analysis
* [ ] Tyre analysis
* [ ] Strategy analysis
* [ ] Weather analysis
* [ ] Performance metrics

---

## Phase 6 — Machine Learning

* [ ] Feature engineering
* [ ] Baseline models
* [ ] Race prediction
* [ ] Driver performance models
* [ ] Strategy models
* [ ] Model evaluation
* [ ] Explainability

---

## Phase 7 — Multi-Agent AI

* [ ] Master Agent
* [ ] Race Data Agent
* [ ] Strategy Agent
* [ ] Prediction Agent
* [ ] Weather Agent
* [ ] Event Agent
* [ ] F1 Knowledge/RAG Agent
* [ ] Explanation Agent
* [ ] Simulation Agent

---

## Phase 8 — Web Application

* [ ] React frontend
* [ ] FastAPI backend
* [ ] AI chat interface
* [ ] Race explorer
* [ ] Driver dashboards
* [ ] Constructor dashboards
* [ ] Circuit pages
* [ ] Interactive visualizations
* [ ] Agent activity interface

---

## Phase 9 — Simulation & Advanced Intelligence

* [ ] What-if simulations
* [ ] Strategy simulation
* [ ] Race outcome scenarios
* [ ] Advanced predictions
* [ ] AI-powered race explanations

---

# ⚠️ Development Principles

PodiumAI will prioritize:

### Accuracy over speed

Datasets will be validated before being used downstream.

### Year-by-year development

We will not attempt to download and process the entire historical dataset at once.

### Raw data preservation

Original downloaded data will be kept separate from processed data.

### Reproducibility

Data pipelines should be repeatable and understandable.

### Modular architecture

Agents, datasets, models, and application components should remain independent and reusable.

### Data-grounded AI

The AI should use actual F1 data when answering data-related questions.

### No fabricated analytics

Predictions and simulations should be based on trained models and measurable data rather than invented statistics.

---

# 📌 Current Status

**Project Stage: Foundation**

The project is starting from a clean repository.

Current focus:

```text
PodiumAI
   │
   ▼
FastF1 Exploration
   │
   ▼
2018 Race Results
   │
   ▼
Validation
   │
   ▼
Commit to main
```

The AI agents, machine learning, simulations, and frontend will be built **after the underlying data foundation is reliable**.

---

# 🏆 Long-Term Goal

PodiumAI aims to become an intelligent Formula 1 companion where users can move beyond traditional statistics.

Instead of simply asking:

> **"Who won the race?"**

users should eventually be able to ask:

> **"Why did they win?"**

> **"What caused the performance difference?"**

> **"Which strategy was better?"**

> **"What would have happened if the strategy changed?"**

And PodiumAI should be able to investigate the data, coordinate specialized AI agents, analyze the evidence, and explain the answer.

---

# 🏁 PodiumAI

### **Ask F1. Analyze the race. Understand the podium.**

Built with **FastF1 + Jolpica + Machine Learning + Multi-Agent AI**.
