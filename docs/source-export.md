# Source Export Notes

The live implementation currently exists in the hosted app environment. This repository is prepared as the GitHub home for that source.

## Goal

Export or clone the hosted app source, then commit the application code into this repository.

## Expected source contents

The exported code should include:

- setup page
- MCP endpoint
- Discord API integration
- token-connection flow
- proposal/review flow
- database schema or migrations required by the runtime

## Sensitive data rules

Do not commit:

- Discord bot tokens
- hosted-app write credentials
- OAuth secrets
- temporary bypass tokens
- environment variable values
- user-specific stored Discord connection data

Use `.env.example` for non-secret variable names only.

## Follow-up work

After export, open a follow-up PR that adds the actual source code and verifies the app still runs through its deployment process.
