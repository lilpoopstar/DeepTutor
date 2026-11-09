# Progress Tracking

DeepTutor stores learner progress in its learning journal and memory, not in
loose files. Record only what the learner has confirmed, and keep identifying
or sensitive details (full names, schools, health, family matters) out.

## Where Things Go

| What | Tool | Example |
|------|------|---------|
| Subject, goal, level | `learning_update` `op=set_mission` | topic "multiplication facts", why "4th-grade unit test", level "knows 1–6 tables" |
| Session summary + next focus | `learning_update` `op=note_session` | "Practised 7s and 8s; 7×6, 7×7 solid; 8×7 still tricky. Next: 8s with arrays." |
| Lasting insight | `learning_update` `op=add_record` | "Visual arrays work better than rote drills for this learner." |
| Stated preference | `write_memory` | "Prefers diagrams over long explanations." |
| Guided Learning mastery | mastery tools | Use them inside a Mastery Path; don't duplicate mastery in the journal. |

Read back with `learning_status` (mission, handoff, records) and `read_memory`
(profile and preferences).

## A Good Session Note

Cover, in a few sentences:
- Subject and topic
- About how long the session lasted, and how engaged the learner was
- What went well
- What needs work
- Next focus

## When to Update

| Event | Update |
|-------|--------|
| Session start | Check the mission and handoff; `learning_status` if history matters |
| New subject or goal | `set_mission` |
| Session end | `note_session` |
| Concept mastered or a stubborn pattern found | `add_record` |
| Learner states a preference | `write_memory` |
| Learner or parent asks for a report | Write the report in the reply (see below) |

## Progress Reports

When asked, build the report from `learning_status` and give it in the reply
(or save it to a notebook when one is available):

```markdown
# Progress Report — <learner>
**Period:** <start>–<end>
**Sessions:** <count> (<total time>)

## Highlights
- Mastered 7s multiplication table
- Growing confidence with word problems

## Areas of Focus
- 8s and 9s multiplication
- Fractions introduction

## Recommendations
- Practise the 8s table at home (5 min/day)

## Next Steps
- Complete the multiplication unit
```

## Pattern Recognition

Track across sessions:
- **Error patterns**: are the same mistakes coming back?
- **Energy patterns**: better in the morning or the evening?
- **Subject avoidance**: is one area always skipped?
- **Breakthroughs**: which approach finally worked?

Use the patterns to adjust teaching and to inform reports.

## Red Flags

Recommend that the learner (or, for a minor, their parent or guardian) seek
further support if you see:
- A steady decline over 3 or more sessions
- No engagement at all, session after session
- Mentions of anxiety or distress
- Signs that may point to a learning disability
- Worrying emotional states

For anything urgent, follow `safety.md`.
