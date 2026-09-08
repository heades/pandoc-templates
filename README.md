# Homework Pandoc Template

A Pandoc to LaTeX template for producing homework assignments.

## YAML Options

The following YAML metadata options are supported by the template.

| Option | Type | Description |
|---|---|---|
| `title` | string | Assignment title. If provided, the title is displayed using `\maketitle`. |
| `date` | string | Date displayed with the title. Defaults to an empty date if omitted. |
| `course` | string | Course name displayed below the assignment title. |
| `due-date` | string | Due date displayed below the course name. |
| `instructions` | string | Instructions displayed in a centered block beneath the title. |
| `documentclass` | string | LaTeX document class. |
| `fontsize` | string | Document font size, e.g. `11pt` or `12pt`. |
| `papersize` | string | Paper size, e.g. `letter` or `a4`. |
| `classoption` | list | Additional options passed to the LaTeX document class. |
| `fullpage` | boolean | If `true`, loads the `fullpage` package. |
| `geometry` | list | Options passed to the `geometry` package. |
| `numbersections` | boolean | If `true`, enables numbered sections. |
| `secnumdepth` | integer | Controls the depth to which sections are numbered. Defaults to `5` when `numbersections` is enabled. |
| `cancel` | boolean | If `true`, loads the LaTeX `cancel` package. |
| `babel-lang` | string | Main language passed to the LaTeX `babel` package. |
| `babel-otherlangs` | list | Additional languages passed to `babel`. |
| `bibliography` | list | Bibliography files used by Pandoc. |
| `biblio-title` | string | Custom title for the bibliography. |
| `natbib` | boolean | Enables Pandoc's `natbib` bibliography handling. |
| `biblatex` | boolean | Enables Pandoc's `biblatex` bibliography handling. |
| `nocite-ids` | list | Citation IDs to include in the bibliography even if they are not cited in the document. |
| `header-includes` | list | Raw LaTeX commands inserted into the document preamble. |

## Example

```yaml
---
title: "Homework 3"
course: "SEC 4100"
due-date: "September 15, 2026"

instructions: |
  Answer all questions. Show your work where appropriate.

documentclass: article
fontsize: 11pt
papersize: letter

geometry:
  - margin=1in

numbersections: true
---