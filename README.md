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
| `explainers/sapiens.html` | *Sapiens: A Brief History of Humankind*, Yuval Noah Harari (all 20 chapters across the four revolutions, a 13.8-billion-year timeline, and a lab in each chapter such as a species timeline, the wheat trap, a cuneiform number writer, the imperial cycle, Lind's scurvy trial, a credit multiplier and a happiness thermostat) |
| `explainers/thinking-fast-and-slow.html` | *Thinking, Fast and Slow*, Daniel Kahneman (all 38 chapters across the five parts, with a lab in each such as the Add-1 game, a rigged anchoring wheel, the cab problem, a regression-to-the-mean golf tournament, a loss-aversion curve, decision weights and a peak-end pain builder) |
| `explainers/exactly-what-to-say.html` | *Exactly What to Say*, Phil M. Jones (all 23 sets of magic words in five stages of a conversation, each with a sample exchange, a lab to write or test your own version, a quick check, and a personal script book that keeps the lines you save) |
| `explainers/influence.html` | *Influence: The Psychology of Persuasion*, Robert B. Cialdini (all nine chapters of the new and expanded edition, the seven principles including unity, the classic experiment behind each one as a lab you can rerun, such as Langer's copier queue, the restaurant mint, the crowd on the pavement, Milgram's shock board and the billboard on the lawn, plus how to say no and a seven-question defence kit) |
| `explainers/how-to-win-friends.html` | *How to Win Friends and Influence People*, Dale Carnegie (all 30 principles across the four parts, each with the story Carnegie tells, a sample exchange, a lab such as a smile reader, a name trainer, an "I" vs "you" counter, an argument model, a "but" detector and a praise simulator, a quick check, and a phrasebook that keeps the lines you save) |
| `explainers/personal-power.html` | *Personal Power*, Tony Robbins (the 30-day audio program: all 20 sessions across the month, each with the day's assignment, a quick check, and a graphic lab such as an aim-and-adjust target, a pain and pleasure scale, a habit groove you rewire, a state dial, a belief table you knock the legs out from, an anchor timing game, a compounding chart, a fear-movie scrambler and the success cycle, plus a 30-day tracker and a power journal that keeps what you write) |
| `explainers/principles.html` | *Principles: Life and Work*, Ray Dalio (the opening story and all 21 principles: five for life and sixteen for work, each with the story behind it and a graphic lab such as a career timeline, a Holy Grail diversification chart, a pain-plus-reflection spiral, a five-step radar, a believability-weighted balance, a root-cause drill-down, a machine you tune, a boiling-frog simulation and a checks-and-balances map, plus a builder for writing your own principles) |
| `explainers/dare-to-lead.html` | *Dare to Lead*, Brené Brown (the introduction and every section across the four skill sets of courage, each with a story from the book, a try-it-this-week line and a lab such as a team culture check, who gets a seat in the arena, a square squad, paint done, sixteen plates of armour to take off, an empathy responder, a curiosity curve, a narrow-to-two values picker, a marble jar with BRAVING bars, tactical breathing and a shitty-first-draft builder) |
| `explainers/the-one-thing.html` | *The ONE Thing*, Gary Keller with Jay Papasan (all 18 chapters: going small, the domino effect, the six lies, the focusing question and how to live it, each with a story from the book and a graphic lab such as two rabbits, a domino line that reaches the Moon, a Pareto funnel, a task-switching timeline, a habit curve, a willpower battery, a counterbalance seesaw, a big-and-specific quadrant, a happiness treadmill, a goal ladder from someday to right now, a weekly time-block planner and an E-to-P curve, plus a 66-day streak tracker) |
| `explainers/war-of-art.html` | *The War of Art*, Steven Pressfield (all three parts in fifteen chapters, from Resistance and its disguises to turning pro and the higher realm, each with the story from the book and a graphic lab such as a wall of Resistance you build, a Resistance compass, a finish-line surge, a critic's mirror, an excuse you stamp "true, but not a reason", a year of waiting for inspiration against a year of showing up, an Iditarod pacing chart, a you-and-your-work overlap, a ritual clock and a labour-or-fruit tree, plus a commitment and a 28-day sit-down log) |

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
2. Add one entry to the `BOOKS` array at the top of the script in `index.html` (title, spine, author, optional `by` line, year, optional display date `when` such as "c. 5th century BC", chapters, tag, url, blurb, extras, spine colours `c`/`k`, size `h`/`w`, an optional short spine name `au`, and a `mark` icon: `star`, `peak`, `mic`, `crown`, `sword`, `nodes`, `layers`, `hand`, `pencil`, `speech`, `magnet`, `smile`, `bolt`, `gear`, `shield`, `domino` or `nib`).

All explanations are written in original wording. They summarise the source material and are not affiliated with its authors.
