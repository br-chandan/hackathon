## HACKATHON OVERVIEW

This hackathon focuses on designing and implementing a **multi-agent, automated AI system** capable of performing structured, multi-stage tasks reliably and with minimal human intervention. The event challenges participants to combine **LLM intelligence**, **agent orchestration frameworks**, and **automation platforms** to build an end-to-end workflow that can operate autonomously.

---

## Core Theme

Participants must build a **coordinated multi-agent workflow** that can perform tasks in sequential stages such as:

• Researching or analyzing a given brief
• Generating structured outputs (e.g., problems, content, MCQs)
• Solving or interpreting the outputs
• Validating correctness
• Iterating until the results meet defined quality criteria
• Publishing or exporting the final results automatically

The system should function like an “AI assembly line,” with each agent handling one specialized function.

---

## Key Requirements

1. **Use of Multi-Agent Architecture**
   The hackathon emphasizes decomposing the system into multiple independent agents (e.g., a research agent, a generator agent, a solver agent, a validator agent). Each agent must have a clearly defined role, input/output formats, and deterministic behavior.

2. **Structured and Verifiable Outputs**
   Outputs must follow strict formats such as JSON or structured objects.
   These will later be validated programmatically, so consistency is critical.

3. **Reasoning and Error Correction**
   The challenge includes situations where LLMs typically fail: arithmetic, logical consistency, multi-step reasoning, or conflicting outputs.
   Participants must design a system that can detect mistakes and automatically correct or retry.

4. **Orchestration and Workflow Automation**
   The system must incorporate some form of orchestration using tools like:
   • LangChain (agents, chains, tools)
   • LangGraph (state management, branching logic, retries)
   • n8n as an automation layer for integration and external workflows

5. **Automatic Publishing or Deployment**
   Final validated outputs are expected to be automatically exported to a downstream medium such as:
   • Google Sheets
   • Google Forms
   • JSON/HTML dashboards
   • External APIs
   • GitHub repositories
   n8n may be used to implement this publishing layer.

6. **Reliability Under Stress**
   The system must be robust enough to handle deliberate ambiguity and edge cases in the tasks.
   It should not rely on a single LLM call but should use agent loops, validators, or watchers to maintain correctness.

---

## Expected Deliverables

Teams are typically required to deliver:
• A working multi-agent pipeline
• A clear explanation of each agent and its role
• Structured outputs demonstrating the system’s correctness
• Evidence of validation and retry logic
• A final published result via Sheets/Forms or another integration
• Optional UI, API, or automation flows (e.g., via n8n)

---

## Overall Objective

The goal of the hackathon is to push participants to think beyond single-model prompts and instead design **system-level AI architectures** that combine:

• Agent decomposition
• Multi-stage processing
• Automated validation loops
• External integrations
• Real-world automation

It evaluates the participant’s ability to combine **systems engineering**, **automation tools**, and **LLM orchestration** to produce a fully autonomous, reliable AI workflow.

