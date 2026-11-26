# worth-building

![worth-building. Another idea. Another dead end? An AI skill to help you find problems worth solving. A clock, star, coin, and battery sit among tangled strands. Three intact mesh screens catch the red, yellow, and purple strands. The green strand breaks through its own mesh and continues beneath a smiling face.](assets/banner.png)

## Is this idea worth building?

You have a new idea. You can already picture the features, and part of you wants to spend the weekend building it. Maybe the last idea felt just as convincing. Who has this problem today? What do they already do about it? What would you need to see before giving this idea another weekend?

**worth-building** is an open-source AI skill for validating startup ideas, side projects, and product features. Tell it what you're thinking of building. It helps you find the problem behind the idea, figure out what you still need to learn, and decide what to do next with the time and money you actually have.

## Try it with your idea

[Install worth-building](docs/installation.md) for Codex, Claude Code, or Gemini CLI. Invoke it in your client and explain your idea as you would to a friend. Use this prompt as a starting point.

> I'm thinking of building an app to help independent bookshops track special orders. I have Saturday morning and know two shop owners I can talk to. Is this worth building? Walk me through what to find out first.

With that starting point, the skill could help you ask the owners to walk through their last special order and look for where the current process breaks down. If the problem shows up in both shops, you can compare a change to the existing workflow with an app before you commit to either. [See the worked example](examples/worked-examples.md#a-guided-review-from-one-idea).

## How the guided validation works

- **You have a rough idea.** Start with who would use it, the last time the problem came up, and how they handled it. If you have yet to choose an idea, start with a workflow you can observe.
- **You have some evidence.** Bring customer interviews, web research, or notes from a pilot. The skill checks what they support and asks which missing fact would change your decision.
- **You have a real problem and several ways to solve it.** Compare the options against the same outcome. Check how each would fit the customer's workflow, what switching would take, and what it would cost you to deliver and maintain.
- **You have several projects competing for your time.** Compare them over the same period. Make room for the work you already care about and decide what each new commitment would displace.

You can work through the decision in conversation or get a quick first read. As you bring back evidence, the recommendation can change.

| Decision | What to do next |
| --- | --- |
| **GO** | Take the specific step the evidence supports, with a limit and a review date. |
| **TEST** | Run the smallest credible check that could change your decision. |
| **HOLD** | Revisit when a specific constraint clears. |
| **STOP** | Close this direction when the evidence or a binding constraint rules it out. |

## Install it

Copy the complete [skill folder](skills/worth-building/SKILL.md), including its supporting files. The [installation guide](docs/installation.md) covers Codex, Claude Code, Gemini CLI, and a manual chat option. The skill consists of Markdown instructions. For web research, use a client with browsing or provide links and notes yourself.

## Explore the method

- [Find and compare problems](skills/worth-building/references/opportunity-mapping.md)
- [Research alternatives](skills/worth-building/references/web-research.md) and [run customer discovery interviews](skills/worth-building/references/interviews.md)
- [Assess the evidence](skills/worth-building/references/evidence.md) and [check what the project would displace](skills/worth-building/references/reflection.md)
- [Design an experiment](skills/worth-building/references/experiments.md) and [record the decision](skills/worth-building/assets/decision-brief.md)
- [Worked examples](examples/worked-examples.md) and [Worth Building's self-assessment](examples/self-assessment.md)

The worked examples are fictional. The self-assessment explains what would demonstrate that builders find the skill useful and choose to use it again.

## License

[MIT](LICENSE)
