# Excursion Log

One entry per excursion, newest at the top. Short is fine.

Template:

## \[date] — \[the idea, in a few words]

* **What we looked at:** one or two sentences
* **What clicked:** the part that made sense or gave pleasure
* **Still fuzzy:** anything to revisit (a good place to start next time)
* **Threads that opened:** new questions (copy any worth keeping to the curiosity list)

***

## Oct 22, 2026 — Arrows on a curved space, and what a tensor is (Tensor part 1)

* **What we looked at:** A ship's arrow doesn't bend along the Earth; it lives in the flat tangent plane touching the surface at that point. Every point has its own tangent plane, its own little vector space, so arrows at Boston and Tokyo can't simply be added. Writing an arrow as numbers needs a chart, and different charts give different numbers for the same arrow (like dollars vs. euros), converted by the Jacobian.
* **What clicked:** A tensor is anything with a rule for how its numbers change between charts, chosen so the thing itself stays the same. An arrow is the simplest (Jacobian once). The metric, a ruler at each point (a 2-by-2 grid on a surface), converts with the Jacobian twice; knowing it everywhere gives all distances and the curvature (Riemann, 1854). "A tensor is something that transforms like a tensor": defined by what it does, like the negatives. Einstein's gravity is the metric of spacetime, a 4-by-4 grid at every point. In machine learning, "tensor" loosely means any grid of numbers, with no chart-switching rule.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** The metric as a ruler (a flat map of the globe, where an inch means different distances in different places). Carrying an arrow around a triangle on a sphere: it comes back turned, and the turning is the curvature.

## Oct 21, 2026 — Manifolds: curved spaces that look flat up close (Manifold part 1)

* **What we looked at:** The Jacobian's zooming trick applied to space itself. A manifold is a space where every small patch looks like flat ordinary space. Examples: a circle (1-D), a sphere's surface and a doughnut's surface (2-D). Non-example: a figure 8, whose crossing point zooms to an X. No flat map of the Earth keeps all distances (Gauss, 1827), so we use an atlas of overlapping charts with conversion rules between them, and those rules have Jacobians.
* **What clicked:** "Atlas" and "chart" really are borrowed from mapmaking. Riemann's 1854 qualifying lecture (Gauss chose the topic from three offered): space itself might be curved, describable entirely from inside. Einstein (1915): spacetime is a 4-D manifold curved by mass.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** How an ant on a sphere detects curvature from inside (a big triangle's angles add to more than 180°). Arrows on a curved space, which leads to tensors.

## Oct 21, 2026 — Backpropagation: a chain of Jacobians (Jacobian part 2)

* **What we looked at:** A network is a chain: layer 1, layer 2, … then one number, the loss. Stretches multiply along a chain (2 then 3 makes 6: the chain rule, Leibniz, 1670s). In many dimensions each layer's stretch is its Jacobian, and chaining them means multiplying the matrices. Backpropagation starts at the narrow end (the single loss number) and passes sensitivity back one layer at a time, each step reusing the next one's result. The bend's Jacobian is simple: stretch 1 where a value was positive, 0 where it was flattened.
* **What clicked:** A relay of blame: each layer is told "this much is yours; pass the rest on." Backward gets every slope in one sweep, roughly the cost of running the network once or twice, instead of one sweep per weight. Blame passes through active spots and stops at flattened ones. History: Linnainmaa 1970; Rumelhart, Hinton and Williams 1986.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** (none new; this closes the backpropagation thread)

## Oct 21, 2026 — The Jacobian: a matrix at every point (Jacobian part 1)

* **What we looked at:** Bent motions (an unevenly stretched rubber sheet, the round Earth flattened onto a map) curve the grid lines, so no single matrix describes them. Zoom in on one point, though, and a tiny square becomes almost exactly a parallelogram: the motion acts like a matrix there. That matrix is the Jacobian at that point. Example: each point at distance x moves to x². Near x = 1 the Jacobian is 2 0 / 0 1; near x = 3 it's 6 0 / 0 1.
* **What clicked:** The Jacobian is the derivative grown into a matrix (the slope of x² at 3 is 6, the same 6). "Same recipe, new ingredients" still works for bent motions, but locally, with a fresh matrix at every point. Named for Carl Jacobi (1841).
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** The area factor: how much tiny squares grow or shrink at each spot (6 times near x = 3), and why it matters when switching maps. Onward to manifolds.

