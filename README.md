# Reinforcement Learning lecture transcripts

An indexed archive of English captions from the first 34 lectures of the IIT Madras NPTEL course, *Introduction to Reinforcement Learning* by Balaraman Ravindran.

The rendered transcripts and their source caption tracks are in [captions/](captions/README.md). The Markdown files preserve the caption text, with timestamp links back to the corresponding video. They are intended for personal study, including use with a preferred AI study tool.

## Rebuild the transcripts

The repository includes the downloaded WebVTT tracks and metadata required to regenerate the archive:

```bash
python3 build_markdown.py
```

The script writes the lecture Markdown files, `captions/README.md`, and `captions/manifest.json`.

## Source

[NPTEL YouTube playlist — Introduction to Reinforcement Learning](https://www.youtube.com/playlist?list=PLEAYkSg4uSQ0Hkv_1LHlJtC_wqwVu6RQX)
