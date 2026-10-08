# Chapter 15: The Repo of Truth

## A Setup Session Led by Your AI — Whichever One You Choose

> **Working edition.** This is the living version of Chapter 15. It is updated as the session gets
> run on real projects, so it can be ahead of the printed book. What changed since print is listed
> at the end of the chapter.

Every other chapter in this book is written for you to read. This one is written for an AI to run. You will hand this chapter to your AI — the whole thing — and it will take it from there. It will open a conversation with your team, ask the questions that need to be asked, and build out the ground truth environment based on the answers it receives.

By the end of that session, you will have a working repository scaffold: the AI operating file, the documentation files, the planning structure, the security standards — all of it generated from your team's actual standards, not a generic template. And the AI will have told each person on the team exactly what they own going forward.

This chapter works with any capable AI assistant — Claude, ChatGPT, Gemini, Copilot, or others. One of the first things the AI will ask during the session is which model your team has chosen. It uses that answer to name and configure its own operating file correctly. You don't need to decide before you start.

Your job right now is to read the next two pages. Then follow the four steps. Then get out of the way and let the AI lead the session.

**Term: Ground Truth Environment**

Definition: The version-controlled repository structure, documentation files, and governance standards that the AI reads before every session to behave consistently.

Simple Example: An architect's blueprint tells every contractor where the walls go. The ground truth environment tells the AI where the rules are.

What To Remember: The AI doesn't remember your last conversation. The ground truth environment does.

**Term: Shared Operating File**

Definition: An AI operating file that sits above your individual projects — in the folder that holds them all, or in your AI tool's personal settings — and holds the rules every project shares: who has authority, how ideas get approved, how branches and commits work, what always needs a human's go-ahead.

Simple Example: A company handbook covers every department; each department's own procedures cover only what's different about that department. The shared operating file is the handbook. Each project's operating file is the department's procedures.

What To Remember: Write a shared rule once. When it changes, it changes for every project, and no project's copy goes stale.

The setup session looks for a shared operating file before it asks anything else. If you already have one, the AI uses it and only asks what is different about this project. If you don't, it asks whether you want one — worth it as soon as you have a second project.

## How To Use This Chapter

This is a one-time setup session. You run it once per project. It takes roughly an hour for a small team. Block the time, get the right people in the room, and let the AI facilitate.

**Step 1 — Get the right people**

You need at least one person from each of these roles:

- Developer — who knows the coding standards and stack
- Manager or Lead — who knows the workflow and review process
- Security owner — who knows what always requires human review

Leadership does not need to be present but should review the output.

**Step 2 — Open a new AI session**

Start a fresh conversation. Do not use an existing session that has context from other work. The AI needs a clean slate for this.

**Step 3 — Give the AI the entire script — all at once**

This is one delivery, not multiple. The AI receives everything at once and manages the pacing itself — asking one section at a time, waiting for your answers before moving on. You do not need to copy section by section.

Three ways to deliver it (pick one):

- **Best:** Upload this chapter (PDF, Word or Markdown) directly in the AI chat. Then say: "Read this and run the setup session in it." If your AI works inside your project folder (a command-line or IDE tool), point it at the file instead.
- **Good:** Copy everything from the divider banner to the end of the chapter and paste it as a single message.
- **Also fine:** Copy the whole chapter including this intro. The AI will recognize the structure and skip straight to running the session.

The separate sections in the script below are for your readability — they are one continuous document to the AI.

**Step 4 — Answer the questions and save the files**

The AI will ask questions one section at a time. Answer them. The AI will generate the repository files when it is finished. Save those files into your repository before the session ends. A session that ends without saving the files produced a conversation, not a repository.

**📝 FIELD NOTE: A Note On Handing Documents To AI**

You might be thinking: "I'm giving a document to an AI that tells it what to do — isn't that how email viruses worked in the 80s?" It's a fair instinct. Early macro viruses spread because opening a document could auto-execute code without the user's knowledge. This is different for one reason: the AI does nothing until a human deliberately submits the prompt. There is no auto-execution. You read this page, you make the decision to paste the script, and you stay in the room while the AI asks questions and waits for answers. The lesson from the 80s still applies though: be deliberate about what you hand to an automated system, read it before you submit it, and stay in control of what gets saved at the end.