## Oct 20, 2026 — Learning as walking downhill; the wrap-up (What is a vector space? part 6, final)

* **What we looked at:** Mistakes become one number, the loss. Each setting of the weights is a point in a landscape (a vector), with loss as height. Calculus gives the slope for each weight; together the slopes make the gradient, which points uphill, so you step the other way (gradient descent, Cauchy 1847). Billions of weights means billions of dimensions, but the rule never mentions dimension. Backpropagation (made famous 1986) finds all the slopes in one backward sweep. Caveats: step size matters, and you can get stuck in a small dip (less of a problem in practice than feared, and not fully understood why).
* **What clicked:** This is Danka's "calculus as optimization language": calculus says which way is down. All four of his suggestions have now been touched as ideas. Summary written as what-is-a-vector-space.md.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** Backpropagation in small steps.

## Oct 20, 2026 — Neural network drawings are matrices (What is a vector space? part 5)

* **What we looked at:** The familiar drawing of dots in columns joined by weighted lines is a matrix drawn as a graph: one row per output, one column per input, one entry per line. Each output is its incoming lines added up, weight times input. Stacked matrices alone collapse into one motion, so a bend goes between layers (any negative becomes zero), like folding graph paper instead of only slanting it.
* **What clicked:** A neural network is matrix, bend, matrix, bend. The weights aren't chosen; they start random and get nudged to reduce mistakes. The machinery isn't magic, though why it generalizes so well is still not fully understood. Outside source: 3Blue1Brown, _Neural Networks_, chapter 1.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** The folding paper: why bends plus matrices separate what straight motions can't.

## Oct 20, 2026 — PageRank: the web as a matrix (What is a vector space? part 4)

