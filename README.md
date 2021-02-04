Check out my dank dependently typed categorical language done in
makam.  I don't even have normalization properly worked out lol.

Yeah so basically it's just like the Calculus of Constructions but instead of

    (λ "a" : * . λ "x" : "a" . "x") Z 3

being type

    Z

We have

    (λ "a" : 1 → * . λ "x" : 1 → "a" . "x") Z 3

being type

    term → Z

Also we flip arrows around so you can do

    λ "a" : Z → 0.

whatever that means.

Function "f x" application is explicitly

   f pass x

You can do

   f lift x

for a first-order version.

based the language off Calculus of Constructions/the Kappa Zeta
Decomposition [1] plus the opposite rules simply obtained by flipping
arrows.

For rapid prototyping purposes the inconsistency object : 1 -> object
is introduced.  Some sort of hierarchy of universes would have to be
introduced as usual to handle the matter in a proper tool.
Also a few integer extras are introduced.
These arent really core to the main idea.

I suspect this language is classical or even inconsistent in the same
way having both exponentials/coexponentials would reduce things to
binary values of true/false.  To obtain a constructive/refutative
interpretation one would probably have to eliminate forall/zeta rules
or restrict them in some way.

Even removing this rule and the forall/zeta/pass rules there is no
proof the remaining system is consistent or constructive.  I am still
figuring all this out.

1. Decomposing typed lambda calculus into a couple of categorical programming languages
In Proc. 6th International Conference on Category Theory and Computer Science (CTCS'95), Springer LNCS 953 (1995) 200-219
'http://www.kurims.kyoto-u.ac.jp/~hassei/papers/ctcs95.html