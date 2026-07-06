# EchoCast Architecture

## Overview

EchoCast converts AI conversations written in Markdown into a natural podcast using Google Cloud Text-to-Speech (Chirp3).

```
chat_original.md
        │
        ▼
 Markdown Parser
        │
        ▼
 Dialogue Analyzer
        │
        ▼
 Podcast Rewriter
        │
        ▼
 Voice Selector
        │
        ▼
 Google Cloud TTS (Chirp3)
        │
        ▼
 Audio Generator
        │
        ▼
 OGG Merger
        │
        ▼
 BGM Mixer
        │
        ▼
 podcast_final.ogg
```

---

## Components

### Markdown Parser

Reads the source Markdown file and extracts each dialogue.

---

### Dialogue Analyzer

Determines:

- Speaker
- Text
- Emotion (future)
- Pause (future)

---

### Podcast Rewriter

Converts chat logs into natural spoken dialogue.

Examples:

- Remove repetitive wording
- Add filler words
- Improve flow

---

### Voice Selector

Assigns voices.

Current plan

Gemini
- Bright male voice

Human
- Calm low female voice

---

### Google Cloud TTS

Uses Cloud Text-to-Speech Chirp3.

Output:

- Individual OGG files

---

### Audio Generator

Generates

001.ogg

002.ogg

003.ogg

...

---

### OGG Merger

Concatenates all generated audio files.

---

### BGM Mixer

Adds intro/outro music.

Adds background jazz.

Automatically adjusts volume.

---

### Output

Final output

podcast_final.ogg
