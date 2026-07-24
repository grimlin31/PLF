# Bootcamps

**Version:** 1.0.0  

## Project–folder convention

Every ChatGPT Project selects its Bootcamp by exact name:

```text
Project name == Bootcamps/<Project name>/
```

Do not select a Bootcamp through its `ACTIVE` status. Multiple Bootcamps may be
active simultaneously.

If the matching folder does not exist, the first `hola` starts the conversational
bootstrap defined by the Framework. The assistant gathers the required data and
creates the instance after approval; the user does not prepare configuration
files manually.
**Status:** Approved  
**Framework:** Professional Learning Framework

This directory contains independent learning programs created from PLF.

Each Bootcamp specializes the generic Framework for:

- one profession or discipline;
- one target level;
- one student instance;
- one curriculum;
- one set of competencies, projects and milestones.

## Required structure

```text
Bootcamp-Name/
├── README.md
├── 00-BOOTCAMP-CONFIG.md
├── 01-KNOWLEDGE-INDEX.md
├── 02-MENTOR-LOG.md
├── 03-LEARNING-PROFILE.md
├── 04-CURRICULUM-MAP.md
├── 05-BOOTCAMP-STATE.md
├── Chapters/
├── Projects/
├── Interviews/
└── Assets/
```

## Rules

- A Bootcamp inherits the rules in `Framework/00-MASTER-CONTEXT.md`.
- Framework documents remain generic.
- Profession-specific information belongs inside the Bootcamp.
- Each theory chapter has its own directory and chat or session.
- Related laboratories use `X.1`, `X.2`, and subsequent numbering.
- The Bootcamp State is the primary transfer document between sessions.
- Evidence paths must refer to artifacts inside the repository or to an explicitly documented external location.
- Changes to the generic method belong in the Framework Changelog.

## Creating a Bootcamp

1. Create a directory using a stable descriptive name.
2. Configure the profession, mentor and student profiles.
3. Instantiate the official Framework documents.
4. Define competencies and dependencies.
5. Create the curriculum and milestones.
6. Initialize the Bootcamp State.
7. Begin the first eligible chapter.

Do not place active Bootcamp content directly in this directory.
