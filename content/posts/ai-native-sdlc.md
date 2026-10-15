---
date: '2026-10-14T11:20:00+02:00'
title: 'Close the Border Between Jira and GitLab'
---
Picture a border crossing between two countries that don't trust each other's paperwork. One side runs on Jira, Linear, Azure Boards, speaking in story points and sprint velocity. The other runs on GitLab, GitHub, Jenkins, speaking in commits and pull requests. Nothing moves from one territory to the other without a human at the checkpoint: reading the ticket, translating it into something engineering understands, stamping it, waving it through, then translating the status back on the way home.

That checkpoint is most software delivery organizations today.

That's the overhead. Not the tools themselves. The handoff between them.

Anthropic's [AI-Native SDLC Playbook](https://academy.claude.com/courses/ai-native-sdlc-playbook) closes it with a chain of plain Markdown files, each one handed forward instead of retyped.

An idea starts as [`intent.md`](https://academy.claude.com/courses/ai-native-sdlc-playbook/capture-intent): the person with the idea talks straight to Claude, who writes down the problem, the constraints, and the success criteria in their own words. No backlog entry, no refinement meeting, no ownership transfer. Claude turns that into [`spec.md`](https://academy.claude.com/courses/ai-native-sdlc-playbook/requirements-and-design), requirements and design in one sitting, checked against the organization's own policies as it's written rather than discovered weeks later in review. Then comes [`plan.md`](https://academy.claude.com/courses/ai-native-sdlc-playbook/plan-mode): the exact files that change and the order they change in, approved before a single line of code exists. Correcting a plan is a five-minute edit. Correcting a finished diff is a rewrite.

Each file is the handoff. Not a meeting about the handoff, not a status update summarizing the handoff: the artifact itself, committed, versioned, readable by the next person or the next model without translation.

Underneath all three sits [`CLAUDE.md`](https://academy.claude.com/courses/ai-native-sdlc-playbook/claude-md), the standing orders that used to live in someone's head and a wiki nobody read. Make the same mistake twice, and the correction goes in the file instead of staying tribal knowledge that walks out the door with whoever remembers it.

None of this removes judgment. A human still approves the spec, still signs off the plan. What disappears is the retyping: a ticket becoming a task becoming a status update becoming a different ticket, four lossy translations of one idea.

The organizations that win the next few years won't have the best Jira workflow or the cleanest GitLab pipeline. They'll be the ones who noticed the throughput loss was never inside either tool. It was the retyping between them, and a chain of three Markdown files is what makes retyping unnecessary.

Stop staffing the border. Let the engineers engineer.
