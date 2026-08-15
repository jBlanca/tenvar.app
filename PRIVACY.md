# Privacy

Tenvar is built for work that cannot leave the room — sessions, interviews, case files, records.
This page describes exactly what the software does with your data. It describes the software, not
intentions: everything below is enforced in the application itself.

## Your content stays on your machine

Recordings, transcripts, documents, images, notes, marks and reports are written to your own disk
and nowhere else. They are **encrypted at rest** with a key held in your operating system's
credential store — the Windows Credential Manager, the macOS Keychain, or your Linux login keyring.

There is no account. There is no sign-in. There is no server holding a copy.

Transcription, speaker identification, search, question answering, OCR and read-aloud all run
**on your own processor or graphics card**, using models stored on your disk. No part of a
recording or a document is sent anywhere to be processed.

## Everything Tenvar ever sends

The application's interface is blocked from making network requests at all, by a content security
policy. Every request below is made deliberately by the application core, and **every one is
written to an audit log you can read at Settings → Privacy → Network activity.**

| What | When | What it carries |
| --- | --- | --- |
| **Model downloads** | Only when you choose to install a model | The model's address. Nothing about you or your files. |
| **Web and email import** | Only if you switch it on — **off by default** — and then give Tenvar an address to read | That address. |
| **Update check** | Only when you press *Check GitHub* in Settings | Nothing but the request itself. |
| **Licence activation** | Once when you activate a key, then at most weekly | Your licence key and a machine identifier, to [Polar](https://polar.sh). Nothing else. |

That table is the complete list. There is no analytics, no crash reporting, no usage measurement,
no advertising identifier, and no background check of any kind.

### About the licence check

A licence key is verified with [Polar](https://polar.sh), the payment provider, when you activate
it, and re-checked at most once a week afterwards. The machine identifier sent with it is a
**hash** — your hardware identity is not stored anywhere in readable form, and its only purpose is
to enforce the activation limit so one key cannot be shared indefinitely.

**Being offline is never treated as a verdict.** If the check cannot complete for any reason, your
licence stays active and the application carries on. Only an explicit statement that a key was
revoked will deactivate it.

Activating a licence does require an internet connection once. Everything else in Tenvar works
without one.

## What Tenvar cannot do

- It cannot read your files without being pointed at them.
- It cannot send a recording, transcript, document or report anywhere.
- It cannot install or update itself without you pressing the button.
- It cannot record your screen or microphone without you starting a recording.

## Your data is portable, and yours to destroy

A folder can be exported as a single password-encrypted file and restored on another machine.
Deleting a recording deletes its file, its transcript, and everything derived from it. Clearing
your library removes all of it from disk.

If you identify speakers by name, the voice signatures that make recognition possible are stored
with your library, are listed at **Settings → Privacy → Known voices**, and can be removed there
individually. They never leave your machine.

## Payments

Licences are sold through [Polar](https://polar.sh), which handles payment and holds whatever
billing details you give it under its own privacy policy. Tenvar itself never sees your payment
details; the application only ever handles the licence key you paste into it.

## Changes

If this policy changes in a way that affects what leaves your machine, it will be stated in the
[changelog](CHANGELOG.md) for the version that changes it — not silently amended here.

Questions: [open an issue](https://github.com/jBlanca/tenvar.app/issues).
