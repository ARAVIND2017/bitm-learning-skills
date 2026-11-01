---
name: story-teaching-boards
description: Creates beginner-friendly, story-first teaching boards on Excalidraw for any subject, day by day from a course plan - exactly two boards per course (Teaching Story Board + Code Board) holding theory, programs, 20-question banks, revision and project. Use when a teacher asks to prepare a class, a day's board, a lesson, practice questions, a question bank, revision or quiz, or says "next day", "continue" or "add below".
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
3. **One answer = one drawing.** Draw the whole answer in ONE `create_view` call
   (up to about 250 elements), so the user sees one finished board, not several pieces.
   Restore the latest checkpoint first and add the new part BELOW. Never move, edit or
   delete anything above unless asked.
4. **Fixed boards, no extra files.** The teaching skill keeps exactly two boards per
   course (Teaching Story Board + Code Board); each coach keeps one board per subject.
   Remember each board's latest checkpoint and always continue the right one. Start a
   new board only when the user says "new board" or changes subject.
   Show the latest checkpoint id in each reply ("Board id: ..."). In a new chat, if the user
   pastes an id, restore it and continue; if it cannot be restored, start the board with a
   "Continued from <last day/topic>" band.
5. **Short chat reply (2-4 lines):** which board was updated and what was added, any
   questions the user should answer, and one next-step question. The board carries the content.
6. **If Excalidraw is not connected:** say so in one line and use another visual
   (Whiteboard artifact or inline visual) in the same order. Plain text is the last resort.
7. **Easy to understand.** One idea per box; short lines (about 8-12 words); everyday word
   first, technical word only after CONNECT; every new term defined before it is used;
   prefer a picture, arrow or table over a paragraph.

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
- Labelled shapes with manual line breaks so text never overflows. Keep labels short
  so a whole answer fits in one call. Only if it truly cannot fit, finish in a second
  call and tell the user that the LAST drawing in the chat is the complete board.
  cameraUpdate 800x600 (4:3 sizes only) per section; finish on the questions section.
- No emojis.

## Visual features (same in all three BITM skills)

Use Excalidraw's own features so the board reads like a guided lesson:
1. **Guided camera tour.** Before each section, move the camera to it (600x450 for a
   close-up of the story or a key idea, 800x600 for a normal section). End on the
   questions, then one final 1600x1200 overview, so the lesson unfolds like slides.
2. **Section zones + number badges.** Put each section on a light background zone
   (opacity 30) with a small numbered circle (1-8) at its top-left, so the eye always
   knows where it is.
3. **Legend strip** under the title of every new board: Story | Definition | Code |
   Output | Mistake | Practice, in their colours.
4. **Draw the story, don't just write it.** Simple shapes for people (circle head +
   rounded body), objects (plates, coaches, registers) and places, with 1-3 word labels.
5. **Link arrows.** Dashed coloured arrows from each story object to its technical word,
   so students see the mapping.
6. **Animate processes** (loops, stack/queue, sorting, linked-list insert, traversal, data
   flow): draw a state, nudge the camera, delete the changing elements and redraw them in
   the new position or colour with NEW ids, step by step. Also keep a numbered
   "Step 1 -> Step 2 -> ..." strip beside it so the board still reads after the animation.
7. **Memory pictures for code:** variables as labelled boxes with values, pointers as
   arrows, arrays as indexed cells, trace tables as grids.
8. **Highlight what matters:** a yellow "EXAM POINT" tag beside must-write definitions,
   and a red border on the one thing students most often get wrong.

## Accuracy rules (same in all three BITM skills)

1. **Run it, don't guess.** Before any output goes on a board, run the code when a code
   tool (bash/sandbox) is available: C with `gcc -Wall -std=c11` then run; Python with
   `python3`; SQL on a small SQLite database built from exactly the tables and rows shown
   on the board (watch for SQLite vs MySQL differences). Copy the real output exactly; for
   programs that read input, run them with the sample input shown on the board. If no code
   tool is available, trace by hand with a trace table and label the box
   "OUTPUT (hand-traced)". Never draw an output that was neither run nor traced. The same
   applies to every question-bank solution.
2. **Follow the real syllabus.** If the user or the Project provides a syllabus, lab list
   or textbook, read it first and use its module numbers, topic order, lab numbers and
   terms; mark anything outside it "Extra (not in syllabus)". If none is given, say once
   that the plan is a typical order to be matched with the official syllabus. Never
   invent course codes, module numbers, lab numbers or marking schemes.
3. **Final check before replying.** After drawing, check: (a) the standard order is
   followed; (b) every output was run or hand-traced and every answer matches its
   question; (c) definitions use standard textbook meaning - say "not sure" rather than
   guess; (d) text fits its box (estimate width as characters x font size x 0.55 and keep
   it under the box width minus 20), nothing overlaps, no font below 16; (e) nothing above
   the new part changed. Fix anything that fails before sending. End the chat reply with
   "Checked: outputs run" or "Checked: outputs hand-traced".

