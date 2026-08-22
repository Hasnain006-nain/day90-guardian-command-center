GuardianOS: AI Employee Command Center

Governed AI Employee for People Operations

GuardianOS is an autonomous AI employee that helps People Operations
teams detect workforce risks, analyze operational signals, coordinate
specialized AI operators, and execute safe actions with human approval.

GuardianOS is not a simple dashboard or chatbot. It is a governed AI
operating system with:

-   Multi-agent orchestration
-   Policy-based decision making
-   Human-in-the-loop approval
-   Explainable recommendations
-   Audit trails
-   Secure Slack and Asana workflows

  One AI employee, not five disconnected automations.

------------------------------------------------------------------------

Problem

Modern organizations have employee information distributed across:

-   Employee records
-   Onboarding tasks
-   Access provisioning
-   Compliance systems
-   Payroll workflows
-   Manager follow-ups
-   Learning milestones
-   Engagement signals

Each system only shows part of the employee journey.

GuardianOS creates a complete operational loop:

Evidence → AI Analysis → Policy Decision → Human Approval → Safe Action
→ Audit Trail

------------------------------------------------------------------------

AI Employee Architecture

GuardianOS is built as one AI employee composed of specialized
operators.

    flowchart LR

    A["HR Data Sources<br/>Supabase + CSV"] --> B["AI Employee Orchestrator"]

    B --> C["Data Quality Operator"]

    B --> D["Onboarding & Access Operator"]

    B --> E["Engagement & Confidentiality Operator"]

    C --> F["Evidence Validation"]

    D --> F

    E --> F

    F --> G["Risk & Policy Evaluation"]

    G -->|Green| H["No Action"]

    G -->|Amber| I["Human Review"]

    G -->|Red / Confidential| J["Restricted Workbench"]

    I --> K["Approved Slack + Asana Action"]

    J --> L["Audit Trail"]

    K --> L

    H --> L

------------------------------------------------------------------------

AI Operators

  -----------------------------------------------------------------------
  Operator                            Responsibility
  ----------------------------------- -----------------------------------
  HR Data Quality Operator            Validates employee records,
                                      lifecycle stage, ownership, and
                                      data completeness

  Onboarding & Access Operator        Reconciles onboarding tasks with
                                      system access evidence

  Engagement & Confidentiality        Detects engagement signals while
  Operator                            protecting confidential information

  Risk & Policy Operator              Applies governance rules and
                                      determines routing

  Intervention Operator               Creates approved operational
                                      actions and records outcomes
  -----------------------------------------------------------------------

------------------------------------------------------------------------

System Architecture

    flowchart TB

    Frontend["Next.js Command Center"]

    Backend["FastAPI Backend"]

    Agents["AI Employee Orchestration Layer"]

    Policy["Policy Engine"]

    Database["Supabase"]

    Fallback["CSV Dataset"]

    Supervity["Supervity AI Workflow"]

    Slack["Slack"]

    Asana["Asana"]

    Frontend --> Backend

    Backend --> Agents

    Database --> Agents

    Fallback --> Agents

    Agents --> Supervity

    Agents --> Policy

    Policy --> Backend

    Backend --> Slack

    Backend --> Asana

------------------------------------------------------------------------

Data Architecture

    flowchart LR

    A["HR Data Sources"]

    B["Data Validation"]

    C["AI Specialist Operators"]

    D["Risk Calculation"]

    E["Policy Engine"]

    F["Human Approval"]

    G["Operational Action"]

    A --> B

    B --> C

    C --> D

    D --> E

    E --> F

    F --> G

Data sources include:

-   Workers
-   Onboarding tasks
-   Provisioning records
-   Engagement records
-   Manager directory
-   Locations
-   Compliance items
-   Payroll records
-   Learning milestones
-   Attrition context
-   Cross-team dependencies

------------------------------------------------------------------------

Governance and Safety

GuardianOS avoids unsafe automation.

    flowchart LR

    Case["Detected Case"]

    Case --> Decision{"Risk Classification"}

    Decision --> Green["Green<br/>No Action"]

    Decision --> Amber["Amber<br/>Human Approval"]

    Decision --> Red["Red<br/>Restricted Review"]

    Decision --> Confidential["Confidential<br/>Internal Only"]

    Decision --> Data["Data Quality<br/>Fix Required"]

Rules:

-   Confidential information remains protected
-   Sensitive cases require human approval
-   External actions require approval
-   Decisions are recorded
-   Unsafe data conditions stop automation

------------------------------------------------------------------------

Product Features

Dashboard

-   Workforce health
-   Risk routes
-   Operator status
-   Integration status
-   Audit history

AI Workbench

Human review center for:

-   Amber cases
-   Red cases
-   Confidential cases
-   Data quality issues

AI Policies

Controls:

-   Risk thresholds
-   Routing rules
-   Approval requirements

Data Manager

Shows:

-   Source lineage
-   Connected systems
-   Computed signals

AI Manager

Allows users to ask:

-   Why is this employee at risk?
-   Which team has onboarding problems?
-   What action should happen next?
-   What policies are active?

------------------------------------------------------------------------

Integration Architecture

    flowchart LR

    GuardianOS["GuardianOS"]

    GuardianOS --> Supabase["Supabase"]

    GuardianOS --> Supervity["Supervity Auto"]

    GuardianOS --> Slack["Slack"]

    GuardianOS --> Asana["Asana"]

------------------------------------------------------------------------

API Architecture

  Endpoint                                  Purpose
  ----------------------------------------- ---------------------------
  GET /api/day90/dashboard                  Command center metrics
  GET /api/day90/data-profile               Data lineage and signals
  GET /api/day90/workbench                  Human review queue
  POST /api/day90/runs/trigger              Start AI workflow
  POST /api/day90/operators/{key}/trigger   Trigger specific operator
  POST /api/day90/workbench/{id}/decision   Approve or reject action

------------------------------------------------------------------------

Technology Stack

Frontend: - Next.js - TypeScript - React

Backend: - FastAPI - Python

AI: - Multi-agent orchestration - LLM reasoning - Policy-based
workflows - Human-in-the-loop AI

Infrastructure: - Docker - Supabase - Vercel

------------------------------------------------------------------------

Deployment

Frontend:

    Next.js
       |
       v
    Vercel

Backend:

    FastAPI
       |
       v
    Vercel

------------------------------------------------------------------------

Local Development

Requirements:

-   Docker Desktop
-   Git
-   Node.js
-   Python

Run:

    docker compose up --build -d

Frontend:

    http://127.0.0.1:3001

API:

    http://127.0.0.1:8001/api/docs

------------------------------------------------------------------------

Security

Production requirements:

-   Store secrets only in environment variables
-   Never commit .env files
-   Keep approval gates before external actions
-   Protect confidential cases
-   Maintain complete audit records

------------------------------------------------------------------------

Vision

GuardianOS explores how AI employees can become reliable operational
teammates.

The goal is not replacing People Ops teams.

The goal is building AI systems that understand context, follow rules,
and help humans make better decisions.
