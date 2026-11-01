# Compact set — ImageGen prompts

Built-in ImageGen. User's supplied twelve-panel sheet is the visual reference.

## 01_Methods_and_Restrictions

Use case: scientific-educational. The supplied image is a STYLE REFERENCE only: emulate its compact, information-dense revision-sheet design very closely. Create one flat portrait PNG, 2:3 aspect, high resolution for printing. Navy banner, large white serif title, thin colored borders, light pastel blue/rose/yellow/green/purple panels, small numbered serif panel headings, tightly typeset black body text, proper mathematical fractions, factorials and superscripts, small blue 'Example' and answer highlights. MULTIPLE NARROW COLUMNS with nested subpanels like the supplied twelve-panel reference. Efficient space, very little padding, modest title area; compact typography with clear hierarchy. No pictorial illustrations, icons, cartoons or decorative diagrams, no giant four-panel lesson layout, no huge heading bars or empty panels. Source text below is authoritative: reproduce ALL questions, choices, equations and explanations faithfully. You may organize its sections into smaller subpanels to create a dense reference sheet; preserve meaning. Do not add new examples, numerical claims or omit content. Mathematical symbols must be correct and text unclipped. Render all source content below on this single page. Markdown heading symbols are structural instructions, not literal text.
Use three columns and about 12 tightly arranged numbered panels. Split definition/formula/example subpanels sensibly, exactly like the supplied reference. Preserve the two original topic groupings in small section labels.

# COUNTING • METHODS AND RESTRICTIONS

GATE DA 2027 | Compact worked revision

## Start with four questions
What is one outcome? Does order matter? Can a choice repeat? Are the objects distinct?
Assigning president and secretary creates ordered outcomes. Choosing a committee creates unordered outcomes.

## The four basic models
Choose r items from n distinct choices:
• Ordered, no repetition: P(n,r) = n!/(n−r)!.
• Unordered, no repetition: C(n,r) = n!/[r!(n−r)!].
• Ordered, repetition allowed: n^r.
• Unordered, unlimited repetition: C(n+r−1,r), n≥1.
For no repetition, 0≤r≤n. Also 0!=1.
Do not confuse repeated choices with identical objects.

## Product rule — successive decisions
If every partial choice has n₁, then n₂, … continuations, multiply: n₁n₂···nₖ.
Example: assign 3 different offices to 8 people.
First office: 8 choices. Second: 7. Third: 6.
Total = 8×7×6 = 336.
Independent probabilities are not required to count successive choices.

## Sum rule — disjoint cases
Add counts only when cases do not overlap.
Example: a 4-person team from 6 engineers and 5 statisticians must include both groups.
Split by engineer count: 1, 2, or 3.
C(6,1)C(5,3)+C(6,2)C(5,2)+C(6,3)C(5,1)
= 60+150+100 = 310.

## Why divide by r!?
Each r-person committee appears in r! orders.
Choose 3 people from 8: C(8,3)=336/3!=56.
AB and BA are different assignments but the same pair.

## Identical objects and circles
Linear arrangements with multiplicities n₁+···+nₖ=n:
n!/(n₁!···nₖ!).
BANANA: 6!/(3!2!)=60.
MISSISSIPPI: 11!/(4!4!2!)=34,650.
For n distinct people at an unnumbered round table, rotations agree: (n−1)!.
Reflections remain different unless the question also identifies mirror images. Then use (n−1)!/2 for n>2.
Quick checks: C(n,r)=C(n,n−r); Σ from r=0 to n of C(n,r)=2^n.

## Together: build a block
For k specified distinct objects together among n distinct objects:
(n−k+1)! × k!.
Example: 5 books; A and B adjacent.
Treat AB as one block: 4! external orders.
Inside the block: AB or BA, so 4!×2!=48.
Block order and internal order are separate decisions.

## Not together: subtract the bad cases
7 distinct people; two specified people must not be adjacent.
All arrangements = 7!=5,040.
Adjacent arrangements = 2×6!=1,440.
Valid = 5,040−1,440=3,600.
“At least one” often means total minus none.

