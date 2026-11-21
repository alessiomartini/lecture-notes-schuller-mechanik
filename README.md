# Mechanik, TP-1 (Schuller): lecture notes

LaTeX study notes of Frederic P. Schuller's *Theoretische Physik 1: Mechanik* (FAU Erlangen, SS 2014, German, 23 lectures, 40.3 h),
followed by a part on his papers on port-Hamiltonian systems. One chapter per lecture, every point linked to the second of the video.

- Videos: YouTube (channel "Vorlesungen Physik", ids in `lecture-notes/videos.tex`),
  [FAU.tv](https://www.fau.tv/series/theoretische-physik-1-mechanik-tp-1-s14).
- Build: `cd lecture-notes && python build.py all` (latexmk + scroll book `build/book.pdf`).
- Transcripts: `python -I -X utf8 tools/transcripts.py` turns YouTube captions or whisper output in
  `materials/transcripts/raw/` into `materials/transcripts/CXX-VYY.txt` (C = chapter, V = video of the chapter);
  `tools/whisper.py` transcribes lectures without captions. `materials/` is gitignored (third-party material, never committed).

## Backup sources (checking only, never copied)
- Backup notes (checking only, never copied): Apoorv Potnis, [apoorvpotnis/schuller_classical](https://github.com/apoorvpotnis/schuller_classical) (English, work in progress, from auto-translated subtitles). No licence stated: all rights reserved.

Full inventory of Schuller's material: `../lecture-notes-schuller-courses/SOURCES.md` (local).
All rights on the lectures belong to their authors; these are personal, non-commercial study notes.
