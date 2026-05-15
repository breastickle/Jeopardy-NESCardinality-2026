# Jeopardy! NESCardinality 2026 (IPS Patch)

A custom-content romhack of *Jeopardy! 25th Anniversary Edition* (NES). Apply this `.ips` patch to a clean dump of the original USA cartridge to play through Episode 1.

## Background

The patch is in homage of **NESCardinality**, who has held the *Jeopardy! 25th Anniversary Edition* (1990) world record in the Win (Versus) category since May 23, 2018, with a time of **16m02s**.

## Source ROM verification

Before patching, confirm your ROM is the No-Intro dump this patch targets. A mismatched dump (different region, header variant, prior romhack, or corrupted bytes) will produce a broken patched ROM.

The fastest check: drop your `.nes` file into [**Hasher-js at romhacking.net**](https://www.romhacking.net/hash/). The file is processed in-browser &mdash; your ROM never leaves your machine &mdash; and you'll get every hash and database match below in a couple of seconds.

| Field | Value |
| --- | --- |
| Title | *Jeopardy! 25th Anniversary Edition (USA)* |
| No-Intro database | Nintendo Entertainment System (v. 20210216-231042) |
| File SHA-1 | `44AE6D2E2FFB202F3BBDB678FCADE84340415B4E` |
| File CRC32 | `FB72E586` |
| ROM SHA-1 | `317FB395B4D408F3A4BEF73DD54C92FBB7748F4D` |
| ROM CRC32 | `0BDD8DD9` |

**File** hashes cover the whole `.nes` file (16-byte iNES header + cartridge data); **ROM** hashes cover just the cartridge data (header stripped).

On NES, the **ROM** hash is the authoritative identifier &mdash; per Hasher-js's NES guidance. If your **ROM SHA-1** matches but your **File SHA-1** doesn't, your dump is almost certainly fine: the iNES header is just carrying stray data, usually harmless. A header cleaner can normalise it if a particular emulator chokes on the patched output. A matching database name is a hint; always verify against the hashes themselves.

> **Hasher-js display quirk** &mdash; the CRC32 fields drop leading zeros, so this ROM's CRC32 shows up as `BDD8DD9` (7 hex digits) in the Hasher-js output. The canonical 32-bit value is `0BDD8DD9`. If a check gives you a 7-character CRC32, pad it with a leading zero before comparing.

## What's in the patch

Three running themes shape the rewritten clue set:

1. **NES and other video games** &mdash; console-era trivia, the wider 8- and 16-bit catalogue, and adjacent gaming history.
2. **Canadian and American geography** &mdash; provinces, states, capitals, landmarks, and regional culture.
3. **Modernized facts** &mdash; updates to outdated factoids, world events, and pop-culture references that have aged out since the original game was shipped.

Great care was taken with spelling, alternate replies, and a wide-ranging difficulty curve. No guarantees are made for performance, spelling, grammatical or factual errors, or fun.

A handful of quality-of-life conveniences are baked in. Last names of famous people, numerals in place of spelled-out numbers, and the other expected NES Jeopardy shorthand should all be accepted. There's no penalty for overly verbose answers as long as your input phrase matches the desired response.

Easter-egg names are scattered through the NPC roster &mdash; be sure to drop them into your games from time to time.

I tried to make the Final Jeopardy prompts fun, thoughtful, but not always impossible.