## No adjacency: use gaps
Length-8 binary strings, exactly 3 zeros, no adjacent zeros:
Place the five identical ones: _1_1_1_1_1_.
There are 6 gaps; put at most one zero in a chosen gap.
Count = C(6,3)=20.
Do not multiply by 3!: the zeros are identical.
General count for r nonadjacent identical zeros in length n: C(n−r+1,r), when n≥2r−1.

## Leading zero: split by the last digit
How many 4-digit even numbers use digits 0–5 without repetition?
Case 1: last digit 0. First digit: 5 choices. Middle digits: 4×3.
Count = 5×4×3=60.
Case 2: last digit 2 or 4. Last: 2 choices. First: 4 nonzero choices. Middle: 4×3.
Count = 2×4×4×3=96.
Total = 60+96=156.
A digit code can begin with zero; a 4-digit number cannot.

## Exactly / at least: select groups
Exactly 2 objects from a specified group of 4, in a size-5 subset of 12:
Choose 2 of the 4, then 3 of the remaining 8.
C(4,2)C(8,3)=6×56=336.
At least one engineer AND one statistician:
C(11,4)−C(6,4)−C(5,4)=330−15−5=310.

## Subsets and overlaps
Each element is either included or excluded: 2^n subsets.
Nonempty subsets: 2^n−1. Size-r subsets: C(n,r).
Two overlapping conditions: |A∪B|=|A|+|B|−|A∩B|.
Three: add singles, subtract pairwise overlaps, add the triple overlap.
Before finalizing: check distinctness, empty cases, leading zero, and whether your cases overlap.

## 02_Distributions_and_Verified_Examples

Use case: scientific-educational. The supplied image is a STYLE REFERENCE only: emulate its compact, information-dense revision-sheet design very closely. Create one flat portrait PNG, 2:3 aspect, high resolution for printing. Navy banner, large white serif title, thin colored borders, light pastel blue/rose/yellow/green/purple panels, small numbered serif panel headings, tightly typeset black body text, proper mathematical fractions, factorials and superscripts, small blue 'Example' and answer highlights. MULTIPLE NARROW COLUMNS with nested subpanels like the supplied twelve-panel reference. Efficient space, very little padding, modest title area; compact typography with clear hierarchy. No pictorial illustrations, icons, cartoons or decorative diagrams, no giant four-panel lesson layout, no huge heading bars or empty panels. Source text below is authoritative: reproduce ALL questions, choices, equations and explanations faithfully. You may organize its sections into smaller subpanels to create a dense reference sheet; preserve meaning. Do not add new examples, numerical claims or omit content. Mathematical symbols must be correct and text unclipped. Render all source content below on this single page. Markdown heading symbols are structural instructions, not literal text.
Use three columns and about 12 tightly arranged numbered panels. Split definition/formula/example subpanels sensibly, exactly like the supplied reference. Preserve the two original topic groupings in small section labels.

# COUNTING • DISTRIBUTIONS AND EXAM EXAMPLES

GATE DA 2027 | Compact worked revision

## Stars and bars: what the formula counts
Distribute n identical items into k labeled boxes.
Equivalent: x₁+···+xₖ=n.
The stars are identical items; k−1 bars separate boxes.
Example: ★★|★|★★ represents (2,1,2).
Box labels matter. This is not the formula for unlabeled boxes.

## Empty boxes allowed
For xᵢ≥0, n≥0, k≥1:
Count = C(n+k−1,k−1).
12 identical items into 4 labeled boxes:
C(15,3)=455.
Reason: choose positions for 3 bars among 15 symbols.

## Every box nonempty
For xᵢ≥1, reserve 1 item for each box.
Set yᵢ=xᵢ−1≥0; the new total is n−k.
Count = C(n−1,k−1), when n≥k; otherwise 0.
12 items into 4 nonempty labeled boxes:
C(11,3)=165.

## Lower and upper bounds
Lower bounds xᵢ≥aᵢ: subtract aᵢ from each variable first.
Upper bound example: x₁+x₂+x₃=9, xᵢ≥0, x₁≤2.
All solutions: C(11,2)=55.
Bad solutions x₁≥3: set y₁=x₁−3.
Then y₁+x₂+x₃=6: C(8,2)=28.
Valid = 55−28=27.
For several upper bounds, subtract their union using inclusion–exclusion.

