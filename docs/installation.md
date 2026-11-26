# Install Worth Building

The portable package is `skills/worth-building/` in this repository. Copy the entire folder, including `SKILL.md`, `references/`, `assets/`, and `LICENSE`. The final path must end in `worth-building/SKILL.md`. The install commands below use macOS or Linux shell syntax and start from the repository root. Replace an older copy deliberately if you have already installed one.


Get the repository locally if needed.

```sh
git clone https://github.com/ferdinandobons/worth-building.git
cd worth-building
```

The paths and invocation methods were checked against the official documentation on November 26, 2026. [Agent Skills specification](https://agentskills.io/specification)

## Codex

To install for your account, copy the skill into the user skills directory.

```sh
mkdir -p "$HOME/.agents/skills"
cp -R skills/worth-building "$HOME/.agents/skills/"
```

For one project, copy it into that project's `.agents/skills/` instead. In Codex CLI or the IDE extension, run `/skills` or type `$` and select `worth-building`. In the desktop app, look for it in Skills or select it in the composer. Restart the client if it does not appear after copying. [OpenAI's local installation and invocation guide](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)

## Claude Code

To install for your account, copy the skill into Claude Code's personal skills directory.

```sh
mkdir -p "$HOME/.claude/skills"
cp -R skills/worth-building "$HOME/.claude/skills/"
```

For one project, copy it into that project's `.claude/skills/` instead. Start a local Claude Code session, type `/` to look for the skill, and invoke `/worth-building` followed by your question. The above personal directory applies to local Claude Code. [Anthropic's Claude Code skill guide](https://code.claude.com/docs/en/skills#choose-where-skills-load)

## Gemini CLI

To install for your account, copy the skill into Gemini CLI's user skills directory. If you already copied it into `~/.agents/skills/` for Codex, Gemini CLI also discovers it there.

```sh
mkdir -p "$HOME/.gemini/skills"
cp -R skills/worth-building "$HOME/.gemini/skills/"
```

For one workspace, copy it into that workspace's `.gemini/skills/` or `.agents/skills/`; project discovery is subject to workspace trust. In an interactive session, run `/skills list`. If installed during the session, run `/skills reload`, then `/skills list`. Ask Gemini to use `worth-building` by name and follow the client's approval prompt if one appears. [Google's Gemini CLI skill guide](https://geminicli.com/docs/cli/skills/)

## Check that it works

In a client that selects skills automatically, start a new conversation and send a plain-language prompt.

> I have an idea for a paid app that gives freelancers a place to share updates with clients. Is it worth building? Help me figure out what I'd need.

A suitable reply identifies the likely problem as a hypothesis and starts with a useful question or check, such as how a freelancer handled their last client update. The host decides whether to select the skill. In Gemini CLI, approve activation if prompted. You can also select `worth-building` explicitly using the instructions for your client above.

To uninstall, remove only the installed `worth-building` folder from the location where you copied it and start a fresh session if necessary.

## Use it manually in another chat

If your client has no Agent Skills loader, attach or paste `SKILL.md`, the [evidence rubric](../skills/worth-building/references/evidence.md), and the [reflection rubric](../skills/worth-building/references/reflection.md). Add the opportunity mapping, web research, interview, or experiment guide when relevant. Explicitly ask the assistant to apply those instructions to your decision. A chat without file or web tools can still work from material you paste. This gives you a manual workflow within that conversation.
