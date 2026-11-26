# worth-building

![worth-building. Another idea. Another dead end? An AI skill to help you find problems worth solving. A clock, star, coin, and battery sit among tangled strands. Three intact mesh screens catch the red, yellow, and purple strands. The green strand breaks through its own mesh and continues beneath a smiling face.](assets/banner.png)

## Is this idea worth building?

You can already picture the first version. Before you give it another weekend, find out who has the problem, what they do about it today, and what would make the next step worth your time.

**worth-building** is an open-source AI skill for independent builders doing startup idea validation, customer discovery, or deciding whether to continue a side project. Bring the idea you're tempted to start. You'll work toward one decision and a next step that fits what you know and the time and money you can spare.

## Try it with your idea

[Install Worth Building](#install-it) on your preferred assistant. Replace the bracketed text with your idea and tell your assistant what you're thinking of doing.

> I'm thinking about [what you'd like to build or try]. Is it worth pursuing? What would I need to make it work?

If your client selects skills automatically, talking about a new idea can bring in Worth Building. The skill starts from what you've said, then asks the question most likely to change your next step. Bring back what you learn and pick up from there. [See the worked example](examples/worked-examples.md#a-guided-review-from-one-idea).

Expect it to ask what you've actually seen and what could prove the idea wrong. When it can browse, it checks public claims against sources and looks for existing alternatives. The recommendation changes when new evidence changes the case.

## From the first idea to the next decision

- **You're unsure what the problem is.** Reconstruct the last time someone faced it. Use interviews and web research to check how they handled it and what it cost them.
- **You have several ideas or ways to solve a problem.** Compare the outcomes, what each option would displace, and which small test could change your choice.
- **You know what to test but keep putting it off.** Set up a repeatable first action. If you need to reach people, share one useful piece of work and look for specific responses from people who've faced the problem.
- **People are already using or paying for a pilot.** Carve out one complete result you can deliver within a fixed limit. Check the time, cost, and quality, and see whether someone else can run it before you expand.

| Decision | What to do next |
| --- | --- |
| **GO** | Take the specific step the evidence supports, with a limit and a review date. |
| **TEST** | Run the smallest credible check that could change your decision. |
| **HOLD** | Revisit when a specific constraint clears. |
| **STOP** | Close this direction when the evidence or a binding constraint rules it out. |

## Install it

Worth Building packages the same [open-source skill](skills/worth-building/SKILL.md) for OpenAI and Claude. It uses your assistant's web search when available. You can also provide links and notes yourself.

### Codex

Run in a terminal with a recent Codex CLI.

```sh
codex plugin marketplace add ferdinandobons/worth-building
codex plugin add worth-building@worth-building-tools
```

Start a new session and select Worth Building from the composer, or ask Codex to use it by name. In the ChatGPT desktop app, you can also open the cloned repository in Codex, then install Worth Building from its repository source in **Plugins**. For the Codex IDE extension, use the [standalone skill](docs/installation.md#standalone-skill). [OpenAI plugin commands](https://learn.chatgpt.com/docs/developer-commands?surface=cli#codex-plugin)

### ChatGPT and ChatGPT Work

For a private install, create the [OpenAI plugin ZIP](#build-the-plugin-zips). In ChatGPT Work, attach it in a chat with **Plugin Creator** and ask it to save the archive as a private plugin. Open the returned plugin link and select **+** to install. In a new Chat or Work conversation, select **@Worth Building**. Use the same account or workspace where you saved it. This route requires access to Plugin Creator and permission to install custom plugins. [OpenAI plugin guide](https://learn.chatgpt.com/docs/plugins#install-and-use-a-plugin)

Workspace admins can also go to **Admin → Plugins → Add → Import marketplace** and enter `https://github.com/ferdinandobons/worth-building`. Leave **Path** empty, review the import, and set who can install it. [OpenAI workspace import guide](https://learn.chatgpt.com/docs/enterprise/plugin-management#configure-a-marketplace-sync)

### Claude Code

Run in a terminal with a recent Claude Code installation.

```sh
claude plugin marketplace add ferdinandobons/worth-building
claude plugin install worth-building@worth-building-tools
```

Start a new Claude Code session and use `/worth-building:worth-building` followed by your idea. If you already enabled the plugin in your Claude account, it also syncs to Claude Code 2.1.273 or later when you sign in to the same account. [Claude Code plugin guide](https://code.claude.com/docs/en/plugins/install)

### Claude and Cowork

In Claude on the web, open **Plugins → Add → Add marketplace**, enter `ferdinandobons/worth-building`, then open the marketplace and add Worth Building. For a ZIP install, create the [Claude plugin ZIP](#build-the-plugin-zips) and select it via **Plugins → Add → Upload plugin**. If your interface shows **Customize**, open **Customize → Plugins** to find these options.

Check that Worth Building is enabled in **Your plugins**. In a new Claude chat or Cowork task on the same account, open the skill picker with **+** or **/** and select Worth Building. Plan and organization settings control which install options are available. [Claude plugin guide](https://support.claude.com/en/articles/13837440-use-plugins-in-claude)

### Build the plugin ZIPs

Run these commands in a terminal. Each ZIP includes its platform's manifest and all the skill's supporting files.

```sh
git clone https://github.com/ferdinandobons/worth-building.git
cd worth-building
git archive --format=zip -o ../worth-building-openai.zip HEAD plugin.json skills/worth-building
git archive --format=zip -o ../worth-building-claude.zip HEAD .claude-plugin/plugin.json skills/worth-building
```

The [installation guide](docs/installation.md) covers standalone installs for Codex, Claude Code, and Gemini CLI, plus updates, removal, and use in other chats.

## Explore the method

- [Find and compare problems](skills/worth-building/references/opportunity-mapping.md)
- [Research alternatives](skills/worth-building/references/web-research.md) and [run customer discovery interviews](skills/worth-building/references/interviews.md)
- [Assess the evidence](skills/worth-building/references/evidence.md) and [check what the project would displace](skills/worth-building/references/reflection.md)
- [Generate and try creative options](skills/worth-building/references/creative-discovery.md) and [make learning repeatable](skills/worth-building/references/learning-rhythm.md)
- [Design an experiment](skills/worth-building/references/experiments.md) and [record the decision](skills/worth-building/assets/decision-brief.md)
- [Share work to learn from feedback](skills/worth-building/references/sharing-and-feedback.md) and [test whether delivery is sustainable](skills/worth-building/references/delivery-and-operations.md)
- [Worked examples](examples/worked-examples.md) and [Worth Building's self-assessment](examples/self-assessment.md)

The worked examples are fictional. The self-assessment explains what would demonstrate that builders find the skill useful and choose to use it again.

## License

[MIT](LICENSE)
