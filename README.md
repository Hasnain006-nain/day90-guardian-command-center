Day90 Guardian Command Center

Governed AI Employee for People Operations

Day90 Guardian helps People Ops teams identify onboarding, access,
compliance, payroll, manager-follow-up, and engagement risks before they
become operational problems.

It is not just a dashboard. It is a governed AI command center with:

-   Policy gates
-   Human review queues
-   Audit trails
-   AI specialist operators
-   Secure Slack and Asana workflows

  One AI employee, not five disconnected automations.

  Day90 Guardian validates evidence, coordinates specialist operators,
  applies explicit policies, and keeps humans accountable for important
  decisions.

------------------------------------------------------------------------

What Problem It Solves

The first 90 days of employment involve many connected processes:

-   Employee onboarding
-   Access provisioning
-   Compliance requirements
-   Payroll checks
-   Manager follow-ups
-   Learning milestones
-   Engagement signals

These signals are usually distributed across different systems.

Humans often discover problems too late because each system only shows
one part of the employee journey.

Day90 Guardian creates one governed workflow:

1.  Validate whether employee data is complete and reliable.
2.  Reconcile onboarding tasks with access evidence.
3.  Protect confidential engagement information.
4.  Apply People Ops policies.
5.  Route cases through human review.
6.  Create safe operational actions.

------------------------------------------------------------------------

Why Day90 Guardian Is Different

Most operational dashboards only report problems.

Day90 Guardian creates an accountable AI operating loop:

    Evidence
        ↓
    Specialist AI Operators
        ↓
    Policy Decision
        ↓
    Human Approval
        ↓
    Safe Action
        ↓
    Audit Trail

The system does not blindly automate sensitive decisions.

Examples:

  Situation                       Guardian Behavior
  ------------------------------- -----------------------------------
  Missing laptop access           Creates safe remediation workflow
  Confidential employee concern   Keeps information restricted
  Missing ownership data          Stops and requests correction
  Operational delay               Routes to the correct reviewer

------------------------------------------------------------------------

Core Product Surfaces

Dashboard

Executive command view showing:

-   Workforce health
-   Risk routes
-   Operator activity
-   Integrations
-   Audit history

Workbench

Human review environment for:

-   Amber cases
-   Red cases
-   Confidential cases
-   Data quality issues

AI Policies

Governance layer controlling:

-   Routing rules
-   Risk thresholds
-   Approval requirements

AI Insights

Provides:

-   Operational patterns
-   Bottlenecks
-   Anomalies
-   Recommended actions

Data Manager

Provides transparency into:

-   Source systems
-   Data lineage
-   Computed signals

AI Manager

Conversational control layer for understanding:

-   Current risks
-   Policies
-   Operational status
-   Recommended actions

------------------------------------------------------------------------

AI Employee Architecture

Day90 Guardian is modeled as one orchestrated AI employee made from
specialized operators.

AI Operators

  -----------------------------------------------------------------------
  Operator                            Responsibility
  ----------------------------------- -----------------------------------
  HR Data Quality and Lifecycle       Validates worker records, lifecycle
  Operator                            stages, manager references,
                                      locations, and data completeness

  Onboarding Task and Access          Compares onboarding status with
  Reconciliation Operator             laptop, badge, VPN, email, and
                                      system access evidence

  Engagement and Confidentiality      Detects engagement signals while
  Guard Operator                      protecting confidential information

  Retention Risk and Policy           Applies policies and routes cases
  Evaluation Operator                 into Green, Amber, Red,
                                      Confidential, or Data Quality

  Intervention Execution and Outcome  Creates approved Slack/Asana
  Operator                            interventions and records outcomes
  -----------------------------------------------------------------------

------------------------------------------------------------------------

Architecture Flow

    flowchart LR

    A["Supabase HR records<br/>CSV fallback"] --> B["Data Quality & Lifecycle"]

    B --> C["Onboarding & Access<br/>parallel"]

    B --> D["Engagement & Confidentiality<br/>parallel"]

    C --> E["Evidence fan-in"]

    D --> E

    E --> F["Retention Risk & Policy"]

    F -->|"Amber"| G["Human review + safe intervention"]

    F -->|"Red / Confidential / Data Quality"| H["Restricted Workbench gate"]

    G --> I["Masked Slack notice<br/>Assigned Asana task"]

    H --> J["Decision and audit trail"]

    I --> J

------------------------------------------------------------------------

Data Model

Day90 Guardian computes signals from:

  Data Source               Purpose
  ------------------------- ---------------------------
  Workers                   Employee lifecycle
  Onboarding Tasks          Progress tracking
  Provisioning Records      Access verification
  Engagement Records        Operational signals
  Manager Directory         Ownership validation
  Locations                 Organization context
  Compliance Items          Requirement tracking
  Payroll Records           Process validation
  Learning Milestones       Development tracking
  Attrition Context         Risk analysis
  Cross-team Dependencies   Operational relationships

Primary source:

    Supabase

Controlled fallback:

    CSV Dataset

------------------------------------------------------------------------

Governance and Privacy

Day90 Guardian intentionally avoids unsafe automation.

Safety Rules

-   Confidential information is protected.
-   Red and confidential cases require human review.
-   Unsafe data joins stop automation.
-   External actions only happen after approval.
-   Decisions are recorded.

Risk Routing

  Route          System Behavior                External Visibility
  -------------- ------------------------------ ------------------------
  Green          Safe outcome recorded          None
  Amber          Human approval before action   Safe summary only
  Red            Restricted review              Restricted access only
  Confidential   Internal handling              No external action
  Data Quality   Fix data before decision       No action

------------------------------------------------------------------------

Integrations

Configured integrations:

  Integration      Purpose
  ---------------- ---------------------------
  Supabase         Operational data source
  Supervity Auto   AI workflow orchestration
  Slack            Masked notifications
  Asana            Reviewer tasks

------------------------------------------------------------------------

Technical Architecture

Backend

-   FastAPI
-   Python

Frontend

-   Next.js
-   TypeScript

AI Layer

-   Multi-agent orchestration
-   LLM reasoning
-   Policy-based workflows
-   Human-in-the-loop AI

Infrastructure

-   Docker
-   Supabase
-   Vercel

------------------------------------------------------------------------

API Endpoints

  Endpoint                                  Purpose
  ----------------------------------------- ----------------------------
  GET /api/day90/dashboard                  Main command center data
  GET /api/day90/data-profile               Source lineage and signals
  GET /api/day90/workbench                  Human review cases
  POST /api/day90/runs/trigger              Start AI workflow
  POST /api/day90/operators/{key}/trigger   Trigger operator
  POST /api/day90/workbench/{id}/decision   Approve or reject action
  GET /api/day90/integrations               Integration status
  GET /api/day90/policies                   Active policies

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

Open:

Frontend:

    http://127.0.0.1:3001

API:

    http://127.0.0.1:8001/api/docs

------------------------------------------------------------------------

Security

Production requirements:

-   Keep secrets in environment variables.
-   Never commit .env.
-   Use approval gates before external actions.
-   Protect confidential cases.
-   Maintain audit history.

------------------------------------------------------------------------

Vision

Day90 Guardian explores how AI employees can become reliable operational
teammates.

The goal is not replacing People Ops teams.

The goal is building AI systems that understand context, follow rules,
explain decisions, and help humans make better decisions.
