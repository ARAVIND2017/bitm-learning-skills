---
name: story-teaching-boards
description: Creates beginner-friendly, story-first teaching boards on Excalidraw for any subject, day by day from a course plan - theory boards, programs sheets, 20-question banks with solutions, revision/quiz and mini-project boards. Use when a teacher asks to prepare a class, a day's board, a lesson, practice questions, a question bank, revision or quiz, or says "next day", "continue" or "add below".
---

# Story Teaching Boards (for faculty)

Turn a course plan into day-by-day teaching boards that complete beginners can follow.

Why story first: beginners cannot hold an abstract term until they have a concrete
picture to hang it on. A story first makes the definition feel obvious; code or
formulas first makes students switch off. Never break the order, even for "easy" topics.

## 0. Output rule (same in all three BITM skills)

1. **Draw, don't type.** Every answer is drawn on an Excalidraw board. Call the
   Excalidraw `read_me` tool once per session, then draw with `create_view`.
2. **Same order on every board:** STORY -> CONNECT -> DEFINITION -> SYNTAX/FORMULA ->
   EXAMPLE (code + OUTPUT + trace, or worked solution with units) -> MISTAKES ->
   PRACTICE/CHECK QUESTIONS -> NEXT STEP. Each section sits under a dark band heading.
3. **Grow, never rewrite.** Same topic or course -> restore the latest checkpoint and
   add the new part BELOW. Never move, edit or delete anything above unless asked.
   New subject, or the user says "new board" -> start a new board.
4. **Short chat reply (2-4 lines):** what was drawn, any questions the user should
   answer, and one next-step question. The board carries the content.
5. **If Excalidraw is not connected:** say so in one line and use another visual
   (Whiteboard artifact or inline visual) in the same order. Plain text is the last resort.

## Drawing standard (same in all three BITM skills)

- Width 1160 from x=20. Title 40; band headings 24 in white on #1e1e2e; body 18-20;
  code 16 in monospace (fontFamily 3). Never below 16 - split a long program into two
  code boxes instead of shrinking it.
- Columns: 2 at x=20/610 (width 570); 3 at x=20/415/810 (width 370);
  4 at x=20/315/610/905 (width 275). Gaps 20-40 px.
- Colours: story #fff3bf (stroke #f59e0b); connect #fff3bf -> #e7f5ff; definition #d0bfff;
  code white; output #1e1e2e with #e5e5e5 text; notes #ffd43b; correct #b2f2bb;
  mistakes #ffe3e3 (stroke #ef4444); in-class/check questions #a5d8ff; homework #ffc9c9;
  next step #b2f2bb.
- Flowcharts: ellipse = start/stop, rectangle = process, diamond = decision,
  parallelogram = input/output (closed line polygon, text on top); label Yes/No;
  loop-back arrows go around the side.
- Labelled shapes with manual line breaks so text never overflows. About 40-60 elements
  per call; split bigger sections across calls using the checkpoint. cameraUpdate
  800x600 (4:3 sizes only) per section; finish on the questions section.
- No emojis.

## 1. What this skill produces

| Output | Where it goes |
|---|---|
| Theory board (one per day) | Main board for the unit |
| Programs sheet (worked-problems sheet for non-programming subjects) | One separate board |
| Question bank: 20 questions per day + solutions | Same separate board, added below the programs |
| Revision / quiz board | Main board, end of week or unit |
| Project-launch board | Main board, when a mini project starts |

## 2. Before starting

Use what the teacher already gave. If everything needed is there, start drawing at once.
Otherwise ask only for what is missing, in one message (at most 4 short questions):
subject, day/date and topics; class length (default 90 min); student level (default
complete beginners); syllabus or lab list so matching items can be marked (e.g. "VTU Lab 7").
If a day has more than 4 topics, confirm the list first.

## 3. Theory board

**Level 1 - simple picture page (always first):** one story, 3-5 boxes, very few words.
A student who reads only this page should still understand the idea.

**Level 2 - detailed page (below Level 1), in the standard order:**
1. STORY - one everyday story used for the whole day.
2. CONNECT - each part of the story -> the matching technical word.
3. DEFINITION - exam-ready, 1-2 lines.
4. SYNTAX/FORMULA - concept table Real world | Definition | Syntax | Example
   (non-programming: Formula/Rule | Worked example; decisions and loops: a mini flowchart).
   Add a how-it-works picture: memory diagram, flowchart, trace table or comparison.
5. EXAMPLE - 2-4 program cards: title, "Real world:" line, complete code, OUTPUT
   (or full worked solution with units).
6. MISTAKES - exactly 6 red boxes, wrong vs right.
7. PRACTICE - 2 in-class (blue) + 2 homework (pink).
8. NEXT STEP - next class, one green box.

**"Part 2" deep dive** ("explain clearly", "in detail", "more"): overview picture of all
types -> per type Real world | Syntax | Program | Output | How it works -> comparison
table -> rules -> one program showing all types together. Dashed grey divider before it;
thick black divider before a new day.

**Time plan** ("is this enough?"): minute-by-minute split, optional items marked,
40-50% hands-on. Be honest about what does not fit.

**Content rules:** same story all day; Indian everyday context (Rs, canteen, UPI, Aadhaar,
USN, hostel, auto fare, cricket); Kannada/Hindi analogies fine, technical terms in English.
Programs must compile; trace every output by hand. C: `int main(void)`, `return 0;`;
never `void main`, `conio.h`, `getch()`, `gets()` or undefined behaviour. Add an exam
definition, a 2-mark answer and a predict-the-output item where useful.

## 4. Programs sheet (separate board)

Title "Programs: Day by Day"; one band per day; cards P1, P2...: Title -> "Real world:" ->
code -> OUTPUT; a REMEMBER box per day; programs different from the theory board.
Non-programming: "Worked Problems: Day by Day", Given -> Formula -> Substitution -> Answer.

## 5. Question bank (same separate board, below the programs)

Band "DAY n PRACTICE: <topics> (20 questions)", two columns Q1-Q10 / Q11-Q20, easy -> hard.
Band "DAY n SOLUTIONS: how to think -> code -> output"; one card per question: title,
HOW TO THINK (yellow, 3-4 plain lines), code or working (white), OUTPUT/answer (dark).

## 6. Revision / quiz board

Session plan -> journey row of the week's topics -> revision table (Topic | Real world |
Definition | Syntax, ~10 rows) -> spot-the-error (10 pairs) -> 10 MCQs + answer key ->
practical test (2 programs; write-up 20 / execution 60 / viva 20) -> holiday homework pack.

## 7. Project-launch board

Menu screen mock-up -> "which topic is used where" table -> starter code -> rubric ->
timeline to demo -> alternative project ideas.

## 8. Coverage check

After each unit or "any topics left?": table Topic | Why it matters | Where it fits,
split into "important" and "good to know"; offer a gap-filler board.

## 9. Handling teacher feedback

- "Too complex": halve the words, Level-1 style boxes, more pictures, one idea per box.
- "Not added" / "you changed the top": the newest drawing at the bottom of the chat is
  the current board; older drawings in the chat do not update. Continue from the latest checkpoint.
- "Next" / "continue" / "yes": move to the next item in the plan without re-asking.

## 10. Check before sending

- [ ] Standard order kept; one story all day
- [ ] Every output or answer traced by hand
- [ ] No banned functions or undefined behaviour
- [ ] Exactly 6 mistakes; 2 in-class + 2 homework
- [ ] Nothing above the new content changed
- [ ] Text fits in its boxes; no font below 16
