# Self-hosted Vellum alternatives: Kortix is open source

Kortix is the open-source AI Operating System. Self-hosting it runs the whole platform on a server you control: one Docker Compose stack that the `kortix self-host` CLI installs, configures, and updates. The same commands are covered in the [self-hosting guide](https://kortix.com/docs/host).

## What self-hosting changes

Self-hosting moves the control plane onto your own machine. You run the app, the API, and the database, and you own the uptime, the backups, and the upgrade schedule. Model calls still go to the provider you connect, and agent sessions still run on a cloud sandbox provider, so the server has to be reachable from the internet for those sessions to call back.

For a team already running its own infrastructure, that trade is the point. Your data, your keys, and the configuration of every agent stay inside a boundary you set, and one repo the team owns holds the agents, the skills, the memory, and the connectors.

## The open source options that fit

- [Kortix](https://kortix.com/docs): the full platform as one Docker Compose stack, installed and updated by the `kortix self-host` CLI. Self-host is free, and sessions run on a cloud sandbox provider (Daytona, Platinum, or E2B).
- [Vellum assistant](https://github.com/vellum-ai/vellum-assistant): open source, running on your own machine locally or in Vellum Cloud. Its repository documents a self-hosted mode that shares one codebase and one data model with the managed version.
- [Langfuse](https://langfuse.com): an open source LLM engineering platform for tracing, prompt management, and evals, self-hostable with Docker Compose, Kubernetes, or a single server.
- [Promptfoo](https://github.com/promptfoo/promptfoo): an open source CLI for LLM evals and red-teaming that runs locally, so your prompts stay on your machine.

## Running Kortix on your own server

The guide offers three reachability modes. Domain mode is the production setup; a Cloudflare tunnel is for a trial on your own machine. On a server that already has Docker and its Compose plugin, install by hand:

```bash
curl -fsSL https://kortix.com/install | bash
kortix self-host init --domain kortix.example.com --admin-email you@example.com
kortix self-host start
```

Before the first start, line up:

- A Linux server with a public IP.
- DNS A or AAAA records for the domain and its `api` subdomain, pointed at the server.
- Ports 80 and 443 open inbound.
- A sandbox provider key for Daytona, Platinum, or E2B. Without one, sessions do not start.
- A model provider key, added in the app after the first sign-in.

Then sign up with the admin email, connect GitHub, create a project, and add a model key. Run `kortix self-host doctor` and fix every failing check. The setup asks a short list of questions and no model key, the stack carries no Redis and no separate worker, and one Compose project holds every service.

## Which option fits

Self-hosting is worth it when control of the data and the keys matters more than the work of running a server. A team that wants its agents to land work through review, with every session on its own cloud computer, gets that from Kortix. Someone who wants an assistant built around one person finds a shorter path in the Vellum assistant. A team that needs to trace and score model calls without running the agents can use Langfuse or Promptfoo.
