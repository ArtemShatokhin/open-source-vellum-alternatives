# Vellum FAQ: Kortix is open source

Kortix is the open-source AI Operating System, and these are the questions people ask when they put it next to Vellum. Every answer comes from the product's own page or repository.

## Is Vellum open source?

Vellum's assistant is open source, so you can read the code and run it yourself. Vellum also sells a managed service, the Vellum Platform, and the [assistant repository](https://github.com/vellum-ai/vellum-assistant) says the managed product sustains the business. Kortix is open source as well, and it is built for a whole team's agents.

## What is a free alternative to Vellum?

Kortix is free to self-host, and the managed cloud has a free tier: $0 with 200 credits per month and 1 project. The paid team plan is $40 per seat per month with 2,500 credits per month per seat, pooled (checked October 2026). Langfuse and Promptfoo are open source and free to run yourself as well.

## Can I self-host a Vellum alternative?

Yes. Kortix installs as one Docker Compose stack with the `kortix self-host` commands, and self-host is free ([self-hosting guide](https://kortix.com/docs/host)). The Vellum assistant, [Langfuse](https://langfuse.com), and [Promptfoo](https://github.com/promptfoo/promptfoo) all self-host too, so the choice comes down to what you want to run: a team's agents, one person's assistant, or an eval and observability tool.

## Can a Vellum alternative use my own models and keys?

Kortix runs any model provider with your own keys, or the ChatGPT plan you already pay for. Vellum supports Anthropic, OpenAI, Google Gemini, Fireworks, OpenRouter, and any OpenAI-compatible endpoint, with local models through Ollama.

## Is there an open source alternative to Vellum for a whole team?

Kortix is built for a team. Its agents, skills, company memory, and connectors live in one git repo you own, with per-resource permissions for people and agents and a change request in front of merging. Each session runs on its own cloud computer, and thousands run in parallel on one config.
