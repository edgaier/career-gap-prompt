# Career Gap Analysis: A Prompt System for AI-Assisted Career Planning

A structured sequence of prompts for using an AI assistant to analyze job descriptions, assess your existing experience, identify gaps, and build a development plan grounded in your real work — with courses and certifications added where they actually earn their cost.

Works with any capable AI assistant (Claude, ChatGPT, Gemini, etc.).

---

## What This Is

Most career advice tells you to take courses. This prompt system starts somewhere different: with the work you are already doing and asks how to stretch it toward the roles you want.

The process runs as a single conversation in eight steps. Each prompt builds on the previous one. By the end, you have a gap analysis tied to specific roles, a plan for closing each gap through real projects where possible, and an honest accounting of what certifications and courses are actually worth your time and money.

---

## What You Need Before You Start

1. **Your resume or LinkedIn profile** — plain text is fine. Copy and paste it. Do not worry about formatting.
2. **Two to five job descriptions** for roles you want to work toward. Paste the full text. More is better — patterns across multiple JDs reveal what actually matters versus what is filler.
3. **A list of any personal or work projects** you are currently running or have recently completed. These do not need to be career-relevant yet — the process will find what transfers.
4. **An honest sense of your timeline.** Are you applying now, in six months, or planning for the next one to two years? This shapes everything.

---

## How It Works

A quick orientation before you start. Each step is a separate prompt you paste into the conversation in order.

1. **Input Collection** — Paste your resume and job descriptions. The LLM confirms receipt and does nothing else yet.
2. **Job Description Analysis** — The LLM identifies required skills, groups platform parallels, and summarizes what these roles actually want.
3. **Resume Assessment** — The LLM evaluates what you bring on its own terms, before comparing anything.
4. **Gap Analysis** — Every requirement gets marked Covered, Adjacent, or Missing, with a priority ranking.
5. **Project Discovery** — Your existing projects are mapped to gaps. New projects are recommended for anything not covered.
6. **Certifications and Courses** — Specific credentials are recommended with honest assessments of cost, timing, and whether they are actually required.
7a. **Career Development Plan** — A phased timeline with SMART goals applied to the highest-priority milestones.
7b. **Costs and Open Gaps** — A full cost summary and an honest list of what the plan cannot address.

---

## How To Use This

Start a new conversation with your AI assistant. Send the **Meta-Prompt** first, then paste each numbered prompt in order. Do not skip steps — the analysis in later prompts depends on what was established earlier.

Each prompt is inside a code block. Copy the entire block and paste it as your message. Follow the instructions labeled **[YOUR INPUT]** to add your materials before sending.

**If a response is thin or misses something obvious**, re-prompt before moving on. Do not carry weak output into the next step — each prompt feeds the next. A few patterns that work:

- *"That gap analysis feels incomplete. Look again at [job title] and identify requirements you missed."*
- *"The project recommendations are too generic. I need something specific to [tool or skill]."*
- *"You skipped [X]. Address it before we continue."*

---

## Meta-Prompt

Send this before Prompt 1. It orients the LLM to the full arc and sets the rules for the entire session.

```
I am going to guide you through a structured career gap analysis. The process has eight steps. Here is the sequence:

1. I will paste my resume and job descriptions. You will confirm receipt only — no analysis yet.
2. You will analyze the job descriptions and identify required skills, platform patterns, and what these roles actually want.
3. You will assess my resume on its own terms, before comparing anything.
4. You will compare the two and produce a gap analysis: Covered, Adjacent, or Missing.
5. I will describe my current projects. You will map them to gaps and recommend new ones where needed.
6. You will recommend specific certifications and courses with honest assessments of cost, timing, and whether they are required.
7a. You will produce a phased career development plan with SMART goals for the highest-priority milestones.
7b. You will produce a cost summary and an honest list of what the plan cannot address.

Instructions that apply throughout this entire session:

- If anything in my materials is ambiguous or if missing information would meaningfully change your output, ask me what you need before generating your response. Do not guess.
- Be honest. Do not soften gaps or inflate my qualifications. An accurate picture is more useful than a flattering one.
- If you do not know something — a tool's current pricing, whether a certification is widely recognized, what a specific platform does — say so. Do not invent an answer.

Confirm you understand the process and are ready for step one.
```

---

## Prompt 1 — Input Collection

> **[YOUR INPUT]** Replace the bracketed sections below with your actual materials before sending. Keep the labels so the assistant knows what each block is.

