# Vellum vs Kortix: Kortix is open source

Kortix is the open-source AI Operating System, and both it and Vellum publish the facts this head-to-head rests on. The short version: Vellum is a personal assistant for one person, and Kortix is an operating system for a team's agents.

## What Vellum is

Vellum is a personal AI assistant. Its [home page](https://www.vellum.ai/) describes an assistant you own and customize, reachable from Mac, iOS, Android, the web, voice, email, Telegram, Slack, and the terminal, with the same memory, chats, and schedules on every surface. By default the assistant runs locally, and Vellum says the code is open source.

The [Vellum assistant repository](https://github.com/vellum-ai/vellum-assistant) documents the parts: eight memory types, skills defined by a SKILL.md and a TOOLS.json, computer use inside a sandbox with every action permission-gated, and model support for Anthropic, OpenAI, Google Gemini, Fireworks, OpenRouter, MiniMax, and any OpenAI-compatible endpoint, with local models through Ollama. The assistant is open source. Vellum also sells a managed service, the Vellum Platform, and the assistant can run on it or self-hosted from the same codebase.

## What Kortix is

Kortix is the open-source AI Operating System: your agents, their skills, your company memory, and every connector in one git repo you own, with the agents working on real cloud computers. The [Kortix docs](https://kortix.com/docs) describe a project as a git repo with a `kortix.yaml` at its root, a session as one agent run on its own sandbox and branch, and a change request as the reviewed merge back toward the default branch.

Kortix is for teams that want agents producing finished work, reviewed by people. Run it on Kortix Cloud, in your VPC, or on your own on-prem network.

## Where they differ

| Dimension | Kortix | Vellum |
| --- | --- | --- |
| Shape | Operating system for a team's agents | Personal assistant for one person |
| Built for | Teams and companies | An individual |
| Your configuration | One git repo the team owns | The assistant's files, local or Cloud |
| Memory | Company memory, kept as files | Eight memory types about one person |
| Models | Any provider, your own keys | Anthropic, OpenAI, Gemini, Ollama |
| Hosting | Cloud, VPC, on-prem | Your machine or Vellum Cloud |

Each cell follows from the pages these products publish: the [Kortix home](https://kortix.com) and [about page](https://kortix.com/about) on one side, and the [Vellum home](https://www.vellum.ai/) and [assistant repository](https://github.com/vellum-ai/vellum-assistant) on the other.

Vellum is free to download, and its Cloud plans start at $30 per month for Mighty, $100 for Super, and $200 for Ultra (checked October 2026, [Vellum pricing](https://www.vellum.ai/pricing)). Kortix self-hosts for free, and the managed cloud starts on a free tier of $0 with 200 credits per month and 1 project.

## Who each fits

Pick Vellum when one person wants an assistant that remembers them, runs on their own machine, and acts across their own tools. The assistant is open source, and it covers the personal surfaces a single user needs.

Pick Kortix when a team wants the agents, skills, company memory, and connectors in one repo it owns. Kortix adds per-resource permissions for people and agents, runs each session on its own cloud computer, and puts a change request in front of anything that merges. It also reaches further than one person's tools, with 3,000+ apps plus MCP, OpenAPI, Postman, GraphQL, and raw HTTP.

## Sources

- [Vellum home](https://www.vellum.ai/)
- [Vellum pricing](https://www.vellum.ai/pricing)
- [Vellum assistant](https://github.com/vellum-ai/vellum-assistant)
- [Kortix home](https://kortix.com)
- [Kortix docs](https://kortix.com/docs)
- [Kortix about](https://kortix.com/about)
- [Kortix on GitHub](https://github.com/kortix-ai/suna)
