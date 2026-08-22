🚀 GuardianOS: AI Employee Command Center

A Governed Multi-Agent AI Employee for People Operations

Detect risks. Understand context. Coordinate AI operators. Take safe
action with human control.

------------------------------------------------------------------------

🧠 What is GuardianOS?

GuardianOS is not another HR dashboard and not another chatbot.

It is a governed AI employee that continuously analyzes People
Operations workflows, detects hidden risks, coordinates specialized AI
operators, and prepares safe interventions with human approval.

GuardianOS creates a complete operational intelligence loop:

                     Evidence
                        |
                        v
              AI Specialist Operators
                        |
                        v
                Policy Evaluation
                        |
                        v
              Human Approval Layer
                        |
                        v
              Safe Operational Action
                        |
                        v
                  Audit Trail

------------------------------------------------------------------------

🎯 The Problem

Modern organizations have employee information scattered across multiple
systems.

  System       Hidden Problem
  ------------ ------------------------------------
  Onboarding   Employees blocked by missing tasks
  IT Access    Delayed laptop, VPN, email access
  Compliance   Missing mandatory requirements
  Payroll      Incorrect or incomplete records
  Managers     Missed follow-ups
  Engagement   Early warning signals ignored

The problem is simple:

  Companies have data everywhere, but no intelligent system connecting
  the signals together.

------------------------------------------------------------------------

💡 The GuardianOS Solution

GuardianOS acts as an AI teammate for People Operations.

It combines:

✅ Data validation
✅ Multi-agent reasoning
✅ Policy-based decisions
✅ Human approval workflows
✅ Safe external actions
✅ Complete audit history

------------------------------------------------------------------------

🏗️ AI Employee Architecture

GuardianOS uses one AI employee composed of specialized operators.

    flowchart LR

    A["HR Data Sources<br/>Supabase + CSV"] --> B["AI Employee Orchestrator"]

    B --> C["Data Quality Operator"]

    B --> D["Onboarding & Access Operator"]

    B --> E["Engagement & Confidentiality Operator"]

    C --> F["Evidence Validation"]
    D --> F
    E --> F

    F --> G["Risk & Policy Engine"]

    G -->|Green| H["No Action"]

    G -->|Amber| I["Human Review"]

    G -->|Red / Confidential| J["Restricted Workbench"]

    I --> K["Approved Slack + Asana Action"]

    J --> L["Audit Trail"]

    K --> L
    H --> L

------------------------------------------------------------------------

🤖 AI Operator System

  -----------------------------------------------------------------------
  AI Operator                         Responsibility
  ----------------------------------- -----------------------------------
  HR Data Quality Operator            Validates employee records,
                                      lifecycle stages, ownership, and
                                      data completeness

  Onboarding & Access Operator        Checks onboarding progress against
                                      access evidence

  Engagement & Confidentiality        Detects engagement risks while
  Operator                            protecting sensitive information

  Risk & Policy Operator              Applies governance rules and
                                      determines case routing

  Intervention Operator               Creates approved actions and
                                      records outcomes
  -----------------------------------------------------------------------

------------------------------------------------------------------------

⚙️ System Architecture

    flowchart TB

    Frontend["Next.js Command Center"]

    Backend["FastAPI Backend"]

    AI["AI Employee Layer"]

    Policy["Policy Engine"]

    Database["Supabase Database"]

    Workflow["Supervity AI Workflow"]

    Slack["Slack"]

    Asana["Asana"]

    Frontend --> Backend

    Backend --> AI

    Database --> AI

    AI --> Workflow

    AI --> Policy

    Policy --> Backend

    Backend --> Slack

    Backend --> Asana

------------------------------------------------------------------------

🖥️ Product Experience

📊 Command Dashboard

Provides:

  Feature              Purpose
  -------------------- --------------------------------
  Workforce Overview   Understand operational health
  Risk Routes          View Green / Amber / Red cases
  Operator Status      Monitor AI activity
  Audit Timeline       Track decisions

------------------------------------------------------------------------

🛠️ AI Workbench

A human decision center for:

-   🟡 Amber cases
-   🔴 Red cases
-   🔒 Confidential cases
-   ⚠️ Data quality issues

Humans remain responsible for important decisions.

------------------------------------------------------------------------

📜 AI Policy Engine

Controls:

  Policy           Example
  ---------------- ---------------------------------------
  Risk Threshold   When escalation happens
  Approval Rules   When humans must review
  Privacy Rules    What information can leave the system

------------------------------------------------------------------------

🔎 Data Manager

Provides visibility into:

-   Data sources
-   Data lineage
-   Computed signals
-   Operational records

------------------------------------------------------------------------

💬 AI Manager

Ask questions like:

  “Why is this employee considered high risk?”

  “Which department has onboarding problems?”

  “What actions should happen today?”

------------------------------------------------------------------------

🔄 Operational Flow

    flowchart LR

    A["Employee Data"]

    B["Validation"]

    C["AI Analysis"]

    D["Risk Scoring"]

    E["Policy Decision"]

    F["Human Approval"]

    G["Action"]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
    F --> G

------------------------------------------------------------------------

🔐 Governance & Safety

GuardianOS is designed for responsible AI operations.

  Risk Type         System Behavior
  ----------------- -------------------------
  🟢 Green          Record outcome
  🟡 Amber          Human approval required
  🔴 Red            Restricted review
  🔒 Confidential   Internal only
  ⚠️ Data Quality   Fix before decision

------------------------------------------------------------------------

🔌 Integrations

    flowchart LR

    GuardianOS["GuardianOS"]

    GuardianOS --> Supabase["Supabase"]

    GuardianOS --> Supervity["Supervity Auto"]

    GuardianOS --> Slack["Slack"]

    GuardianOS --> Asana["Asana"]

------------------------------------------------------------------------

🧬 Data Architecture

GuardianOS processes:

  Data Source            Purpose
  ---------------------- ----------------------
  Workers                Employee lifecycle
  Onboarding Tasks       Progress tracking
  Provisioning Records   Access verification
  Engagement Records     Operational signals
  Manager Directory      Ownership validation
  Compliance Items       Requirement tracking
  Payroll Records        Process validation
  Learning Milestones    Development tracking

------------------------------------------------------------------------

🛠️ Technology Stack

  Layer             Technology
  ----------------- -------------------------------------------
  Frontend          Next.js + TypeScript
  Backend           FastAPI + Python
  AI                Multi-Agent Orchestration + LLM Reasoning
  Database          Supabase
  Workflow Engine   Supervity Auto
  Deployment        Vercel + Docker

------------------------------------------------------------------------

🌐 Live Demo

Frontend

https://day90-guardian-command-center-ui.vercel.app/

Backend

https://day90-guardian-api-git-main-waseem-mushtaqs-projects.vercel.app/api/health

------------------------------------------------------------------------

🚀 Running Locally

Requirements

-   Docker Desktop
-   Git
-   Node.js
-   Python

Start

    docker compose up --build -d

Open

Frontend:

    http://127.0.0.1:3001

API:

    http://127.0.0.1:8001/api/docs

------------------------------------------------------------------------

🔮 Vision

GuardianOS explores the future of AI employees.

The goal is not replacing People Operations teams.

The goal is building AI teammates that:

-   understand context
-   follow governance rules
-   explain decisions
-   help humans act faster

------------------------------------------------------------------------

⭐ Built for the AI Builders Hackathon

GuardianOS demonstrates how autonomous AI agents can work inside real
operational workflows while keeping humans in control.
