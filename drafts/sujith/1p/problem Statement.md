🚀 Challenge Title:

# THE SELF-VALIDATING QUANT WORD-PROBLEM GENERATOR & DEPLOYER

## MISSION OBJECTIVE

Build a multi-agent system that can autonomously:
1. Research how to design valid and solvable quantitative word problems
2. Generate original MCQ-based quant questions (story-based problems)
3. Self-validate each question using two independent solver agents
4. Reject and regenerate hallucinated or mathematically invalid questions
5. Auto-create a Google Form (or mock quiz) containing the validated questions
6. Produce an accuracy report showing validation performance
Your final system should behave like a real autonomous assessment generator.

## THE TYPE OF QUESTIONS YOU MUST GENERATE

You are required to generate Quantitative Word Problems, not numerical puzzles.

These are everyday scenario-based questions like:
Examples:

* Two trains starting from different stations, moving at different speeds, meeting time, crossing time, etc.
A worker completing a job alone vs with another worker (work & time).
Two pipes filling or emptying a tank with different flow rates (pipes & cisterns).
Profit, loss, discount situations in business transactions.
Ratios & mixtures, like mixing liquids or sharing money.
Distance-time-speed movement scenarios involving buses, bikes, runners, boats.
Age problems, where relationships across years are described in words.
These questions require:
Word comprehension → math model → correct calculation
Multiple steps of reasoning
Almost always produce LLM hallucinations or arithmetic mistakes
Are not easily copy-paste solvable
# 🚀 The Self-Validating Quant Word-Problem Generator & Deployer

## Mission objective

Build a multi-agent system that can autonomously:

1. Research how to design valid and solvable quantitative word problems.
2. Generate original MCQ-based quantitative questions (story-based problems).
3. Self-validate each question using two independent solver agents.
4. Reject and regenerate hallucinated or mathematically invalid questions.
5. Auto-create a Google Form (or a mock quiz) containing the validated questions.
6. Produce an accuracy report showing validation performance.

The final system should behave like a real autonomous assessment generator.

## The type of questions to generate

You must generate quantitative word problems (not numerical puzzles). These are everyday scenario-based questions such as:

- Two trains starting from different stations (meeting time, crossing time, etc.).
- Work & time problems (worker completes job alone vs with another worker).
- Pipes & cisterns (filling/emptying a tank with different flow rates).
- Profit, loss, and discount situations.
- Ratios & mixtures (mixing liquids, sharing money).
- Distance–time–speed scenarios (buses, bikes, runners, boats).
- Age problems (relationships across years described in words).

These questions require:

- Converting word comprehension into a math model.
- Multiple steps of reasoning.
- Careful unit handling and arithmetic accuracy.

Generative models commonly hallucinate or make arithmetic mistakes on such problems; this challenge is intended to force agentic system design to overcome those weaknesses.

## Why this challenge

Generative AI struggles with:

- Multi-step arithmetic
- Converting story → algebra
- Keeping units consistent
- Ensuring MCQ options align with the correct solution
- Preventing hidden contradictions
- Ensuring answers are physically and mathematically possible

Your task is to build agents that research, reason, generate, validate, and deploy high-quality quant questions.

## Mandatory agent architecture

The system must contain the following agents.

### 1. Research Agent

Responsibilities:

- Study resources on time–speed–distance, work & time, ratio/mixtures, profit/loss and common traps.
- Study LLM hallucination patterns and common arithmetic errors.

Output: a structured document titled **Quant Problem Design Rules** containing:

- Valid pattern templates
- Correct formula sets
- Criteria to avoid impossible scenarios
- Steps to ensure MCQ correctness

### 2. Problem Generator Agent

Responsibilities:

- Use the design rules to create story-based quantitative questions.
- Produce for each question: a realistic story prompt, 4 MCQ options, one correct answer, and a hidden step-by-step derivation (for validation).

Mandatory coverage: the generator must produce questions across at least three of the following domains:

- Time, Speed & Distance
- Work & Time
- Pipes & Cisterns
- Profit & Loss
- Mixtures & Ratio
- Age-Based Problems

### 3. Solver Agent A

Responsibilities:

- Independently solve each generated problem.
- Output the modeled equation, step-by-step reasoning, final answer and confidence estimate.

### 4. Solver Agent B

Responsibilities:

- Solve the same question with a different method (e.g., reverse approach, brute-force numeric substitution, unit-based reasoning, or logical reasoning instead of pure algebra).
- Output answer and explanation.

