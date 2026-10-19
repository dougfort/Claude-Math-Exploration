# Excursion Log

One entry per excursion, newest at the top. Short is fine.

Template:

## \[date] — \[the idea, in a few words]

* **What we looked at:** one or two sentences
* **What clicked:** the part that made sense or gave pleasure
* **Still fuzzy:** anything to revisit (a good place to start next time)
* **Threads that opened:** new questions (copy any worth keeping to the curiosity list)

***

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
