<div align="center">

<img src="https://raw.githubusercontent.com/Nomploy/.github/main/profile/assets/banner.png" alt="Nomploy — Deploy your applications with ease" width="720">

**A free, self-hostable PaaS that runs your apps and databases on [HashiCorp Nomad](https://www.nomadproject.io/).**

[Website](https://nomploy.com) · [Docs](https://docs.nomploy.com) · [Templates](https://templates.nomploy.com) · [Nomad Packs](https://packs.nomploy.com)

</div>

---

## What we do

Nomploy is an open source alternative to Vercel, Netlify and Heroku that you run
on your own servers. It is a fork of [Dokploy](https://github.com/dokploy/dokploy)
that swaps the orchestrator from Docker Swarm to **Nomad**, while keeping the
parts people liked: a clean UI, git-driven deploys, domains and automatic SSL,
backups, monitoring and notifications.

Everything we publish is licensed openly — no source-available enterprise tier,
no feature gates behind a paywall.

### Why Nomad

| | Docker Swarm | Nomploy on Nomad |
|---|---|---|
| Scheduling | Swarm services | Nomad jobs, with real bin-packing and constraints |
| Deploy artifact | Compose / stack files | Nomad HCL generated from the compose you already write |
| Service discovery | Swarm overlay + Traefik | Consul catalog + Traefik, with Let's Encrypt TLS |
| Scaling | Manual replicas | Replicas plus autoscaling via `x-nomad-scaling` |
| Workloads | Containers only | Containers today, other Nomad drivers ahead |

## Projects

| Repository | What it is |
|---|---|
| **[nomploy](https://github.com/Nomploy/nomploy)** | The platform itself — dashboard, API, build pipeline, Nomad bootstrap, backups and monitoring. AGPL-3.0. |
| **[nomad-packs](https://github.com/Nomploy/nomad-packs)** | A curated [Nomad Pack](https://developer.hashicorp.com/nomad/tools/nomad-pack) registry: databases, object storage, messaging, observability, identity and dev tools. Apache-2.0. |
| **[website](https://github.com/Nomploy/website)** | Marketing site and documentation monorepo behind nomploy.com and docs.nomploy.com. |
| **[templates](https://github.com/Nomploy/templates)** | One-click application templates for the dashboard. A fork of Dokploy's catalogue, being adapted for Nomad. |
| **[cli](https://github.com/Nomploy/cli)** | Command line client for driving an instance from your terminal or CI. A fork of Dokploy's CLI, being adapted. |
| **[mcp](https://github.com/Nomploy/mcp)** | Model Context Protocol server, so AI agents can manage deployments. A fork of Dokploy's MCP package, being adapted. |

## Try it

On a fresh Debian/Ubuntu or RHEL-family VPS:

```bash
curl -sSL https://raw.githubusercontent.com/Nomploy/nomploy/main/install.sh | sh
```

That installs Docker, Consul, Nomad, the CNI plugins, Traefik, Postgres and
Redis alongside the app, then prints the URL to open. Full walkthrough in the
[installation docs](https://docs.nomploy.com/docs/core/installation).

Adding Nomad to a server you already manage? Use **Bootstrap Nomad** in that
server's settings inside the dashboard.

Want the batteries too:

```bash
nomad-pack registry add nomploy github.com/Nomploy/nomad-packs
nomad-pack run monitoring --registry nomploy
```

## Get involved

- **Issues and ideas** — open them on the repository they belong to; each project's
  `CONTRIBUTING.md` explains the branch and commit conventions.
- **Security** — please report vulnerabilities privately to
  [contact@nomploy.com](mailto:contact@nomploy.com) rather than in a public issue.
- **Packs** — a missing piece of infrastructure is usually a small pull request
  against [nomad-packs](https://github.com/Nomploy/nomad-packs); `AGENTS.md` there
  walks through authoring one.

<div align="center">
<sub>Built on <a href="https://github.com/dokploy/dokploy">Dokploy</a>'s foundation · AGPL-3.0</sub>
</div>
