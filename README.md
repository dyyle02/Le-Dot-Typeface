# Le Dot

A typeface created by **Dylan Le**. Le Dot experiments with a systematic yet experimental design
language following a grid format. Every letter is assembled from circles that snap to a fixed
matrix. Nothing drawn freehand, nothing sitting off-grid. It reads as engineered rather than
lettered, and legibility arrives as a consequence of the system instead of a compromise with it.
Five cuts run from a workable text weight through to a full-bleed display matrix.

Structurally: dots are 13 units across on a 14-unit pitch, built at 250 units on a 1000-unit em, so
one dot and one row each measure a quarter of an em. The cap box is four rows tall and descenders
drop one row below the baseline. All five cuts share that matrix and those metrics conventions, but
Round and Block are distinct dot arrangements, Round sparser than Regular and Block denser, while
Display and Grid Display carry Regular's exact glyphs, respaced to set flush. 97 glyphs per cut.

---

## The cuts

| Cut | Sidebearing | Word space | Notes |
| --- | --- | --- | --- |
| **Le Dot** | 1 circle | 2 columns | The text cut. Start here. |
| **Le Dot Round** | 1 circle | 2 columns | Sparser arrangement — 566 dots against Regular's 607. Lighter on the page. |
| **Le Dot Block** | 1 circle | 2 columns | Densest arrangement — 648 dots. Heaviest on the page. |
| **Le Dot Display** | none | 1 column | Regular's glyphs, set flush for large sizes. Letters butt dot to dot. |
| **Le Dot Grid Display** | none | 1 column | Display, plus every unlit cell of the matrix printed at 20%. |

97 glyphs each: uppercase, lowercase, figures, and punctuation.

## Metrics

Drawn on a 250-unit grid at 1000 units per em, so one dot = ¼ em and one row = ¼ em.

- **Cap box** — 4 rows (1 em)
- **Descender** — 1 row below the baseline
- **Seamless leading** — `1.25` for Regular, Round, Block and Display; `1.5` for Grid Display,
  whose glyph box carries an extra faint row above the caps and below the baseline

Set leading explicitly. "Auto" is usually close, but Figma and Adobe sometimes pad it, which breaks
the grid alignment between lines.

## Le Dot Grid Display

Grid Display is a **two-color font** (`COLR`/`CPAL`): the 20% grid is part of each glyph, not a
layer you composite yourself. Lit dots take the text color; unlit dots print at 20% of black. It
works anywhere `COLR` is supported — every current browser, Figma, Illustrator, Keynote. Renderers
that ignore `COLR` fall back to the plain letterforms, which degrades safely rather than breaking.

## Install

**Desktop** — double-click any `.ttf` in `fonts/`, or drop it into your system font folder.

**Web**

```css
@font-face {
  font-family: "Le Dot";
  src: url("fonts/LeDot-Regular.ttf") format("truetype");
  font-weight: 400;
}

h1 {
  font-family: "Le Dot", monospace;
  line-height: 1.25;
}
```

## Specimen

`index.html` is a self-contained specimen — open it locally or serve it from GitHub Pages
(Settings → Pages → deploy from branch root). It has a live tester, a size waterfall, the full
character set, and a before/after record of the symbol redraws.

## License

[SIL Open Font License 1.1](LICENSE) with **Le Dot** as a Reserved Font Name. Free to use, embed and
sell with your work; derivatives must stay under the OFL and ship under a different name. Swap this
out if you'd rather license it differently — nothing in the fonts depends on it.
