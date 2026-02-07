## Skills
A skill is a set of local instructions stored in a `SKILL.md` file. Use the skills below when the user asks for them by name or when the request clearly matches the described workflow.

### Available skills
- shaping: Collaborative shaping for iterating requirements (R), solution options (S), fit checks, and transitions into slicing. (file: /Users/stephan/codex-shaping-skills/shaping/SKILL.md)
- breadboarding: Build affordance/wiring maps (UI + non-UI), places, and vertical slices from an existing workflow or shaped parts. (file: /Users/stephan/codex-shaping-skills/breadboarding/SKILL.md)

### How to use skills
- Trigger rules: If the user names `$shaping` or `$breadboarding` (or plain `shaping` / `breadboarding`), use that skill. Also trigger when the task clearly matches the description.
- Discovery: Read the selected skill file first and follow its workflow before improvising.
- Progressive loading: Only open additional referenced files if needed; avoid loading unrelated content.
- Coordination: If both skills apply, do shaping first, then breadboarding.
- Fallback: If a skill file is missing or unreadable, state that briefly and proceed with the best manual equivalent.

### Output expectations
- Treat skill artifacts as source-of-truth tables and keep them complete (no partial rows unless the skill explicitly allows it).
- Keep notation stable across updates so prior decisions remain traceable.

### Quick examples
- `$shaping`: "I want to create a simple TUI app that fetches timezone data fresh each load and shows a multi-locale hour table; use your shaping skill to capture requirements and tease apart shapes before coding."
- `$shaping`: "Shape this interaction: default locales are preloaded, default window is next 12 hours, and natural-language commands can add/remove locales or set a date window (for example 'show me times Feb 12 in Brasil')."
- `$shaping`: "We already selected Shape F. Show only the R x F fit check and list what is still unsolved."
- `$breadboarding`: "Breadboard this TUI flow end-to-end: input command -> tool call -> timezone fetch -> table state update -> render."
- `$breadboarding`: "Given shaped parts, produce UI and non-UI affordance tables by place, then cut vertical slices that each end in demo-able UI."
- Combined flow: "Start with `$shaping` to settle R and pick a shape, then use `$breadboarding` to map wiring and define the first implementation slices."
