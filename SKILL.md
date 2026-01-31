---
name: "skill-record-doc"
description: "Extracts core content from audio recordings into a Word document. Invoke when user wants to convert audio/video to a summary Word file."
---

# Record Doc Generator (skill-record-doc)

This skill extracts the core content from an audio/video recording file and generates a structured Word document summary.

## Functionality
- **Input**: Audio or Video file path (e.g., .mp3, .mp4, .wav).
- **Processing**: 
  - Simulates transcription (or connects to ASR service).
  - Extracts key themes, decisions, and action items.
- **Output**: A Microsoft Word (.docx) file containing the summary.

## Usage

### 1. Basic Usage
Invoke the skill when the user asks to "generate a document from recording" or "summarize this audio file".

```bash
python skills/skill-record-doc/scripts/audio_to_word.py --input "path/to/audio.mp3"
```

### 2. Output Format
The generated Word document will include:
- **Title**: Derived from filename or content.
- **Meeting Information**: Date, Participants (inferred).
- **Core Content**: 
  - Key Topics
  - Discussion Points
  - Conclusions
- **Action Items**: List of tasks and owners.

## Dependencies
- `python-docx`: For Word document generation.
- `argparse`: For command line argument parsing.

## Example
User: "Help me turn `interview.mp3` into a Word report."
Agent: Runs the `audio_to_word.py` script.