## Repeated selections are distributions
Choose 6 scoops from 4 flavors, order ignored, unlimited supply.
Let xᵢ be scoops of flavor i. Then x₁+x₂+x₃+x₄=6.
Count = C(9,3)=84.
If scoop positions mattered, the count would instead be 4^6.

## Probability: check uniformity first
P(event)=favorable outcomes / total outcomes only for equally likely outcomes.
3 distinct balls independently enter 2 boxes, each with probability 1/2.
There are 2^3=8 equally likely assignments.
Occupancy (3,0) has 1 assignment; (2,1) has 3.
The four occupancy vectors are not equally likely.
A uniformly sampled occupancy vector and independently assigned balls are different experiments.
Always state what is sampled uniformly.

## Official GATE DA 2026 • Q19
Question, paraphrased: A nonempty subset of {1,…,2026} is chosen at random. Find the probability that its product is even.
Use the uniform-subset interpretation underlying the key.
1. All nonempty subsets: 2^2026−1.
2. Odd product requires only odd elements. There are 1,013 odd numbers.
3. Nonempty odd-only subsets: 2^1013−1.
4. Even-product count: 2^2026−2^1013.
Answer: (2^2026−2^1013)/(2^2026−1).
Official final key: C. Paper page 13.
Trap: exclude the empty subset from the denominator.

## Official GATE DA 2026 • Q20
Question, paraphrased: A program returns a random nonnegative integer solution of n₁+n₂+n₃+n₄=20. Find the probability all four values are positive.
Use the uniform-solution interpretation underlying the key.
1. Total solutions: C(23,3)=1,771.
2. Put yᵢ=nᵢ−1≥0. New total: 16.
3. Favorable solutions: C(19,3)=969.
Answer: C(19,3)/C(23,3)=969/1771.
Official final key: A. Paper page 13.
Trap: positive means at least 1, not at least 0.

## Supplement from the supplied question bank
Source: da questions.pdf, page 409, section 9.6.1.
Question: A box has 6 red and 4 green balls. Select 4 uniformly without replacement. Find the probability of 2 red and 2 green.
Treat individual balls as distinct.
Favorable hands: C(6,2)C(4,2)=15×6=90.
All hands: C(10,4)=210.
Answer: 90/210=3/7.
Other-exam supplement; answer independently derived.
The bank duplicates this item under a different exam date on page 418, so its exam provenance is unverified.

## Challenge method: pairings
If a bijection f satisfies f(f(x))=x, every element is fixed or paired with one other element.
On 5 elements:
0 pairs: 1.
1 pair: C(5,2)=10.
2 pairs: choose 4 elements, then pair them in 3 ways: C(5,4)×3=15.
Total = 1+10+15=26.
This is an authored extension, not a quoted DA PYQ.

## Final habit
Define the outcome → choose a counting model → apply restrictions → check overcounting → use a ratio only under a uniform model.

## 03_Checkpoint_Q1_16

Use case: scientific-educational. The supplied image is a STYLE REFERENCE only: emulate its compact, information-dense revision-sheet design very closely. Create one flat portrait PNG, 2:3 aspect, high resolution for printing. Navy banner, large white serif title, thin colored borders, light pastel blue/rose/yellow/green/purple panels, small numbered serif panel headings, tightly typeset black body text, proper mathematical fractions, factorials and superscripts, small blue 'Example' and answer highlights. MULTIPLE NARROW COLUMNS with nested subpanels like the supplied twelve-panel reference. Efficient space, very little padding, modest title area; compact typography with clear hierarchy. No pictorial illustrations, icons, cartoons or decorative diagrams, no giant four-panel lesson layout, no huge heading bars or empty panels. Source text below is authoritative: reproduce ALL questions, choices, equations and explanations faithfully. You may organize its sections into smaller subpanels to create a dense reference sheet; preserve meaning. Do not add new examples, numerical claims or omit content. Mathematical symbols must be correct and text unclipped. Render all source content below on this single page. Markdown heading symbols are structural instructions, not literal text.
QUESTION-ONLY: sixteen compact numbered question panels in three columns. Keep ALL question wording and choices. No answers, hints or working lines: working is done on separate paper. Do not mark any choice correct.

