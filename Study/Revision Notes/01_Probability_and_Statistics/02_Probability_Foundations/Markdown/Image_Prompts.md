# Probability Foundations — image prompts

Built-in ImageGen; the saved compact Counting sheet is the style reference.

## 00_Compact_Overview

Use case: scientific-educational. The supplied image is a STYLE REFERENCE only, not content to copy. Produce ONE flat print-ready portrait PNG page matching its dense educational cheat-sheet design: deep navy title banner, white serif title, compact black serif body, multiple narrow columns, numbered pastel panels, thin colored borders, small nested headings, blue example/answer highlights, crisp mathematically typeset fractions, superscripts and subscripts. Efficient compact layout, usually three columns. No large illustrations, cartoons, decorative icons, oversized headings, huge whitespace or giant four-panel layout. Include ALL authoritative text below faithfully, with no invented examples, questions, answer choices or new math. Do not change conditions, values or answers. You may arrange sections as compact subpanels. Use highest useful resolution for small printed text; avoid clipping. Markdown headings are structural; math should be typeset semantically.
Use twelve compact numbered panels in three columns. Tables must preserve all cell counts and totals exactly. Include probability conditions and complete worked arithmetic. No copied Counting content.

# PROBABILITY FOUNDATIONS
GATE DA 2027 | Compact overview

## 1. Sample space and events
S contains all possible outcomes. An event A is a subset of S.
Example: one die, S={1,2,3,4,5,6}; A=even={2,4,6}.
An outcome is one result; an event can contain many outcomes.

## 2. Event operations
A∩B: both. A∪B: at least one. Aᶜ: not A.
A\B = A∩Bᶜ.
Neither A nor B = (A∪B)ᶜ.
De Morgan: (A∪B)ᶜ=Aᶜ∩Bᶜ; (A∩B)ᶜ=Aᶜ∪Bᶜ.

## 3. Probability axioms
P(A)≥0; P(S)=1.
For countably many pairwise disjoint events Aᵢ:
P(⋃ᵢ Aᵢ)=ΣᵢP(Aᵢ).
Consequences: P(∅)=0; 0≤P(A)≤1.
If A⊆B, then P(A)≤P(B).

## 4. Complement and uniform counting
P(Aᶜ)=1−P(A).
For a finite sample space with equally likely outcomes only:
P(A)=|A|/|S|.
At least one head in 3 independent fair tosses:
1−P(TTT)=1−1/8=7/8.

## 5. Addition and probability bounds
P(A∪B)=P(A)+P(B)−P(A∩B).
For three events: add singles, subtract pair intersections, add the triple intersection.
max(0,P(A)+P(B)−1)≤P(A∩B)≤min(P(A),P(B)).
Example: P(A)=0.7, P(B)=0.6 ⇒ intersection is between 0.3 and 0.6.

## 6. Conditional probability
For P(B)>0:
P(A|B)=P(A∩B)/P(B).
The condition B becomes the reference group.
Die: A=even, B=greater than 3.
A∩B={4,6}; B={4,5,6}.
P(A|B)=2/3.

## 7. Joint probability and chain rule
Joint means both events: P(A∩B).
P(A∩B)=P(B)P(A|B).
Also P(A∩B)=P(A)P(B|A), when defined.
P(A∩B∩C)=P(A)P(B|A)P(C|A∩B), when the conditions have positive probability.
Multiply conditional probabilities along a path.

## 8. Marginal probability
Sum joint probabilities over a partition:
P(A)=ΣᵢP(A∩Bᵢ).
In a two-way table: cells are joints; row/column totals are marginals.
For P(A∩B)=0.18 and P(A∩Bᶜ)=0.22:
P(A)=0.18+0.22=0.40.

## 9. Mutually exclusive events
A∩B=∅: cannot happen together.
P(A∩B)=0 and P(A∪B)=P(A)+P(B).
Example: one die showing 1 versus showing 2.
Positive-probability disjoint events are dependent.

## 10. Independent events
Definition: P(A∩B)=P(A)P(B).
If P(B)>0: independence ⇔ P(A|B)=P(A).
Independent A,B imply Aᶜ,B are independent.
Example: P(A)=0.6, P(B)=0.2:
P(Aᶜ∩B)=(1−0.6)(0.2)=0.08.
Independence does not mean no overlap.