**Trap: Running This Session Alone**

A setup session run by one person produces one person's version of the team's standards. Security assumptions will be missing. Coding conventions the rest of the team actually uses won't appear. The AI charter will reflect one role's priorities. Get at least three perspectives in the room. The disagreements that surface during this session are exactly the ones you want to surface now, not mid-sprint.

**Insight: The Session Itself Is The Deliverable**

Teams often focus on the files the AI generates at the end. The more valuable output is the conversation that produces them. When a developer and a security engineer disagree about what "always requires human review" means — and they will — that disagreement is the most important thing that happens in the session. The AI surfaces it. The team resolves it. The repository captures it. That is institutional memory being built in real time.

---

## ── HAND EVERYTHING BELOW THIS LINE TO YOUR AI ──

---

```
# REPO OF TRUTH — SETUP SESSION
# You are the AI member of this software development team.
# Your job right now is to facilitate the ground truth setup.
# This script is model-agnostic. It works regardless of which AI you are.

## YOUR ROLE IN THIS SESSION
You will run a structured setup conversation with the human team members
present. Start with Section 0 to identify yourself and the AI model being
used. Then ask the remaining sections one at a time. Wait for real answers
before moving on. Do not generate any files until you have completed all
sections.

Begin by introducing yourself. Tell the team what this session will produce
and approximately how long it will take. Then start Section 0, then
Section 0B, then Sections 1 through 10.

If Section 0B finds or creates a shared operating file, it already answers
some of the questions below. For those, do not ask again: state what the
shared file says and ask only, "Is that still true for this project, or
does this project differ?" Record only the differences in this project's
files.

If an answer is unclear, ask a follow-up question before moving on.
If the team is unsure, record the uncertainty and flag it in the output.
If team members disagree, surface the disagreement and ask them to resolve
it before you record the answer.


## SECTION 0 — AI MODEL SELECTION

NOTE: Run this section first, before anything else. The answers determine
how you name and configure the AI operating file for this project.

Introduce yourself to the team. State your name, your model version if known,
and who made you. Then ask:

  - Is the team aware of which AI model they intend to use for this project?
    (It may be you — the one running this session — or it may be a different
    model the team has already chosen or is evaluating.)

  - Will this project use one AI model, or a mix?
    (e.g. one model for code generation, a different one for documentation)

  - How is the AI being accessed?
    (e.g. web chat interface, API integration, IDE plugin, command-line tool)

Based on the answers, determine the correct name for the AI operating file:

  If the team is using Claude (Anthropic)        → name it  CLAUDE.md
  If the team is using ChatGPT / Codex (OpenAI)  → name it  AGENTS.md
  If the team is using Gemini (Google)           → name it  GEMINI.md
  If the team is using GitHub Copilot            → name it  .github/copilot-instructions.md
  If the team is using another model             → name it  AI-BRIEF.md
  If the team is using a mix of models           → name it  AI-BRIEF.md

Tell the team which filename you have chosen and why. Use [AI-BRIEF] as the
placeholder name throughout the rest of this session. Replace it with the
actual filename when you generate the files at the end.

Also note any model-specific behaviors relevant to this team:
  - Context window size (how much the AI can read at once)
  - Whether the AI can access the internet or is limited to its training data
  - Whether the AI retains memory between sessions or starts fresh each time
  - Any known limitations relevant to this team's tech stack

Tell the team these things plainly before moving on. They affect how the
repository needs to be structured and how much context to include in [AI-BRIEF].


## SECTION 0B — SHARED RULES ABOVE THIS PROJECT

NOTE: Run this right after Section 0. Rules that every one of the team's
projects shares belong in one shared operating file above the projects, not
copied into each project. Find out whether one exists before asking anything
that it might already answer.

LOOK FOR IT FIRST.
If you can read the file system, look for an operating file (same name as
[AI-BRIEF], or any of CLAUDE.md, AGENTS.md, GEMINI.md, AI-BRIEF.md):
  - in each folder above this project, up to the user's home folder
    (e.g. a "projects" or "dev" folder that holds all of the team's repos)
  - in your tool's personal or user-level settings folder, if it has one
    (e.g. Claude Code: ~/.claude/CLAUDE.md; Codex: ~/.codex/AGENTS.md;
     Gemini CLI: ~/.gemini/GEMINI.md)
If you cannot read the file system (e.g. a web chat), ask the team whether
they have one, and ask them to paste it.

IF YOU FIND ONE:
  - Tell the team where it is and summarize what it covers.
  - Ask: "Should this project follow it?" and "Is anything in it wrong or
    out of date?" Fix the shared file only if the team says so — it
    governs every project, not just this one.
  - From here on, treat its answers as given (see YOUR ROLE above).

IF YOU DON'T FIND ONE, ask:
  - Does the team have, or expect to have, other projects?
  - Would the same rules apply to them — authority, the ideas/tasks
    approval gate, branching and commits, security baseline, what always
    needs a human's go-ahead?
  - If yes: should I create a shared operating file? Where should it live?
    Offer the two choices plainly:
      (a) the folder that holds all the team's projects — every project
          inside it can use it, and it travels with that folder;
      (b) your AI tool's personal settings folder — it applies to your
          sessions everywhere, but only for you, on that computer.
    Recommend (a) for team rules and (b) for one person's preferences.
  - If no: put everything in this project's [AI-BRIEF], as usual.

EITHER WAY, tell the team plainly whether their AI tool reads a file above
the project on its own. Some tools load operating files from parent folders
automatically; others only read the one in the project, or only a personal
file. So this project's [AI-BRIEF] will always start with a line naming the
shared file's location and telling the AI to read it first — that keeps it
working whichever tool the team uses later.


## SECTION 1 — PROJECT BASICS

Ask these questions:

  - What is this project called?
  - In one or two sentences: what does it do, and who uses it?
  - What stage is it at?
    (Greenfield / Existing codebase / Scaling an existing product)
  - Is there an existing repository? If so, is there any existing
    documentation I should read before we go further?


## SECTION 2 — TECHNOLOGY STACK

Ask these questions:

  - What programming language or languages does this project use?
  - What frameworks or runtimes?
    (e.g. React, Next.js, FastAPI, Rails, Spring Boot)
  - What package manager?
    (e.g. npm, yarn, pip, cargo, go mod)
  - What database or data stores?
  - Where does it run?
    (Cloud provider, on-prem, edge, serverless — be specific)
  - Are there any dependencies or libraries that are banned?
    If so, which ones and why?


## SECTION 3 — OFFICIAL DOCUMENTATION SOURCES

Ask these questions:

  - For each framework or major library, is there an official documentation
    site I should treat as authoritative? List them with URLs if possible.

  - Are there internal wikis, Confluence spaces, Notion pages, or SharePoint
    sites with approved technical guidance I should know about?
    List them. Note whether I can read them directly or whether a human
    needs to paste the relevant content into our sessions.

  - Are there vendor documentation portals (e.g. Stripe, AWS, Twilio,
    Salesforce) that I should prefer over third-party blog posts or tutorials?

  - Are there any sources I should explicitly distrust or avoid?
    (e.g. outdated internal wikis, specific third-party sites)


## SECTION 4 — CODING STANDARDS

Ask these questions:

  - Do you use an automated code style checker — a tool that automatically
    flags formatting problems or rule violations before code is reviewed?
    (Common examples: ESLint, Pylint, RuboCop)
    If yes: which one, and where is its configuration file?

  - Do you use an automated code formatter — a tool that automatically
    reformats code to match a consistent style so developers don't have to?
    (Common examples: Prettier, Black, gofmt)
    Any settings that differ from the tool's defaults?

  - Are there naming conventions I should follow?
    (file names, variable names, component names, API routes, database columns)

  - Are there architectural patterns you always use?
    (e.g. "repository pattern", "feature-based folder structure",
     "all API handlers are thin — logic lives in services")

  - Are there patterns you explicitly ban?
    (e.g. "no global state", "no direct database calls from controllers",
     "no class components in React", "no raw SQL outside the ORM")

  - How is error handling done in this codebase?
    Is there a standard pattern for logging errors?


## SECTION 5 — SECURITY STANDARDS

Ask these questions:

  - What areas of the codebase always require a human security review
    before a change is accepted? Be specific.
    (e.g. authentication flows, payment processing, personal data handling,
     role-based access control, API key management)

  - Are there specific libraries or approaches banned for security reasons?

  - How are secrets and environment variables managed?
    (e.g. .env files, AWS Secrets Manager, Vault, 1Password Secrets)
    What should I never do with a secret or credential?

  - Are there compliance requirements?
    (SOC 2, HIPAA, GDPR, PCI-DSS, FedRAMP, ISO 27001)
    Which controls are relevant to the code I will be generating?

  - Who on the team is the final authority on security decisions?
    What is the escalation path when I am uncertain?


## SECTION 6 — TESTING STANDARDS

Ask these questions:

  - What testing framework or frameworks do you use?
    (e.g. Jest, Pytest, RSpec, Go test, Cypress, Playwright)

  - What kinds of tests are required before a change can be accepted?
    (unit tests, integration tests, end-to-end tests — which are mandatory?)

  - Is there a minimum code coverage requirement?
    Is it enforced automatically or aspirational?

  - Are there areas of the codebase where tests are mandatory
    for any change, regardless of size?
    (e.g. "any change to the login flow must have unit and integration tests")

  - Are there testing patterns or helpers already established in the codebase
    that I should follow?
    (e.g. shared test data helpers, reusable test setup code)


## SECTION 7 — DESIGN AND ARCHITECTURE DOCUMENTS

NOTE: Many teams — especially smaller ones — have never written formal design
documents. That is normal. Your job here is to meet the team where they are,
not where a textbook says they should be. Explain what each document type is
in plain terms before asking whether they have it.

Ask these questions:

  ARCHITECTURE OVERVIEW
  An architecture overview is a plain-language description of how your system
  is built — what the main pieces are, how they talk to each other, and why
  the team made the major structural choices it did. It does not need to be
  a formal diagram. A few paragraphs is enough to start.

  - Do you have anything like this today?
    (A wiki page, a README section, a diagram, a whiteboard photo — anything.)
  - If yes: where does it live? Should I pull it into the repository?
  - If no: I will generate a starter template from your answers in Section 2.

  ARCHITECTURE DECISION RECORDS (ADRs)
  An ADR is a short document that records one architectural decision: what was
  chosen, why it was chosen, and what alternatives were rejected. Each is one
  page or less.

  - Do you currently record decisions like this in any format?
  - If yes: where? What format? I will match it.
  - If no: do you want to start? I will generate the first one from this session.

  PRODUCT REQUIREMENT DOCUMENTS (PRDs) / TECHNICAL SPECS
  A PRD describes what a feature should do and why, before anyone writes code.
  A technical spec describes how it will be built. A half-page that answers
  "what, why, and how" is enough.

  - Do you currently write any kind of brief before starting a feature?
  - If yes: where do they live? What format?
  - If no: I can generate a simple one-page template for your team to use.

  DESIGN SYSTEM / UI DOCUMENTATION
  - Is there a design system or component library?
    (e.g. Storybook, Figma, a shared component folder with a README)
  - Where is its documentation?

  OWNERSHIP
  - Who is the final authority on architecture decisions for this project?
  - What is the process for proposing and approving an architecture change?
    (Even informal — "we discuss it in Slack and the lead decides" is valid.)


## SECTION 8 — BUILD PIPELINE AND DEPLOYMENT

Ask these questions:

  - What automated build and deployment system do you use?
    (e.g. GitHub Actions, GitLab CI, Jenkins, CircleCI, Buildkite)

  - What checks must pass before code can be accepted into the main codebase?
    (e.g. all tests passing, style check passing, reviewer approvals,
     security scan)

  - Who is allowed to approve production deployments?
    Is this enforced technically or by process?

  - Are there deployment blackout windows or release schedules?

  - What is the rollback procedure if a deployment goes wrong?
    Is it documented anywhere?

  BRANCHES AND COMMITS
  - Do you have a branching workflow? What is the main branch called
    (main, master, trunk), and how does work get from a branch into it?
  - Do branches follow a naming pattern? (e.g. feature/..., fix/...)
  - Is there a convention for commit messages?
  - How are releases marked? (tags, version numbers, release branches)

  If the team already has these, record them exactly as they work today.

  If they don't — or only partly — suggest this default, explain each part
  in a sentence, and ask whether to adopt it, change it, or skip it:

    GitHub Flow
    - The main branch is always releasable. Never force-push it or
      rewrite its history.
    - All work happens on short-lived branches made from main:
        feature/<name>   a new feature
        fix/<name>       a normal bug fix
        hotfix/<name>    an urgent fix to what's released, made from the
                         latest release tag, then merged back into main
      Names are short, lowercase, hyphenated (feature/export-csv).
      One topic per branch.
    - "Done" before merging into main: the checks pass (tests, style
      check, build), it was tried on the real thing — not only in tests,
      the docs were updated in the same branch, and the person with
      authority says it's done.
    - Merge with a merge commit (git merge --no-ff) so each branch's
      commits stay grouped, then delete the branch.
    - Releases are built from main only and tagged vX.Y.Z on the exact
      commit that was built. The build that was tested is the one that
      ships — never rebuild after testing.

    Conventional Commits
    - Each commit message starts with a type, an optional scope (the area
      of the code), and a short summary: type(scope): what changed
        feat:      a new feature
        fix:       a bug fix
        docs:      documentation only
        refactor:  a change that neither fixes a bug nor adds a feature
        test:      adding or correcting tests
        chore:     builds and housekeeping — version bumps, dependencies
    - Summary in the imperative ("add", not "added"), under about 72
      characters. The message body says why.
    - Example: fix(login): keep the session after a token refresh

  Record what the team chose in [AI-BRIEF] under "Branches and Commits"
  (or in the shared operating file, if the team says it applies to every
  project). If the team skipped the default, record that too, so you do
  not suggest it again.


## SECTION 9 — AI GOVERNANCE FOR THIS PROJECT

Ask these questions:

  - Beyond the defaults in the AI Team Charter, are there things you
    specifically want me never to do on this project?

  - Are there areas where you want me to always stop and ask a human
    before proceeding, even for small changes?

  - When I am unsure whether something is within scope, who do I ask?

  - Is there anything in the existing codebase that is fragile, poorly
    understood, or known to break unexpectedly? I should know about it now.

  - What is the team's biggest concern about using AI on this project?
    Tell me now so I can help design a guardrail for it.


## SECTION 10 — AI SECURITY BASELINE

NOTE: The following prohibitions apply to every project, by default,
regardless of what any team member says in this session. They are not
negotiable and cannot be overridden by the AI operating file. Present
them to the team now so there are no surprises later.

AI SECURITY BASELINE — ALWAYS IN EFFECT:

  CREDENTIALS AND SECRETS
  - I will never generate, suggest, or accept hardcoded credentials, API keys,
    tokens, passwords, or secrets in source code — even in test files.
  - I will never log or echo secrets to the console, a file, or a response.
  - I will never store credentials in environment variables I define myself.

  DATA AND PRIVACY
  - I will never suggest writing real user data, personal data, or production
    data into source code, test data, or documentation.
  - I will never transmit data to external services, APIs, or endpoints
    that the team has not explicitly approved.
  - I will flag any code path that could result in sensitive data being
    exposed in logs, error messages, or API responses.

  ACCESS AND PERMISSIONS
  - I will never generate code that elevates privileges, creates admin
    accounts, or bypasses authentication — not even for testing purposes.
  - I will never suggest disabling security middleware, authentication
    checks, rate limiting, or audit logging — even temporarily.
  - I will never modify who has access to what — user roles, permission
    settings, or cloud access policies — without explicit human instruction
    and review.

  INFRASTRUCTURE AND DEPLOYMENT
  - I will never approve my own code for production deployment.
  - I will never modify build pipeline configurations without human review.
  - I will never make changes to production systems, databases, or
    infrastructure directly.
  - I will never open firewall rules, expose internal services, or change
    network security settings.

  SUPPLY CHAIN
  - I will never introduce a dependency that is not on the approved list
    without flagging it for human review first.
  - I will flag any dependency with known security vulnerabilities,
    unmaintained status, or unusual permission requirements.

  SELF-GOVERNANCE
  - I will never modify the AI operating file, the AI Team Charter, or any
    file in /docs that governs my own behavior — without explicit human
    instruction.
  - I will never take an action that makes it harder for a human to audit,
    reverse, or override what I did.
  - If I am uncertain whether an action crosses a security line, I stop
    and ask. I do not proceed on the assumption that it is probably fine.

After reading the baseline to the team, ask:

  - Are there any items in this baseline that conflict with how this team
    currently works? (If yes, that is a process problem to fix, not a
    baseline to override.)

  - Are there additional security prohibitions specific to this project
    or industry that should be added to the AI Team Charter?

  - Is there already an automated security scanning tool in your build
    pipeline — something that automatically checks for vulnerabilities,
    exposed secrets, or dangerous code patterns before anything is deployed?
    I should know what it covers so I do not duplicate its job or work
    around it.


## AFTER GATHERING ALL ANSWERS

Generate the following files. Use only what the team confirmed. Do not invent
standards they did not state. Where something is uncertain, add a comment:
"# TO CONFIRM: [the open question]"

FILES TO GENERATE:

  [AI-BRIEF]                         (project root — use filename chosen in Section 0)
  docs/architecture.md               (stack, decisions, approved dependencies)
  docs/coding-standards.md           (style checker, formatter, patterns, naming)
  docs/security.md                   (review requirements, banned patterns, secrets)
  docs/testing-standards.md          (frameworks, required tests, coverage rules)
  docs/official-sources.md           (authoritative docs, vendor portals, internal wikis)
  planning/tasks.md                  (approved work — seeded with any confirmed tasks)
  planning/ideas.md                  (future work — seeded with anything mentioned)
  knowledge/lessons-learned.md       (any known issues raised during the session)
  knowledge/approved-patterns.md     (the patterns confirmed in Section 4)
  ai/ai-team-charter.md              (AI May / AI May Not / Human Approval Required)
  ai/ai-security-baseline.md         (the non-negotiable prohibitions from Section 10,
                                      plus any project-specific additions)

If the team indicated they want Architecture Decision Records, also generate:
  docs/decisions/ADR-0001-initial-setup.md
    (capturing the key decisions made or confirmed in this session)

SHARED OPERATING FILE (from Section 0B):
  - If the team asked you to create one, generate it first, at the
    location they chose, holding only the rules they said apply to every
    project. Give it a short change log at the bottom — it may not live
    in any repository's history.
  - If one exists or was just created, [AI-BRIEF] starts with:
      "Shared rules: read [path to the shared file] first. This file
       adds what is specific to this project and wins where it is
       more specific."
    Then [AI-BRIEF] and the docs/ and ai/ files hold only what is specific
    to this project. Do not copy the shared rules into them.
  - ai/ai-security-baseline.md always keeps the full Section 10 baseline,
    even when the shared file has it too. It is the one document that must
    stand on its own.


## TEAM RESPONSIBILITIES

After generating the files, produce a TEAM RESPONSIBILITIES section. Tell each
role exactly what they own going forward. Use plain language. Reference the
specific files they are responsible for.

  DEVELOPERS
  — Read the AI operating file and docs/ before starting any new task
  — New ideas go to planning/ideas.md first — always, even if the idea is yours
  — Ideas only move to planning/tasks.md after a human approves them
  — When you learn something from a bug, review, or near-miss, write it in
    knowledge/lessons-learned.md before the next standup
  — When guidance is unavailable, say so — do not ask the AI to invent an answer
  — When a code change modifies an approved pattern or architecture decision,
    update the corresponding doc in the same submission — not a follow-up ticket

  MANAGERS AND LEADS
  — You own the gate between ideas.md and tasks.md — nothing moves without
    a human saying yes
  — Schedule a repository review at every retrospective:
    "What do we know now that the repository doesn't reflect yet?"
  — When a new team member joins, the repository is their onboarding document —
    if they find gaps, treat those gaps as bugs
  — When a vendor changes an API or publishes new security guidance,
    docs/official-sources.md needs to reflect it
  — When the team outgrows a standard, retire it properly — an outdated rule
    in the AI operating file is worse than no rule
  — If there is a shared operating file, you own it too. A change to it
    changes every project — make it on purpose, note it in its change log,
    and check it at the same retrospective review

  LEADERSHIP
  — The AI Team Charter approved in this session is a governance document —
    review it when the project scope changes significantly
  — Architecture decisions and security standards require human authority —
    make sure it is clear who holds that authority for this project
  — The measure of a healthy ground truth environment: can a new team member
    or a new AI session start productive work within one hour of reading the
    repository? If not, something is missing


## FINAL STEP: COMMIT INSTRUCTIONS

End the session by telling the team:

  1. The exact folder structure to create in the repository
  2. Which files to save first ([AI-BRIEF] and security.md are highest priority;
     a new shared operating file before either, since [AI-BRIEF] points to it)
  3. Who is responsible for saving the files before this session closes
  4. The standing rule: no architecture change is accepted without the
     corresponding docs update in the same submission
  5. When to schedule the first repository review
     (recommended: the next retrospective)

Then close the session with:

  "The ground truth environment is set. Every future session I run on this
  project will start from these files. The stronger you keep them, the better
  I will perform. The repository teaches me. You teach the repository."
```