# COUNTING • CHECKPOINT

GATE DA 2027 | Authored practice. Suggested time: 55–70 minutes. Work on separate paper. Q11 is a written response; Q12 is an optional challenge.

Show your model and working. Q11 is written practice, not exam NAT. Q12 is a challenge.

## Q1 • MCQ
Eight candidates are available for president, secretary, and treasurer. No person can hold two offices. How many assignments are possible?
(A) 56  (B) 336  (C) 512  (D) 8,000

## Q2 • MCQ
How many different 3-person committees can be selected from 8 people when there are no roles?
(A) 56  (B) 112  (C) 336  (D) 512

## Q3 • NAT
How many distinct linear arrangements of the letters in MISSISSIPPI are there?

## Q4 • NAT
How many length-8 binary strings contain exactly three zeros, with no two zeros adjacent?

## Q5 • NAT
Five distinct books are arranged on a shelf. Books A and B must be adjacent. How many arrangements are possible?

## Q6 • NAT
A 4-person committee is selected from 6 engineers and 5 statisticians; the groups are disjoint. How many committees contain at least one person from each group?

## Q7 • NAT
Find the number of nonnegative integer solutions to a+b+c+d=14.

## Q8 • NAT
Find the number of positive integer solutions to x₁+x₂+x₃+x₄+x₅=17.

Show your model and working. Q11 is written practice, not exam NAT. Q12 is a challenge.

## Q9 • NAT
Six scoops are chosen from four ice-cream flavors. A flavor may be selected multiple times and scoop order does not matter. How many selections are possible?

## Q10 • NAT
How many 2-card hands from a standard 52-card deck contain exactly one ace?

## Q11 • SHORT RESPONSE
A nonempty subset of {1,…,12} is chosen uniformly from all nonempty subsets. What is the probability its product is divisible by 3? Give a reduced fraction.

## Q12 • NAT • CHALLENGE
How many bijections f on a 5-element set satisfy f(f(x))=x for every element x?

## Q13 • NAT
Seven distinct people stand in a row. How many arrangements have two specified people not adjacent?

## Q14 • NAT
How many nonnegative integer solutions to x₁+x₂+x₃=9 satisfy x₁≤2?

## Q15 • MSQ
Which statements are correct? Assume valid nonnegative integer parameters, 0≤r≤n and n₁+n₂≤n.
(A) Length-r strings from n symbols, repetition allowed: n^r.
(B) r-person committees from n people: P(n,r).
(C) n objects, with n₁ identical copies of one type and n₂ of another, all others distinct: n!/(n₁!n₂!).
(D) Nonempty subsets of an n-element set: 2^n−1.

## Q16 • NAT
A subset of size 5 is selected from 12 distinct objects. How many such subsets contain exactly 2 objects from a specified group of 4?

## 04_Solutions_Q1_8

Use case: scientific-educational. The supplied image is a STYLE REFERENCE only: emulate its compact, information-dense revision-sheet design very closely. Create one flat portrait PNG, 2:3 aspect, high resolution for printing. Navy banner, large white serif title, thin colored borders, light pastel blue/rose/yellow/green/purple panels, small numbered serif panel headings, tightly typeset black body text, proper mathematical fractions, factorials and superscripts, small blue 'Example' and answer highlights. MULTIPLE NARROW COLUMNS with nested subpanels like the supplied twelve-panel reference. Efficient space, very little padding, modest title area; compact typography with clear hierarchy. No pictorial illustrations, icons, cartoons or decorative diagrams, no giant four-panel lesson layout, no huge heading bars or empty panels. Source text below is authoritative: reproduce ALL questions, choices, equations and explanations faithfully. You may organize its sections into smaller subpanels to create a dense reference sheet; preserve meaning. Do not add new examples, numerical claims or omit content. Mathematical symbols must be correct and text unclipped. Render all source content below on this single page. Markdown heading symbols are structural instructions, not literal text.
Eight numbered question panels in THREE columns with smaller nested 'Question', 'Working' and 'Answer' callouts, dense newspaper-style packing like the reference. Each question including all options must be reproduced in FULL before its explanation. Use compact mathematical typesetting, no pictures, no big blank panels. Preserve all eight complete questions and all explanations.

