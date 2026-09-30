# Manual Testing Checklist

Use this checklist after source changes or redeployments.

## Plugin connection

- Open the private setup page.
- Confirm the Discord connection status shows connected for the signed-in user.
- In ChatGPT, select the assistant plugin.
- Run a read-only connection check.

## Read-only Discord tests

- List accessible channels in an authorized server.
- Read a small bounded set of recent messages from an authorized channel.
- Confirm links and code snippets are summarized as text only.
- Confirm the assistant does not open URLs from Discord messages.

## Management proposal tests

- Prepare a harmless server-management proposal.
- Confirm the proposal requires approval before Discord changes.
- Approve only during testing.
- Revert the test change and confirm the original state is restored.

## Regression checks

- No bot token appears in responses, logs, repo files, or screenshots.
- Read-only commands do not mutate Discord.
- Management commands show clear proposed changes before execution.
