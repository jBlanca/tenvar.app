# Changelog

## v0.4.0 — early access

Longer writing projects, Apple Notes imports, and clearer speaker identification.

**Manuscripts**

- Arrange your notes into manuscripts with parts, chapters and scenes, an editable outline,
  and word counts.
- Read the manuscript in order, save named drafts, and restore a draft as an independent copy.
- Export a captured manuscript to DOCX or PDF. Saved drafts retain their supporting sources
  and pictures and follow the project's password protection.

**Apple Notes on macOS**

- Browse Apple Notes from Shelves and add individual notes to a project, or import a library.
- Imports create editable copies with available attachments. Apple Notes itself is unchanged.
- Rescan an imported library to bring in new notes and update untouched copies. Your Tenvar
  edits are preserved when the two copies conflict.

**Speaker identification**

- Nemotron 3 is the default speaker-identification engine, automatically detecting up to
  eight speakers. The Classic engine remains available when you need to specify a count.
- Redo speaker identification from the transcript and correct speaker assignments for
  individual passages. Colored labels make dialogue easier to follow.

**Linux downloads**

- Built against the Ubuntu 24.04 / glibc 2.39 baseline.
- AppImages include the native GTK video output and codec components needed for common
  video and audio formats, including HEVC video and E-AC-3 soundtracks.
- Standard and NVIDIA CUDA builds remain available as both AppImage and Debian packages.

**Free-plan allowances**

- The free plan now includes **one Tenvar project plus one imported library**, choosing
  either Obsidian or Apple Notes. The two allowances are separate.
- Existing projects and imported libraries remain usable, including those above the limits.
  A license removes both limits.

**Limitations and compatibility**

- Windows installers remain unsigned and may show a SmartScreen warning.
- Apple Notes import is macOS-only. Locked notes are skipped, Apple-specific formatting
  is not guaranteed, and unavailable attachments are reported rather than silently dropped.
- Linux requires glibc 2.39 or newer; older distributions need an OS upgrade.
- Backups containing manuscripts use a newer format and require Tenvar 0.4.0 or later to
  restore. Earlier backup formats remain readable.

## v0.3.0 — early access

A release about Obsidian: bringing a vault in whole, keeping what makes it a vault,
and leaving the original exactly where it is.

**Bring an Obsidian vault in**
- Convert a vault into a Tenvar folder. Tenvar copies it and owns the copy — **your
  original vault is never moved, edited or written to.** It stays a working Obsidian
  vault, and you can keep using it.
- A converted vault opens as its own graph, with your wikilinks drawn between notes and
  your folder tree still down the side.
- Notes keep what they were: equations, code blocks, callouts, nested lists, embedded
  notes, tags, properties, and the dates they were actually written.
- Links between notes survive the move, and links that pointed at attachments still find
  them.
- Obsidian Bases come across as collections you can read.
- If a conversion is interrupted, it picks up where it stopped rather than starting over.
- Leave whenever you like: export the whole folder back out as ordinary Markdown, in its
  own tree, with its media beside it.
- Tenvar now asks about a vault it finds in a folder you already watch, once, rather than
  deciding for you.

**Transcription**
- The Fast engine (Parakeet) now uses your graphics card. It was CPU-only before.
- Long recordings transcribe faster, and progress reflects real position throughout.
- Word-level timing is back on the accurate path, so clicking a line lands on the right
  moment and subtitles line up.

**Answers you can check**
- Extraction now reads across every part of a document, not just the first.
- Evidence from several pages is merged into one answer instead of competing.
- Flashcards and follow-up questions carry their citations with them.
- AI results keep their provenance when copied.

**Files**
- TIFF images display. Every picture gets a real thumbnail instead of a spinner.
- Describe an image from its own workspace, and the map reads that description.

**The map**
- Rebuilt so a folder's shape is legible at a glance, with depth and a little parallax.
- A file shows what it still needs — transcribing, or indexing — and now says **why** when
  it cannot be made searchable, and offers the model.

**Licensing**
- The free plan is **two Tenvar folders and one converted Obsidian vault**. These are
  separate: converting a vault does not use up a folder place. Shared sources use neither.
- Folders you already have keep working, including any above these limits.

**Your copy of the terms**
- The licence agreement, the privacy policy and the licence of every third-party component
  now ship inside the app, on all three platforms, readable offline in Settings. The 0.2.0
  Windows and macOS builds went out without them; this closes that.
