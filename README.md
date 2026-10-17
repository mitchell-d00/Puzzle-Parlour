<p align="center"><img src="logo.svg" width="96" alt="Puzzle Parlour logo"></p>

# Puzzle Parlour

A puzzle lounge in a single HTML file. Walk up to any of ten tables and
play: a Rubik-style colour cube (2×2 and 3×3), slide puzzles, jigsaws cut from
your own photos, Lights Out, Tower of Hanoi, Flood, Ball Sort, Maze Runner,
the Glitters & Sparkles match game and Block Stack (solo, Zen or against the
computer at five skill levels), plus **20 Questions**, where the computer
guesses what you're thinking from 1,004 things (and learns new ones) or you
guess what it's thinking. Next door, **The Show** is a studio of 20 easy card tricks: you
make one simple choice at a time, the computer does the magic, then it shows
you how to do it yourself.
A jukebox plays ten original music tracks while you play. Every table
has a live teacher, Professor Pip, who watches your moves, shows the next one
right on the puzzle, and teaches you the method so you can solve it alone.

It is free, with no ads, purchases or sign-up. Because it is one HTML file it
also runs offline once saved, and it is built for touch screens: tap, swipe,
drag, pinch and twist.

## Play

Open `index.html` in any browser. There is nothing to install or build.

To put it online, turn on GitHub Pages for this repository (Settings → Pages →
deploy from the `main` branch, root folder). The parlour will be served at
`https://<your-username>.github.io/<repo-name>/`.

Your stars, stats and settings are saved in the browser. Photos you use for
jigsaws and slide puzzles never leave your device.

## The floor

| Table | What's in it | How the teacher teaches it |
| --- | --- | --- |
| Color Cube | 2×2 and 3×3 cubes in 3D. Swipe a sticker to turn its row (middle slices too), drag the felt to look around, two fingers to twist. Notation pad, scramble, undo, timer | The seven-step beginner method (white cross, white corners, middle layer, yellow cross, Sune, A-perm, U-perm); the 2×2 in three steps. The layer to turn glows and every sticker shows an arrow. Practise any single step from the lessons |
| Slide Puzzle | 8, 15 and 24 puzzles with numbers or your own photo; tiles coloured by row | The row-and-column method: top row, left column, repeat, finish the 3×3. Finished parts lock; the hard last-tile-of-a-row loop is shown move by move |
| Jigsaw Studio | Any picture cut into **50, 100 or 500** real interlocking pieces, each one different. Snapping groups, optional rotation (tap to turn), pinch-zoom, ghost image, peek | Corners → edges → frame → colour patches. **Edges** sorts the border pieces into the empty frame; **Find a piece** highlights one and its spot |
| Lights Out | 3×3 to 7×7, classic or three-colour | “Chase the lights”, plus the exact presses (solved by Gaussian elimination over GF(2) or GF(3)) |
| Tower of Hanoi | 3–8 disks; tap or drag | Recursion. Shows the optimal next move from *any* position and how many moves remain |
| Flood | 10×10, 14×14, 18×18 | Head for the centre, then grow; two-move lookahead. The move limit comes from the teacher's own solution plus a few spare, and it warns you (with a rewind) when you can no longer finish in time |
| Ball Sort | 4–9 colours | Keep spare tubes empty; a solver plans the route and replans if you go your own way. If your own moves trap the rack, it works out exactly how many moves to rewind |
| Maze Runner | A new random maze every game at 5 skill levels: Stroll, Easy, Medium, Hard and Expert (big, branching, looped and foggy). Trace the path with your finger (the dot follows you; drag back along your trail to back up), junctions are hexagons that become tap-to-return save spots once you pass them, swipe to run to the next junction, tap to step, arrow keys | The right-hand rule and dead-end spotting; gold dots light up the shortest way out |
| Glitters & Sparkles | Match-3 with six colour-and-shape gems. The shape of a match makes magic: 4 in a line makes a Blaster, a T makes a Bomb, an **L sends out 4 gnomes** that smash 4 helpful gems (specials to set off, gems whose fall makes a new match, number gems), a **2×2 square makes a Wild gem** that counts as any colour when you swap it in, and 5 in a line makes a Prism. Number gems (×2, ×3, ×5) multiply the match; two numbers in one match set off a Number Storm. Cascades build combos, and swapping two specials makes mega effects. Levels, 90-second and Zen modes | Points out the best swap and why (which shape and special it makes) |
| Block Stack | Falling-block stacking with hold, next queue and ghost piece. **Solo** speeds up every 10 lines, **Zen** never ends, **Vs AI** trades junk rows when you clear 2+ lines. The AI has five skill settings: Rookie (slow, blunders), Easy, Normal, Hard (uses Hold) and Master (fastest, uses Hold and plans a block ahead) | Shows the spot its own AI would choose for your block, with tips on holes and height |

