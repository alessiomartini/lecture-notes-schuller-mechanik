# Instructions for Claude: Schuller, Mechanik notes

@~/.claude/templates/lecture-notes/RULES.md
Setup copied from `../lecture-notes-schuller-geometric-anatomy` (which copies Brunton/Mehrling): same preamble
machinery, `build.py`, `scroll.py`. When in doubt, do as that repo does.

## Sources and how to use them
- The repo is **public**. `materials/` (transcripts, audio, PDFs, notes by others) is gitignored: check
  `git status` before every commit.
- One chapter per lecture (`chapters/chNN-<slug>.tex`), sections in the order of the lecture.
- Main source = the lecture itself: `materials/transcripts/CXX-VYY.txt` (`[m:ss] text`, from YouTube
  captions or local whisper). Paraphrase in clean English, fix mis-hearings. Mis-hearings found so far: (none yet, fill in as found).
  **Never drop content**: every definition, theorem, proof, example, remark, digression and student question goes
  in (side remarks in `aside`/`coursenote`, skippable material in `secondary`).
- Formal style: Definition / Theorem / Proof as on the blackboard, proofs in full. Ambiguous blackboard notation:
  reconstruct from context and the backup notes, mark `[?]` if unsure. Lecture wins over notes; note relevant
  differences in `secondary`.
- `\ts{C}{V}{m:ss}` on every point (C = chapter number, V = video of the chapter, normally 1), `\seg{C}{1}{text}` in the Sources box.
- Backup notes (Potnis, `materials/backup/`, auto-translated, work in progress) only to check symbols and statements, never copied (no licence).
- Each chapter starts with Sources + a `reading` box pointing to the matching chapters of the other Schuller sets
  (Geometric Anatomy, Gravity and Light, Quantum) and to his papers where useful.
- Exercises: short in the text, long ones verbatim in `appendices/appA-exam.tex`; passages taken out of the text go
  to `\section*{Set aside}` at the chapter end. Chapter end: `keyconcepts` box.
- Chapter number = lecture number (ch01-ch23), then ch24-ch28 for the five port-Hamiltonian papers (arXiv ids in the ROADMAP;
  no video: no `\ts`, cite the paper section/equation instead). `\ts{C}{1}{m:ss}` with C = lecture number.
- **Language**: the lectures are German and written in English; the first occurrence of a term keeps the German in parentheses,
  e.g. "phase space (Phasenraum)".

## Build and check
`cd lecture-notes && python build.py all`, then grep `build/main.log` for `\.tex:[0-9]+:`, `undefined`, `Overfull`
and look at the rendered pages. When writing LaTeX through the shell backslashes get mangled: use Edit/Write.
