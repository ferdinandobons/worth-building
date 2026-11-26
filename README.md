# worth-building

![worth-building. Another idea. Another dead end? An AI skill to help you find problems worth solving. A clock, star, coin, and battery sit among tangled strands. Three intact mesh screens catch the red, yellow, and purple strands. The green strand breaks through its own mesh and continues beneath a smiling face.](assets/banner.png)

The last idea felt right, too. Before the next one takes over your evenings or budget, find out who has the problem, what it costs them, and how they handle it today.

**worth-building** is an open-source Agent Skill for independent builders and small product teams. Bring a rough idea, a handful of observations, or two projects competing for the same time. The skill helps you find a problem worth investigating, check the evidence, and decide how much to commit next.

## Try it

After [installing the skill](docs/installation.md), select or invoke it in your AI client and give it a concrete decision.

> I have six hours this week and keep getting ideas for tools for independent bookshops. Help me find a problem worth investigating. My current priority is finishing a project I already promised to deliver. Start with workflows I can observe. Then tell me what evidence would justify spending more time.

> I'm considering two ideas and can pursue one this month. Here's what people actually did, what they said they might do, and what each option would displace. Give me a decision for each and one observation that could change your mind.

For a quick judgment, share the situation, what you have seen, and how much you are about to spend. For a deeper review, add relevant links or redacted interview notes.

## What you get

- **Find opportunities** by starting with real situations where people wait, rework, improvise, pay for help, or give up.
- **Check the case** through sourced web research, interviews grounded in specific past events, and small experiments with criteria set in advance.
- **Check your own fit** by naming what the idea would displace and what work you would still choose when the novelty passes.
- **Make the next decision** with an evidence trail, countercase, and a limit on the commitment.

| Decision | Next step |
| --- | --- |
| **GO** | Take the named, bounded step supported by the evidence. |
| **TEST** | Run the smallest credible check that could change your decision. |
| **HOLD** | Revisit when a stated constraint clears or at a scheduled review. |
| **STOP** | Close this direction on relevant counterevidence or a binding constraint. |

## Install it

Copy the complete [skill folder](skills/worth-building/SKILL.md), including its supporting files. The [installation guide](docs/installation.md) covers Codex, Claude Code, and Gemini CLI, with official documentation, verification steps, and a manual chat fallback. The skill consists of Markdown instructions and has no runtime dependencies of its own. Web research needs a client with browsing or sources you provide.

## Read or reuse the method

- [Evidence rubric](skills/worth-building/references/evidence.md) and [builder reflection rubric](skills/worth-building/references/reflection.md)
- [Web research workflow](skills/worth-building/references/web-research.md) and [interview workflow](skills/worth-building/references/interviews.md)
- [Decision brief template](skills/worth-building/assets/decision-brief.md)
- [Find and compare problems](skills/worth-building/references/opportunity-mapping.md) and [design the next experiment](skills/worth-building/references/experiments.md)
- [Worked examples](examples/worked-examples.md) and [Worth Building's self-assessment](examples/self-assessment.md)

The repository includes fictional practice cases. Its own usefulness and repeat adoption are still hypotheses. See the self-assessment for the proposed first test.

## License

[MIT](LICENSE)