* **What we looked at:** A matrix read as a graph: dots and arrows. Three pages: A links to B and C, B to C, C to A. A crowd of random surfers splits along the links each round; the matrix columns record the splits. The crowd settles at A 40%, B 20%, C 40%, a split the matrix leaves unchanged, which is an eigenvector with stretch 1.
* **What clicked:** A has only one incoming link but ties with C, because that link comes from an important page. "A page matters if pages that matter link to it" is circular, and the eigenvector is the one ranking that agrees with itself. Page and Brin, 1998, plus the bored surfer who jumps at random. A matrix and a network of arrows are the same object written two ways (Danka's point).
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** Multiplying a matrix by itself counts two-step paths.

## Oct 20, 2026 — Eigenvectors: directions that only stretch (What is a vector space? part 3)

* **What we looked at:** Most arrows get turned and stretched by a matrix, but some only stretch. Sideways stretch by 3: "right" and "up" are special, the diagonal gets tilted. The matrix sending right to (2, 1) and up to (1, 2): (1, 1) → (3, 3), stretched by 3; (1, −1) → (1, −1), stretched by 1. These are eigenvectors (_eigen_ = "own"), and the stretch amounts are eigenvalues.
* **What clicked:** Use eigenvectors as the ingredients, and the matrix just stretches each one: same recipe, new ingredients, chosen to make it simple. Pure tones are the eigenvectors of sound, which is why equalizers, echoes and concert halls treat each tone separately and why Fourier is so useful. Quantum energy levels are eigenvalues.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** The quarter turn has no such directions, and i rescues it. PageRank as an eigenvector.

## Oct 20, 2026 — Why x⁵ fails: the icosahedron (Galois part 3, final)

* **What we looked at:** Five solutions can be shuffled 5 × 4 × 3 × 2 × 1 = 120 ways, and for a typical x⁵ (e.g. x⁵ − x − 1 = 0) all 120 are allowed. One square root peels that to 60, and then it's stuck: the 60 can't be peeled at all ("simple," like a prime that can't be factored). So no formula. The 60 are the turns of an icosahedron, which shuffle five hidden sets of perpendicular axes (Klein's 1884 book). Lower degrees peel: x² has 2 shuffles, x³ has 6 (triangle), x⁴ has 24 (cube). Some x⁵ equations, like x⁵ = 2, have smaller groups and are solvable.
* **What clicked:** The reason there's no formula for x⁵ is, in a real sense, the symmetry of a 20-sided die. The structures solved the problem algebra started with. Added as chapter 9 of what-is-algebra.md.
* **Still fuzzy:** (nothing noted; the proof that the 60 can't be peeled was given as a conclusion, not shown)
* **Threads that opened:** Why the 60 can't be peeled, sketched in small steps. Optional: Galois's life, fact vs. legend.

## Oct 20, 2026 — Shuffling the solutions: x² = 2 (Galois part 2)

* **What we looked at:** x² = 2 has two solutions, a = √2 and b = −√2. Using only ordinary numbers and +, −, ×, ÷, every true statement about them stays true when you swap them (a² = 2, a + b = 0, a × b = −2). "Positive" tells them apart, but that's order, not arithmetic. So the allowed shuffles are "do nothing" and "swap," the smallest non-trivial group (same pattern as 1 and −1). Contrast: x² = 4 (solutions 2 and −2), where "a − 2 = 0" breaks under the swap, so only "do nothing" is allowed.
* **What clicked:** x² = 4 needs no root and its group is just "do nothing"; x² = 2 needs √2 and its group has a swap. Taking a root is what separates twins. Each root peels one simple layer off the group, and a formula exists exactly when the group can be peeled down layer by layer to nothing.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** Why x⁵ fails: 120 shuffles of five solutions, with an unpeelable core of 60, the rotations of an icosahedron. Optional: Galois's life, fact vs. legend.

## Oct 19, 2026 — The formula hunt ends: Abel and Galois (Galois part 1)

* **What we looked at:** The formula hunt: x² (completing the square, square roots), x³ (Cardano, 1545), x⁴ (Ferrari, same book). For x⁵, nearly 300 years of failure. Abel (1824; Ruffini nearly, 1799) proved no formula using +, −, ×, ÷ and roots solves every x⁵ equation. The solutions still exist and can be calculated; only the recipe is missing. Galois (1811–1832): failed the Polytechnique entrance twice, expelled from the École Normale, jailed for republican activity, manuscripts lost or rejected, a letter summarizing his ideas the night before the duel (the "invented it all in one night" story is legend). Liouville published his work in 1846.
* **What clicked:** Abel showed _that_ it's impossible; Galois explained _why_. Instead of hunting for the formula, look at the solutions and ask how they can be shuffled without the equation telling the difference. Those shuffles form a group, and a formula exists exactly when that group can be taken apart in a particularly simple way. For the general x⁵ it can't.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** What "shuffling the solutions" means, starting with x² = 2 (√2 and −√2). Optional: more on Galois's life, separating fact from legend.

## Oct 19, 2026 — Rings, and the wrap-up (What is algebra? part 8, final)

* **What we looked at:** A ring is the rule-list for two operations: adding (a group where order doesn't matter), multiplying (grouping rule, usually a 1, no undo required), and distribution linking them. Examples: whole numbers, matrices, quaternions, clock arithmetic (9 + 5 = 2; 3 × 4 = 0, two non-zeros making zero), and a modern version of Boole's logic. Emmy Noether (Göttingen, 1920s) made rings central.
* **What clicked:** The ring rules are exactly the rules that _forced_ negative × negative = positive in part 2. The rules that had to survive became the definition, so the fact holds in every ring. The answer to "What is algebra?" is the study of structures: collections with ways of combining that obey rules, apart from what the members are. Summary written as what-is-algebra.md.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** Galois and the missing formula for x⁵ (still open).

## Oct 18, 2026 — Groups: the pattern without the material (What is algebra? part 7)

* **What we looked at:** The 8 symmetries of a paper square (4 turns including "do nothing", 4 flips). Combining = doing one move then another. A group is any collection with a way of combining that obeys four rules: combining stays inside, there's a "do nothing," every move has an undo, grouping doesn't matter. No numbers needed.
* **What clicked:** The square's four turns combine exactly as 1, i, −1, −i multiply (quarter turn ↔ i, half turn ↔ −1). It's the same group in completely different materials, so the pattern itself becomes the subject. Whole numbers under adding are a group too (the undo of 5 is −5). The square's flips show order mattering, as with Hamilton.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** Galois (d. 1832 at 20): groups explain why there's no formula for x⁵. Rings (done in part 8).

## Oct 17–18, 2026 — Lists of numbers as vectors (What is a vector space? part 2)

* **What we looked at:** A list of 2 numbers is an arrow in the plane, 3 numbers an arrow in space, 1,000 numbers an arrow in 1,000-dimensional space. Add lists item by item, stretch by multiplying every item; the rules hold. "Dimension" is how many ingredients the recipe needs. Examples: a kitchen recipe (flour, sugar, butter, eggs) is a point in 4-D, and doubling it is stretching. A 100×100 black-and-white photo is a point in 10,000-D, and averaging two photos lands halfway between them.
* **What clicked:** Nobody pictures 10,000 dimensions. You reason in 2 or 3 and let the rules carry it, since they never mention dimension (the old joke: picture 3-D and say "fourteen" very firmly). A neural-network layer is a matrix doing "same recipe, new ingredients": 10,000 numbers become a shorter list of weighted blends.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** Closeness: distance works in any dimension, so similar photos are nearby points, the root of machine recognition. Where the 3-D picture fails (a high-dimensional orange is almost all peel).

## Oct 17, 2026 — Vector spaces as a rule-list; sounds are vectors (What is a vector space? part 1)

* **What we looked at:** A vector space is anything you can add and stretch by numbers, following about eight unsurprising rules (order of adding doesn't matter, a zero element, opposites that cancel, stretching distributes over adding). Peano wrote the list down in 1888, building on Grassmann. The payoff is Viète's again: prove it once, and it holds for everything that fits.
* **What clicked:** Sounds are vectors. Play two together to add them; make them louder, softer, or flipped (noise-cancelling headphones) to stretch them. Pure tones are the ingredients, as in Fourier, but infinitely many of them. "Same recipe, new ingredients" carries over: a linear change to sound treats each pure tone separately.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** An audio equalizer as a "matrix for sound." Ingredients a motion only stretches, never turns, have a name and matter enormously.

## Oct 17, 2026 — Matrices, and how two arrows fix the whole plane (What is algebra? part 6)

* **What we looked at:** After Hamilton, new arithmetics appeared quickly: octonions (Graves, Cayley; 8 numbers, grouping matters), Boole's algebra of logic (x × x = x), Grassmann's arrows in any number of dimensions (1844, largely unread), and matrices (Cayley's 1858 memoir). A matrix is a grid of numbers that _moves space_. A 2-by-2 grid records only where "one step right" and "one step up" land. The quarter turn is the grid 0 −1 / 1 0, which does what multiplying by i does. Multiplying matrices means doing one motion, then the other, so order matters.
* **What clicked:** Every point is a recipe ("3 rights + 2 ups"). Linear motions keep grid lines straight, parallel, and evenly spaced, so each point keeps its recipe and only the ingredients change: same recipe, new ingredients. Quarter turn: (3, 2) → 3 ups + 2 lefts = (−2, 3). The argument used only adding arrows and stretching them, and a vector space is any collection where those two operations make sense and follow the rules. Fourier's waves as recipes of pure tones have the same structure. A neural-network layer is mostly this move with thousands of ingredients.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** Vector spaces as a rule-list, and surprising things that turn out to be vectors (moved to "What is a vector space?"). Boole's arithmetic. Outside source: 3Blue1Brown, _Essence of Linear Algebra_, chapter 3.

## Oct 17, 2026 — Hamilton and the quaternions (What is algebra? part 5)

* **What we looked at:** Hamilton wanted numbers that do for 3-D space what i does for the plane. Triples failed for years ("can you multiply triplets yet, Papa?"). A rough reason: a turn-and-stretch in space needs an axis (2 numbers), an angle, and a stretch, which makes 4, not 3. On 16 October 1843, walking by Dublin's Royal Canal, he found quaternions (three imaginary directions i, j, k, each squaring to −1) and carved the rules into Broom Bridge.
* **What clicked:** The price was giving up "order doesn't matter": i × j = k but j × i = −k. That isn't a defect, because turns in space themselves depend on order (try the two quarter turns of a book in both orders). Unlike the negatives, where the rules _forced_ the answer, Hamilton _chose_ which rule to drop. Algebra could now pick its rules. That answered "could different rules give a consistent arithmetic?": yes.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** What the four parts of a quaternion do, and how a quaternion turns an object. Outside source: eater.net/quaternions (3Blue1Brown and Ben Eater, interactive).

## Oct 16, 2026 — The quarter turn: imaginary numbers get a picture (What is algebra? part 4)

* **What we looked at:** Multiplying by −1 is a half turn around zero on the number line, and twice is a full turn (negative × negative = positive, seen as motion). Multiplying by i twice must equal multiplying by −1, a half turn, so multiplying by i is a _quarter turn_, which points off the line into a new direction. 1 → i → −1 → −i → 1.
* **What clicked:** The "impossible" numbers were never missing, just _off_ the line. 3 + 2i is a point in a plane: 3 along, 2 up. Wessel (1797, unread), Argand (1806), and Gauss (1831, decisive) gave the picture. After 250 years the scaffolding turned out to be a building. These numbers are the language of turning and stretching in the plane, and Hamilton wanted the same for space.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** Why multiplying any two plane numbers is "turn by an angle, then stretch."

## Oct 16, 2026 — The impossible numbers (What is algebra? part 3)

* **What we looked at:** No number times itself is negative (positive × positive and negative × negative are both positive), so a square root of −121 "can't exist." Cardano published a formula for cubic equations in 1545, causing a scandal over a broken promise. On x³ = 15x + 4, whose answer is plainly 4, the formula requires √−121 on the way.
* **What clicked:** Unlike negative answers, which could be set aside as "false," these impossible numbers sit _on the road_ to a real answer and can't be avoided. Bombelli (1572) calculated with √−1 using the ordinary rules plus one new rule (√−1 × √−1 = −1). The impossible parts cancel in pairs and leave 4, like scaffolding taken down once the building stands. Trust in the rules ran ahead of any picture by about 250 years.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** The picture that made imaginary numbers real (a quarter turn, c. 1800). Hamilton (1843) and breaking a × b = b × a; Fog is especially interested. Optional: Bombelli's cancellation step by step.

## Oct 15–16, 2026 — From words to symbols, and what symbols forced (What is algebra? part 2)

* **What we looked at:** Algebra's three stages: words (al-Khwarizmi), abbreviations (Diophantus c. 250; Italian _p_ and _m_; Recorde's equals sign, 1557), full symbols. Viète's move (1591): letters for the _given_ numbers too, so a whole family of problems (x² + bx = c) can be solved once, and the method becomes an object you can study. Symbols then produced answers pictures couldn't hold. x² + 10x = 39 also has x = −13, which al-Khwarizmi never mentions. Europe called negative roots "false" into the 1700s; Brahmagupta (c. 628) had already treated negatives as debts.
* **What clicked:** A negative number is defined by what it does: −5 is the number that, added to 5, gives 0. "Negative times negative is positive" isn't a choice. It's forced if the distribution rule, a × (b + c) = a×b + a×c, is to keep working: (−3)×(5 + (−5)) = 0 leaves (−3)×(−5) no option but 15. The question shifts from "what _is_ it?" to "what must it be, if the rules are to survive?" That's the road to algebra as the study of rules themselves.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** Could different rules give a consistent arithmetic? The "impossible" square roots of negatives in 1500s cubic formulas.

## Oct 15, 2026 — al-Khwarizmi and the birth of algebra (What is algebra? part 1)

* **What we looked at:** al-Khwarizmi (Baghdad, c. 820), whose book gave us the word "algebra" from _al-jabr_, "restoring" (adding a subtracted quantity back to both sides). His algebra used no symbols, only words: "a square and ten roots equal thirty-nine" (x² + 10x = 39).
* **What clicked:** He solved it with a picture: a square of side x, two 5-by-x strips, and a missing 5-by-5 corner. Filling the corner makes a square of area 64, side 8, so x = 3. Early algebra meant treating the unknown as a thing in hand and manipulating it until it reveals itself.
* **Still fuzzy:** (nothing noted)
* **Threads that opened:** Why "completing the square" works for every problem of this shape. Next: how algebra went from words to symbols.
