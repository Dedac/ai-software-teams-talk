# Are Traditional Software Teams a Thing of the Past?

*How AI changes the work, the workflow, and the shape of effective teams.*

## Presentation

View the [live deck on GitHub Pages](https://dedac.github.io/ai-software-teams-talk/),
open the [presentation](presentation/index.html) locally in a browser, or see the
[presenting and PDF export guide](presentation/README.md). The deck uses large,
high-contrast type for a large audience and includes presenter notes.

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

Second through-line: **the value of completed work, not the amount of work
completed.** Cheap code makes choosing what to build the scarce skill.

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
- Anonymized enterprise cases:
  - **"The Three-Year Rewrite" (before AI tools):** from the presenter's
    own experience. Several teams spent more than three years rewriting an
    app, then found it cost more to run than it could ever earn. It was
    scrapped.
  - **Case A, "The Relay" (2025):** an enterprise service template plus a
    separate agent workflow implementation: a reusable instruction file, bootstrap and
    validation prompts, and role agents (ideator → planner → coder → tester)
    that pass work forward through written plans. Used across an AI
    reference architecture (document ingestion, chat orchestration, web UI).
  - **Case B, QRSPI+ (2026):** used by a real enterprise
    team. Its v0.7.2 release was planned, built,
    integrated, and acceptance-tested by the previous version of the
    workflow: 38 tasks in 20 waves, 32 tracked issues closed, 2,083
    automated tests passing
    ([PR #299](https://github.com/dfrysinger/qrspi-plus/pull/299),
    [v0.7.3 release](https://github.com/dfrysinger/qrspi-plus/releases/tag/v0.7.3)).

### External research

| Study | Key finding | Used in |
|---|---|---|
| [DORA 2025 State of AI-assisted Software Development](https://cloud.google.com/blog/products/ai-machine-learning/announcing-the-2025-dora-report) and [AI Capabilities Model](https://services.google.com/fh/files/misc/2025_dora_ai_capabilities_model.pdf) | AI amplifies a team's existing strengths and weaknesses; higher throughput comes with more instability. Small batches, strong version control, internal platforms, and AI access to internal data help. | 1, 8 |
| [METR study of experienced open-source developers](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/) (2025) | Tasks took 19% longer with AI, yet developers believed AI made them about 20% faster. | 2 |
| [METR update](https://metr.org/blog/2026-02-24-uplift-update/) (Feb 2026) | AI now likely speeds developers up, but selection effects (developers refusing to work without AI) prevent a reliable estimate. Present the 2025 result as historical. | 2, 6 |
| [Chroma, "Context Rot"](https://research.trychroma.com/context-rot) (2025) | All 18 models tested got worse as input grew longer. Supports focused context per step. | 2, 3, 6 |
| [Stack Overflow Developer Survey 2026](https://survey.stackoverflow.co/2026/ai) and [results summary](https://stackoverflow.blog/2026/10/06/the-results-of-the-2026-developer-survey-are-here/) | 73% of respondents using AI coding assistants or agents use them daily. 48% trust AI when they can easily validate the answers; only 16% extend that trust to most tasks that are not important work decisions. 38% say their organizations set limits on AI usage. Self-selected survey of Stack Overflow users. | 4, 6 |
| [Mozilla and Ubisoft study of AI review comments](https://www.mozillafoundation.org/ca/research/library/impact-of-llm-based-review-comment-generation-in-practice-a-mixed-open-closed-source-user-study/) | About 7–8% of AI review comments were accepted as written. Small sample with one tool: a single research tool (RevMate) on one off-the-shelf model, across about 587 patch reviews at two organizations. Treat it as indicative that automated review needs human triage, not as a general acceptance rate. | 4 |
| [GitHub Blog, "60 million Copilot code reviews and counting"](https://github.blog/ai-and-ml/github-copilot/60-million-copilot-code-reviews-and-counting/) (2026) | GitHub tunes Copilot code review with a continuous evaluation loop: internal tests against known issues plus production signals (developer reactions and whether flagged issues are fixed before merge). It prioritizes signal over comment volume: in 29% of reviews it says nothing. Vendor-reported figures. | 4, 6 |
| [GitHub's Agentic Engineering System (AES)](https://github.com/resources/insights/agentic-engineering-system) (2026) and [Well-Architected implementation guide](https://learn.github.com/well-architected/governance/recommendations/agentic-engineering-system-on-github) | A tool-agnostic framework for scaling agent use: three "stocks" (governance, shared knowledge, customer value), three activities (define, deliver, detect), and three modes that people or agents can hold (director, performer, assessor). Its test of healthy adoption: as agent use grows, escaped defects stay flat or fall and shared knowledge improves alongside delivery speed. A vendor framework, not an empirical study. | 6 |
| [Stanford, "Canaries in the Coal Mine"](https://digitaleconomy.stanford.edu/news/canariesaug26/) (revised Aug 2026) | Employment of 22–25-year-olds fell in AI-exposed jobs, including software development, mainly through reduced hiring; experienced workers in jobs built on tacit knowledge grew. Descriptive, not causal. | 7 |
| [Anthropic, "How AI Impacts Skill Formation"](https://arxiv.org/abs/2601.20245) (2026) | Developers learning a new library with AI scored 50% vs 67% without, with the biggest gap in debugging; using AI to explain concepts preserved learning. | 7 |
| [HBS and P&G, "The Cybernetic Teammate"](https://aiinstitute.hbs.edu/the-cybernetic-teammate-how-ai-is-reshaping-collaboration-and-expertise-in-the-workplace/) | In a randomized study of 776 professionals, individuals with AI matched two-person teams without AI, and AI reduced expertise silos. Product development, not software. | 7 |
| [Anthropic Economic Index: software development](https://www.anthropic.com/news/impact-software-development) (2025) | 79% of Claude Code conversations were automation (delegation) rather than augmentation. | 5, 7 |

## Outline (about 50 minutes before Q&A)

### 0. Cold open: "The app worked. It just existed twice." (3 min)

- Show BeamRS working.
- Reveal the bug from the Leptos upgrade: the browser built a second copy of
  the whole interface instead of attaching to the page the server had already
  rendered.
- Ask: *"Would you have approved this if the demo looked right?"*
- Deliver the thesis.

### 1. The bottleneck moved (6 min)

- Ask: *"If code took no time to write tomorrow, what would still stop your
  team from shipping?"*
- Use the answers (unclear requirements, review, integration, risk) to frame
  the shift.
- **Enterprise case: "The Three-Year Rewrite" (before AI tools).** Several
  teams spent more than three years rewriting an app. When it was done, the
  app cost more to run than it could ever earn in revenue, and it was
  scrapped.
  - The teams didn't have a speed problem. They completed a great deal of
    work; none of it could ever pay for itself.
  - Ask: *"With today's agents, what would have changed?"* Answer: they
    could have reached the same dead end in one year instead of three, or
    built something three times bigger that lost three times as much.
  - Hook: *"Agents make building cheap. They don't make it worth building."*
  - Hook: *"We measured how much we finished. Nobody measured whether it
    was worth finishing."*
- **Value of completed work over amount of work completed:**
  - **Output isn't outcome.** Tasks closed, pull requests merged, story
    points, and lines generated measure activity, not value. Agents inflate
    all of them.
  - **Unfinished work is inventory.** Until it reaches users and earns or
    saves something, it's a cost. Agent-written code adds to that pile
    faster.
  - **Every line is a liability.** Code has to be reviewed, run, secured,
    and maintained. Cheap to write doesn't mean cheap to own.
  - **Know the economics early.** What will it cost to run, per user or
    transaction, including agent and model costs, against what it will earn
    or save? Ship a thin slice to production early to find out.
  - **Agree on stopping criteria up front.** Decide what result would make
    the team stop, before the sunk cost makes stopping feel impossible.
  - Visual: [“Museum of Meaningless Metrics”](https://gambleblog.blob.core.windows.net/backgrounds/post-359-feature-1782352019832-Museum_of_Meaningless_Metrics.png), credited to Gamble Blog on the corresponding deck slide.
- Analogy: agents add lanes, but review is still a one-lane exit ramp. And
  the highway still has to lead somewhere worth going.
- Research: DORA 2025 calls AI an amplifier. It raises throughput and
  instability together, and magnifies whatever system it lands in,
  including a team building the wrong thing.
- Transition: if the constraint moved, the process has to change too, and
  it has to start with why the work is worth doing.

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
  hard limits. Chroma's "Context Rot" study backs the direction: every model
  tested degraded as input grew.
- Audience moment: ask how much faster AI makes them, then show METR 2025
  (19% slower while feeling about 20% faster). Follow immediately with METR's
  2026 update: AI likely helps now, but self-perception is unreliable.
  *"Plausible isn't proven applies to how fast we feel, too."*
- **Enterprise case A: "The Relay."** Named for its role agents
  (ideator → planner → coder → tester), each handing a written plan to the
  next like a baton. It worked well
  enough to ship real features, and it shows all three lessons:
  - **What worked:** an 11-line human feature request became a
    ~290-line, agent-written plan with research, tasks, and validation
    gates. Standard validation scripts (start, health check, test, lint,
    logs, stop) gave agents one dependable way to run and check the
    system.
  - **Instruction overload:** one instruction file holds a wall of
    "ALWAYS" and "NEVER" rules, repeated in each agent file.
  - **Magic words:** the instructions tell the agent to "ULTRATHINK" for
    hard problems. A literal magic word.
  - **Persuasive plans:** plans grew to 700–1,400 lines and ended with the
    agent's own confidence score.
  - **The agent graded its own homework:** a validation report marks
    "unit tests pass with >90% coverage" as ✅ PASS, and its own evidence
    column says 83%. Other criteria were marked done because the code
    "was verified," not because anyone tested them.
  - Hook: *"The report said PASS. The number next to it said otherwise.
    Plausible isn't proven."*
  - Hook: *"Our first process asked the agent how confident it was. Our
    second asked another agent to prove it wrong."*

### 3. Turn the process into infrastructure (7 min)

- QRSPI+ as one implementation, not the only answer. Three blocks:

  | Block | What happens | Human responsibility |
  |---|---|---|
  | **Align** | Goals, research, design, delivery slices | Decide what to build and why |
  | **Execute** | Task specs, safe parallel work, isolated implementation | Set boundaries, resolve big decisions |
  | **Verify and learn** | Review, integrate, test, replan | Own the outcome, improve the process |

- Ideas to highlight: written records at each step, focused context, approval
  gates, vertical slices, rules the process enforces rather than reminders.
- Value comes first: the first step records why each goal matters before
  any research or code, and vertical slices reach working software early
  enough to test whether it's worth continuing. The Three-Year Rewrite had
  neither.
- Hook: *"We deliberately hide from the research agent what we want"*, like a
  blind trial.
- Hook: *"The agent cannot write production code until a failing test
  exists."*
- Be honest about costs: more steps and slower starts. Use the quick-fix route
  for small changes.
- **Enterprise case B: QRSPI+ in a real enterprise (2 min).** The same workflow used by an enterprise team also built its own
  next release.
  - **The run:** one release of 38 tasks, split into 20 waves of parallel
    work, each task built in isolation, then merged, reviewed, and
    acceptance-tested. It closed 32 tracked issues and finished with 2,083
    automated tests passing.
  - **What the gates caught:** during acceptance testing, an independent
    test-writing agent found that a security safeguard had silently
    disappeared. A merge labeled as combining two tasks had actually
    combined the wrong pair, so the safeguard's task was dropped. Integration
    review missed it; the acceptance agent caught it, and the fix was
    re-landed with 4 of 4 acceptance tests passing.
  - **Honest reporting:** the release record left 3 of 7 acceptance criteria
    unchecked and explained why, instead of declaring everything done.
    Contrast with The Relay's self-graded ✅ PASS next to 83%.
  - **The process improved itself:** the run filed 15 new issues about its
    own gaps. The next release (v0.7.3) added an automatic check that every
    merge contains exactly the planned tasks, and capped the active
    instructions under a measured budget (under 30,000 tokens), a direct
    answer to The Relay's instruction overload.
  - Two implementations side by side:

    | | The Relay | QRSPI+ |
    |---|---|---|
    | Who checks the work | The agent grades itself | Independent agents, then a person |
    | Instructions | One growing file of rules | Focused steps, measured size budget |
    | Research | Knows what we want | Hidden from what we want |
    | Code before tests | Not enforced | Blocked until a test fails |
    | When something slips | Report still says PASS | Caught, re-landed, and turned into a new automatic check |

  - Hook: *"The safeguard vanished in a merge. Integration review missed it.
    An agent whose only job was to doubt the result caught it."*
  - Hook: *"The Relay asked each runner how their leg went. QRSPI+ asked
    another agent to prove the work wrong, then added a check so that mistake
    can't slip through silently again."*
- What carried over from The Relay: standard validation scripts and
  shared instruction files became the foundation, not the whole process.

### 4. Two layers of agent review (8 min)

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

Research context:

- Stack Overflow 2026: 48% of developers trust AI when they can easily
  validate the answers. Layered review is how a team makes answers easy to
  validate.
- Mozilla and Ubisoft: only about 7–8% of AI review comments were accepted as
  written. This was a small study of one research tool, so treat it as
  indicative rather than a general rate. Contrast with BeamRS, where findings
  were specific and actionable, and note that humans still triaged every one.
- GitHub Blog (2026): Copilot code review is tuned for signal rather than
  comment volume, using evaluation against known issues and whether flagged
  issues are fixed before merge. Vendor-reported, but it shows a reviewer
  being evaluated and improved like any other system.

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

### 6. The hard parts of agentic engineering systems (5 min)

An agent workflow is itself a system that has to be engineered: evaluated,
limited, connected, and maintained. These problems remain even when the
workflow works.

- **English is the programming language.** Natural-language instructions are
  inherently imprecise, and the model running them is non-deterministic. The
  same prompt can produce different results, and every ambiguity is
  interpreted differently on each run.
  - Pin intent down with things that are precise: acceptance tests, worked
    examples, schemas, and scripts.
  - Hook: *"When English is the programming language, every ambiguity is a
    bug you haven't found yet."*
- **Defining how to evaluate and improve the system.** Decide what a better
  run means before changing the workflow: a fixed set of representative
  tasks, a baseline, and outcome measures such as validated delivery time,
  rework, escaped defects, review effort, and cost.
  - Case B filed 15 issues about its own process gaps, then turned them into
    automatic checks in the next release. Improvement needs that loop, not
    occasional prompt tweaks.
  - GitHub's Copilot code review team describes the same loop: evaluate
    against known issues, then track production signals such as whether
    flagged issues get fixed.
- **Setting usage limits.** Agents spend tokens, model requests, time, and
  money, and can retry or loop without converging. Set budgets per task and
  per run, cap retries and parallel work, and stop or escalate when a limit
  is reached.
  - The cost to run the process belongs in the same economics as the cost to
    run the product.
  - Stack Overflow 2026: 38% of respondents say their organizations set
    limits on AI usage.
- **Deterministic handoffs.** When one agent hands work to another through
  prose, the next agent has to interpret it. Hand off structured artifacts
  that a script can check: required sections, task IDs, file lists, and
  test results.
  - The Relay passed long written plans forward. Case B added an automatic
    check that every merge contains exactly the planned tasks after a merge
    silently dropped a security safeguard.
- **Confirmation bias about the system itself.** Teams judge a workflow by a
  few memorable runs. That can mean keeping a change that made results worse
  because it feels better, or abandoning a useful one after a single bad run.
  - Compare against the baseline across several runs; the METR results
    showed how unreliable "it feels faster" can be.
  - Hook: *"We hid our preferences from the research agent. Hide them from
    the evaluation too."*
- **Trimming the fat.** Workflows accumulate steps, rules, reviewers, and
  instructions. Each one costs time, tokens, and attention, and extra
  instructions bring back instruction overload.
  - Track what each gate catches; remove or merge steps that never catch
    anything. Case B's measured instruction budget is one example; the
    quick-fix route is another.
  - Hook: *"Every step in the process should earn its place, just like every
    line of code."*
- **One framework for all of it: GitHub's Agentic Engineering System
  ([AES](https://github.com/resources/insights/agentic-engineering-system)).** The lessons in this talk map onto its parts:
  - **Stocks:** governance (unskippable checks, permissions, limits), shared
    knowledge (focused context, structured handoffs), and customer value
    (value of completed work, not amount of work completed).
  - **Activities:** define, deliver, detect. Roughly the QRSPI+ blocks of
    align, execute, and verify and learn.
  - **Modes:** director, performer, assessor. Not job titles; people and
    agents move between them depending on risk.
  - Its health check matches our evaluation advice: as delivery speeds up,
    escaped defects should stay flat or fall, and shared knowledge should
    get better, not worse.
  - Transition: the modes lead straight into what changes for careers and
    teams.

### 7. What changes for careers and teams (7 min)

- Organize around responsibilities, not invented job titles:

  | Responsibility | How it changes |
  |---|---|
  | Product and domain leadership | Makes intent, constraints, success criteria, and the value case explicit |
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
  - Stanford "Canaries" (Aug 2026): early-career employment fell in AI-exposed
    jobs, mainly through reduced hiring (descriptive, not causal).
  - Anthropic skill-formation study: learning with AI scored 50% vs 67%,
    with the biggest gap in debugging, unless AI was used as a tutor.
- Team shape: HBS/P&G "Cybernetic Teammate" found individuals with AI matched
  two-person teams without it and broke down expertise silos. Ask: *"If one
  person with AI performs like a team, what is the team for?"*
- Anthropic Economic Index: 79% of coding-agent conversations were delegation,
  not collaboration. The work is shifting from doing to directing and
  verifying.
- Career skill: *"Could you explain why that code was wrong?"* And: *"Could
  you explain why it was worth building?"* Engineers who understand the cost
  to run and the value delivered become more valuable as code gets cheaper.
- Org chart exercise: add agents as boxes and ask, *"Where do the review
  arrows go?"*
- Enterprise cases: two or three contrasting team designs, including one that
  did not work.

### 8. The process is a product (4 min)

**This talk was built the same way (1 min).** Show the outline repository's
history as a short case study:

- **Start from intent:** the abstract went to an agent, which proposed a
  first set of sections.
- **Add sources, then research:** the blog post, QRSPI+, GitHub Agentic
  Workflows, BeamRS, and outside studies were added in rounds.
- **Repeated passes:** separate passes for flow, messaging, hooks, and the
  final outline, rather than one big prompt.
- **Check claims against evidence:** BeamRS details were checked against git
  history and pull request review comments. Research figures were checked
  against the original papers, which disagreed with some secondary summaries.
- **The human corrected the story:** the agent's first draft said people
  found the BeamRS problems. The author corrected it: agents found all of
  them. The author also made editorial calls, such as dropping a source.
- **Coordinate the agents:** when two agent sessions started the same update,
  one was stopped before it could push conflicting changes.
- **Keep a record:** the outline lives in a version-controlled repository, so
  every change is visible.
- Hook: *"Even this talk went through goals, research, review, and human
  correction. The agent drafted; I decided what was true and what mattered."*

- Start small: one workflow, clear permissions, defined checks, learn from
  each run.
- Measure the value of completed work, not the amount of work completed:
  outcomes reached by users, cost to run (including agent and model costs),
  validated delivery time, review effort, rework, and late defects. Not
  tasks closed, pull requests merged, or code generated.
- Hook: *"Every finding should make the next run harder to fool."*
- One next step per audience:
  - **Individual contributors:** write goals and a design before involving an
    agent on one change this week; compare with your usual approach.
  - **Managers:** measure how much time people spend reviewing agent output
    before adding more agents. For your next large project, write down what
    it must earn or save, what it will cost to run, and what would make you
    stop.
  - **Platform leaders:** turn one repetitive repository task into an
    automated workflow with clear permissions and review.

### Close

- Return to the opening BeamRS screen: *"How would your team have known?"*
- Then to the rewrite: *"And how would they have known it was worth
  building at all?"*
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
- Tell the Three-Year Rewrite as a personal story without naming the company,
  app, or teams. Use only figures you can stand behind.
- Describe Case B only as used in a real enterprise; don't name the
  enterprise or team.
- Anonymize Case A before showing anything: remove internal application
  IDs, file paths, user names, and service names. Present it as a
  implementation that worked and taught us, not as a failure.
- Check every research figure against its primary source before putting it on
  a slide.