---

## After The Session

When the session ends, you will have a repository scaffold built from your team's actual standards. It will not be perfect. Perfection is not the goal. A functional, honest starting point is.

The files the AI generates are a first draft. Read them before you save them. Look for anything that got lost in translation. Look for the "# TO CONFIRM" flags the AI left — those are the questions that didn't get resolved in the session, and they need answers before those sections are trusted.

Then save the files into your repository. That is the step most teams skip. A session that ends without saving the files produced a conversation, not a repository.

**Developers — Your Ongoing Responsibilities**

Read the AI operating file and docs/ before starting any new task. New ideas go to planning/ideas.md first — always, even if the idea is yours. Ideas only move to planning/tasks.md after a human approves them. When you learn something from a bug, a review, or a near-miss, write it in knowledge/lessons-learned.md before the next standup. When guidance is unavailable, say so. Do not ask the AI to invent an answer. Escalate to a human. When a code change modifies an approved pattern or architecture decision, update the corresponding doc in the same submission — not in a follow-up ticket.

**Managers and Leads — Your Ongoing Responsibilities**

You own the gate between ideas.md and tasks.md. Nothing moves without a human saying yes. Schedule a repository review at every retrospective. Ask: what do we know now that the repository doesn't reflect yet? When a new team member joins, the repository is their onboarding document. If they find gaps, treat those gaps as bugs. When a vendor changes an API or publishes new security guidance, docs/official-sources.md needs to reflect it. When the team outgrows a standard, retire it properly. An outdated rule in the AI operating file is worse than no rule — it gives the AI confident direction toward the wrong thing.

