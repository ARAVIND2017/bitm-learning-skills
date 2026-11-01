---
name: story-teaching-boards
description: Creates beginner-friendly, story-first teaching boards (Excalidraw) for any subject, day by day from a course plan - theory boards, programs or worked-problems sheets, 20-question practice banks with solutions, revision/quiz boards and mini-project boards. Use when a teacher asks to prepare a class, a day's content or board, a lesson, practice questions, a question bank, a revision or quiz board, or says "next day", "continue" or "add below" in a course.
---

# Story Teaching Boards (for faculty)

Turn a course plan into day-by-day teaching boards that complete beginners can follow.

## The one rule: fixed teaching order

**Real-world story -> connect to the topic -> clear definition -> syntax/formula -> example -> programs/problems**

Why: beginners cannot hold an abstract term until they have a concrete picture
to hang it on. A story first makes the definition feel obvious; code or formulas
first makes students switch off. Never break this order, even for "easy" topics.

## What this skill produces

| Output | Where it goes |
|---|---|
| Theory board (one per day) | Main board for the unit |
| Programs sheet (or worked-problems sheet for non-programming subjects) | One separate board |
| Question bank: 20 questions per day + solutions | Same separate board, added below the programs |
| Revision / quiz board | Main board, end of week or unit |
| Project-launch board | Main board, when a mini project starts |

---

## 1. Before starting

Use what the teacher already gave. Ask only for what is missing, in one message,
at most 4 short questions:

- Subject, day number, date, topics for the day
- Class length (default 90 minutes)
- Student level (default: complete beginners)
- Syllabus or lab list, so matching items can be marked (e.g. "VTU Lab 7")

If the day has more than 4 topics, confirm the list before drawing.
If everything needed is already given, start drawing straight away.

---

## 2. Theory board

### Level 1 - simple picture page (always first)
One story, 3-5 boxes, very few words. A student who reads only this page should
still understand the idea.

### Level 2 - detailed page (below Level 1)

1. **Story picture** - one everyday story, used for the whole day (yellow).
2. **Mapping** - each part of the story -> the matching technical word.
3. **Definition** - exam-ready, 1-2 lines.
4. **Concept table** - Real world | Definition | Syntax | Example.
   - Non-programming subjects: Real world | Definition | Formula/Rule | Worked example.
   - Decisions and loops: the 4th column is a mini flowchart; the program goes below.
5. **How-it-works picture** - memory diagram, flowchart, trace table or comparison.
6. **Programs / problems** - 2-4 cards: title, "Real world:" line, complete code
   (or full worked solution with units), OUTPUT/answer box.
7. **Common mistakes** - exactly 6 red boxes, each showing wrong vs right.
8. **Practice** - 2 in-class (blue) + 2 homework (pink).
9. **Next class** - one green box.

### "Part 2" deep dive (teacher says "explain clearly", "in detail", "more")
Overview picture of all types -> for each type: Real world | Syntax | Program | Output | How it works
-> comparison table -> rules -> one program that shows all types together.

### Time plan (teacher asks "is this enough?" or "how do I split the time?")
Minute-by-minute split, optional items marked, 40-50% of the time hands-on.
Be honest: if the content does not fit, say what to cut.

### Content rules
- Same story for the whole day. Indian everyday context: Rs, canteen, UPI, Aadhaar,
  USN, hostel, auto fare, mobile recharge, cricket. Kannada/Hindi analogies are fine;
  technical terms stay in English.
- Every program must compile under standard C/C++/Python as relevant. Trace every
  output by hand before writing it on the board.
- C programs: `int main(void)` and `return 0;`. Never `void main`, `conio.h`,
  `getch()`, `gets()` or anything with undefined behaviour.
- Where useful add: exam definition, a 2-mark answer, a predict-the-output item.
- Code lines about 55 characters at font 16 (13-14 for long programs).
- No emojis.

---

## 3. Programs sheet (separate board)