```
You are acting as a career coach and skills analyst. I am going to give you my resume and a set of job descriptions for roles I want to work toward. Do not analyze anything yet. Just confirm that you have received the materials and briefly list what you received: how many job descriptions, the job titles, and the approximate seniority level of my resume based on years of experience.

Here is my resume:
[PASTE YOUR RESUME OR LINKEDIN PROFILE TEXT HERE]

Here are the job descriptions:
[PASTE EACH JOB DESCRIPTION, SEPARATED BY A CLEAR LABEL SUCH AS "--- JOB 1: TITLE ---"]

Wait for my next message before beginning any analysis.
```

---

## Prompt 2 — Job Description Analysis

```
Now analyze the job descriptions I provided — not my resume yet, just the roles.

Do the following:

1. List the hard skills required across all roles (technical tools, platforms, languages, certifications). For each skill, note which roles require it and whether it is listed as required or preferred.

2. List the soft skills and leadership qualities that appear across the roles. Flag any that appear in three or more descriptions — these are likely non-negotiable for this type of work.

3. Identify platform and tool patterns. Where two or more tools serve the same general function (for example, two different CRM platforms, two different data warehouses, two different workflow automation tools), group them and name the underlying skill category they represent. This matters because experience on one platform often transfers to another.

4. Summarize the experience level and context these roles expect. For example: are they hiring individual contributors or managers? Do they expect vendor-side or internal operations experience? Do they want builders, operators, or strategists?

Be specific. If a skill appears in only one JD, say so. Do not inflate the importance of niche requirements.

If you are uncertain about what a tool or platform does, say so rather than guessing.
```

---

## Prompt 3 — Resume and Experience Assessment

```
Now assess my resume. Do not compare it to the job descriptions yet — just evaluate what I bring on its own terms.

Do the following:

1. List the hard skills and platforms that are evident in my experience. Note how recently each was used and at what depth (for example: used as an end user, built with it, managed a team using it, architected a solution with it).

2. Identify the strongest proof points in my resume — the accomplishments, metrics, or projects that would be most credible and compelling to a hiring manager in the types of roles I shared.

3. Identify the experience context I come from. For example: vendor-side or client-side, individual contributor or manager, technical or strategic, internal operations or external-facing. This context matters when evaluating fit for the target roles.

4. Note anything that appears to be missing from my resume that a hiring manager would reasonably expect to see given my seniority and field. Flag it as an absence, not a gap — I may have the experience but simply not have documented it.

If something in my resume is ambiguous, ask me to clarify before drawing conclusions. Do not assume skills I did not document.
```

---

## Prompt 4 — Gap Analysis

```
Now compare my resume to the job descriptions and produce a structured gap analysis.

For each skill, platform, or experience type identified in the job descriptions, do one of the following:

- Mark it COVERED if my resume demonstrates it clearly.
- Mark it ADJACENT if I have related experience that transfers but is not an exact match. Name the parallel specifically (for example: "Databricks experience is adjacent to Snowflake — same data warehouse paradigm, different platform").
- Mark it MISSING if there is no evidence of it in my resume and no close parallel.

Then produce two outputs:

1. A gap table with columns: Skill or Requirement | Roles That Require It | Status (Covered / Adjacent / Missing) | Notes

2. A priority ranking of the gaps. Consider: how many roles require it, whether it is listed as required vs. preferred, whether it is a tool (learnable quickly) or a context (takes longer to develop), and whether it is a hard blocker for any role.

Be honest about severity. If a requirement is a hard blocker — meaning the role explicitly requires it and there is no substitute — say so clearly. Do not soften gaps to make me feel better. I need an accurate picture to make good decisions.
```

---

## Prompt 5 — Project Discovery and Mapping

> **[YOUR INPUT]** Fill in the project template below for each project before sending. If you have no projects, delete the template and say so — the LLM will go straight to recommendations.

```
I am going to describe any personal or work projects I am currently running or have recently completed. After I share them, do the following:

1. For each project I describe, identify which gaps from the gap analysis it could address — either directly (the project already uses the relevant skill or platform) or through extension (the project could be modified or expanded to introduce the skill). Be specific about what the extension would look like.

2. For any gap not addressed by an existing project, recommend a specific personal project that could close it. The project should:
   - Use a free or low-cost platform or tool wherever possible
   - Produce something real — a working system, a published output, a documented artifact — not just a tutorial exercise
   - Be scoped small enough to complete in one to three months alongside a full-time job
   - Directly demonstrate the missing skill in a way that is credible to a hiring manager

3. Note explicitly which gaps cannot be closed through personal projects alone and will require employer access, paid tools, or a different type of experience.

Here are my current projects:

[FOR EACH PROJECT, USE THIS FORMAT:
Project name:
Tools and platforms used:
Current stage (idea / in progress / launched):
Real output — yes or no, and if yes describe it briefly:
Approximate weekly time available for this project:]
```