# COUNTING • SOLUTIONS Q1–8

GATE DA 2027 | Authored practice. Every question is repeated with its explanation and answer.

## Q1 • MCQ
Question: Eight candidates are available for president, secretary, and treasurer. No person can hold two offices. How many assignments are possible?
(A) 56  (B) 336  (C) 512  (D) 8,000

Solution: The offices are distinct. Choose occupants in sequence: 8×7×6=336. Equivalently P(8,3).
Answer: B (336).

## Q2 • MCQ
Question: How many different 3-person committees can be selected from 8 people when there are no roles?
(A) 56  (B) 112  (C) 336  (D) 512

Solution: The same people form one committee regardless of order. Divide ordered selections by 3!: C(8,3)=(8×7×6)/6=56.
Answer: A (56).

## Q3 • NAT
Question: How many distinct linear arrangements of the letters in MISSISSIPPI are there?

Solution: 11 letters: M×1, I×4, S×4, P×2. Divide by permutations of identical copies: 11!/(4!4!2!)=34,650.
Answer: 34,650.

## Q4 • NAT
Question: How many length-8 binary strings contain exactly three zeros, with no two zeros adjacent?

Solution: The other five symbols are ones. Place them first to create 6 gaps. Choose 3 different gaps for the identical zeros: C(6,3)=20.
Answer: 20.

## Q5 • NAT
Question: Five distinct books are arranged on a shelf. Books A and B must be adjacent. How many arrangements are possible?

Solution: Treat A and B as one block. The block and 3 books have 4! orders. AB and BA give 2 internal orders: 4!×2=48.
Answer: 48.

## Q6 • NAT
Question: A 4-person committee is selected from 6 engineers and 5 statisticians; the groups are disjoint. How many committees contain at least one person from each group?

Solution: All committees: C(11,4)=330. Remove all-engineer and all-statistician committees: 330−C(6,4)−C(5,4)=330−15−5=310.
Answer: 310.

## Q7 • NAT
Question: Find the number of nonnegative integer solutions to a+b+c+d=14.

Solution: Four labeled variables, each at least 0. Stars and bars: C(14+4−1,4−1)=C(17,3)=680.
Answer: 680.

## Q8 • NAT
Question: Find the number of positive integer solutions to x₁+x₂+x₃+x₄+x₅=17.

Solution: Set yᵢ=xᵢ−1≥0. The new total is 17−5=12. Stars and bars: C(12+5−1,4)=C(16,4)=1,820.
Answer: 1,820.

## 05_Solutions_Q9_16

Use case: scientific-educational. The supplied image is a STYLE REFERENCE only: emulate its compact, information-dense revision-sheet design very closely. Create one flat portrait PNG, 2:3 aspect, high resolution for printing. Navy banner, large white serif title, thin colored borders, light pastel blue/rose/yellow/green/purple panels, small numbered serif panel headings, tightly typeset black body text, proper mathematical fractions, factorials and superscripts, small blue 'Example' and answer highlights. MULTIPLE NARROW COLUMNS with nested subpanels like the supplied twelve-panel reference. Efficient space, very little padding, modest title area; compact typography with clear hierarchy. No pictorial illustrations, icons, cartoons or decorative diagrams, no giant four-panel lesson layout, no huge heading bars or empty panels. Source text below is authoritative: reproduce ALL questions, choices, equations and explanations faithfully. You may organize its sections into smaller subpanels to create a dense reference sheet; preserve meaning. Do not add new examples, numerical claims or omit content. Mathematical symbols must be correct and text unclipped. Render all source content below on this single page. Markdown heading symbols are structural instructions, not literal text.
Eight numbered question panels in THREE columns with smaller nested 'Question', 'Working' and 'Answer' callouts, dense newspaper-style packing like the reference. Each question including all options must be reproduced in FULL before its explanation. Use compact mathematical typesetting, no pictures, no big blank panels. Preserve all eight complete questions and all explanations.

