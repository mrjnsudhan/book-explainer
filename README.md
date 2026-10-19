# Book Explainer

Interactive, chapter-by-chapter explainers for books, podcasts and topics, plus a bookshelf home page that links them together. Every page is a single self-contained HTML file with no build step.

## What's inside

| Page | What it covers |
| --- | --- |
| `index.html` | The Explainer Shelf: the home page with every explainer as a spine on a shelf |
| `explainers/brief-answers.html` | *Brief Answers to the Big Questions*, Stephen Hawking (10 chapters) |
| `explainers/the-mountain-is-you.html` | *The Mountain Is You*, Brianna Wiest (7 chapters) |
| `explainers/naval-harsh-truths.html` | Naval Ravikant on Modern Wisdom with Chris Williamson, episode #922 (10 chapters, golden nuggets, timestamp links) |
| `explainers/bezos-lex-fridman.html` | Jeff Bezos on the Lex Fridman Podcast, episode #405 (10 chapters, golden nuggets, timestamp links) |
| `explainers/48-laws-of-power.html` | *The 48 Laws of Power*, Robert Greene (all 48 laws, each with its own illustration, plus six workshops) |
| `explainers/art-of-war.html` | *The Art of War*, Sun Tzu (all 13 chapters, each with its own illustration and key principles, plus five workshops) |
| `explainers/transformers.html` | The Transformer model, a topic rather than a book, based on *Attention Is All You Need* (Vaswani et al., 2017) (10 chapters, a hands-on lab in each: tokenizer, meaning map, attention heatmaps, query steering, translation, temperature) |
| `explainers/ai-engineering.html` | *AI Engineering: Building Applications with Foundation Models*, Chip Huyen (10 chapters, each with a worked example in real numbers, a live lab such as a sampling desk, a BM25 retriever, a GPU memory calculator, a KV cache sizer and a batching simulator, reflection prompts and a three-question quiz) |

Each explainer has plain-language chapter summaries, an interactive exercise per chapter, a quick quiz, a light/dark toggle, and "I understand this chapter" progress saved in the browser's localStorage.

## Viewing it

Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

To host it, turn on GitHub Pages for this repository (Settings → Pages → deploy from the `main` branch, root folder).

## Adding a new explainer

1. Add the page as `explainers/<slug>.html`, using the same shell as the others (Instrument Serif, Geist and Geist Mono; chapter rail; light/dark toggle; a "Back to the bookshelf" link to `../index.html`).
2. Add one entry to the `BOOKS` array at the top of the script in `index.html` (title, spine, author, optional `by` line, year, optional display date `when` such as "c. 5th century BC", chapters, tag, url, blurb, extras, spine colours `c`/`k`, size `h`/`w`, an optional short spine name `au`, and a `mark` icon: `star`, `peak`, `mic`, `crown`, `sword`, `nodes` or `layers`).

All explanations are written in original wording. They summarise the source material and are not affiliated with its authors.
