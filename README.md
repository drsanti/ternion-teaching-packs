# TERNION Teaching Packs

Ready-to-teach courses for [TERNION](https://github.com/drsanti/ternion-presenter): each pack is an ordinary TERNION content pack
(`.ternion-plugin`) with `teaching.json` course metadata (ADR 0051). Teachers get them from the **Teaching Library** in the app, without
a GitHub account; lessons are imported as their own editable copies.

| Pack | Language | Lessons | Time |
| --- | --- | --- | --- |
| `intro-to-ternion-en` — Introduction to TERNION | English | Your first deck · Live data and widgets · The interactive classroom | 110 min |
| `intro-to-ternion-th` — แนะนำ TERNION | ไทย | สไลด์ชุดแรกของคุณ · ข้อมูลสดและวิดเจ็ต · ห้องเรียนแบบโต้ตอบ | 110 นาที |

No equipment is needed: lesson 2 uses built-in demo signals and lesson 3 a simulated board.

## Layout

```text
packs/<pack id>/
  manifest.json      the plugin manifest (kind "pack")
  teaching.json      course metadata: title, levels, lessons, guides, licence
  lessons/*.json     the lesson decks
  guides/*.md        teacher and student guides
dist/
  <pack id>-<version>.ternion-plugin   the release files
  catalog-entries.json                 each file's SHA-256, for the app's catalog
```

## Building a release

The packs are built and checked with the app's own pack tool, so a pack that builds is a pack the app can install:

```bash
# in a checkout of ternion-presenter, next to this repository
pnpm pack:sample
```

This rewrites `packs/` and `dist/` here. The same sources always give the same bytes, so the SHA-256s only change when a pack changes.

Then publish the two `.ternion-plugin` files as assets of a GitHub Release tagged `v<version>` (for example `v1.0.0`), and copy the
`sha256` values from `dist/catalog-entries.json` into the app's bundled catalog. The app refuses a file whose SHA-256 doesn't match, so
a release must never be replaced in place: publish a new version instead.

## Licence

The course content is licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — attribution: TERNION.
