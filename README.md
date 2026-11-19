A skills-based AI plugin for designing, building, and reviewing distinctive responsive websites. Version 0.1.0 is an initial authoring version; it has not yet been evaluated across generated websites or verified through a host installation.
**A skills-based AI plugin for designing, building, and reviewing distinctive, responsive websites.**

## Contents
Website Studio gives a coding agent a reusable workflow for turning a website brief into an implemented experience: choose a visual direction, build working interactions, inspect the result, and fix observed issues.

It packages design guidance and quality criteria in a focused `website-builder` skill. The goal is to improve consistency while leaving room for each website to have its own identity.

> **Status: v0.1.0 — initial development.** The skill structure has passed validation and the plugin manifest has passed JSON parsing. Host installation and evaluations on generated websites are still pending.

## What it covers

- `plugin.json`: portable plugin identity.
- `skills/website-builder/SKILL.md`: the end-to-end website workflow.
- `skills/website-builder/references/`: design, interaction, and review guidance.
- `evals/briefs.md`: repeatable manual evaluation briefs and scoring criteria.
- **Visual direction:** typography, color, spacing, imagery, and composition suited to the audience and brand.
- **Responsive layouts:** deliberate adaptation for mobile and desktop screens.
- **Working interactions:** navigation, forms, filters, tabs, dialogs, and relevant UI states.
- **Accessibility checks:** keyboard navigation, visible focus, semantic controls, readable contrast, and reduced-motion behavior.
- **Scoped redesigns:** respect existing frameworks, brand choices, routes, and working features.
- **Quality review:** inspect rendered pages when browser tools are available, run relevant project checks, and report verification gaps accurately.
- **Truthful prototypes:** clearly identify sample content and simulated behavior when a real backend is absent.

These are instructions for the agent to follow, not guarantees that every generated website will meet every criterion automatically.

## How it works

1. **Understand the brief.** Inspect the project and identify the audience, content, primary action, and required interactions.
2. **Choose a direction.** Establish a coherent visual system grounded in the brief.
3. **Build the experience.** Implement the requested pages and interactions using an appropriate stack.
4. **Review and refine.** Check the main user journey, responsive layouts, and relevant accessibility behavior.
5. **Deliver.** Explain the result, provide run instructions where applicable, and distinguish completed checks from outstanding work.

User requirements and existing project conventions take priority over the skill's defaults.

## Requirements

The plugin supplies instructions and reference material. The host must supply file editing/code execution to build sites, and browser tools to verify rendered output. Image generation, deployment, external services, and paid APIs are not included or required. No server, API key, or npm installation is needed for the plugin itself. Generated websites may have their own dependencies.
The plugin itself contains Markdown guidance and a JSON manifest. It does not require an API key, server, or npm installation.

## Try the workflow locally
The coding agent's environment needs:

Before installation, open a separate website project in your coding agent and explicitly ask it to read this repository's `skills/website-builder/SKILL.md` and its linked references. Supply the full local path so the agent can find them. This tests the workflow without implying the plugin is installed.
- Access to read the skill and its supporting references.
- File editing and code execution to build and run websites.
- Browser tools for rendered-page inspection and interaction checks.

Example brief:
Generated websites may require their own dependencies. Image generation, hosting, deployment, and external service integrations are not bundled. If a tool is unavailable, the skill directs the agent to report the resulting limitation.

> Use the Website Studio website-builder skill to create a responsive website for a fictional independent pottery studio. Choose a warm editorial visual direction, implement workshop filtering, and inspect mobile and desktop layouts. There is no booking backend; label sample content and keep booking behavior honest.
## Quick start: try the local workflow

After the host installs and exposes the skill, invoke it using the skill name supported by that host. In Codex the skill invocation is `$website-builder`.
1. Download or clone this repository to your computer.
2. Open a separate website project in your coding agent.
3. Give the agent the full path to this repository's `skills/website-builder/SKILL.md` and ask it to follow that file and its linked references.
4. Describe the website you want, including any brand assets, content, technical constraints, or reference designs.

## Package and install
Example prompt — replace the path with your actual local path:

The repository is the plugin root. Its manifest follows the portable layout documented in the [OpenAI plugin packaging guide](https://developers.openai.com/plugins/build/plugins). Register the repository through the target host's supported plugin/marketplace installation flow; a Git push alone does not install it. Installation has not been performed by this scaffold.
```text
Read /absolute/path/to/website-studio/skills/website-builder/SKILL.md
and follow its linked references.

Codex is the first intended host. Instructions and references are reusable, but Claude Code/Gemini support and packaging must be tested separately before claiming compatibility.
Build a responsive website in the current project for a fictional pottery
studio called Clay & Light. Use warm editorial styling, a workshop list,
and a working category filter. No booking backend exists, so clearly label
sample content and keep booking behavior honest.

## Development
Inspect desktop and mobile layouts using available tools, fix observed
issues, and tell me which checks you completed.
```

Keep generated customer websites outside this repository. Start with this focused skill and split it only when real workflows need different activation rules or resources. Add templates or scripts when evaluations demonstrate their value rather than imposing one stack or appearance on every brief.
This explicit file-based trial tests the workflow; it does not install the plugin or enable automatic skill discovery.

Use short-lived branches for meaningful improvements and merge after reviewing representative results. See [evaluation briefs](evals/briefs.md) before calling a version production-ready. No distribution license has been selected yet; choose one before inviting public reuse.
## Plugin installation and compatibility

The repository root contains `plugin.json`, with the skill under `skills/website-builder/`. Installation must use the target host's supported plugin or marketplace process. Pushing the repository to GitHub alone does not install it.

Codex is the first intended host. Installation has not yet been verified. Claude Code and Gemini compatibility have not been tested; the reusable instructions do not establish that the same package will install unchanged in those apps.

See the [official plugin packaging documentation](https://developers.openai.com/plugins/build/plugins) when configuring host installation.

## More example briefs

Use these after loading the skill through the local workflow or a verified installation.