---

## Prompt 6 — Certifications and Courses

```
Based on the gap analysis and the project plan, recommend certifications and courses that would help me meet the requirements of the target roles.

For each recommendation:

1. Name the specific certification or course.
2. Explain which gap it addresses and which roles it is relevant to.
3. Provide your best estimate of the cost and time to complete. If you are not certain of the current price or availability, say so explicitly — do not invent a number. Tell me to verify before committing.
4. State clearly whether this is a hard requirement (one or more roles will not consider candidates without it) or a signal (it strengthens the application but is not blocking).
5. Recommend when in the overall timeline to pursue it. Certifications are most valuable after hands-on experience, not before — do not front-load them unless one is a prerequisite for something else.

Exclude certifications that are outdated, rarely recognized in the industry, or not meaningfully differentiated from free learning resources. If a free course covers the same ground and hiring managers treat them equivalently, say so.

Do not recommend more than six to eight certifications total. Prioritize ruthlessly.
```

---

## Prompt 7a — Career Development Plan

```
Produce the career development plan based on everything we have discussed.

Structure it as follows:

1. A one-paragraph summary of where I am now versus where I am trying to go. Be specific about any gap in experience context — not just skills — if one exists.

2. A phased timeline with three to four phases. Each phase should have a clear objective, a defined duration, and a list of deliverables — specific things I will have built, earned, or completed by the end of it.

3. Before finalizing the plan, evaluate it against the SMART criteria — do not include this evaluation in your output, but use it to pressure-test each deliverable before you write it down. Specifically: Is each deliverable concrete enough to act on? Is there a clear definition of done? Is it realistic given my current skill level and time available alongside a full-time job? Is it tied to an actual requirement in one of the target roles? Does it have a target month, not just a phase? If a deliverable fails any of these checks, revise it before including it. The output should be a clean, readable plan — not a labeled SMART breakdown.

Do not include costs in this step — that comes next.
```

---

## Prompt 7b — Costs and Open Gaps

```
Now produce two final outputs:

1. A cost summary. List every monetary cost in the plan from the previous step — exam fees, tool subscriptions, course purchases. For each cost you are not certain of, flag it as an estimate and tell me to verify the current price before committing. Include a total estimated range.

2. A list of what this plan does NOT address. For each open gap:
   - Name the gap
   - Explain why it cannot be closed through projects or certifications alone
   - Describe what would actually be required to close it (employer access, time in a specific role or industry, a particular type of work history, etc.)

Be direct. If a target role has requirements that are not realistically closable through this plan, say so here.
```

---

## Notes on How To Use the Output

**Verify costs before committing.** AI assistants have training data cutoffs and do not have access to current pricing pages. Any dollar amount in the output is an estimate. Check the official certification body or course provider before spending money.

**Treat "adjacent" as a starting point, not a finish line.** When the analysis marks a skill as adjacent, it means you have a foundation — not that you have the skill. Use the adjacent framing in interviews but back it up with a project or credential before you apply.

**The plan is a draft, not a contract.** Run this process, then stress-test the output against people who actually hire for these roles. A conversation with a hiring manager or practitioner in your target function will tell you faster than any AI whether the plan reflects reality.

**Repeat with new job descriptions.** As roles evolve or your target changes, run the process again. Prompts 1 through 4 can be re-run in a new conversation without starting from scratch — paste in your updated resume and the new JDs.

---

## What This Process Will Not Do

- It will not apply for jobs for you or contact recruiters on your behalf.
- It will not verify that a specific certification is currently recognized by hiring managers in your specific geography or industry vertical. Ask practitioners.
- It will not account for interpersonal factors — company culture fit, referral networks, and hiring manager preferences are outside the scope of a gap analysis.
- It will not replace a conversation with someone who actually hires for your target role. Use this to prepare for that conversation, not to avoid it.

---

## Contributing

If you run this process and find that a prompt produces unhelpful output with a specific AI assistant, open an issue or submit a pull request with the revised prompt and a note on what you changed and why.