## The Show

Twenty easy card tricks the computer performs for you. Each one has a step
tracker at the top ("1 Think of a card · 2 Pick a pile · 3 Reveal"), asks you
for one simple thing at a time — think of a card, tap a pile, answer yes or
no — and shows what it is doing. Afterwards **How it works** explains the
secret in plain words, ending with **Do it yourself** instructions for a real
deck. Every explanation is also a page in the lesson book.

| # | Act | What you do |
| --- | --- | --- |
| 1 | The 21-Card Trick | Think of a card, say which pile three times |
| 2 | Your Lucky Number (27 cards) | Pick a number and a card; it ends up at your number |
| 3 | Row and Column | Say which row, then which row again |
| 4 | Yes or No | Four yes/no answers about 16 cards |
| 5 | The Card Detective | Think of any card in the deck; watch it get found in six questions |
| 6 | The Missing Card | Take a card away; the computer adds up the rest |
| 7 | Think of a Number | Four easy sums land you on the predicted card |
| 8 | The 10–20 Trick | Pick 10–19, deal, add the digits, count back |
| 9 | Pick a Card, Any Card | Choose a card, cut as often as you like |
| 10 | I Know the Top Card | Cut the deck; it names the top card |
| 11 | Twin Cards | Ask for perfect shuffles; top and bottom stay twins |
| 12 | Chase the Kings | Cut; all four Kings land in one pile |
| 13 | Red and Black | Deal in pairs; the red and black piles match |
| 14 | Five and Five | Cut and flip pairs; exactly five end face up |
| 15 | The 1089 Prediction | Pick three cards, two sums, always 1089 |
| 16 | Last Card Standing | Deal down, move under — the last card was predicted |
| 17 | Pick a Pair | Remember a pair, say two rows |
| 18 | Spell It Out | Spell A-C-E, T-W-O… each card appears on cue |
| 19 | Around the Clock | Pick an hour; the card at your hour is the prediction |
| 20 | Spell Your Name | Pick a card, spell your name, it turns up on the last letter |

The Show has its own shop tab with card-back kits and a dye.

## 20 Questions

The computer knows **1,004 things** across 30 groups — animals (from ferrets
to axolotls), birds, fish, bugs, dinosaurs, fruit and vegetables, meals,
sweets, drinks, flowers and trees (orchids included), vehicles (battleships
included), kitchen things, furniture, clothes, instruments, sports kit, toys,
gadgets, tools, places and landmarks, space and weather, jobs, sports and
games, body parts and creatures from stories — described by **208 yes/no
questions**.

