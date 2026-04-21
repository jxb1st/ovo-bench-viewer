# OVO-Bench Viewer

Case-by-case web viewer for [OVO-Bench](https://github.com/JoeLeelyf/OVO-Bench) — ships with a 24-sample representative subset (2 per task × 12 tasks).

**Live site:** https://jxb1st.github.io/ovo-bench-viewer/

## Tasks (grouped by temporal category)

**Backward Tracing** — reason about past events in the already-seen video
- EPM (Episodic Memory), ASI (Action Sequence Identification), HLD (Hallucination Detection)

**Real-time Visual Perception** — answer about the current frame/probe timestamp
- STU (Spatial), OJR (Object), ATR (Attribute), ACR (Action), OCR, FPD (Future Prediction)

**Forward Active Responding** — decide when to respond across a sequence of probes
- CRR (Clue Reveal Responding), SSR (Sequential Step Recognition), REC (Repetition Event Count)

## Contents

- `index.html` — single-file viewer (probe timeline + clip viewer + MCQ display)
- `data/ovo_bench_new.json` — filtered to 24 samples
- `data/chunked_videos/` — 59 re-encoded 480p mp4s (forward tasks have one clip per probe)
- `file_durations.json` — duration lookup
- `selection_report.md` — which samples were picked

## Local preview

```bash
cd ovo-bench-viewer
python3 -m http.server 8000
# open http://localhost:8000/
```

## Full benchmark

For the full dataset and evaluation code, see the [official OVO-Bench repo](https://github.com/JoeLeelyf/OVO-Bench).
