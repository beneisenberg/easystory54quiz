# פְּלִשְׁתִּים הֵשִׁיבוּ אֶת־אֲרוֹן יהוה

An interactive Biblical Hebrew comprehension game on 1 Samuel 5–6, the return of the ark from Philistine territory. Twenty multiple-choice questions, entirely in Hebrew with full niqqud, built for communicative / comprehensible-input classrooms.

Companion to [Lesson 141](https://www.youtube.com/watch?v=kXQMvxq65iM) (Level 54 — פְּלִשְׁתִּים הֵשִׁיבוּ אֶת־אֲרוֹן יהוה).

## What it does

Students answer in Hebrew and the cart carrying the ark advances along the road, passing אַשְׁדּוֹד, גַּת, עֶקְרוֹן, בֵּית שֶׁמֶשׁ and קִרְיַת יְעָרִים in narrative order. Each correct answer earns a כְּלִי זָהָב, echoing the golden objects the priests tell the Philistines to send back with the ark in chapter 6.

After every answer — right or wrong — the corresponding line of the biblical text appears, with Masoretic cantillation intact. The reward for answering is more Hebrew input, not a score animation. Questions missed along the way are collected into a review list at the end, so students can take them back to the video.

There is no English anywhere in the interface.

## Running it

One self-contained HTML file. No build step, no dependencies, no server-side anything. Open `index.html` in a browser and it works, including offline.

Nothing is transmitted or stored: no accounts, no analytics, no cookies, no saved progress. Students need only the link.

## Typography

Hebrew is set in **SBL Hebrew** (Tiro Typeworks, v1.56a), embedded in the file so every student sees the same rendering regardless of what is installed on their machine. The `@font-face` rule lists `local("SBL Hebrew")` first, so anyone who already has it installed loads their own copy and skips the ~315 KB download.

Type is set in the regular weight throughout. SBL Hebrew ships no bold, and synthetic bold smears badly over niqqud and taamim, so hierarchy runs on size and color instead. Leading is opened up well beyond a Latin-typeface default to keep cantillation above and below the baseline from colliding between lines.

## Adapting it

All twenty questions live in the `Q` array near the bottom of `index.html`. Each entry has the question (`q`), four options (`o`), and the verse shown as feedback (`v`). **The correct answer is always first in `o`** — options are shuffled at runtime, so order in the source carries no meaning beyond that. The five road stations are in `STATIONS`, each with the question number it begins at.

To build a game for a different passage, replace those two arrays and the title. Nothing else is passage-specific.

## License

The game — text, questions, code, design — is released into the **public domain (CC0)** by Ben Eisenberg / Lingua Deo Gloria, for the free use of the global church. Copy it, translate it, adapt it, teach with it, sell it, no attribution required.

**The embedded font is not covered by that dedication.** SBL Hebrew is © John Hudson, Tiro Typeworks, 2003 & 2007; SBL Hebrew is a trademark of the Society of Biblical Literature. It is redistributed here unmodified, with its embedding bit unaltered, under clauses 3 and 5 of the [SBL Font End User License Agreement](https://www.sbl-site.org/wp-content/uploads/2024/05/SBL_Font_End_User_License_Agreement.pdf), which permit free redistribution of the unmodified software and embedding in non-commercial electronic documents including web pages. The full license text travels inside `index.html`.

That license covers non-commercial use only. If you intend to use this commercially, contact the Society of Biblical Literature for a font license, or swap the `@font-face` rule for an open-licensed Hebrew face with cantillation support — Taamey Frank CLM, Taamey David, Keter YG, Ezra SIL and Cardo are all good candidates.
