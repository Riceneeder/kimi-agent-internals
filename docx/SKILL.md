---
name: docx
description: >
  Use this skill whenever the user requests creating, generating, or editing a
  Word document (.docx). Trigger scenarios include: writing a new document from
  scratch, filling a provided .docx template, adding or resolving comments,
  applying tracked changes (insertions/deletions), producing professional
  documents with cover pages, tables of contents, charts, or CJK content.
  Do NOT use this skill when the task is only to read or summarize text from
  an existing .docx (use the Read tool instead), or when the output format is
  PDF, spreadsheet (.xlsx), or a web application.
license: CC0-1.0
---

# docx

Skill for generating and editing Word documents via the C# OpenXML SDK (new
documents) and Python/lxml (editing existing documents).

## Getting started

Run once in the skill directory to install dependencies:

```bash
cd /app/.agent/skills/docx/
./scripts/docx init
```

## Key entry points

| Task | Where to look |
|------|---------------|
| Create a new document | `assets/templates/Example.cs`, `assets/templates/CJKExample.cs` |
| Edit an existing document (comments / track changes) | `references/EditingGuide.md` |
| Build / validate | `./scripts/docx build` |

## Directory layout

```
docx/
├── SKILL.md                          ← this file
├── references/
│   └── EditingGuide.md               ← Python editing API reference
├── scripts/
│   ├── docx                          ← unified entry-point script
│   ├── docx_lib/                     ← Python editing library
│   ├── fix_element_order.py
│   ├── generate_backgrounds.py
│   ├── generate_inkwash_backgrounds.py
│   ├── generate_chart.py
│   ├── validate_all.py
│   └── validate_docx.py
├── assets/
│   └── templates/                    ← C# project and example templates
└── validator/                        ← OpenXML validator configs
```

See `references/EditingGuide.md` for the complete editing API reference.
