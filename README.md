# FUUZ Skills

Claude Code skills for building applications on the [FUUZ](https://fuuz.app) MES platform — covering data modeling, package generation, screen design, data flows, GraphQL/JSONata, industrial operations, and ML telemetry.

## What Are FUUZ Skills?

FUUZ Skills are [Claude Code skill files](https://docs.anthropic.com/en/docs/claude-code/skills) (`.skill` archives) that teach Claude how to build, deploy, and manage applications on the FUUZ platform. Each skill is self-contained and can be imported into any Claude Code environment via the admin console.

They're designed for **FUUZ developers, partners, and customers** who want Claude to understand FUUZ platform conventions, data model patterns, and best practices out of the box.

## Skills

| Skill | Version | Description |
|-------|---------|-------------|
| **fuuz-packages** | v2.1.1 | FUUZ package generation — 71 golden rules for building valid `manifest.json`, `definition.json`, and `package-data.json` files. Covers ISA-88/ISA-95 patterns, deployment lifecycle, and enterprise tenant architecture. |
| **fuuz-schema** | v2.0.0 | Data model design — relationship TRIPLETS, usable/active patterns, 24 critical rules, data retention tiers, field metadata shapes, and naming conventions. |
| **fuuz-screens** | v1.3.0 | Screen builder — MainFormContainer patterns, action pipelines, OEE dashboards, Stimulsoft reports, ISA-101 compliance, and component library reference. |
| **fuuz-flows** | v1.3.0 | Data flow design — 50+ node types, webhook configuration, JSONata iteration rules, 5 manufacturing flow patterns, and flow documentation standards. |
| **fuuz-platform** | v1.5.0 | Platform fundamentals — 294 JSONata bindings, GraphQL query/mutation patterns, integration landscape (500+ systems), and Script Editor runtime reference. |
| **fuuz-industrial-ops** | v1.2.0 | Industrial operations — OPC UA quality codes, OEE/TEEP/MTBF/MTTR formulas, ideal cycle time fallback, UNS patterns, and alarm management. |
| **fuuz-ml-telemetry** | v1.0.0 | ML and telemetry — algorithms, telemetry collection patterns, data models, and validation checklists. |

## Repository Structure

```
fuuz-skills/
├── README.md
├── SKILLS_VERSION_MANIFEST.md    # Version tracking and change log
├── .gitignore
│
├── fuuz-packages/                # Package generation skill
│   ├── SKILL.md                  #   Deployed skill (with YAML frontmatter)
│   ├── fuuz-package-creator-skill.md  #   Source skill (71 golden rules)
│   └── references/
│       └── package-deployment-lifecycle.md
│
├── fuuz schema/                  # Data model design skill
│   ├── SKILL.md
│   └── references/               #   8 reference files
│
├── fuuz screens/                 # Screen builder skill
│   ├── SKILL.md
│   ├── fuuz-screens-v1.md
│   └── references/               #   11 reference files
│
├── fuuz flows/                   # Data flow design skill
│   ├── SKILL.md
│   └── references/               #   12 reference files
│
├── fuuz-platform/                # Platform fundamentals skill
│   ├── SKILL.md
│   └── references/               #   10 reference files
│
├── fuuz-industrial-ops/          # Industrial operations skill
│   ├── SKILL.md
│   └── references/               #   5 reference files
│
├── fuuz-ml-telemetry/            # ML and telemetry skill
│   ├── SKILL.md
│   └── references/               #   5 reference files
│
└── *.skill                       # 7 packaged skill archives (ZIP)
```

## Installation

1. Download the `.skill` file for the skill you need
2. Open the **Claude Code admin console**
3. Import the `.skill` file
4. Skills are loaded one at a time — each is fully self-contained

## Updating Skills

New training data can be added via the `NewTrainingData/` workflow:

1. Drop new `.md` files into `NewTrainingData/`
2. Review and compare against existing skill content
3. Copy to the appropriate `{skill}/references/` directory
4. Update the skill's `SKILL.md` to reference the new file
5. Repackage the `.skill` archive
6. Update `SKILLS_VERSION_MANIFEST.md`
7. Re-import into Claude Code admin console

## Versioning

All skills follow [semantic versioning](https://semver.org/):

- **Major** — significant structural changes, new sections, many new rules
- **Minor** — new rules added, existing sections updated
- **Patch** — typo fixes, clarifications, minor corrections

See [`SKILLS_VERSION_MANIFEST.md`](SKILLS_VERSION_MANIFEST.md) for the complete version history and change log.

## About FUUZ

[FUUZ](https://fuuz.app) is a Manufacturing Execution System (MES) platform supporting ISA-88 batch processing, ISA-95 enterprise integration, OEE tracking, and industrial IoT — built for manufacturers who need flexible, configurable production management.

## Resources

| Resource | Link | Description |
|----------|------|-------------|
| **Free Trial** | [fuuz.app](https://fuuz.app) | Request your free trial of FUUZ |
| **Get Started** | [getstarted.fuuz.com](https://getstarted.fuuz.com) | Introductory videos and walkthroughs to get up and running |
| **FUUZ Academy** | [academy.fuuz.com](https://academy.fuuz.com) | Online LMS with structured courses and certifications |
| **Support & Community** | [support.fuuz.com](https://support.fuuz.com) | Knowledge base, documentation, and customer community |
