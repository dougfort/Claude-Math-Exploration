# What is a vector space?

_A one-page summary of the exploration, Oct 17–20, 2026. Prompted by Tivadar Danka's four suggestions: learn linear algebra, see matrices as graphs, see calculus as optimization language, and learn vector spaces until neural networks stop looking like black magic._

## The short answer

A vector space is anything you can **add** and **stretch by numbers**, as long as those two operations follow the familiar rules. Arrows, sounds, recipes, photos and lists of a billion numbers all qualify. Whatever you prove from the rules alone holds for every one of them.

## How we got there

**1. Two arrows fix the whole plane.** Every point on graph paper is a recipe: "3 rights + 2 ups." A matrix is a small grid of numbers that records where "right" and "up" land. Because grid lines stay straight and evenly spaced, every point keeps its recipe and only the ingredients change. **Same recipe, new ingredients.** The quarter turn is the grid 0 −1 / 1 0, which does what multiplying by i does.

**2. The rule-list (Grassmann 1844, Peano 1888).** Strip the picture away and keep the rules for adding and stretching. Anything that obeys them is a vector space. **Sounds are vectors:** play two together to add them, turn one up or down to stretch it. Pure tones are the ingredients, as Fourier found.

**3. Lists of numbers, any length.** A list of 2 numbers is an arrow in the plane. A list of 10,000 is an arrow in 10,000 dimensions, and a small photo is one such point. Nobody pictures that. You reason in 2 or 3 dimensions and let the rules carry the result up, because the rules never mention dimension.

**4. Eigenvectors: directions that only stretch.** Most arrows get both turned and stretched by a matrix, but some special ones only stretch. Use those as the ingredients, and a tangled motion becomes "this much here, that much there." Pure tones are the eigenvectors of sound, which is why an equalizer works on them one at a time. An atom's energy levels are eigenvalues.

**5. Matrices as graphs; PageRank (Page and Brin, 1998).** The same grid of numbers is also a map of arrows between dots. Web pages and their links form a matrix, and a crowd of random surfers settles into a split that the matrix leaves unchanged: an eigenvector. "A page matters if pages that matter link to it" sounds circular, but the eigenvector is the one ranking that agrees with itself.

**6. Neural networks: matrix, bend, matrix, bend.** The familiar drawing of dots and weighted lines _is_ a matrix drawn as a graph. Matrices alone would collapse into one motion, so a small bend between layers (negatives become zero) lets the network fold space instead of only slanting it.

**7. Learning as walking downhill (Cauchy 1847; backpropagation 1986).** Mistakes become one number, the loss. Every setting of the weights is a point in a landscape, with loss as height. Calculus gives the slope, and the network steps downhill thousands of times. With billions of weights, the landscape has billions of dimensions, and the same rule works.

## The thread through it all

One move kept coming back: **same recipe, new ingredients**, plus the freedom to _choose_ the ingredients that make a problem simple. The "black magic" of neural networks turned out to be this move done at enormous scale, with bends in between and weights found by walking downhill. What remains genuinely mysterious is _why_ it works as well as it does.

## Still open

* A matrix with no eigenvectors (the quarter turn), and how i rescues it
* Multiplying a matrix by itself counts two-step paths through its graph
* The folding paper: why bends plus matrices can separate what straight motions can't
* Backpropagation: how one backward sweep finds every slope at once
* Closeness in high dimensions, and the high-dimensional orange that is almost all peel
