---
name: story-teaching-boards
description: Create beginner-friendly Excalidraw teaching boards for any subject - story-based theory boards, programs sheets, 20-question practice banks with how-to-think solutions, revision/quiz boards and project-launch boards, day by day from a course plan. Use when a teacher asks for class content, a day's board, practice questions, a revision board or a mini-project board.
---

# Story Teaching Boards (for faculty)

Turn a course plan into day-by-day teaching boards that a beginner can follow.
Every topic follows ONE fixed order:

**Real-world story -> connect to the topic -> clear definition -> syntax/formula -> example -> programs/problems**

## Outputs this skill makes

1. **Theory board** - one per day (story first, then the concept).
2. **Programs sheet** - short simple programs per topic (separate board).
3. **Question bank** - 20 questions per day + solutions (same separate board as the programs sheet).
4. **Revision / quiz board** - end of a week or unit.
5. **Project-launch board** - mini-project brief, starter code and rubric.

---

## 1. Before starting

Collect (ask only what is missing, at most 4 short questions):

- Subject, day number, date, topics for the day
- Class length (default 90 minutes)
- Student level (default: complete beginners)
- Syllabus / lab list (mark matching programs, e.g. "VTU Lab 7")
- What comes in the next class

If the plan has many topics, confirm the topic list for the day before drawing.

---

## 2. Theory board (fixed order)

### Level 1 - simple picture page (always first)
One story, 3-5 boxes, very few words. A student who reads only this page must
still get the idea.

### Level 2 - detailed page (BELOW Level 1)

1. **Story picture** - one everyday story used for the whole day (yellow).
2. **Mapping** - each part of the story -> the matching technical word.
3. **Definition** - exam-ready, 1-2 lines.
4. **Concept table** - columns: Real world | Definition | Syntax | Example.
   - Non-programming subjects: Real world | Definition | Formula/Rule | Worked example.
   - Decisions/loops: 4th column is a mini flowchart; the program goes below.
5. **How-it-works picture** - memory diagram, flowchart, trace table or comparison.
6. **Programs** - 2-4 cards. Each card: title, "Real world:" line, complete code, OUTPUT box.
7. **Common mistakes** - exactly 6, red boxes, wrong vs right.
8. **Practice** - 2 in-class (blue) + 2 homework (pink).
9. **Next class** - one green box.

### Deep-dive "Part 2" (when the teacher says "explain clearly" / "in detail")
Overview picture of all types -> per type: Real world | Syntax | Program | Output | How it works
-> comparison table -> rules -> one "proof" program that shows all types together.

### Time plan (when asked "is this enough?" / "how to split time")
Give a minute-by-minute split, mark optional items, keep 40-50% hands-on.

### Content rules
- Simple first. Never show code before the story and the definition.
- Same story for the whole day.
- Indian context: Rs, canteen, Aadhaar, USN, hostel, UPI, auto fare, mobile recharge.
  Kannada/Hindi analogies are fine; technical terms stay in English.
- Code must compile. Hand-verify every output and show the working.
- No undefined behaviour. Use `int main(void)` and `return 0;`.
  Never use `void main`, `conio.h`, `getch()` or `gets()`.
- Include an exam definition, a 2-mark answer and a predict-the-output item where useful.
- Keep code lines about 55 characters at font 16 (font 13-14 for long programs).
- No emojis.

---

## 3. Programs sheet

- Board title: "Programs: Day by Day".
- One dark band per day.
- Cards P1, P2, ...: Title -> "Real world:" -> code -> OUTPUT.
- A REMEMBER box with key points after each day.
- Short programs, different from the ones on the theory board.

---

## 4. Question bank (same board as the programs sheet, added below)

- Band: "DAY n PRACTICE: <topics> (20 questions)".
- Two columns: Q1-Q10 and Q11-Q20, easy -> hard.
- Band: "DAY n SOLUTIONS: how to think -> code -> output".
- One card per question:
  - title
  - HOW TO THINK (yellow, 3-4 lines in plain words)
  - code (white, monospace)
  - OUTPUT (dark)
- Verify every output by tracing.

---

## 5. Revision / quiz board

1. Session plan with minutes.
2. Journey row - all topics of the week in order.
3. Revision table: Topic | Real world | Definition | Syntax (about 10 rows).
4. Spot-the-error: 10 wrong/right pairs.
5. 10 MCQs + answer key.
6. Practical test: 2 programs + marking (write-up 20 / execution 60 / viva 20).
7. Holiday homework pack if a holiday follows.

---

## 6. Project-launch board

Band -> menu screen mock-up -> "which topic is used where" table -> starter code
(struct + menu) -> rubric -> timeline to demo -> alternative project ideas.

---

## 7. Coverage check

Automatically after each unit, or when asked "any topics left?":
table Topic | Why it matters | Where it fits. Split into "important" and "good to know".
Offer a gap-filler board.

---

## 8. Excalidraw drawing rules

- Call the Excalidraw `read_me` tool first in a session.
- Grid: total width 1160 starting at x=20. Title 40, headings 26, body 16-20,
  code 13-16 with fontFamily 3 (monospace).
- 4 columns: x = 20, 315, 610, 905, width 275.
- 2 columns: x = 20 and 610, width 570.
- Gaps of 40-60 px between sections.
- Colours:
  - story: fill #fff3bf, stroke #f59e0b
  - definitions: #d0bfff or #e7f5ff
  - code: white
  - output: #1e1e2e with #e5e5e5 text; notes #ffd43b
  - correct: #ebfbee / #b2f2bb
  - mistakes: #ffe3e3 with #ef4444
  - in-class practice #a5d8ff, homework #ffc9c9, next class #b2f2bb
  - section bands: #1e1e2e with white text
- Flowcharts: ellipse = start/stop, rectangle = process, diamond = decision,
  parallelogram = input/output (closed line polygon with the text on top).
  Label Yes/No. Loop-back arrows go around the side.
- **Growing a board:** restore the latest checkpoint and add content BELOW it.
  Never change anything above unless the teacher asks.
  Thick black divider before a new day; dashed grey divider before a "Part 2".
- Use a unique id prefix per section. Keep about 200 elements per call; split larger sections.
- cameraUpdate 800x600 per section; finish with a 1600x1200 overview.
- Start a new board only when the unit changes or the teacher says so.
  The programs sheet and question bank share one separate board.
- Tell the teacher that the latest drawing (at the bottom of the chat) is the current one.
- If Excalidraw is not connected: say so, and use a Whiteboard artifact, a Docs artifact
  or an inline visual with the same order and colours.

---

## 9. Reply format

One line saying what was added and where -> numbered list of sections -> one next-step question.

## 10. Lessons learned

- Simple first; beginners reject crowded boards.
- Never code before story and definition.
- Be honest about the time split.
- Pair related programs to show contrast (e.g. recursion printing before vs after the call: 5..1 vs 1..5).
