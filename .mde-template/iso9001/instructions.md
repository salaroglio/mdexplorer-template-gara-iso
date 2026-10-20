## ISO 9001

- `quality/` is the group's quality system: `processes.md` (the processes and their workflows), `proposals/` (the
  workflow proposals), `audit/` (the audit plan, the reports, the actions). When you are asked about the quality system,
  start from `quality/processes.md`, and follow the `iso9001-processes` skill.
- The rounds are the workflow `.mde-template/iso9001/workflows/process.md` (a process becomes a workflow) and
  `.mde-template/iso9001/workflows/audit.md` (the internal audit): do not start their agents yourself and do not write
  their files in their place.
- To put an approved workflow to work use the `mde-workflow` and `mde-agent` skills, and check it with the
  `check_workflow` tool before adding it to the project.
- The method's theory, if the project asked for it, is in `theory/iso9001/`: use it to explain how a process becomes a
  workflow and how to get ready for the audit. If it is missing and would help, offer to download it (`add_theory` tool,
  id `iso9001`) and download it only after the person says yes.
- Do not make up the standard: describe the clauses in your own words with their number, and refer to the official text.
- The files in `.mde-template/iso9001/` belong to the method and arrive with its updates: do not change them.
