# BITM Learning Skills for Claude

Three Claude skills that teach the **story-first** way:

**Real-world story -> connect to the topic -> definition -> syntax/formula -> example -> programs/problems**

| Skill | For | What it does |
|---|---|---|
| `story-teaching-boards` | Faculty | Day-by-day Excalidraw teaching boards, programs sheet, 20-question banks with solutions, revision/quiz boards, mini-project boards |
| `story-study-coach` | Students | Personal tutor: one concept at a time, checks understanding, revision notes, exam and lab help, study plans |
| `interview-prep-coach` | Students | Placement prep plan, core subjects, coding practice, aptitude, mock technical + HR interviews with scores |

Works for any engineering subject. It was first built and tested on a C programming bridge course for lateral-entry students.

---

## Folder structure

```
bitm-learning-skills/
├── README.md
├── LICENSE
├── skills/
│   ├── story-teaching-boards/SKILL.md
│   ├── story-study-coach/SKILL.md
│   └── interview-prep-coach/SKILL.md
└── dist/                      <- ready-to-upload zips for claude.ai
    ├── story-teaching-boards.zip
    ├── story-study-coach.zip
    └── interview-prep-coach.zip
```

---

## Install on claude.ai (web / desktop / mobile app)

1. Download the zip you want from the `dist/` folder of this repo
   (open the file on GitHub, then click **Download raw file**).
2. In Claude, open **Customize > Skills** (on some accounts: **Settings > Capabilities > Skills**).
3. Click **+ > Create skill > Upload a skill** and choose the zip.
4. Make sure the skill is switched **on**.
5. Start a new chat and try one of the example prompts below.

Notes:
- Skills are private to your account. Each faculty member or student uploads them into their own account.
- Do not unzip. Each zip contains one folder whose name matches the skill name, which is what Claude expects.
- `story-teaching-boards` draws best when the **Excalidraw** connector is turned on. Without it, the skill falls back to other visual formats.

## Install in Claude Code

```bash
git clone https://github.com/ARAVIND2017/bitm-learning-skills.git
mkdir -p ~/.claude/skills
cp -r bitm-learning-skills/skills/* ~/.claude/skills/
```

Restart Claude Code. The skills load automatically when a request matches. You can also call one directly, for example `/story-study-coach`.

---

## How to use (after installing)

You do not need to open a skill. Start a **new chat** and ask in plain words; Claude picks the matching skill.
To force one, name it: *"Use story-study-coach: teach me arrays."*

- Use the **same chat** to continue a course or topic, and a **new chat** for a new subject.
- Students: answer the check questions yourself. If an answer is wrong, the coach explains again in a different way.
- Say "make it simpler" or "shorter" any time.

### Troubleshooting

| Problem | Fix |
|---|---|
| Skill does not seem to run | Check it is switched on in Customize > Skills, then name it in your message |
| Upload error on claude.ai | Upload the zip from `dist/` as it is; do not unzip or rename it |
| No drawings for teaching boards | Turn on the Excalidraw connector, or accept the fallback format |

---

## Example prompts

**Faculty: story-teaching-boards**
- "Day 7 of my C course: if, if-else, else-if ladder. 90 minutes, beginners. Make the theory board."
- "Add the 20 practice questions with solutions for Day 7 to the question bank."
- "Make the Week 1 revision and quiz board."
- "Any topics left from the syllabus?"

**Students: story-study-coach**
- "Teach me pointers in C from zero. I am a diploma student."
- "My DBMS exam is in 5 days. Make me a study plan."
- "Explain Thevenin's theorem with a story and a solved problem."
- "Lab help: matrix multiplication program with viva questions."

**Students: interview-prep-coach**
- "I have 6 weeks before campus placements for software roles. Make me a plan."
- "Give me the top 10 OOP interview questions with answers."
- "Take a mock technical interview on C and DSA."
- "Help me answer 'Tell me about yourself'."

---

## Updating a skill

1. Edit `skills/<skill-name>/SKILL.md`.
2. Rebuild the zip from the repo folder:
   ```bash
   cd skills && zip -r ../dist/<skill-name>.zip <skill-name> && cd ..
   ```
3. Commit and push. Users upload the new zip again on claude.ai, or run `git pull` and copy again for Claude Code.

## Credits

Created by the faculty of BITM with Claude. Free to use and adapt for teaching (see LICENSE).