## 1. Exactly two boards per course

| Board | What goes on it (added below, day after day) |
|---|---|
| **1. TEACHING STORY BOARD** | Course plan, every day's theory (Level 1 + Level 2), Part 2 deep dives, revision/quiz, project launch, coverage check |
| **2. CODE BOARD** | Every day's programs (worked problems for non-programming subjects), then that day's 20 questions + solutions |

Never create a third board for the same course. Every reply names the board it updated,
e.g. "Teaching Story Board: added Day 1 below the course plan."

## 2. Before starting

Use what the teacher already gave. If everything needed is there, start drawing at once.
Otherwise ask only for what is missing, in one message (at most 4 short questions):
subject, day/date and topics; class length (default 90 min); student level (default
complete beginners); syllabus or lab list so matching items can be marked (e.g. "VTU Lab 7").
If a day has more than 4 topics, confirm the list first.

## 3. Theory board

**Course plan (first time only):** when asked to list topics, draw the plan at the top of the
Teaching Story Board: one box per day (day number + 1-2 line topic), coloured by module, a
legend, today's box with a thick red border, and holiday/flex/revision days marked.

**RECAP strip (Day 2 onwards):** 3 small boxes recalling the previous day's key ideas,
drawn before Level 1.

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
7. PRACTICE - 2 in-class (blue) + 2 homework (pink) + 1 EXIT TICKET (predict the output
   or a one-line answer, checked in the last 3 minutes).
8. NEXT STEP - next class, one green box.

**"Part 2" deep dive** ("explain clearly", "in detail", "more"): overview picture of all
types -> per type Real world | Syntax | Program | Output | How it works -> comparison
table -> rules -> one program showing all types together. Dashed grey divider before it;
thick black divider before a new day.

**Time plan** ("is this enough?"): minute-by-minute split, optional items marked,
40-50% hands-on. Be honest about what does not fit.

**Content rules:** same story all day; Indian everyday context (Rs, canteen, UPI, Aadhaar,
USN, hostel, auto fare, cricket); Kannada/Hindi analogies fine, technical terms in English.
One running example for the whole course (e.g. the same Student table every DBMS day).
Programs must compile and be run (Accuracy rule 1). C: `int main(void)`, `return 0;`;
never `void main`, `conio.h`, `getch()`, `gets()` or undefined behaviour. Add an exam
definition, a 2-mark answer and a predict-the-output item where useful.

## 4. Code Board - programs (board 2)

Title "<Subject> - Code Board"; one band per day; cards P1, P2...: Title -> "Real world:" ->
code -> OUTPUT; a REMEMBER box per day; programs different from the theory board.
Non-programming: "Worked Problems: Day by Day", Given -> Formula -> Substitution -> Answer.
Lab programs (e.g. "VTU Lab 7"): add a LAB CARD - Aim -> Algorithm -> Program ->
Sample input/output -> 5 viva questions with answers.

## 5. Code Board - question bank (board 2, below that day's programs)

Band "DAY n PRACTICE: <topics> (20 questions)", two columns Q1-Q10 / Q11-Q20, easy -> hard.
Band "DAY n SOLUTIONS: how to think -> code -> output"; one card per question: title,
HOW TO THINK (yellow, 3-4 plain lines), code or working (white), OUTPUT/answer (dark).
Tag each question with marks (2/5/10) and level (Remember / Apply / Analyse).

## 6. Revision / quiz (Teaching Story Board)

Session plan -> journey row of the week's topics -> revision table (Topic | Real world |
Definition | Syntax, ~10 rows) -> spot-the-error (10 pairs) -> 10 MCQs + answer key ->
practical test (2 programs; write-up 20 / execution 60 / viva 20) -> holiday homework pack.

## 7. Project launch (Teaching Story Board)

Menu screen mock-up -> "which topic is used where" table -> starter code -> rubric ->
timeline to demo -> alternative project ideas.

## 8. Coverage check

After each unit or "any topics left?": table Topic | Why it matters | Where it fits,
split into "important" and "good to know"; offer to add gap-filler days to the
Teaching Story Board.

## 9. Handling teacher feedback

- "Too complex": halve the words, Level-1 style boxes, more pictures, one idea per box.
- "Not added" / "you changed the top": the newest drawing at the bottom of the chat is
  the current board; older drawings in the chat do not update. Continue from the latest checkpoint.
- "Next" / "continue" / "yes": move to the next item in the plan without re-asking.

## 10. Check before sending

- [ ] Standard order kept; one story all day
- [ ] Every output run (or marked hand-traced); syllabus followed
- [ ] No banned functions or undefined behaviour
- [ ] Exactly 6 mistakes; 2 in-class + 2 homework + exit ticket
- [ ] Nothing above the new content changed; only the two boards used
- [ ] Whole answer drawn in one call
- [ ] Text fits in its boxes; no font below 16