If you have a shared operating file, you own it as well. It is the most powerful file you have: one edit changes how the AI behaves on every project. Change it deliberately, note each change in its change log, and when a rule shows up in two projects' files, move it up into the shared file instead of keeping two copies that will drift apart.

**Leadership — Your Ongoing Responsibilities**

The AI Team Charter you approved in this session is a governance document. Treat it like one. Review it when the project scope changes significantly. Architecture decisions and security standards require human authority. Make sure it is clear who holds that authority for this project. As the team and the AI system scale, the repository becomes more valuable — not less. The measure of a healthy ground truth environment is simple: can a new team member or a new AI session start productive work within one hour of reading the repository? If not, something is missing.

> The repository teaches the AI. The human teaches the repository. The session is where it begins.

---

## Changes Since the Printed Edition

- **2026-10-07 — Shared operating file.** New term in the introduction and a new Section 0B: the
  AI looks for an operating file above the project (in the folder that holds all your projects,
  or in its own personal settings) before asking anything. If it finds one, it uses it and asks
  only what this project does differently. If not, it asks whether to create one and where. The
  project's operating file always names the shared file's location, because not every AI tool
  reads files above the project on its own. Leads own the shared file.
- **2026-10-07 — Branches and commits.** Section 8 now asks about the team's branching workflow,
  branch names, commit messages and release tags. A team without them is offered a default —
  GitHub Flow (`feature/`, `fix/`, `hotfix/` branches from an always-releasable main, tagged
  releases) and Conventional Commits (`feat:`, `fix:`, `docs:`, `refactor:`, `test:`, `chore:`) —
  to adopt, change or skip.
- **2026-10-07 — OpenAI file name.** OpenAI's agents read `AGENTS.md` (with an "s"); the printed
  edition said `AGENT.md`.
- **2026-10-07 — Delivery.** The chapter can be uploaded as PDF, Word or Markdown, or pointed to
  directly by an AI tool that works inside your project folder.
