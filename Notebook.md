**Project:** Low-Cost Teaching Vehicle Model
**Course:** MIE243 – Mechanical Engineering Design I
## Team

| Member      | Role                                   |
| ----------- | -------------------------------------- |
| Shangkai Ji | Product Owner, Meeting Recorder, Developer |
| Mo Zhou     | CAD Design Owner, Developer            |
| Hongru Liu  | Scrum Master, Developer                |
| Peiwen Sun | Concept Development Owner, Developer |

## All entries

```base
filters:
  and:
    - file.inFolder("Entries")
formulas:
  commit: 'if(commits, commits.map(link(value, value.split("/")[4] + "@" + value.split("/")[6].slice(0, 7))), "")'
properties:
  formula.commit:
    displayName: Commits
views:
  - type: table
    name: All entries
    order:
      - file.name
      - date
      - authors
      - sprint
      - formula.commit
      - tags
    sort:
      - property: date
        direction: DESC
```

## Export

```dataviewjs
for (const p of dv.pages('"Entries"').sort(p => p.file.name, "asc")) {
  const date = p.date ? dv.date(p.date).toFormat("yyyy-MM-dd") : ""
  const authors = [].concat(p.authors ?? []).join(", ")
  const byline = [date, authors].filter(Boolean).join(" · ")
  if (byline) dv.paragraph(`*${byline}*`)
  dv.paragraph(`![[${p.file.path}]]`)
}
```
