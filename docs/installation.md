# Install Worth Building

[Start with the plugin instructions](../README.md#install-it) for Codex, ChatGPT, ChatGPT Work, Claude Code, Claude, and Cowork. Use the standalone skill for a project-local install, Gemini CLI, or a client without plugin support. Keep one enabled copy per client to make skill selection and updates predictable.

## Standalone skill

Copy the complete `skills/worth-building/` folder, including `SKILL.md`, `references/`, `assets/`, and `LICENSE`. The final path must end in `worth-building/SKILL.md`. The commands below use macOS or Linux shell syntax and start from the repository root. Replace an older copy deliberately if you have already installed one.

```sh
git clone https://github.com/ferdinandobons/worth-building.git
cd worth-building
```

### Codex

To install for your macOS or Linux user, copy the skill into the user skills directory.

```sh
mkdir -p "$HOME/.agents/skills"
cp -R skills/worth-building "$HOME/.agents/skills/"
```

For one project, copy it into that project's `.agents/skills/` instead. In Codex CLI or the IDE extension, run `/skills` or type `$` and select `worth-building`. In the desktop app, look for it in Skills or select it in the composer. Restart the client if it does not appear after copying. [OpenAI's local installation and invocation guide](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)

### Claude Code

To install for your account, copy the skill into Claude Code's personal skills directory.

```sh
mkdir -p "$HOME/.claude/skills"
cp -R skills/worth-building "$HOME/.claude/skills/"
```

For one project, copy it into that project's `.claude/skills/` instead. Start a local Claude Code session, type `/` to look for the skill, and invoke `/worth-building` followed by your question. The above personal directory applies to local Claude Code. [Anthropic's Claude Code skill guide](https://code.claude.com/docs/en/skills#choose-where-skills-load)

### Gemini CLI

To install for your account, copy the skill into Gemini CLI's user skills directory. If you already copied it into `~/.agents/skills/` for Codex, Gemini CLI also discovers it there.

```sh
mkdir -p "$HOME/.gemini/skills"
cp -R skills/worth-building "$HOME/.gemini/skills/"
```

For one workspace, copy it into that workspace's `.gemini/skills/` or `.agents/skills/`; project discovery is subject to workspace trust. In an interactive session, run `/skills list`. If installed during the session, run `/skills reload`, then `/skills list`. Ask Gemini to use `worth-building` by name and follow the client's approval prompt if one appears. [Google's Gemini CLI skill guide](https://geminicli.com/docs/cli/skills/)

### ChatGPT direct skill upload

If your workspace has **Plugins → Skills → Create → Upload**, open the cloned repository and package the skill folder with its supporting files.

```sh
git archive --format=zip -o ../worth-building-skill.zip HEAD:skills worth-building
```

Upload `worth-building-skill.zip` in that menu. The upload option depends on plan and workspace settings. [OpenAI's custom skill guide](https://help.openai.com/en/articles/20001066-skills-in-chatgpt)

## Check that it works

In a client that selects skills automatically, start a new conversation and send a plain-language prompt.

> I have an idea for a paid app that gives freelancers a place to share updates with clients. Is it worth building? Help me figure out what I'd need.

A suitable reply identifies the likely problem as a hypothesis and starts with a useful question or check, such as how a freelancer handled their last client update. The host decides whether to select the skill. In Gemini CLI, approve activation if prompted. You can also select `worth-building` explicitly using the instructions for your client above.

## Update or uninstall

| Installation | Update | Uninstall |
| --- | --- | --- |
| Codex plugin from GitHub | Run `codex plugin marketplace upgrade worth-building-tools`, then run `codex plugin add worth-building@worth-building-tools` to reinstall the updated package. | Run `codex plugin remove worth-building@worth-building-tools`. |
| Claude Code plugin from GitHub | Run `claude plugin marketplace update worth-building-tools`, then `claude plugin update worth-building@worth-building-tools`. | Run `claude plugin uninstall worth-building@worth-building-tools`. |
| Plugin saved to your ChatGPT account | Rebuild the OpenAI ZIP and use Plugin Creator to update the existing plugin. | Open the plugin in **Plugins** and select **Uninstall plugin**. |
| Plugin in your Claude account | For a marketplace install, refresh the marketplace in **Plugins**. For an upload, rebuild the Claude ZIP and upload it again. Confirm the version and enabled state in **Your plugins**. | Open the plugin in **Your plugins** and use its remove action. |
| Standalone skill | Pull the repository and replace your installed `worth-building/` folder with the latest complete copy. | Remove the installed `worth-building/` folder. |

Start a new session after updating. Workspace-managed plugins follow the workspace's installation policy. [OpenAI plugin commands](https://learn.chatgpt.com/docs/developer-commands?surface=cli#codex-plugin) · [Claude Code plugin commands](https://code.claude.com/docs/en/plugins/cli-reference)

## Repository layout

- `skills/worth-building/` is the source for both plugins and the standalone skill.
- `plugin.json` is the portable OpenAI manifest. `.codex-plugin/plugin.json` supports Codex clients that use the compatibility format.
- `.claude-plugin/plugin.json` is the Claude plugin manifest.
- `.agents/plugins/marketplace.json` and `.claude-plugin/marketplace.json` point Codex and Claude Code at the repository root.

## Use it manually in another chat

If your client has no Agent Skills loader, attach or paste `SKILL.md` and the guides for the decision you are making. Start with the [evidence rubric](../skills/worth-building/references/evidence.md) or [builder reflection](../skills/worth-building/references/reflection.md) if you need a first read. Each path in `SKILL.md` links to its guide. Ask the assistant to apply those instructions to your idea. A chat without file or web tools can still work from material you paste.
