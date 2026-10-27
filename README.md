# AI Assistants

`ai_assistants` is the backend/runtime module for assistant definitions.

It owns:

- assistant config in `ai_assistants.settings`
- admin pages for adding/editing assistants
- route planning for direct, single-agent, and multi-agent requests
- backing-agent execution
- approval resume flow
- durable thread storage in session or database

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
