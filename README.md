# Norrsaga

Norrsaga is an audiobook and podcast client for self-hosted
[Audiobookshelf](https://www.audiobookshelf.org/) servers, made by
[Koeda Studio](https://koeda.studio). It runs on iPhone, and in the car on
Android Automotive OS.

This repository is the public home of the project: what Norrsaga is, how to
get help, and where to report bugs and request features. The app source code
itself is not public.

## The apps

- **iOS** — Audiobookshelf client for iOS, with offline downloads, an Up Next
  queue that follows you between devices, new-episode notifications for
  podcasts, and much more.
- **Android Automotive OS** — browse, play and resume your library on the car
  screen, straight against your own server.

Both apps are in pre-release. Store and TestFlight links will appear here
when they are out.

## Listening to ebooks

Ebooks in your library that have no audio can be narrated on the fly by
[norrsaga-narrator](https://github.com/koedastudio/norrsaga-narrator), a small
open-source sidecar you run next to Audiobookshelf. It turns any epub into an
audio stream that starts within seconds and keeps your reading position in
sync, so you can switch between reading and listening. It is optional; the
apps work fine without it.

## What you need

- An Audiobookshelf server, version 2.36 or newer recommended.
- HTTPS on that server. Release builds refuse plain `http://`.
- Optionally, a running norrsaga-narrator for ebook narration.

## Privacy

No analytics, no accounts, no third parties. The apps talk to your server and
nothing else, with one exception: if you turn on new-episode notifications on
iOS, Audiobookshelf's own notification passes through a small relay we run,
which hands it to Apple and stores nothing.

## Bugs, ideas and questions

- Open an [issue](https://github.com/koedastudio/norrsaga/issues/new/choose)
  here. There are templates for bug reports and feature requests, each with a
  dropdown for which app you mean.
- Problems with the ebook narration itself (the audio, the sidecar, its API)
  belong in the
  [norrsaga-narrator issues](https://github.com/koedastudio/norrsaga-narrator/issues).
- Security problems: please report them privately, see
  [SECURITY.md](SECURITY.md).

## Source code and licensing

The Norrsaga apps are closed source for now. Everything around them is open:

- [norrsaga-narrator](https://github.com/koedastudio/norrsaga-narrator) — the
  ebook narration sidecar, GPL-3.0.
- [Norrklang](https://github.com/koedastudio/norrklang) — our sibling app for
  music: a car client for Navidrome, other Subsonic servers and Plex, GPL-3.0.
  Norrsaga grew out of Norrklang and shares much of its design.
