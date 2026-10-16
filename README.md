<p align="center"><img src="logo.svg" width="96" alt="Puzzle Parlour logo"></p>

# Puzzle Parlour

A puzzle lounge in a single HTML file. Walk up to any of ten tables and
play: a Rubik-style colour cube (2×2 and 3×3), slide puzzles, jigsaws cut from
your own photos, Lights Out, Tower of Hanoi, Flood, Ball Sort, Maze Runner,
the Arcade Puzzle match game and Block Stack (solo, Zen or against the
computer). A jukebox plays ten original music tracks while you play. Every table
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
| Flood | 10×10, 14×14, 18×18 | Head for the centre, then grow; two-move lookahead. The move limit comes from the teacher's own solution plus a few spare |
| Ball Sort | 4–9 colours | Keep spare tubes empty; a solver plans the route and replans if you go your own way |
| Maze Runner | A new random maze every game at 5 skill levels: Stroll, Easy, Medium, Hard and Expert (big, branching, looped and foggy). Trace the path with your finger (the dot follows you; drag back along your trail to back up), junctions are hexagons that become tap-to-return save spots once you pass them, swipe to run to the next junction, tap to step, arrow keys | The right-hand rule and dead-end spotting; gold dots light up the shortest way out |
| Arcade Puzzle | Match-3 with six colour-and-shape gems. 4 in a line makes a Blaster, an L or T makes a Bomb, 5 in a line makes a Prism. Number gems (×2, ×3, ×5) multiply the match; two numbers in one match set off a Number Storm. Cascades build combos, and swapping two specials makes mega effects. Levels, 90-second and Zen modes | Points out the best swap and why (which special it makes) |
| Block Stack | Falling-block stacking with hold, next queue and ghost piece. **Solo** speeds up every 10 lines, **Zen** never ends, **Vs AI** (easy/normal/hard) trades junk rows when you clear 2+ lines | Shows the spot its own AI would choose for your block, with tips on holes and height |

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

## Files

- `index.html`: the whole parlour: markup, styles, engine and puzzles
- `logo.svg`: repository logo and page icon
- `LICENSE`: MIT licence

## License

MIT. See `LICENSE`.