## 11. Total probability
B₁,…,Bₖ partition S: disjoint and exhaustive.
For positive P(Bᵢ):
P(A)=ΣᵢP(A|Bᵢ)P(Bᵢ).
For two cases: P(A)=P(A|B)P(B)+P(A|Bᶜ)P(Bᶜ).
Weight each conditional probability by its case probability.

## 12. Bayes and final checks
For P(A)>0:
P(Bⱼ|A)=P(A|Bⱼ)P(Bⱼ) / ΣᵢP(A|Bᵢ)P(Bᵢ).
Posterior = target joint / total evidence.
P(A|B) need not equal P(B|A).
Check the denominator, overlap, independence assumption and base rates.
Conditional expectation/variance come later with random variables.

## 01_Worked_Methods_and_Bayes

Use case: scientific-educational. The supplied image is a STYLE REFERENCE only, not content to copy. Produce ONE flat print-ready portrait PNG page matching its dense educational cheat-sheet design: deep navy title banner, white serif title, compact black serif body, multiple narrow columns, numbered pastel panels, thin colored borders, small nested headings, blue example/answer highlights, crisp mathematically typeset fractions, superscripts and subscripts. Efficient compact layout, usually three columns. No large illustrations, cartoons, decorative icons, oversized headings, huge whitespace or giant four-panel layout. Include ALL authoritative text below faithfully, with no invented examples, questions, answer choices or new math. Do not change conditions, values or answers. You may arrange sections as compact subpanels. Use highest useful resolution for small printed text; avoid clipping. Markdown headings are structural; math should be typeset semantically.
Use twelve compact numbered panels in three columns. Tables must preserve all cell counts and totals exactly. Include probability conditions and complete worked arithmetic. No copied Counting content.

# PROBABILITY • WORKED METHODS
GATE DA 2027 | Joint, marginal, conditional and Bayes

## 1. Read a two-way table
In 100 students, A=studies Python and B=studies SQL.
The groups may overlap.
Counts:
             B      Bᶜ      Total
A           18      22       40
Aᶜ          12      48       60
Total       30      70      100
Divide a cell by 100 for its joint probability. Divide a row or column total by 100 for a marginal.

## 2. Joint and marginal worked
Joint: P(A∩B)=18/100=0.18.
Marginal: P(A)=40/100=0.40.
Marginal: P(B)=30/100=0.30.
Union: (18+22+12)/100=0.52.
Check: 0.40+0.30−0.18=0.52.
Neither: 48/100=0.48=1−0.52.

## 3. The direction of conditioning
P(A|B)=18/30=0.60.
P(B|A)=18/40=0.45.
The numerator is the same; the reference group changes.
Neither equals the joint probability 0.18.
P(A|B)×P(B)=0.60×0.30=0.18.

## 4. Test independence
Compare joint to product of marginals.
Here 0.18 ≠ 0.40×0.30=0.12.
Therefore A and B are dependent.
If A,B were independent and P(B)>0, P(A|B) would equal P(A).
The data show 0.60≠0.40.

## 5. Disjointness is different
If A∩B=∅ and P(A),P(B)>0:
P(A∩B)=0 but P(A)P(B)>0.
Therefore they cannot be independent.
Example: a die showing 1 versus showing 2.
P(A|B)=0, not P(A)=1/6.

## 6. Sequential draws
A bag has 4 green and 3 yellow balls.
Two draws without replacement:
P(both green)=P(G₁)P(G₂|G₁)
=(4/7)(3/6)=2/7.
With replacement: (4/7)(4/7)=16/49.
The second probability changes when a ball is removed.

## 7. Partition the causes
Machine M₁ produces 60% of items; M₂ produces 40%.
Their defect rates are 2% and 5%.
D denotes a defective item.
P(M₁)=0.60; P(M₂)=0.40.
P(D|M₁)=0.02; P(D|M₂)=0.05.
The machine events are disjoint and exhaustive.

## 8. Multiply then add
Route M₁ and defect: 0.60×0.02=0.012.
Route M₂ and defect: 0.40×0.05=0.020.
P(D)=0.012+0.020=0.032.
Do not take the unweighted mean of the defect rates.
Check: weighted defect rate lies between 0.02 and 0.05.

