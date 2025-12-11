# Easy Russian
> Type Russian letters with an English keyboard — no layout memorization required.

**Easy Russian** is a tiny web tool that lets you type Russian (Cyrillic) using only Latin letters, based on **shape similarity** and **sound similarity**.

Instead of switching keyboard layouts or memorizing where every Russian key is, you just type with your normal English keyboard and the page converts it to Cyrillic.

---

## Features

- **Real-time transliteration**
  - Example:  
    `privet, kak dela?` → `привет, как дела?`
- **Custom transliteration scheme**
  - Designed around *形近 (shape-similar)* + *音近 (sound-similar)* principles
  - Single letters: `a → а`, `c → с`, `y → у`, `u → и`, etc.
  - Multi-letter combinations with a backslash escape:
    - `\ya → я`
    - `\yu → ю`
    - `\zh → ж`
    - `\ch → ч`
    - `\sh → ш`
    - `\sch → щ`
- **Soft / hard signs**
  - `\"` → `ъ` (hard sign)  
  - `\'` → `ь` (soft sign)  
  - These **never get auto-capitalized** (by design).
- **Longest-match, prefix-safe parsing**
  - Multi-letter sequences are matched greedily (3 → 2 → 1), avoiding conflicts.
- **Built-in mapping table**
  - The web page includes a full mapping table that shows:
    - Type (multi-character / single-character)
    - Input pattern
    - Output Cyrillic
    - Design principles (形近-手写体 / 印刷体, 音近-拼音 / IPA)
    - Notes / mnemonics

Everything is written in **plain HTML + CSS + JavaScript**. No backend, no build step.