- **I guess yours:** answer *Yes, Probably, Don't know, Probably not* or *No*.
  The brain is probabilistic: every thing has a chance of "yes" for every
  question, and each answer updates its confidence in all 1,004 at once
  (Bayes' rule), so a wrong answer lowers the odds instead of ruling the right
  thing out. Each question is the one with the most expected **information
  gain**, and a live chart shows its top guesses and their odds. You can
  change your last answer. It gets 20 questions and 3 guesses, and can ask for
  a bonus round of 5 more.
- **It learns:** every finished game nudges its numbers toward your answers.
  If you stump it, tell it what you were thinking of (and optionally a new
  question) — a brand-new thing starts from the things it most resembles, then
  your answers take over.
- **You guess mine:** search 208 questions, guess by searching 1,004 things.
  The teacher shows how many things still fit and which question is worth the
  most bits.

**How well it plays** (tested on every one of the 1,004 things):

| Player's answers | Found within 20 questions | With the bonus round |
| --- | --- | --- |
| All honest | 100% (about 14 questions on average) | — |
| 1 in 20 answers wrong | 87% | 95% |

Teaching it 10 brand-new things: it found all 10 in the next game. In the
browser each question takes about 20 ms to choose.

Also in the parlour:

- **Live teacher** with three modes: **Live** (every next move shown on the
  puzzle, replans instantly when you deviate), **Ask** (explains the stage,
  shows a move only when you tap Hint), **Off**. **Show me** plays one move;
  **Do this step** plays the rest of the current step. The teacher can read
  its tips aloud.
- **Lesson book** with a page for every step of every method. **Ask** a
  question and it answers only from those pages and tells you which page — the
  same rule as MPLPB: one page owns the question → that page; two tie → it asks
  which; none → "not in the book".
- **Puzzle shop:** every game has its own store tab and remembers its own look.
  Earn stars for every solve (a 50% bonus without hints), collect free daily
  stars, and check the deal of the day. No real money.
  - **Colour kits** are premade colour combos for that game. Buy once, then turn
    them on or off whenever you like.
  - **Table felts** are bought once and can go on any table; each table keeps
    its own.
  - **Dyes** let you pick your own colours for one game. Only the colours you
    change are dyed; the rest follow the active kit. Your colours are remembered
    until you reset them, and switching them off and on is free. Changing them
    again takes another dye.
- **Jukebox:** ten original tracks (Neon Lounge, Brass & Velvet, Cube Waltz,
  Slide Shuffle, Midnight Jigsaw, Arcade Rush, Zen Garden, Maze Runner, Stack
  Fever, Last Light), composed live in the browser with Web Audio — no audio
  files, so they work offline. Pick a track, skip, set the volume; the music
  keeps playing between tables and resumes on your next visit.
- **Tutorials:** a lounge tour and a how-to card the first time you sit at each
  table.
- **Settings:** light, dark or automatic theme; teacher mode; spoken tips;
  animation speed; sounds; vibration; a colour-blind palette.
- **Keyboard:** on the cube, U D F B R L M E S turn faces (Shift for
  counter-clockwise) and Space plays the teacher's next move; arrow keys slide
  tiles and walk the maze (Shift runs); Block Stack uses ← → ↓, ↑/X and Z to
  turn, Space to slam, C to hold and P to pause.

## How the solvers work

The engine is written from scratch in JavaScript and was tested in Node and a
headless browser:

- **Cube:** a 54-sticker model where every move is a permutation computed from
  3D rotations. Each teaching stage is a breadth-first search over the pieces
  that matter, using only the moves a learner would use at that stage (face
  turns for the cross; the corner trick, edge inserts, Sune, A-perm and U-perm
  later), so the plan is the beginner method, not a computer solution. It
  solved every random scramble tested (in under 15 ms each).
- **Slide puzzle:** A* search placing one tile at a time with finished rows and
  columns locked, then the last 3×3 optimally.
- **Lights Out:** linear algebra mod 2 or mod 3.
- **Hanoi:** the optimal next move from any legal position.
- **Ball Sort:** depth-first search with memory of visited positions.
- **Maze:** randomised depth-first (backtracker) and growing-tree generation,
  extra loops on harder levels, breadth-first search for the shortest way.
- **Block Stack AI:** scores every placement by height, holes, bumpiness and
  lines cleared; difficulty changes its speed, mistakes and use of Hold.

## Testing

Every teacher was checked by letting it solve, starting from random positions
and after random wrong moves: 1,200 cube plans (3×3 and 2×2, including slice
moves), 360 slide puzzles, 2,000 Lights Out boards (classic and three-colour,
3×3 to 7×7), 1,800 Tower of Hanoi positions (every move legal and exactly the
shortest), 240 Ball Sort racks, 300 mazes, plus full in-browser playthroughs of
every table — jigsaws of 50, 100 and 500 pieces with rotation, Flood, Arcade,
and Block Stack solo and against the AI — and the shop (buying, turning kits on
and off, felts per table, dyes, reset, and reload) driven by real taps.
The mathematics of all 20 card tricks was checked thousands of times each, and
every act was performed on screen by an automated spectator who kept a secret
card and answered honestly — 40 out of 40 performances correct. The 20
Questions brain was played against all 1,004 things it knows (see above). The five Block Stack AI levels were benchmarked
playing 400 blocks with junk rows: Rookie lasts about 50 blocks, Easy about 80,
Normal about 220, and Hard and Master survive all 400.

## Files

- `index.html`: the whole parlour: markup, styles, engine and puzzles
- `logo.svg`: repository logo and page icon
- `LICENSE`: MIT licence

## License

MIT. See `LICENSE`.