## 9. Reverse the condition
Given a defect, find its machine:
P(M₂|D)=P(M₂∩D)/P(D)
=0.020/0.032=0.625.
P(M₁|D)=0.012/0.032=0.375.
Posterior probabilities sum to 1.
A 5% defect likelihood does not mean a 5% posterior probability.

## 10. Base rates and complements
Bayes must use the prior P(M₂)=0.40.
P(M₂|Dᶜ) differs from P(M₂|D).
Nondefective routes: 0.60×0.98=0.588 and 0.40×0.95=0.380.
P(Dᶜ)=0.968.
P(M₂|Dᶜ)=0.380/0.968≈0.3926.

## 11. Conditioning can simplify
Three independent fair coins; given the first toss is a tail, at least one head requires a head in the last two tosses.
P(at least one H | first T)=1−P(TT)=3/4.
Use the reduced sample space after conditioning.

## 12. Problem-solving sequence
Define events → identify observation/reference group → choose table, tree or event rule → calculate joints → normalize if conditioning → check 0≤P≤1 and that complementary probabilities sum to 1.

## 02_Verified_DA_Examples

Use case: scientific-educational. The supplied image is a STYLE REFERENCE only, not content to copy. Produce ONE flat print-ready portrait PNG page matching its dense educational cheat-sheet design: deep navy title banner, white serif title, compact black serif body, multiple narrow columns, numbered pastel panels, thin colored borders, small nested headings, blue example/answer highlights, crisp mathematically typeset fractions, superscripts and subscripts. Efficient compact layout, usually three columns. No large illustrations, cartoons, decorative icons, oversized headings, huge whitespace or giant four-panel layout. Include ALL authoritative text below faithfully, with no invented examples, questions, answer choices or new math. Do not change conditions, values or answers. You may arrange sections as compact subpanels. Use highest useful resolution for small printed text; avoid clipping. Markdown headings are structural; math should be typeset semantically.
Use twelve compact numbered panels in three columns. Tables must preserve all cell counts and totals exactly. Include probability conditions and complete worked arithmetic. No copied Counting content.

# PROBABILITY • VERIFIED EXAM EXAMPLES
GATE DA 2027 | Official PYQs and a labeled supplement

## 1. DA 2024 Q12 — question
Official question, paraphrased.
Three fair coins are tossed independently. T means at least two heads; S means at least two tails. Find P(T∩S).
Original choices: (A) 0; (B) 0.5; (C) 0.25; (D) 1.

## 2. DA 2024 Q12 — solution
At least two heads in three tosses leaves at most one tail.
Thus T and S cannot occur together: T∩S=∅.
Answer: P(T∩S)=0, option A.
Official final key: A. Official paper PDF page 9.
Trap: the individual tosses being independent does not make every pair of derived events independent.

## 3. DA 2024 Q58 — question
Official question, paraphrased.
P(Tᶜ)=0.6, P(S|T)=0.3, P(S|Tᶜ)=0.6.
Find P(T|S), rounded to two decimal places.

## 4. DA 2024 Q58 — solution
P(T)=1−0.6=0.4.
Joint target: P(T∩S)=0.3×0.4=0.12.
Evidence: P(S)=0.3×0.4+0.6×0.6=0.48.
P(T|S)=0.12/0.48=0.25.
Official final key: 0.25. Official paper PDF page 38.
Trap: the given 0.6 is P(Tᶜ), not P(T).

## 5. DA 2025 Q31 — question
Official question, paraphrased.
Box 1 has 2 black and 1 white balls.
Box 2 has 1 black and 2 white balls.
Box 3 has 3 black and 3 white balls.
The boxes are chosen with probabilities 1/2, 1/6, 1/3 respectively. A random ball from the selected box is white. Find P(Box 2 | white), rounded to two decimals.

## 6. DA 2025 Q31 — likelihood table
Let W=white and Bᵢ=Box i chosen.
Box | Prior P(Bᵢ) | P(W|Bᵢ) | White joint
1   | 1/2         | 1/3      | 1/6
2   | 1/6         | 2/3      | 1/9
3   | 1/3         | 1/2      | 1/6
Evidence P(W)=1/6+1/9+1/6=4/9.

