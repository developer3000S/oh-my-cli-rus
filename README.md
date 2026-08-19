# oh-my-cli

A small code-agent CLI with file and shell tools. Built with Node.js 22, TypeScript, and ESM.

## 🇷🇺 Русская документация

Для русскоязычных пользователей доступна полная документация на русском языке:

- [README на русском](README-RU.md) — полное руководство на русском
- [Первое использование](docs/FIRST-RUN-RU.md) — руководство по первому запуску
- [Политика безопасности](SECURITY-RU.md) — политика безопасности
- [Политика вклада](CONTRIBUTING-RU.md) — внесение вклада в проект
- [Контракт автономности](AUTONOMY-RU.md) — долгосрочное видение продукта
- [Руководство по релизам](docs/RELEASE-RU.md) — процесс выпуска релизов
- [Русское быстрое руководство](docs/RU.md) — быстрое руководство на русском

---

## What is oh-my-cli?

oh-my-cli is a small, self-hosted code agent: a terminal CLI that reads and
edits files and runs shell commands under a strict, inspectable safety plane —
against any OpenAI-compatible endpoint.

What makes it different:

- **Safety is the product** — approval modes with a
  [spoof-resistant approval preview](#approval-preview-is-spoof-resistant), a
  [folder-trust boundary](#folder-trust), workspace path containment, and a
  deterministic [command policy](#command-policy); mutating tools fail closed
  by default.
- **Durable sessions** — every run is a JSONL session you can
  [resume or continue](#resume-a-session), [compact](#session-compaction),
  [export](#session-export), and
  [undo or redo turn by turn](#undo-and-redo-a-completed-turn).
- **Headless-first automation** — a versioned
  [JSON event stream](#headless-json-protocol), privacy-safe
  [run summaries](#run-summary) and [run scorecards](#run-scorecard),
  [spend budgets and run caps](#provider-cost-and-spend-budget),
  [recovery](#run-recovery) from checkpoints, and exportable
  [evidence archives](#evidence-archive).
- **Beyond the terminal** — an Electron [Desktop shell](#desktop-shell) and a
  local [web delivery board](#web-delivery-board) ship alongside the CLI,
  with built-in file, search, and shell [tools](#built-in-tools).
- **Develops itself** — improvements flow through an autonomous,
  evidence-bound queue under a protected governance plane
  ([AUTONOMY.md](AUTONOMY.md)).

New here? Start with [Install](#install) and the
[first-run guide](docs/FIRST-RUN.md).

## Project policies

- [Apache License 2.0](LICENSE)
- [Contribution policy](CONTRIBUTING.md)
- [Security policy](SECURITY.md)
- [Autonomy contract](AUTONOMY.md)

Product improvements enter the autonomous queue from three sources: promoted
user reports, findings from the bounded community-source registry, and
reproducible self-discoveries. Each becomes a normalized Issue authored by the
repository Bot before execution. The autonomy contract, its policy files,
GitHub workflows, and CODEOWNERS form a protected governance plane maintained
by `qqqys`; the Bot may propose governance changes but cannot apply them.