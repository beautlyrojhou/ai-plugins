---
name: receiving-work-transitions
description: The tech lead's playbook for receiving ownership of work from another team — initiative handoffs from shepherds, frameworks from Platform, operational responsibilities from SRE, or any other sustained transfer of logic, patterns, tooling, or processes. Applies Bitwarden's Work Transition Playbook from the receiving side. Use when your team is about to take on transferred work, when you're preparing for a transition session, when the support period is underway, or when you need to run a pulse check or retrospective on a handoff.
---

Bitwarden uses a [Work Transition Playbook](https://bitwarden.atlassian.net/wiki/spaces/EN/pages/2521038855) to move ownership of logic, patterns, tooling, or processes between teams. The most common trigger is Phase 4 → 5 of an initiative: a shepherd has finished Scoping & Commitment and your team is about to own implementation. But the playbook is general — Platform might hand your team a framework, SRE might hand over a runbook, another product team might transfer an integration they no longer own. Same playbook applies.

This skill is written from the **receiving** side. It complements `Skill(navigating-the-initiative-funnel)`, which covers the funnel mechanics more broadly.

## What "Transition" Actually Means

Read this line from the playbook and make sure your team acts on it: **a successful transition is not the moment documentation is shared or a meeting is held — it is the moment the receiving team is confidently operating independently with the transferred work**.

Everything in the six phases below is in service of that outcome. Sessions, documentation, and pulse checks are instruments, not the goal.

## The Six Phases, From Your Side

### Phase 1 — Preparation

Before any transition session is scheduled, the originating team prepares materials. Your job is to evaluate those materials before accepting the transition.

Things to confirm:

- **Documentation is adequate.** You should be able to hand the docs to a competent engineer on your team and have them work with the material independently. If the docs are thin, push back — don't accept a transition you can't sustain.
- **Jira is legible.** Epics have descriptive summaries. Stories exist at a level of detail you can refine further — not so specific that you're handed a pre-written sprint plan, not so vague that your team has to re-research the scope.
- **Stakeholders and points of contact are identified.** You know who from the originating side carries context you may need during the support period. You know which adjacent stakeholders (leadership, PMs, other teams) will care about progress.
- **Your side has a named primary POC** (usually you as the tech lead, sometimes a senior engineer on your team). Your EM is aware and supportive.
- **Post-handoff effort is evaluated honestly.** Transitions that only plan for "adopting the new thing" underestimate the true cost. Evaluate three axes explicitly:
  - **Implementation and integration.** What effort is required to put the transferred work into practice in your team's domain? Adapting patterns, wiring integrations, writing tests, updating workflows.
  - **Phasing out old processes and code.** If the new work replaces something that already exists, decommissioning that thing is its own scope. Your team usually has the deepest knowledge of what the old approach actually does in practice — use it.
  - **Ongoing maintenance and bug fixes.** Once the support period ends, who owns what? For most transitions, you own everything you adopted. For shared frameworks or libraries, the originating team may retain some maintenance — confirm explicitly where the ownership boundary sits.

If any of those are unclear, name it now. The preparation phase is where gaps are cheapest to fill.

### Phase 2 — Transition Sessions

At least two sessions, spaced 1–2 weeks apart. Your job is to show up prepared and come back with sharper questions the second time.

- **Session 1 (context and approach).** Review the documentation before the session — ideally a few business days in advance. In the session: understand the problem being solved, why this approach was chosen, walk the PoC or framework, understand how the work fits into the broader initiative. Open Q&A. This session is mostly listening.
- **Session 2 (hands-on and planning).** By now your team should have spent time with the code or tooling. Bring the questions that only emerge from reading the actual implementation. Discuss how your team will integrate, extend, or schedule the work. Surface gaps in the documentation. Agree on what the support period looks like.

Additional sessions are warranted for complex or high-stakes transitions. Both sides decide at the end of Session 2 whether more are needed.

### Phase 3 — Support Period

After the sessions, the originating team stays available — but shifts from leading to supporting. Typical duration: 4–8 weeks, proportional to complexity.

What to use the originating team for:

- Approach questions, intent, and edge cases that documentation doesn't cover.
- Early-PR alignment review — they catch misalignment with the intended pattern while it's cheap to correct.
- Evaluating options if a production reality suggests the original approach needs adjustment.

What not to use them for:

- Gatekeeping your team's work. They're advisors, not approvers.
- Doing the work for you. A transition is a transfer, not a loaner.

A critical framing from the playbook: **a completed transition does not mean the receiving team will begin work immediately**. The transferred work competes with your team's existing priorities — product roadmap commitments, other initiatives, bugs, tech debt. A delay between handoff and active work is normal and expected.

**What is not normal:** the originating team quietly resuming the work because your team hasn't prioritized it. That's a leadership conversation — between you, the originating team, and engineering leadership — not a workaround. The funnel's Scoping & Commitment phase is where executive capacity is allocated; if that commitment isn't translating into prioritized work, escalate rather than let the originating team fill the gap.

### Phase 4 — Pulse Check (~30 days after transition)

A 15–30 minute conversation, or an async thread. This is the load-bearing checkpoint — it's where "we handed it off" gets prevented from becoming "it was never picked up."

Questions to cover:

- Has your team begun working with the transferred material? If not, what's blocking you?
- Are there unanswered questions, or areas where documentation proved insufficient?
- Is your team comfortable with the approach, or working around it in ways that suggest a mismatch?
- Does the support period need adjustment — extended or shortened?

If your team hasn't started at all, escalate — not punitively. Understand whether it's capacity, priority conflict, or a real gap in the transition. Unaddressed, this is where initiative work dies.

### Phase 5 — Retrospective (~90 days after transition)

A real meeting, 45–60 minutes, with both teams. Goals: assess adoption, give feedback on the transition process, capture lessons for future transitions.

Topics:

- **Adoption assessment.** Is the work being used as intended? Has your team extended it? Are there areas of drift or non-adoption?
- **Transition process feedback.** What worked? What was missing from documentation, sessions, or support period? What would have made it smoother?
- **Lessons for future transitions.** What should change about the playbook itself?
- **Remaining gaps.** Outstanding issues, additional documentation needed, further support required.

Document findings. If the retrospective surfaces process improvements, push them back into the playbook — Bitwarden's transitions get better when teams add what they learned.

### Phase 6 — Closure

The transition is complete when:

- Your team is operating independently with the transferred work.
- The support period has concluded (or been explicitly ended early by mutual agreement).
- The retrospective has been conducted and findings documented.
- Outstanding action items have owners and timelines.

At closure, formally acknowledge the transition is complete. Both teams need the signal: your team is autonomous, the originating team is no longer on the hook unless explicitly re-engaged.

## Adapting the Playbook

The six phases describe a general process. Scale them to the work:

- **Smaller transitions** (single pattern, limited scope): compress the timeline. The pulse check can be a Slack thread; the retrospective can fold into a regular team retro.
- **Larger transitions** (multi-team, high complexity): expect more than two sessions, a longer support period, a more formal retrospective.
- **Urgent transitions** (departures, reorganizations): compress preparation if you must, but do not skip the support period or the follow-up checkpoints. That's where most of the value lives.

The one thing that should not be skipped regardless of scale is the **30-day pulse check**. Everything else can be scaled; that one is the mechanism that prevents silent failure.

## Common Mistakes

- **Accepting a transition with thin documentation.** You will pay for it during Implementation. Push back during Preparation.
- **Treating sessions as the goal.** Sessions are instruments. If your team isn't operating independently 90 days later, the transition failed regardless of how many sessions you ran.
- **Leaving capacity questions unanswered.** "We'll pick it up when we can" is how transitions die. If you don't have allocated capacity, that's a leadership conversation before the transition, not after.
- **Quietly working around the transferred approach.** Drift is cheaper to catch in a pulse check than in a production incident. Surface it.
- **Letting the originating team resume the work.** If your team can't prioritize, escalate to leadership. Don't accept help that re-creates the original ownership.

## Reference

- [Work Transition Playbook](https://bitwarden.atlassian.net/wiki/spaces/EN/pages/2521038855) — canonical. Fetch via `get_confluence_page` for the full phase-by-phase detail, summary table, and adaptation guidance.
- Related: `Skill(navigating-the-initiative-funnel)` for the initiative context that often triggers a transition; `Skill(architecting-solutions)` for the architectural judgment you apply when evaluating what's being handed to your team.
