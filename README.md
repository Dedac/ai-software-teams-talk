# Are Traditional Software Teams a Thing of the Past?

*How AI changes the work, the workflow, and the shape of effective teams.*

## Abstract

Are traditional software teams a thing of the past? With a world of new and
constantly changing AI agents, tools, and assistants, software development
techniques and patterns are changing. There are new patterns and practices to
evaluate, and new shapes of effective teams. As AI further integrates into our
world of software development at the lowest levels, how will you develop your
career to stay relevant? As a manager or director, how will you separate people
into roles and teams to take advantage of these new tools?

We will be examining a set of anonymized work from real teams at enterprises
that are optimized to use AI tooling to develop new software as well as build
on existing software.

## Thesis and through-line

> **Traditional teams aren't disappearing. The bottleneck has moved from
> writing code to trusting it.**

Repeated line: **"Plausible isn't proven."**

Closing answer to the title: **"Traditional teams aren't a thing of the past.
Teams that only write code are."**

## Sources

- [From RPI to QRSPI](https://alexlavaee.me/blog/from-rpi-to-qrspi/): why the
  process is being iterated on
- [QRSPI+](https://github.com/dfrysinger/qrspi-plus): one implementation of a
  structured agent workflow
- [BeamRS](https://github.com/Dedac/BeamRS): local demo and running case study
- [GitHub Agentic Workflows](https://github.github.com/gh-aw/introduction/overview/):
  agents running in the repository on events and schedules
- Copilot code review on BeamRS pull requests
  [#4](https://github.com/Dedac/BeamRS/pull/4) and
  [#6](https://github.com/Dedac/BeamRS/pull/6)
- Anonymized enterprise team cases (to be added per section)

## Outline (about 45 minutes before Q&A)

### 0. Cold open: "The app worked. It just existed twice." (3 min)

- Show BeamRS working.
- Reveal the bug from the Leptos upgrade: the browser built a second copy of
  the whole interface instead of attaching to the page the server had already
  rendered.
- Ask: *"Would you have approved this if the demo looked right?"*
- Deliver the thesis.

### 1. The bottleneck moved (4 min)

- Ask: *"If code took no time to write tomorrow, what would still stop your
  team from shipping?"*
- Use the answers (unclear requirements, review, integration, risk) to frame
  the shift.
- Analogy: agents add lanes, but review is still a one-lane exit ramp.
- Enterprise case: a team that sped up coding, then found review or
  integration became the constraint.
- Transition: if the constraint moved, the process has to change too.

### 2. Why our first agent workflows weren't enough (6 min)

- The move from research–plan–implement to QRSPI.
- Three lessons:
  - **Instruction overload:** important guidance gets lost in a growing prompt.
  - **Magic words:** correct behavior shouldn't depend on a secret phrase.
  - **Persuasive plans:** a plan that reads well can rest on wrong assumptions.
- Quote (Dex Horthy): *"A 1,000-line plan contains as many surprises as 1,000
  lines of code."*
- Hook: *"Is there one person on your team who knows exactly what to say to
  make the agent behave? That's not expertise. It's a single point of
  failure."*
- Treat the blog's context-window numbers as practitioner rules of thumb, not
  hard limits.
- Enterprise case: agent work that looked finished but missed a constraint or
  architecture decision.

### 3. Turn the process into infrastructure (7 min)

- QRSPI+ as one implementation, not the only answer. Three blocks:

  | Block | What happens | Human responsibility |
  |---|---|---|
  | **Align** | Goals, research, design, delivery slices | Decide what to build and why |
  | **Execute** | Task specs, safe parallel work, isolated implementation | Set boundaries, resolve big decisions |
  | **Verify and learn** | Review, integrate, test, replan | Own the outcome, improve the process |

- Ideas to highlight: written records at each step, focused context, approval
  gates, vertical slices, rules the process enforces rather than reminders.
- Hook: *"We deliberately hide from the research agent what we want"*, like a
  blind trial.
- Hook: *"The agent cannot write production code until a failing test
  exists."*
- Be honest about costs: more steps and slower starts. Use the quick-fix route
  for small changes.
- Enterprise case: a team that turned informal conventions into reusable
  instructions or review gates.

### 4. Two layers of agent review (10 min)

All findings in this section were made by agents. People decided which to
accept, made the fixes, and approved the releases.

**Layer 1: the local workflow** reviews the work while it is being built.

- Agentic review found that the first BeamRS version used about 227 lines of
  handwritten JavaScript for behavior the approved design assigned to Rust.
  The fix moved it into Rust (commit *"hydrate BeamRS frontend from Rust"*).
- During the Leptos upgrade, an independent clean Docker build exposed an
  outdated Rust version.

**Layer 2: Copilot code review on the pull request** looks at the finished
change from a fresh start, without the local session's assumptions. It found
seven problems after the local work had passed its own tests and reviews:

| Pull request | What it found | What changed |
|---|---|---|
| [#4](https://github.com/Dedac/BeamRS/pull/4) Leptos upgrade | Browser built a second copy of the interface | Attach to the existing page; browser check for one interface |
| #4 | Runtime deployment settings were thrown away | Keep runtime settings |
| #4 | Profile and frequency pages made duplicate API requests | Removed extra requests; one call per page load |
| #4 | Process record missing the planned integration and replanning steps | Added the missing records |
| [#6](https://github.com/Dedac/BeamRS/pull/6) Load testing | One setting could use enormous memory | Fixed, with regression test |
| #6 | An incomplete response could count as a success | Fixed, with regression test |
| #6 | Worker tasks could keep running after a crash or cancellation | Fixed, with regression test |

**Closing the loop:** each finding got a commit, a reply, and often a
regression test, so the next run is harder to fool.

**The miss:** [#2](https://github.com/Dedac/BeamRS/pull/2) later fixed the
home page's create-frequency button and its accessibility. No review caught it
before merging. Pull requests #1 and #2 had no Copilot code review.

Hooks:

- *"The local process said done. A second agent disagreed, with specific
  examples."*
- *"It reviewed our process as well as our code."* (the missing records)
- *"Don't ask the builder whether the building is safe."*
- *"Green checks are where review starts, not where it ends."*
- *"Write the review into the process instead of relying on someone to
  remember it."*

Keep the balance: agents are not infallible, and agent review adds assurance
without removing human accountability.

### 5. Agents beyond the editor (4 min)

- Copilot code review already runs in the repository on every pull request.
  GitHub Agentic Workflows extend that to events and schedules.
- How it works: Markdown instructions plus settings for triggers and
  permissions, compiled into GitHub Actions. Read-only by default; writes go
  through approved actions such as comments, issues, or pull requests.
- Same principles, new place:

  | Principle | Local workflow | Agentic Workflows |
  |---|---|---|
  | Focused context | Fresh start per step | Defined trigger and instructions |
  | Limited authority | Approval at each step | Read-only by default, approved writes |
  | Visible evidence | Written record per step | Issues, comments, pull requests |

- Hook: *"An agent is working in your repository at 3 a.m. What should it be
  allowed to do, and what should it only recommend?"*
- Examples (not claims about BeamRS): issue clarification, CI failure
  investigation, documentation updates.
- Enterprise case: governed automation for triage or maintenance.

### 6. What changes for careers and teams (8 min)

- Organize around responsibilities, not invented job titles:

  | Responsibility | How it changes |
  |---|---|
  | Product and domain leadership | Makes intent, constraints, and success criteria explicit |
  | Engineering leadership | Owns architecture, decomposition, and integration |
  | Developers | Implement, delegate, debug, and inspect unfamiliar code |
  | Quality specialists | Design evidence that can disprove apparent success |
  | Platform teams | Provide workflows, context, permissions, and observability |
  | Managers | Balance agent capacity against human review and decision capacity |

- Hook: *"Our agents found the mistakes. Our job was deciding what counted as
  a mistake."*
- Junior engineers: *"Who here learned by fixing small bugs? Those are the
  first tasks agents take."* Teams must create new ways to learn debugging,
  decomposition, and judgment.
- Career skill: *"Could you explain why that code was wrong?"*
- Org chart exercise: add agents as boxes and ask, *"Where do the review
  arrows go?"*
- Enterprise cases: two or three contrasting team designs, including one that
  did not work.

### 7. The process is a product (3 min)

- Start small: one workflow, clear permissions, defined checks, learn from
  each run.
- Measure validated delivery time, review effort, rework, late defects, and
  cost, not generated code volume.
- Hook: *"Every finding should make the next run harder to fool."*
- One next step per audience:
  - **Individual contributors:** write goals and a design before involving an
    agent on one change this week; compare with your usual approach.
  - **Managers:** measure how much time people spend reviewing agent output
    before adding more agents.
  - **Platform leaders:** turn one repetitive repository task into an
    automated workflow with clear permissions and review.

### Close

- Return to the opening BeamRS screen: *"How would your team have known?"*
- Final line: *"The advantage isn't having more agents. It's building a
  human-agent system that turns intent into verified outcomes, and improves
  when it finds a gap."*

## Presenter notes

- Cut jargon: mention RPI and QRSPI once as background; describe BeamRS issues
  in plain language.
- Use recorded evidence or a prepared change rather than a long live agent run.
- BeamRS is a demo app with an unauthenticated identity model, not production
  software.
- If a section has no strong enterprise case, shorten or merge it.
