# Agent Ticket privacy policy

_Last updated: 13 October 2026. Publisher: Clearlane, contact: joachim.brindeau@klarc.com._

Agent Ticket is a browser extension and a companion background program ("runtime") that runs on your own
computer. It lets you capture the page you are looking at, annotate it, and hand it to a coding agent that you
have installed and signed in to yourself, so that agent can file a ticket in your project.

## What the extension handles

When you click the toolbar button or press the shortcut, the extension handles:

- a screenshot of the visible part of the current tab, and your annotations on it;
- the page title and address (URL);
- the text you type to describe the problem;
- your settings: the selected project, action and agent, and the address and access token of your local runtime.

## Where that data goes

- **Stored in your browser.** The current screenshot, your draft text and your settings are kept in the
  extension's local browser storage so they survive closing the panel. They are not synced.
- **Sent only to your own runtime.** When you click **Create ticket**, the screenshot, page title, URL and your
  text are sent to the Agent Ticket runtime on your computer (`127.0.0.1`). Nothing is sent anywhere else by the
  extension.
- **Then to the agent you chose.** The runtime saves the screenshot on your computer and passes the report to
  the coding agent you selected (for example Claude Code, Codex, Jcode, Hermes or OpenCode), either on your
  computer or, if you configured a remote project, on the SSH server you configured. That agent then works
  under its own terms and privacy policy with its provider, and writes the ticket wherever your project files
  tickets (for example GitHub, Linear or a Markdown file).

Clearlane does not operate any server for Agent Ticket and receives none of this data. There is no account,
analytics, advertising, tracking or telemetry. Data is never sold or shared with third parties by Clearlane.

The only other network request is when you click **Download for macOS** or **Download update**, which opens the
installer from the public release page on GitHub.

## Permissions

| Permission | Why |
|---|---|
| `activeTab` | Capture a screenshot of the tab you are on, only when you invoke the extension. |
| `storage` | Keep your settings, draft and current screenshot between sessions. |
| `sidePanel` | Show the ticket workspace next to the page (Chrome). |
| `http://127.0.0.1/*`, `http://localhost/*` | Talk to the runtime on your own computer. |
| Optional `https://*/*` | Requested only if you point the extension at a runtime on another HTTPS address. |

## Retention and deletion

Screenshots of submitted tickets are stored by the runtime under `~/.local/share/agent-ticket/runs` on your
computer until you delete them. Removing the extension deletes its browser storage. Uninstalling the runtime
removes the program; your project configuration and run history stay in your home folder until you delete them.

## Contact

Questions or requests: joachim.brindeau@klarc.com.
