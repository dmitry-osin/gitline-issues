# GitLine — Bug Reports and Feature Requests

This repository is the issue tracker for **GitLine**, a plugin that brings Git line history into IntelliJ Platform IDEs. Use it to report bugs, suggest improvements, and ask questions about the plugin.

- **Website and installation:** [dmitry-osin.github.io/getgitline](https://dmitry-osin.github.io/getgitline/en/)
- **Report a bug or suggest a feature:** [GitHub Issues](https://github.com/dmitry-osin/gitline-issues/issues)
- **Author:** [Dmitry Osin](https://github.com/dmitry-osin)

This repository is for issue tracking and discussion. It does not contain the plugin's source code.

## What is GitLine?

GitLine helps you understand who changed a line of code and why, without losing your place in the editor.

Use it to:

- See the author, time and commit summary beside the current, visible or selected lines.
- Inspect commit details in a hover popup and keep line context in the status bar.
- Open the matching commit in Git Log, view its diff, copy the full hash or open it on your Git host.
- Customize Inline, Uncommitted, Hover HTML and Status bar output with FreeMarker templates, Preview, presets and template JSON import/export.
- Adjust annotation appearance, author aliases, filters and commit or issue links.
- Inspect and edit the selected repository/worktree's `.gitconfig`, including identity, line endings and Pull / Fetch / Push policies, with effective values and their sources in view.

The plugin's interface is available in English and Russian. GitLine is free to use under Apache License 2.0.

### Keyboard navigation

Place the caret on a committed line, press **Alt+Enter** and choose **GitLine** to access **Show in Git Log**, **Copy hash**, **Show diff** and **Open in browser**. The same actions are available in the annotation's hover popup.

Actions follow the primary caret's line. They can be available with the inline annotation hidden once commit data is ready. Locally changed lines and unsupported editors do not offer the menu. If no commit URL is available, **Open in browser** stays disabled while the other actions remain available.

## Installation

Visit the [official GitLine website](https://dmitry-osin.github.io/getgitline/en/#install) for getting-started instructions. A Marketplace installation link will appear once a verified public listing URL is available. No public download or release version is announced here yet.

If you already have a plugin ZIP, use **Settings → Plugins → ⚙ → Install Plugin from Disk**. Open a trusted Git project with Git installed, then configure the plugin in **Settings → Tools → GitLine**.

The minimum platform is **IntelliJ Platform 2025.3, build 253**, with **Git4Idea**. Compatibility is checked against specific IDE lines; support for every IDE or future build is not guaranteed. Include your exact IDE name, version and build when reporting a problem.

## What this repository is for

Use this issue tracker for:

- Missing, incorrect or outdated line annotations and commit attribution.
- Problems with hover details, status bar information or Alt+Enter actions.
- Template editing, Preview, presets, JSON import/export or rendering issues.
- Problems with appearance, filters, author aliases or Git host and issue links.
- Repository/worktree `.gitconfig` settings, inheritance, value sources or Apply behavior.
- IDE compatibility, performance or English and Russian translation issues.
- Feature requests, usability improvements and questions about using GitLine.

Before opening an issue, check the [existing issues](https://github.com/dmitry-osin/gitline-issues/issues) to see whether the topic has already been reported. Reports in English or Russian are welcome.

## Reporting a bug

[Open an issue](https://github.com/dmitry-osin/gitline-issues/issues/new) and include:

1. **Problem:** a brief description of what went wrong.
2. **Steps to reproduce:** the actions you took, the relevant GitLine settings and whether the affected line is committed or locally changed.
3. **Expected and actual results:** what you expected and what happened instead.
4. **Environment:** your GitLine version, IDE name/version/build, operating system and Git version.
5. **Example:** a small reproducible repository or code example, an anonymized template, a screenshot or a relevant log excerpt.

If the issue depends on a display mode, filter, project override, file type, multiple Git roots or a worktree, mention that in your report. For `.gitconfig` problems, include the selected scope and relevant effective values or sources, with private information removed.

## Requesting a feature

Describe the task you want to accomplish, what currently makes it difficult, and the behavior you would like to see. A concrete use case helps explain the proposal. Mention any current workaround and the part of your workflow the change would improve.

## Known limitations

- Untracked, ignored and binary files and unsupported editors are excluded. The configurable file limit defaults to **20,000 lines**. Optional filters can be disabled, but the size limit remains.
- Diff editor blame, history across an uncommitted rename, a dedicated Code Vision provider, commit signing and Work/Personal profiles are not implemented. GitLine can coexist with the IDE's own Code Vision.
- Project template overrides apply only to **Inline** and **Uncommitted** in trusted projects. Other templates and advanced options remain application settings.
- Presets and JSON import/export transfer only the **four templates**, including unsaved edits. They do not transfer all IDE or GitLine settings. Imports and presets update the draft; **Apply** saves it.
- The repository-root `.git-blame-ignore-revs` file requires an explicit opt-in setting, off by default. An arbitrary Git config `blame.ignoreRevsFile` is not applied automatically.
- `.gitconfig` **Apply** saves only the selected repository/worktree configuration. It does not edit the global `.gitconfig` or run pull, fetch or push. Pull / Fetch / Push settings are policies for future operations.
- Issue links use one configured ID regex and a URL containing `{id}`. There is no automatic authorization or API synchronization with Jira or GitHub Issues.

## Privacy

GitLine uses your local repository's Git history to display line context. **Open in browser** follows a commit link to the configured Git host.

Issues and attachments in this repository are public. Remove credentials, access tokens, private repository URLs, personal email addresses and confidential code from examples, screenshots and logs before posting.

You do not need to publish your project or provide access to its private repository to report a bug. A minimal example with fictional data is usually enough to describe the problem.