## 7. DA 2025 Q31 — posterior
Target joint: P(B₂∩W)=1/9.
P(B₂|W)=(1/9)/(4/9)=1/4=0.25.
Official final key: 0.25. Official paper PDF page 17.
The box with most white balls is not necessarily the most likely source of a white observation; the prior matters.

## 8. Supplement — supplied bank
Question: Four fair coins are tossed independently. Find the probability of at least one head and at least one tail.
Source: da questions.pdf, PDF page 408, section 9.5.1; bank tags it GATE CSE 2002 Q2.16.
Other-exam supplement. Answer independently derived; not verified against an official CSE key.

## 9. Supplement — solution
The complement contains only HHHH and TTTT.
Each has probability 1/16.
Required probability=1−2/16=14/16=7/8.
Trap: “at least one of each” excludes both extreme outcomes, not just one.

## 10. Translate the words
“Both” → intersection.
“Either or both” → union.
“Neither” → complement of union.
“Given” → restrict to the stated condition.
“Source given observed result” → Bayes.
“No occurrence” or “at least one” → check a complement.

## 11. Checks before computing
Are elementary outcomes equally likely?
Are the cases disjoint and exhaustive?
Are draws with or without replacement?
Is independence stated or proved?
Did you reverse a conditional without Bayes?
Are rounding instructions followed only at the end?

## 12. Source boundary
Included DA answers were checked against official 2024/2025 final keys.
The 2026 conditional exponential question belongs to continuous distributions and is reserved for that later packet.
This is a selected practice set; exhaustive PYQ coverage is not claimed.
Next: attempt the authored checkpoint before viewing its separate full-question solutions.

## 03_Checkpoint_Q1_12

Use case: scientific-educational. The supplied image is a STYLE REFERENCE only, not content to copy. Produce ONE flat print-ready portrait PNG page matching its dense educational cheat-sheet design: deep navy title banner, white serif title, compact black serif body, multiple narrow columns, numbered pastel panels, thin colored borders, small nested headings, blue example/answer highlights, crisp mathematically typeset fractions, superscripts and subscripts. Efficient compact layout, usually three columns. No large illustrations, cartoons, decorative icons, oversized headings, huge whitespace or giant four-panel layout. Include ALL authoritative text below faithfully, with no invented examples, questions, answer choices or new math. Do not change conditions, values or answers. You may arrange sections as compact subpanels. Use highest useful resolution for small printed text; avoid clipping. Markdown headings are structural; math should be typeset semantically.
Twelve numbered question-only panels in three columns. NO answers, NO solutions, NO method hints, NO marked correct options, NO added choices, NO large empty working boxes; work is on separate paper. Include all question text and original options exactly.

# PROBABILITY • CHECKPOINT Q1–12
GATE DA 2027 | Authored practice | Suggested time: 45–55 minutes
Work on separate paper. No answers or hints are included. Q4 and Q12 are written responses.

## Q1 • MCQ
Which statement is always correct?
(A) P(S)=0 for the sample space S.
(B) P(A) may be negative.
(C) If A and B are disjoint, P(A∪B)=P(A)+P(B).
(D) P(A|B)=P(B|A) whenever both are defined.

## Q2 • NAT
P(A)=0.45, P(B)=0.35 and P(A∩B)=0.15. Find P(A∪B).

## Q3 • MSQ
P(A)=0.7 and P(B)=0.6. Which values could P(A∩B) take?
(A) 0.2  (B) 0.3  (C) 0.5  (D) 0.7

## Q4 • SHORT RESPONSE
Roll a fair die. A means even; B means at least 4. Find P(A|B) as a reduced fraction.

## Q5 • NAT
P(B)=0.5 and P(A|B)=0.3. Find P(A∩B).

## Q6 • MSQ
A and B are disjoint, P(A)=0.4 and P(B)=0.3. Which statements are true?
(A) A and B are independent.
(B) P(A|B)=0.
(C) P(A∪B)=0.7.
(D) P(A∩B)=0.12.

## Q7 • NAT
A and B are independent, with P(A)=0.6 and P(B)=0.2. Find P(Aᶜ∩B).

## Q8 • NAT
A bag has 3 red and 2 blue balls. Two balls are drawn without replacement. Given the first ball is blue, find the probability the second is red.