- A one-time notice asks you to accept the agreement, with the full text one click away.

**Fixes**
- Linux: the map was spending seconds a frame drawing shadows. It doesn't any more.
- The status bar reported the Fast engine as running on the CPU when it was on your GPU.
- Recordings and books stopped re-indexing themselves after unrelated edits.
- Meeting-window recording keeps its picture when the window is still or resized.
- A transcription that finished is no longer reported as failed when the helper crashes on
  its way out.
- Builds no longer carry the build machine's own file paths.

## v0.2.0 — early access

A release about the things around your recordings: the files you already have, the
meetings you sit in, and the report you hand over at the end.

**Browse what you already have**
- A new **Shelves** view turns folders you approve into a private library — your audio,
  video, documents, books, comics and notes, listed where they already live. Nothing is
  moved, copied or read until you ask.
- Open a file to look at it first. **Add as source** is the moment it becomes yours to
  transcribe, read, mark and cite, and it is always your decision.
- Find across everything on the shelves by name, by wording, or by meaning.

**Meetings**
- Record a meeting window, with your camera in the corner if you want it. The people on
  the call and your own microphone stay on separate tracks, so each is transcribed on its
  own.
- The recording screen now shows you what is being captured while it happens.

**Reports**
- Reports are written on real pages now — A4, Letter or Legal — and what you see while
  writing is what the PDF gives you.
- A familiar ribbon replaces the old scattered controls.
- A second way to work: **Designed pages**, for when you want to place everything exactly
  where you want it rather than write straight down the page.
- Two handoffs, both self-contained: a web page whose citations still play, and a PDF.

**More kinds of file**
- Word 97, PowerPoint, WordPerfect, Works, iWork and dozens of other office formats,
  through an optional one-time download.
- Saved web pages, previewed before you bring them in.
- iPhone photos (HEIC) on macOS.

**Notes**
- Export a note as a faithful web page, or as a Markdown package with its media beside it.
- One picker for sources, and a marks pane that lists both what you marked and what you
  cited.

**Privacy and safety**
- Protect a folder with a password. Its contents are sealed until you unlock it.
- Problem reports you compose offline and send yourself, if you want to. Tenvar still
  receives nothing.
- The shared folder is now called **Shared**.

**Downloads**
- Windows now comes in two builds, as Linux already did: a standard one that still uses
  your graphics card, and a larger NVIDIA CUDA build. The update check offers the right
  one for your machine.

**Fixes**
- Linux: meeting-window recording keeps its picture, and screen captures are the right
  shape.
- Long recordings no longer run out of memory while transcribing, at any length.
- Subtitles clear from the screen when the speaking stops, and long lines are split.
- macOS: office documents open on a notarized install.
- Many fixes across Shelves, Reports, Notes and playback.

## v0.1.1 — early access

Smaller downloads, and a round of fixes from the first weeks of use.

**Downloads**
- Windows and Linux now come in two builds each. The standard one is a fraction of the old
  size and still uses whatever graphics card you have — AMD, Intel or NVIDIA; the separate
  NVIDIA CUDA build keeps the fastest transcription on those cards. The in-app update check
  offers the build that fits your machine.

**Fixes**
- Linux: camera recording works reliably now — a live self-view while recording, correct
  clip length, and saved takes no longer lose their video.
- Linux: on some built-in microphones the level meter sat near the top in a silent room and
  recordings lost headroom; the signal is re-centred before anything reads it.
- macOS: the notarized build was being denied the camera and the microphone — fixed.
- The screen after saving a recording hands off to the file's own workspace, and the
  just-stopped take previews its whole picture.
- "Delete everything" really deletes everything now, and the app keeps working afterwards
  without needing a restart.
- Closing a media preview inside a note could stop the app responding — fixed.

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

- **The Windows installers are not code-signed yet**, so SmartScreen will warn you the first time;
  see the [README](README.md). The macOS build is signed and notarized and opens normally. Windows
  signing is planned before v1.
- macOS requires Apple Silicon and macOS 14.4. Capturing a specific window requires macOS 15.
- Live captions while recording are not included: the transcript is produced after you stop, which
  is both more accurate and better timed.
- The Linux downloads are large because they carry two graphics acceleration paths.
