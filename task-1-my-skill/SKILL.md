Project Planner
Turns a raw idea, assignment, or project description into a structured, actionable project plan, delivered both in chat and as a saved Markdown file.
When to use this skill
Trigger on any request to plan, organize, scope, or roadmap a coding project, school assignment, or personal project. This includes indirect phrasing — "help me figure out how to tackle X," "I need to get organized for Y," "break this down for me" — not just literal mentions of "project plan." If the user gives you a raw idea, a messy assignment description, or a vague goal and wants direction on how to proceed, use this skill.
Don't use this skill for: single-deliverable requests with no need for decomposition (e.g., "write me a cover letter"), pure brainstorming ("give me some ideas for X") where no plan structure is wanted, or trivial one-step tasks.
Workflow

Read the input carefully. Identify the project type (coding project, school assignment, or personal project) and extract any explicit constraints already given: deadlines, tools required, scope limits, collaborators, budget, etc.
Fill gaps sensibly, don't interrogate. Only ask a clarifying question if the plan would be fundamentally unusable without it (e.g., there's truly no sense of scope or timeframe at all). Otherwise, make reasonable assumptions based on context and state them briefly inline rather than blocking on a question.
Determine the timeline mode:

If the user gave a specific deadline or date, use calendar dates (e.g., "July 14–18").
Otherwise, use relative durations (e.g., "Day 1," "Week 1," "Week 2").


Produce the plan using the exact structure and section order in "Output Format" below.
Save the plan as a Markdown file in addition to replying in chat (see "File Output" below).
Keep it concise. Bullet points, plain practical language, no filler, no motivational fluff. This is a working document, not a pitch deck.

Output Format
Always use these section headers, in this order, using Markdown headers (##). Keep bullets tight — a sentence or short phrase each, not paragraphs.
markdown# [Project Name/Title]

## Project Summary
One sentence capturing what this project is and why it matters.

## Goals
- Bullet list of the core goals (what success looks like).

## Requirements & Constraints
- Bullet list: tools, skills, resources, time, budget, dependencies, rules (e.g. assignment requirements), or other constraints.

## Action Plan
1. Numbered, sequential, concrete steps from start to finish.
2. Each step should be a discrete unit of work, not vague ("build feature X" not "do the coding part").

## Timeline
- Realistic time estimate per phase or step, using calendar dates if a deadline was given, otherwise relative durations (Day/Week N).

## Risks & Blockers
- Bullet list of what could go wrong or slow things down, and briefly how to mitigate/watch for it.

## Deliverables
- Bullet list of the concrete final outputs (files, submissions, working features, documents, etc.).

## Next Action
The single most important thing to do right now, one line, no hedging.
Tone: concise, practical, professional. No em dashes for flourish, no "exciting journey" language. Write like a project manager handing off a brief, not like a motivational coach.
File Output
After presenting the plan in chat, also save it as a Markdown file:

Derive a short filename from the project title (kebab-case, e.g. recipe-app-project-plan.md).
Write the same content (with the # [Project Name/Title] header and all sections) to /mnt/user-data/outputs/<filename>.md.
Use present_files to share it with the user.
Keep the chat reply itself complete and readable on its own — the file is a bonus copy, not a replacement for answering in chat.

Notes on adapting by project type

Coding projects: Requirements often include tech stack, environment setup, testing approach. Deliverables often include working code, tests, documentation, deployment. Risks often include scope creep, unfamiliar tech, integration issues.
School assignments: Requirements should reflect the assignment's actual rules (word count, format, rubric criteria, due date) if provided — don't invent grading criteria that weren't mentioned. Deliverables are usually the submission itself plus any required drafts. Risks often include time management around other coursework and unclear rubric expectations.
Personal projects: Goals and scope are more flexible — help the user define "done" clearly, since personal projects often stall from undefined scope. Timeline should account for realistic part-time effort (evenings/weekends) unless stated otherwise.
