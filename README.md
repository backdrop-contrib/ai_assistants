# AI Assistants

Create an AI assistant that answers directly or calls configured AI agents.
Set its instructions, model, allowed roles, and conversation storage.
[AI Chatbot](https://github.com/backdrop-contrib/ai_chatbot) can present an
assistant in a page block.

## Requirements

- PHP 8.2 or later
- `ai_agents` module

## Installation

Install this module using the official [Backdrop CMS instructions](https://backdropcms.org/user-guide/modules).

1. Open **AI Assistants** at `admin/config/ai/ai-assistants` and add an assistant.
2. Set the system prompt. Choose a model and route mode, then select backing
   agents if your route uses them.
3. Set allowed roles and thread storage, then save.

Find setup, examples, and troubleshooting in the [project wiki](https://github.com/backdrop-contrib/ai_assistants/wiki).

## Developer reference

`ai_assistants` provides the runtime for assistant definitions.

It owns:

- assistant configuration under `ai_assistants.assistant.*` and global settings in `ai_assistants.settings`
- admin pages for adding/editing assistants
- route planning for direct, single-agent, and multi-agent requests
- backing-agent execution
- approval resume flow
- optional thread storage in session or database

Main files:

- `ai_assistants.module`
- `includes/ai_assistants.config.inc`
- `includes/ai_assistants.admin.inc`
- `includes/ai_assistants.routing.inc`
- `includes/ai_assistants.runtime.inc`
- `includes/ai_assistants.thread.inc`

Main runtime entry points:

- `ai_assistants_send()`
- `ai_assistants_resume()`
- `ai_assistants_continue_after_approval()`

Admin path:

- `/admin/config/ai/ai-assistants`

## Issues

Bugs and feature requests should be reported in the [Issue Queue](https://github.com/backdrop-contrib/ai_assistants/issues).

## Current Maintainer

[Justin Keiser](https://github.com/keiserjb)

## Credits

- Created for Backdrop CMS by [Justin Keiser](https://github.com/keiserjb).
- Developed with AI assistance.

## License

This project is GPL v2 software. See the LICENSE.txt file in this directory for complete text.