### 5. Orchestrator Agent (Controller)

Responsibilities:

- Coordinate prompts between agents.
- Compare solver outputs, run reject/regenerate loops, and publish validated problems.
- Produce final accuracy statistics and reports.

## Validation rules (strict)

A quant question is VALID only if all of the following hold:

1. Solver A and Solver B compute the same numeric answer.
2. Both explanations follow mathematical rules with no contradictions.
3. The generated MCQ contains the correct answer.
4. No impossible/impractical scenario is created (e.g., negative time or distance, physically infeasible flows).
5. The generator's reasoning chain does not contradict solver reasoning.
6. Story text is mathematically meaningful (no randomly invented infeasible parameters).

If any rule fails: the question must be rejected and regenerated.

## Required final deliverables

1. Research summary — output of Research Agent describing formulas, patterns and design rules.
2. Validated quant problem bank — 10–12 validated word problems covering a minimum of 3 domains.
3. Accuracy report including total generated, invalid cases, regenerations, final acceptance rate (%), and optional solver-agreement visuals.
4. Published quiz — Google Form or an HTML quiz auto-generated by the Orchestrator.
5. A 5-minute live demo showcasing the agent workflow, real-time validation, the quiz, and accuracy stats.

## Judging criteria (100 points)

- Agentic architecture & reasoning — 25
- Quality of generated quant questions — 20
- Solver reliability & agreement logic — 20
- Deployment (Google Form / Quiz) — 15
- Accuracy report & transparency — 10
- Demo & presentation — 10

### Bonus (+10 points)

Optional features that can earn bonus points:

- Difficulty classifier (Easy / Medium / Hard)
- Equation visualizer
- Duplicate-problem detector
- Error heatmap of hallucination types
- A third solver agent for adversarial testing

## The HydraHacks spirit

Learn the foundations → build intelligent agents → compete to produce the most robust autonomous system.

Welcome to HydraHacks 2025 — good luck, Hydra Builders. May your agents never hallucinate.

---

## Terms & Conditions — HydraHacks 2025

By participating, teams and participants agree to the following.

### 1. Evaluation & ranking

1. All submissions will be evaluated independently by three qualified evaluators.
2. Each evaluator will score teams using the official rubric; aggregate scores determine rankings.
3. In case of ties, the organizing committee may conduct an additional Q&A or weighted tie-break.
4. Evaluators' and organizers' decisions are final.

### 2. Intellectual property & usage rights

1. Participants retain rights to their code, ideas, and pipeline designs.
2. By entering, participants grant Certisured and BuilderThinking.com a perpetual, royalty-free, non-exclusive license to use, reproduce, modify, or adapt any part of the submitted solution for educational, research, or commercial purposes.
3. Participants waive exclusive ownership claims that prevent sponsors from using submitted concepts.
4. Participants may continue to use, expand, publish, or commercialize their solutions.
5. Sponsors will not claim ownership over participants' future work derived from the hackathon project.
6. Do not include confidential information in submissions; assume entries are for open educational use.

### 3. Use of tools & external resources

1. Teams may use public LLM tools, libraries, templates, and open-source assets, provided licensing terms are followed.
2. Use of pirated or unauthorized paid libraries or stolen datasets is prohibited.
3. Plagiarism (code, text, or design) may result in disqualification.

### 4. Team conduct & fair use

1. Teams must work independently; external help is restricted to permitted mentorship.
2. Attempts to manipulate scores, evaluation scripts, or logs will result in disqualification.
3. Teams must ensure demos are reproducible and runnable using the provided orchestrator workflow.

### 5. Submission requirements

1. All teams must submit: research summary, validated question bank, accuracy report, quiz (Google Form or HTML/JSON), and a working code repository.
2. Submissions must be complete and runnable; broken/incomplete pipelines may be penalized.
3. Late submissions may be penalized or rejected unless allowed by organizers.

### 6. Privacy, photos & media

1. By participating, teams agree event photos, videos, and demos may be recorded and used for promotions and archives.
2. Sponsors and organizers may use recorded materials for educational or promotional purposes.
3. Participants waive claims to compensation for such usage.

### 7. Safety, ethics & academic integrity

1. All solutions must follow ethical AI principles.
2. Submissions must not include harmful, discriminatory, or unsafe content.
3. Malicious code or attempts to breach systems will lead to removal from the event.

### 8. Acceptance of terms

By registering and participating, each team acknowledges they have read, understood, and agreed to these terms and conditions.
