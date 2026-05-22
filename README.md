# SEO Skills

SEO research, site-first keyword discovery, DataForSEO validation, SERP analysis, and LLM-assisted SEO strategy skills powered by AIsa.

This repository is part of the [AISA Skills](https://github.com/AISA-skills) collection. Each top-level directory is a self-contained agent skill with a `SKILL.md` file and optional supporting scripts, references, or assets.

## Skills

| Skill | Description |
|---|---|
| [seo-keyword-research](./seo-keyword-research/) | Use this skill when a user asks for SEO keyword research, keyword discovery, search volume analysis, keyword difficulty, search intent mapping, topic clusters, content opportunities, competitor keyword gaps, or a keyword strategy for a domain, URL, product,... |

## Requirements

Most skills in this repository use AIsa APIs and expect one environment variable:

```bash
export AISA_API_KEY="your-aisa-api-key"
```

Get an API key at [aisa.one](https://aisa.one). Keep your key out of commits, screenshots, shared logs, and shell history exports.

## Install

Clone this repository:

```bash
git clone https://github.com/AISA-skills/seo.git
cd seo
```

Install one or more skills into your local agent runtime. For Codex:

```bash
mkdir -p ~/.codex/skills
cp -r seo-keyword-research ~/.codex/skills/
```

For other Agent Skills compatible runtimes, copy the skill folder into that runtime's skills directory, then restart the agent so it can load the skill metadata.

## Usage

Ask your agent to use the relevant skill by name. Example:

```text
Use seo-keyword-research to help me with this task.
```

Each skill contains its own workflow, safety rules, required inputs, and API notes in `SKILL.md`.

## Repository Layout

```text
seo/
|-- README.md
|-- LICENSE
|-- .gitignore
`-- <skill-name>/
    |-- SKILL.md
    |-- scripts/       # optional
    |-- references/    # optional
    `-- assets/        # optional
```

## Contributing

1. Keep each skill self-contained in its own folder.
2. Keep `SKILL.md` focused on agent-facing instructions.
3. Put large endpoint docs, schemas, templates, or examples in `references/`.
4. Put deterministic helper code in `scripts/`.
5. Do not commit local outputs, credentials, caches, or API responses.

## License

MIT. See [LICENSE](./LICENSE).
