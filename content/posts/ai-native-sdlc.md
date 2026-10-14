---
date: '2026-10-14T11:20:00+02:00'
title: 'Close the Border Between Jira and GitLab'
---
Picture a border crossing between two countries that don't trust each other's paperwork. One side speaks in story points, epics, and sprint velocity. The other speaks in commits, pipelines, and pull requests. Nothing moves from one territory to the other without stopping at the checkpoint: a human stands there, reads the ticket, translates it into something the engineering side understands, stamps it, and waves it through. Then, on the way back, the same human does the translation in reverse: status updates, re-estimates, "where are we on this."

That checkpoint is most software delivery organizations today.

Jira, Linear, Azure Boards on one side. GitLab, GitHub, Jenkins on the other. Two sovereign territories, each with its own currency, its own customs, its own paperwork. And standing at the border, forever, are engineering managers, product owners, and tech leads whose real job has quietly become customs clerk: moving intent across a line that two separate tool ecosystems refuse to cross on their own.

That's the overhead. Not the tools themselves. The checkpoint between them.

Anthropic's [AI-Native SDLC Playbook](https://academy.claude.com/courses/ai-native-sdlc-playbook) walks the whole crossing, gate by gate, across all six stages of the SDLC: Plan, Design, Build, Test, Deploy, Maintain. Each gate used to need a person standing in it. Here's what happens when it doesn't.

## The intake counter (Plan)

Today, an idea arrives at the border as a backlog entry, gets interviewed in a refinement meeting, becomes a user story, picks up story points, and changes hands at every step until almost nobody remembers what the traveler originally asked for.

The fix: the person with the idea talks straight to the [consulate officer](https://academy.claude.com/courses/ai-native-sdlc-playbook/capture-intent). Claude asks about scope, users, constraints, and success criteria, then writes it down in the traveler's own words as `intent.md`, a version-controlled proto-spec committed straight into the repo, author and timestamp attached, full history intact. No handoffs. No retelling the story four times to four different people.

## One counter, not two (Design)

Border crossings used to split "what are you bringing" from "how will it be inspected" into two separate queues, staffed by two separate departments, on two separate days. [Requirements and design](https://academy.claude.com/courses/ai-native-sdlc-playbook/requirements-and-design) now happen at the same counter, in the same sitting. Claude reads the `intent.md`, applies the organization's own standing regulations (brand, security, compliance, UX, encoded as skills), and drafts `spec.md`. If the traveler's declared goods conflict with a rule, say a UI pattern collides with a compliance policy, it gets flagged right there and routed to the department that owns that rule instead of being discovered three weeks later at a different gate.

## The stamped itinerary (Build)

Before anyone used to get past the gate, they'd just wing it: code first, explain later, let the reviewer untangle the diff afterward. [Plan mode](https://academy.claude.com/courses/ai-native-sdlc-playbook/plan-mode) hands over a stamped itinerary first, `plan.md`, naming exactly which files change, in what order, and how the work gets verified, before a single line of code is written. Correcting an itinerary is a five-minute edit. Correcting a finished trip is a rewrite. Once the itinerary holds up often enough, the escort stops walking every step with you.

## Standing orders at every booth

A border only runs consistently if every booth enforces the same rule the same way. [`CLAUDE.md`](https://academy.claude.com/courses/ai-native-sdlc-playbook/claude-md) is the standing-orders binder at the local station, the knowledge that used to live in people's heads and in a wiki nobody read. Make the same mistake twice, and the correction goes into the binder. [Skills](https://academy.claude.com/courses/ai-native-sdlc-playbook/skills-as-institutional-knowledge) are the regulation leaflets issued to every booth at once, so a security rule doesn't depend on which officer happens to be on shift. And where a leaflet can still be ignored, a hook is the turnstile arm that mechanically won't lift if the checklist fails.

## More than one lane open

Nothing says a border needs exactly one open lane. With [parallel sessions and subagents](https://academy.claude.com/courses/ai-native-sdlc-playbook/parallel-sessions-and-subagents), one engineer runs several Claude Code sessions at once, each in its own worktree so the bags never get mixed up, while a scoped subagent gets sent to physically confirm a shipment arrived before the lane closes the case. The limit isn't how fast one lane moves. It's how many lanes one person can run well.

## The scanner on the belt (Test)

The old model found problems after the shipment had already crossed: in staging, in a bug report, in production. A [feedback loop](https://academy.claude.com/courses/ai-native-sdlc-playbook/give-claude-a-feedback-loop) puts the scanner right on the belt, so Claude catches and fixes its own mistake on the first pass instead of handing a person a finished diff to untangle. [Continuous evals](https://academy.claude.com/courses/ai-native-sdlc-playbook/continuous-evals-in-ci) retest that scanner against twenty or fifty real past shipments every time its settings change, and every incident that ever got through becomes a permanent test, so it can't get through twice. Review itself stops being one person staring at an entire diff: [named review passes](https://academy.claude.com/courses/ai-native-sdlc-playbook/ai-in-the-pr-review-loop) for bugs, security, and compliance against `spec.md` and `plan.md` catch what a single reviewer reading the diff cold would miss, and surface only what actually needs a human's judgment.

## Not every gate opens the same way (Deploy)

The domestic hall opens on its own. The connecting-flights hall needs a nod or a pre-approved ticket. International arrivals needs a named officer's signature against a specific ticket number, no exceptions, no badge that skips the line. That's [hooks as approval gates](https://academy.claude.com/courses/ai-native-sdlc-playbook/hooks-as-approval-gates) and [tiered autonomy in CI/CD](https://academy.claude.com/courses/ai-native-sdlc-playbook/ci-cd-integration-and-deployment): dev deploys freely, staging needs an approval or a merge to main, production needs a release manager's authorization matching the change. The agent may walk right up to that last gate. It cannot walk through it alone.

## The border never stops watching (Maintain)

Once the crossing is open, it keeps being watched. A small deviation from the baseline just gets logged. A bigger one gets [diagnosed](https://academy.claude.com/courses/ai-native-sdlc-playbook/closing-the-loop-on-metrics) by an agent reading the evidence. A deviation big enough to matter trips a pre-approved, gated response: a rollback runbook, a pull request opened straight into review, nobody paged at 3am for something the system already knows how to fix. Whatever it finds gets written up as a fresh `intent.md`. The loop that started the whole journey starts again, on its own.

## More engineering, less overhead

None of this removes judgment from the process. A human still approves the spec, still signs off the plan, still authorizes the production gate. What disappears is the checkpoint between the people who decide what to build and the people who build it: the retyping, the re-estimating, the status meeting that exists only because two tool ecosystems can't read each other's paperwork.

The organizations that win the next few years of software delivery won't be the ones with the best Jira workflow or the cleanest GitLab pipeline. They'll be the ones who noticed that the real throughput loss was never inside either tool. It was the checkpoint between them, repeated across the entire lifecycle, and they closed every one.

Stop staffing the border. Let the engineers engineer.
