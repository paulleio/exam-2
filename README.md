# Complete Exam 2 calculus walkthrough

The complete user-provided six-page study guide: all 52 numbered problems, including all 21 derivative-table entries and all 10 true/false statements.

The new edition has a neural synthetic voice (Lessac high), a slower pace, normalized volume, large captions visible directly in the video, 200 progressive solution steps, and chapter markers.

## Download

- [Full video](https://github.com/paulleio/exam-2/raw/refs/heads/main/Exam2-Complete-Clear-Voice.mp4)
- [Part 1: derivative table, powers, and basic rules — problems 1–8](https://github.com/paulleio/exam-2/raw/refs/heads/main/Exam2-Full-Part-1.mp4)
- [Part 2: products, quotients, and chain rules — problems 9–27](https://github.com/paulleio/exam-2/raw/refs/heads/main/Exam2-Full-Part-2.mp4)
- [Part 3: implicit/logarithmic differentiation and tangent lines — problems 28–39](https://github.com/paulleio/exam-2/raw/refs/heads/main/Exam2-Full-Part-3.mp4)
- [Part 4: particle motion and related rates — problems 40–47](https://github.com/paulleio/exam-2/raw/refs/heads/main/Exam2-Full-Part-4.mp4)
- [Part 5: approximations, differentials, and true/false — problems 48–52](https://github.com/paulleio/exam-2/raw/refs/heads/main/Exam2-Full-Part-5.mp4)

See `Complete-Lesson-Transcript.md` for the complete equations and narration. The first, shorter video remains available as `Exam2-Calculus-Lesson.mp4`.

## Source details

- Problems 1(f) and 1(i) both print sine x; both are covered as printed.
- Problem 25 treats k as a constant.
- Problem 46 reports the rotation-rate magnitude and explains the direction convention.
- Problem 52(e) is the usual square-root chain rule where f(x)>0. The lesson explains why differentiability of f alone does not guarantee differentiability of its square root at zeros.
- Differential error estimates in problem 51 are first-order estimates, not exact bounds.

## Reproduce or edit

Unzip `Complete-Lesson-Source.zip`. Install Python 3.12, FFmpeg with libass, DejaVu Sans fonts, NumPy, Pillow, Matplotlib, and SymPy. Install `piper-tts==1.8.0` into `vendor`. Download the public voice archive recorded in `voice-PROVENANCE.json`, then extract its ONNX model and adjacent JSON into `voice/vits-piper-en_US-lessac-high/`. Run `python check_math.py` and `python build.py`. To rebuild one section, use `python build.py --part 1` (or 2–5). Run `python check_video.py` after a complete render.

Edit `lesson.json` to change equations and narration. The renderer caches narration by text, so unchanged speech can be reused. Model attribution is included in `VOICE-MODEL-CARD.txt`; model weights are not included in the source ZIP.
