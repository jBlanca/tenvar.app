# Changelog

## v0.1.0 — early access

The first public build. Everything runs on your own machine.

**Recording**
- Record your microphone, your computer's own audio, or both as separate channels.
- Scope a recording to one conference application — Zoom, Teams, Webex, Meet and others — so
  notifications and other apps stay out of it.
- Record several applications at once, each on its own channel.
- Optionally add a camera track, or capture a single window's picture on Windows and macOS.
- Type notes while recording; each line keeps the moment you wrote it.

**Transcription**
- Four speech engines: Whisper, plus Parakeet (25 languages), Qwen3-ASR (52) and Canary, which
  also translates.
- Word-level timing, so clicking a word lands on that word.
- Voice detection and repetition guards, which keep the model from inventing speech over music or
  a silent room.
- Speaker identification, with names that carry across later recordings once you set them.
- Batch transcription, and inline correction of any line.

**Subtitles**
- Export SRT, VTT, ASS, SBV and plain text.
- Embed subtitles into a video, or burn them into the picture.
- Long captions are reshaped and retimed to word boundaries so they stay readable.

**Documents**
- PDF, Word, RTF, PowerPoint, spreadsheets, EPUB, email archives, text and images.
- Scanned pages are read with on-device OCR, accelerated by your graphics card.
- An optional vision model handles dense pages and tables.
- CBZ and CBR comic archives open as a reader, with page order and reading direction.

**Finding things**
- Ask a question of one file, a folder, a thread or a note.
- Answers cite their sources, and a citation plays the moment or shows the page it came from.
- Counts, lists and comparisons are answered exactly from your library, without a model guessing.
- Answers can be read aloud in 31 languages.

**Marking and reporting**
- Mark a passage of speech, a region of a page, a video frame, a picture or a sentence you wrote.
- Collect related marks onto threads that span every file in a folder.
- Compose reports whose citations still play the original audio — in one exported HTML file, with
  no application and no internet.
- Also export to DOCX, PDF, Markdown and a presentation deck, with six citation styles.

**Notes**
- A plain editor that imposes no styling on your words.
- Reference any source, or an exact moment or page inside one.
- Version history, with named snapshots and a view of what changed.

**Bringing things in**
- A web reader that strips ads and trackers, and clips what you keep into your library.
- Save a page as a PDF with real, searchable text.
- Link an Obsidian vault and read it in place, or convert it once into editable notes.

**Privacy and safekeeping**
- Everything encrypted at rest, with the key in your operating system's credential store.
- Optional PIN lock.
- Export a folder as one password-encrypted file and restore it on another machine.
- An audit log of every network request the application has ever made.

### Known limitations

- **The installers are not code-signed yet.** Windows and macOS will warn you the first time you
  open one; see the [README](README.md) for the steps. Signing is planned before v1.
- macOS requires Apple Silicon and macOS 14.4. Capturing a specific window requires macOS 15.
- Live captions while recording are not included: the transcript is produced after you stop, which
  is both more accurate and better timed.
- The Linux downloads are large because they carry two graphics acceleration paths.
