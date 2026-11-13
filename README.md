<img src="assets/icon.png" alt="PinSay" width="96" height="96">

# PinSay for Claude Code

A Claude Code plugin that connects Claude Code to [PinSay](https://pinsay.dev). Your team leaves comments on your
website, and Claude Code reads the ones that are ready, changes your code, commits, and marks them applied.

The plugin adds:

- the hosted PinSay MCP server (`https://app.pinsay.dev/mcp`),
- one skill, `apply-feedback`, that describes the apply loop,
- two commands: `/pinsay:queue` and `/pinsay:apply`.

## Install

```
claude plugin marketplace add pinsay-dev/pinsay-claude-plugin
claude plugin install pinsay@pinsay
```

## First use

Claude Code signs in to PinSay for you. Run `/mcp` in Claude Code, pick `pinsay` and choose **Authenticate**. If you
skip this, it asks you to sign in the first time a PinSay tool is called.

## Commands

- `/pinsay:queue [project]`: list the comments ready to apply. It changes nothing.
- `/pinsay:apply [numbers]`: apply the comments with those numbers, or all ready ones when you give none.

## Use an API key instead

If you cannot sign in from Claude Code, you can connect with a PinSay API key. See
<https://pinsay.dev/docs/mcp.html>.

## Uninstall

```
claude plugin uninstall pinsay
```

## License

MIT. See [LICENSE](LICENSE).