## Q9 • NAT
Machine M₁ supplies 70% of items and M₂ supplies 30%. Their defect rates are 2% and 8% respectively. Find P(defect).

## Q10 • NAT
Machine M₁ supplies 70% of items and M₂ supplies 30%. Their defect rates are 2% and 8%. Given an item is defective, find P(M₂|defect), rounded to four decimal places.

## Q11 • NAT
Three fair coins are tossed independently. Given the first toss is a tail, find the probability of at least one head among the three tosses.

## Q12 • SHORT RESPONSE
Among 100 customers, 30 bought item A, 40 bought item B and 12 bought both. Select one customer uniformly. Find P(A∩B), P(A|B), and decide whether A and B are independent.

## 04_Solutions_Q1_6

Use case: scientific-educational. The supplied image is a STYLE REFERENCE only, not content to copy. Produce ONE flat print-ready portrait PNG page matching its dense educational cheat-sheet design: deep navy title banner, white serif title, compact black serif body, multiple narrow columns, numbered pastel panels, thin colored borders, small nested headings, blue example/answer highlights, crisp mathematically typeset fractions, superscripts and subscripts. Efficient compact layout, usually three columns. No large illustrations, cartoons, decorative icons, oversized headings, huge whitespace or giant four-panel layout. Include ALL authoritative text below faithfully, with no invented examples, questions, answer choices or new math. Do not change conditions, values or answers. You may arrange sections as compact subpanels. Use highest useful resolution for small printed text; avoid clipping. Markdown headings are structural; math should be typeset semantically.
Six numbered panels in three columns with nested Question / Working / Answer boxes. Repeat the ENTIRE question INCLUDING all provided options and conditions, then working and final answer. NEVER add any A/B/C/D options to a NAT or short-response question. Preserve original options only for MCQ/MSQ.

# PROBABILITY • SOLUTIONS Q1–6
GATE DA 2027 | Authored practice | Full questions, working and answers

## Q1 • MCQ
Question: Which statement is always correct?
(A) P(S)=0 for the sample space S.
(B) P(A) may be negative.
(C) If A and B are disjoint, P(A∪B)=P(A)+P(B).
(D) P(A|B)=P(B|A) whenever both are defined.

Working: Probability axioms give P(S)=1 and P(A)≥0. Disjoint events add. Reversing a condition generally changes the value.
Answer: C.

## Q2 • NAT
Question: P(A)=0.45, P(B)=0.35 and P(A∩B)=0.15. Find P(A∪B).

Working: Inclusion–exclusion subtracts the shared outcomes once: P(A∪B)=0.45+0.35−0.15=0.65.
Answer: 0.65.

## Q3 • MSQ
Question: P(A)=0.7 and P(B)=0.6. Which values could P(A∩B) take?
(A) 0.2  (B) 0.3  (C) 0.5  (D) 0.7

Working: The intersection lies between max(0,0.7+0.6−1)=0.3 and min(0.7,0.6)=0.6. Values 0.3 and 0.5 are feasible; 0.2 and 0.7 are not.
Answer: B, C.

## Q4 • SHORT RESPONSE
Question: Roll a fair die. A means even; B means at least 4. Find P(A|B) as a reduced fraction.

Working: Given B, the equally likely outcomes are {4,5,6}. Of these, {4,6} satisfy A. Hence P(A|B)=2/3.
Answer: 2/3.

## Q5 • NAT
Question: P(B)=0.5 and P(A|B)=0.3. Find P(A∩B).

Working: Use the multiplication rule: P(A∩B)=P(B)P(A|B)=0.5×0.3=0.15. Independence is not needed.
Answer: 0.15.

## Q6 • MSQ
Question: A and B are disjoint, P(A)=0.4 and P(B)=0.3. Which statements are true?
(A) A and B are independent.
(B) P(A|B)=0.
(C) P(A∪B)=0.7.
(D) P(A∩B)=0.12.

Working: Disjointness gives P(A∩B)=0. Since 0≠0.4×0.3, the events are dependent. P(A|B)=0/0.3=0; their union has probability 0.4+0.3=0.7.
Answer: B, C.

## 05_Solutions_Q7_12