# COUNTING • SOLUTIONS Q9–16

GATE DA 2027 | Authored practice. Every question is repeated with its explanation and answer.

## Q9 • NAT
Question: Six scoops are chosen from four ice-cream flavors. A flavor may be selected multiple times and scoop order does not matter. How many selections are possible?

Solution: Let xᵢ count scoops of flavor i. Then x₁+x₂+x₃+x₄=6, xᵢ≥0. Count C(9,3)=84.
Answer: 84.

## Q10 • NAT
Question: How many 2-card hands from a standard 52-card deck contain exactly one ace?

Solution: Choose one of 4 aces and one of 48 non-aces. Each unordered hand is counted exactly once: 4×48=192.
Answer: 192.

## Q11 • SHORT RESPONSE
Question: A nonempty subset of {1,…,12} is chosen uniformly from all nonempty subsets. What is the probability its product is divisible by 3? Give a reduced fraction.

Solution: Total nonempty subsets: 2^12−1=4,095. A product not divisible by 3 uses only the 8 nonmultiples of 3: 2^8−1=255 subsets. Favorable: 4,095−255=3,840.
Answer: 3,840/4,095=256/273.

## Q12 • NAT • CHALLENGE
Question: How many bijections f on a 5-element set satisfy f(f(x))=x for every element x?

Solution: Only fixed points and disjoint pairs are possible. Count 0, 1, or 2 pairs: 1+C(5,2)+C(5,4)×3=1+10+15=26.
Answer: 26.

## Q13 • NAT
Question: Seven distinct people stand in a row. How many arrangements have two specified people not adjacent?

Solution: All orders: 7!=5,040. Adjacent orders: treat the pair as a block and allow either internal order, 6!×2=1,440. Subtract.
Answer: 5,040−1,440=3,600.

## Q14 • NAT
Question: How many nonnegative integer solutions to x₁+x₂+x₃=9 satisfy x₁≤2?

Solution: All solutions: C(11,2)=55. Bad solutions have x₁≥3. Subtract 3 from x₁; new total 6 gives C(8,2)=28 bad solutions.
Answer: 55−28=27.

## Q15 • MSQ
Question: Which statements are correct? Assume valid nonnegative integer parameters, 0≤r≤n and n₁+n₂≤n.
(A) Length-r strings from n symbols, repetition allowed: n^r.
(B) r-person committees from n people: P(n,r).
(C) n objects, with n₁ identical copies of one type and n₂ of another, all others distinct: n!/(n₁!n₂!).
(D) Nonempty subsets of an n-element set: 2^n−1.

Solution: A: true, n choices for every position. B: false, committees use C(n,r). C: true, divide out identical copies. D: true, remove the empty subset.
Answer: A, C, D.

## Q16 • NAT
Question: A subset of size 5 is selected from 12 distinct objects. How many such subsets contain exactly 2 objects from a specified group of 4?

Solution: Choose 2 from the specified 4 and the other 3 from the remaining 8: C(4,2)C(8,3)=6×56=336.
Answer: 336.

## Corrections

Second notes page: restored the 1/2 box-selection probabilities and consistent stars-and-bars variable names.

Precise edit to this sheet. Preserve ALL questions, explanations, numeric answers, colors and compact panel layout. Remove the INVENTED multiple-choice lists in question panels 10, 12, 13, 14 and 16 ONLY. They are numerical-answer (NAT) questions and must have NO A/B/C/D options. Specifically remove (A)96 (B)144 (C)192 (D)288 from Q10; (A)10 (B)20 (C)26 (D)32 from Q12; (A)2400 (B)3000 (C)3600 (D)4320 from Q13; (A)21 (B)24 (C)27 (D)30 from Q14; (A)168 (B)224 (C)336 (D)420 from Q16. KEEP the A/B/C/D statements and their full text in Q15, which IS a multiple-select question. Do not add or rewrite any questions. Fill the removed options area by adjusting existing question spacing, no extra text. Keep every solution equation and answer unchanged.