- Title "Programs: Day by Day"; one dark band per day.
- Cards P1, P2, ...: Title -> "Real world:" -> code -> OUTPUT.
- A REMEMBER box with key points after each day.
- Short programs, different from the theory-board programs.
- Non-programming subjects: "Worked Problems: Day by Day", same card layout with
  Given -> Formula -> Substitution -> Answer with units.

## 4. Question bank (same separate board, added below)

- Band "DAY n PRACTICE: <topics> (20 questions)"; two columns Q1-Q10 and Q11-Q20, easy -> hard.
- Band "DAY n SOLUTIONS: how to think -> code -> output".
- One card per question: title, HOW TO THINK (yellow, 3-4 plain lines),
  code or working (white, monospace), OUTPUT/answer (dark).

## 5. Revision / quiz board

Session plan with minutes -> journey row of the week's topics -> revision table
(Topic | Real world | Definition | Syntax, about 10 rows) -> spot-the-error (10 pairs)
-> 10 MCQs with answer key -> practical test (2 programs, marks: write-up 20 /
execution 60 / viva 20) -> holiday homework pack if a holiday follows.

## 6. Project-launch board

Band -> menu screen mock-up -> "which topic is used where" table -> starter code
-> rubric -> timeline to demo -> alternative project ideas.

## 7. Coverage check

After each unit, or when asked "any topics left?": table Topic | Why it matters |
Where it fits, split into "important" and "good to know". Offer a gap-filler board.

---

## 8. Excalidraw drawing rules

- Call the Excalidraw `read_me` tool once per session before the first drawing.
- Layout: total width 1160 from x=20. Title 40, headings 26, body 16-20, code 13-16
  with fontFamily 3 (monospace). 4 columns at x=20/315/610/905 (width 275);
  2 columns at x=20/610 (width 570). 40-60 px gaps.
- Colours: story #fff3bf (stroke #f59e0b); definitions #d0bfff or #e7f5ff; code white;
  output #1e1e2e with #e5e5e5 text; notes #ffd43b; correct #ebfbee/#b2f2bb;
  mistakes #ffe3e3/#ef4444; in-class #a5d8ff; homework #ffc9c9; next class #b2f2bb;
  section bands #1e1e2e with white text.
- Flowcharts: ellipse = start/stop, rectangle = process, diamond = decision,
  parallelogram = input/output (closed line polygon, text on top). Label Yes/No;
  loop-back arrows go around the side.
- **Growing a board:** restore the latest checkpoint and add new content below it.
  Never move, edit or delete anything above unless the teacher asks; teachers notice
  even small changes and lose trust. Thick black divider before a new day,
  dashed grey divider before a Part 2.
- Unique id prefix per section; about 200 elements per call (split bigger sections);
  cameraUpdate 800x600 per section, final 1600x1200 overview.
- New board only when the teacher says so or the unit changes.
- If Excalidraw is not connected: say so in one line and use a Whiteboard artifact,
  Docs artifact or inline visual with the same order and colours.

## 9. Handling teacher feedback

- "Too complex" / "students won't understand": halve the words, keep only Level 1
  style boxes, more pictures, one idea per box. Do not argue.
- "Not added" / "you changed the top": explain that the newest drawing at the
  bottom of the chat is the current board; older drawings in the chat do not update.
  Then continue from the latest checkpoint.
- "Next" / "continue" / "yes": move to the next item in the plan without re-asking.

## 10. Check before sending (every time)

- [ ] Story -> definition -> syntax -> example -> programs order kept
- [ ] One story used throughout the day
- [ ] Every output or answer traced by hand
- [ ] No banned functions or undefined behaviour
- [ ] Exactly 6 mistakes; 2 in-class + 2 homework
- [ ] Nothing above the new content changed
- [ ] Text fits inside its boxes at the stated font sizes

## 11. Reply format

One line saying what was added and where -> numbered list of the sections ->
one next-step question (e.g. "Shall I add the Day 7 question bank?").