Use case: scientific-educational. The supplied image is a STYLE REFERENCE only, not content to copy. Produce ONE flat print-ready portrait PNG page matching its dense educational cheat-sheet design: deep navy title banner, white serif title, compact black serif body, multiple narrow columns, numbered pastel panels, thin colored borders, small nested headings, blue example/answer highlights, crisp mathematically typeset fractions, superscripts and subscripts. Efficient compact layout, usually three columns. No large illustrations, cartoons, decorative icons, oversized headings, huge whitespace or giant four-panel layout. Include ALL authoritative text below faithfully, with no invented examples, questions, answer choices or new math. Do not change conditions, values or answers. You may arrange sections as compact subpanels. Use highest useful resolution for small printed text; avoid clipping. Markdown headings are structural; math should be typeset semantically.
Six numbered panels in three columns with nested Question / Working / Answer boxes. Repeat the ENTIRE question INCLUDING all provided options and conditions, then working and final answer. NEVER add any A/B/C/D options to a NAT or short-response question. Preserve original options only for MCQ/MSQ.

# PROBABILITY • SOLUTIONS Q7–12
GATE DA 2027 | Authored practice | Full questions, working and answers

## Q7 • NAT
Question: A and B are independent, with P(A)=0.6 and P(B)=0.2. Find P(Aᶜ∩B).

Working: P(A∩B)=0.6×0.2=0.12. Subtract from P(B): P(Aᶜ∩B)=0.2−0.12=0.08. Equivalently, (1−0.6)×0.2.
Answer: 0.08.

## Q8 • NAT
Question: A bag has 3 red and 2 blue balls. Two balls are drawn without replacement. Given the first ball is blue, find the probability the second is red.

Working: After the blue first draw, 3 red and 1 blue remain. The conditional reference group has 4 balls. Probability=3/4=0.75.
Answer: 0.75.

## Q9 • NAT
Question: Machine M₁ supplies 70% of items and M₂ supplies 30%. Their defect rates are 2% and 8% respectively. Find P(defect).

Working: Weight each defect rate by its source prior: P(D)=0.7×0.02+0.3×0.08=0.014+0.024=0.038.
Answer: 0.038.

## Q10 • NAT
Question: Machine M₁ supplies 70% of items and M₂ supplies 30%. Their defect rates are 2% and 8%. Given an item is defective, find P(M₂|defect), rounded to four decimal places.

Working: P(D)=0.7×0.02+0.3×0.08=0.038. The target joint is 0.3×0.08=0.024. Bayes gives 0.024/0.038=12/19≈0.6315789. Round at the end.
Answer: 0.6316.

## Q11 • NAT
Question: Three fair coins are tossed independently. Given the first toss is a tail, find the probability of at least one head among the three tosses.

Working: The first toss contributes no head. The last two tosses remain independent and fair. Exclude TT: 1−(1/2)²=3/4=0.75.
Answer: 0.75.

## Q12 • SHORT RESPONSE
Question: Among 100 customers, 30 bought item A, 40 bought item B and 12 bought both. Select one customer uniformly. Find P(A∩B), P(A|B), and decide whether A and B are independent.

Working: Joint: 12/100=0.12. Conditional: 12/40=0.30. Marginals: P(A)=0.30, P(B)=0.40. Their product is 0.12, equal to the joint; hence the events are independent.
Answer: 0.12; 0.30; independent.

## Targeted correction to worked methods

Correct ONE subscript only. In bottom-left panel 10 'Base rates and complements', the bottom boxed formula currently incorrectly says P(M₁|Dᶜ)=0.380/0.968≈0.3926. Change the M₁ in THAT boxed formula to M₂, so it reads P(M₂|Dᶜ)=0.380/0.968≈0.3926. Keep the number values, all other formulas, tables and the full page layout unchanged. Nothing else should be edited.

Edit ONLY the pale blue boxed equation in bottom-left panel 10 'Base rates and complements'. Completely DELETE the existing formula in that box. Replace it with these exact TWO plain-text lines, no M subscripts at all:
'P(Machine 2 | nondefective)'
'= 0.380 / 0.968 ≈ 0.3926'
Make 'Machine 2' visibly read with the normal digit 2. Do not write Machine 1 or M1. Keep ALL other text and panels unchanged. This fixes a mislabelled result for the SECOND machine.

