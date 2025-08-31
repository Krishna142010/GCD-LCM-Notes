<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GCD & LCM Notes - 20 Pages</title>
<style>
    body { font-family: Arial, sans-serif; line-height: 1.6; margin: 0; padding: 0; background-color: #f9f9f9; }
    .page { width: 80%; margin: 40px auto; padding: 30px; background: #fff; box-shadow: 0 0 10px rgba(0,0,0,0.1); border-radius: 10px; }
    h1, h2, h3 { color: #2c3e50; }
    pre { background: #f4f4f4; padding: 10px; border-radius: 5px; overflow-x: auto; }
    ul { margin: 10px 0; }
    .example { background: #e8f6f3; padding: 10px; border-left: 5px solid #1abc9c; margin: 10px 0; }
    .problems { background: #fef3c7; padding: 10px; border-left: 5px solid #f1c40f; margin: 10px 0; }
</style>
</head>
<body>

<!-- Page 1 -->
<div class="page" id="page1">
<h1>Page 1 — Introduction to GCD and LCM</h1>
<p><strong>Greatest Common Divisor (GCD):</strong> For integers a and b, not both zero, the GCD is the largest positive integer that divides both.</p>
<p><strong>Least Common Multiple (LCM):</strong> The LCM of a and b is the smallest positive integer divisible by both.</p>
<ul>
<li>Properties:
<ul>
<li>gcd(a,0)=|a|, gcd(0,0)=0</li>
<li>lcm(a,0)=0</li>
<li>gcd(a,b)=gcd(b,a), lcm(a,b)=lcm(b,a)</li>
<li>gcd(a,b) * lcm(a,b) = |a*b|</li>
</ul>
</li>
</ul>
<div class="example">
<strong>Example:</strong> Find gcd(84,126) and lcm(84,126).<br>
Solution: 84=2²*3*7, 126=2*3²*7 → gcd=42, lcm=252
</div>
<div class="problems">
<strong>Problems:</strong>
<ul>
<li>Find gcd(36,60) and lcm(36,60)</li>
<li>Show that lcm(a,b) = |a*b| / gcd(a,b)</li>
</ul>
</div>
</div>

<!-- Page 2 -->
<div class="page" id="page2">
<h1>Page 2 — Methods to Compute GCD</h1>
<h2>1. Prime Factorization Method</h2>
<p>Factor numbers into primes. GCD: multiply min powers of common primes. LCM: multiply max powers of all primes.</p>
<div class="example">
<strong>Example:</strong> a=180=2²*3²*5, b=240=2⁴*3*5 → gcd=60, lcm=720
</div>
<h2>2. Euclidean Algorithm</h2>
<p>gcd(a,b)=gcd(b, a mod b). Repeat until remainder=0.</p>
<div class="example">
<strong>Example:</strong> gcd(252,105)<br>
252=105*2+42, 105=42*2+21, 42=21*2+0 → gcd=21
</div>
<div class="problems">
<ul>
<li>Compute gcd(391,299) using Euclidean Algorithm</li>
<li>Find integers x,y such that 391x + 299y = gcd(391,299)</li>
</ul>
</div>
</div>

<!-- Page 3 -->
<div class="page" id="page3">
<h1>Page 3 — Properties of GCD</h1>
<ul>
<li>Symmetry: gcd(a,b)=gcd(b,a)</li>
<li>Associativity: gcd(a,gcd(b,c))=gcd(gcd(a,b),c)</li>
<li>Multiplicative by common factor: gcd(ka,kb)=k*gcd(a,b)</li>
<li>Reduction: gcd(a,b)=gcd(a-b,b)</li>
<li>Linear combination: gcd(a,b) = smallest positive integer of the form ax+by</li>
</ul>
<div class="example">
<strong>Example:</strong> gcd(48,180) = 12 = 48*4 - 180*1
</div>
<div class="problems">
<ul>
<li>Prove gcd(a²,b²) = (gcd(a,b))²</li>
<li>Solve 105x + 252y = gcd(105,252)</li>
</ul>
</div>
</div>

<!-- Page 4 -->
<div class="page" id="page4">
<h1>Page 4 — Properties of LCM</h1>
<ul>
<li>Symmetry: lcm(a,b)=lcm(b,a)</li>
<li>Associativity: lcm(a,lcm(b,c))=lcm(lcm(a,b),c)</li>
<li>Multiplicative by common factor: lcm(ka,kb)=k*lcm(a,b)</li>
<li>Relation with GCD: lcm(a,b)*gcd(a,b)=|a*b|</li>
<li>Divisibility: if a|b → lcm(a,b)=b</li>
</ul>
<div class="example">
<strong>Example:</strong> lcm(12,18)=36, lcm(15,20,30)=60
</div>
<div class="problems">
<ul>
<li>Find lcm(21,35,49)</li>
<li>Prove lcm(a,b,c)=lcm(lcm(a,b),c)</li>
</ul>
</div>
</div>

<!-- Page 5 -->
<div class="page" id="page5">
<h1>Page 5 — GCD & LCM of Multiple Numbers</h1>
<ul>
<li>GCD: gcd(a,b,c)=gcd(gcd(a,b),c)</li>
<li>LCM: lcm(a,b,c)=lcm(lcm(a,b),c)</li>
<li>Divisibility property: a1|a2|…|an → gcd=a1, lcm=an</li>
</ul>
<div class="example">
<strong>Example:</strong> gcd(48,180,240)=12, lcm(48,180,240)=720
</div>
<div class="problems">
<ul>
<li>Find gcd(84,126,210) and lcm(84,126,210)</li>
<li>Prove gcd(a,b,c)*lcm(a,b,c) ≤ a*b*c</li>
</ul>
</div>
</div>

<!-- Page 6 -->
<div class="page" id="page6">
<h1>Page 6 — Applications of GCD</h1>
<ul>
<li>Simplifying fractions: divide numerator & denominator by gcd(a,b)</li>
<li>Linear Diophantine equations: ax+by=c → solution exists if gcd(a,b)|c</li>
<li>Real-life: scheduling machines, events</li>
</ul>
<div class="example">
<strong>Example:</strong> Simplify 180/240 → gcd=60 → 3/4
</div>
<div class="problems">
<ul>
<li>Solve 14x+35y=7</li>
<li>Simplify 462/714</li>
<li>Two buses arrive every 24 & 36 minutes → find coincidence</li>
</ul>
</div>
</div>

<!-- Page 7 -->
<div class="page" id="page7">
<h1>Page 7 — Applications of LCM</h1>
<ul>
<li>Scheduling: repeating events coincide</li>
<li>Adding/subtracting fractions: use LCM of denominators</li>
<li>Word problems: traffic lights, machines</li>
</ul>
<div class="example">
<strong>Example:</strong> 3 & 4 minute traffic lights → LCM=12 minutes → blink together
</div>
<div class="problems">
<ul>
<li>Find LCM of 18,24,30</li>
<li>Train every 20 min, bus every 30 min → first common departure</li>
<li>Add 7/10 + 11/15 using LCM</li>
</ul>
</div>
</div>

<!-- Page 8 -->
<div class="page" id="page8">
<h1>Page 8 — Relations Between GCD and LCM</h1>
<ul>
<li>Key formula: gcd(a,b)*lcm(a,b)=|a*b|</li>
<li>Proof via prime factorization: gcd=min exponents, lcm=max exponents</li>
<li>Extension: multi-number inequality: gcd(a,b,c)*lcm(a,b,c) ≤ a*b*c</li>
</ul>
<div class="example">
<strong>Example:</strong> a=12,b=18 → gcd=6,lcm=36 → 6*36=12*18=216
</div>
<div class="problems">
<ul>
<li>Verify gcd(48,180)*lcm(48,180)=48*180</li>
<li>Find three numbers with gcd=6 & lcm=180</li>
</ul>
</div>
</div>

<!-- Page 9 -->
<div class="page" id="page9">
<h1>Page 9 — GCD & LCM of Algebraic Expressions</h1>
<ul>
<li>GCD of polynomials: highest degree polynomial dividing both</li>
<li>LCM: lowest degree divisible by both, LCM(P,Q)=P*Q/gcd(P,Q)</li>
</ul>
<div class="example">
<strong>Example:</strong> P=x³-x,Q=x²-1 → gcd=(x-1)(x+1), lcm=x(x-1)(x+1)
</div>
<div class="problems">
<ul>
<li>Find gcd(x²-4, x²-x-6)</li>
<li>Find lcm(x²-1, x³-x)</li>
</ul>
</div>
</div>

<!-- Page 10 -->
<div class="page" id="page10">
<h1>Page 10 — Olympiad Tricks for GCD & LCM</h1>
<ul>
<li>If gcd(a,b)=1 → gcd(a,bc)=gcd(a,c), lcm(a,bc)=a*lcm(b,c)</li>
<li>Sum-product trick: lcm(a,b)+gcd(a,b) ≤ a+b</li>
<li>Prime factorization: min exponents for GCD, max for LCM</li>
</ul>
<div class="example">
<strong>Example:</strong> Find a,b with gcd=12, lcm=180 → a=12x,b=12y → xy=15, coprime pairs: (1,15),(3,5),(5,3),(15,1)
</div>
<div class="problems">
<ul>
<li>Find integers a,b with gcd=8, lcm=120</li>
<li>If gcd(a,b)=3 & lcm(a,b)=180 → find all solutions</li>
</ul>
</div>
</div>

<!-- Page 11 -->
<div class="page" id="page11">
<h1>Page 11 — GCD & LCM in Sequences</h1>
<ul>
<li>Consecutive integers: gcd(n,n+1)=1, lcm=n(n+1)</li>
<li>Arithmetic sequences: gcd(a,a+d,...)=gcd(a,d)</li>
<li>LCM in sequences: use pairwise extension</li>
</ul>
<div class="example">
<strong>Example:</strong> gcd(21,28,35) → a=21,d=7 → gcd=7
</div>
<div class="problems">
<ul>
<li>Compute gcd(101,102,103)</li>
<li>Compute lcm(5,10,15,20)</li>
</ul>
</div>
</div>

<!-- Page 12 -->
<div class="page" id="page12">
<h1>Page 12 — Practice Problems for Olympiad Preparation</h1>
<ul>
<li>Basic: gcd(270,192), lcm(270,192)</li>
<li>Advanced: gcd(a,b)=5,lcm(a,b)=180 → find a,b</li>
<li>Sequence-based: gcd(101,102,103), lcm of first three multiples of 7</li>
<li>Word problems: traffic lights, machines, repeating events</li>
</ul>
</div>

<!-- Page 13 -->
<div class="page" id="page13">
<h1>Page 13 — GCD & LCM Word Problems</h1>
<ul>
<li>Two pipes 12 & 18 hours → LCM=36 → coincidence time</li>
<li>Train 20 min, bus 30 min → LCM=60 min</li>
<li>Tips: LCM → coincidence, GCD → dividing equally</li>
</ul>
<div class="problems">
<ul>
<li>Three bells 3,5,7 min → when together?</li>
<li>Two runners laps 250,300m → when meet?</li>
</ul>
</div>
</div>

<!-- Page 14 -->
<div class="page" id="page14">
<h1>Page 14 — Mixed Number-Theory Problems</h1>
<ul>
<li>Find two numbers: GCD=6, LCM=180 → a=6x,b=6y,gcd(x,y)=1 → xy=30 → pairs: (1,30),(2,15),(3,10),(5,6)</li>
<li>Trick: gcd(a,b)=1 → lcm(a,b)=a*b</li>
</ul>
<div class="problems">
<ul>
<li>Find integers a,b with GCD=8, LCM=120</li>
<li>Find positive integers a,b: LCM(a,b)-GCD(a,b)=72</li>
</ul>
</div>
</div>

<!-- Page 15 -->
<div class="page" id="page15">
<h1>Page 15 — GCD & LCM in Sequences (Advanced)</h1>
<ul>
<li>Arithmetic sequence: gcd(a,a+d,...)=gcd(a,d)</li>
<li>Geometric sequence: gcd(r^n,r^m)=r^min(n,m)</li>
</ul>
<div class="problems">
<ul>
<li>gcd(16,64,256)</li>
<li>lcm(2,4,8,16)</li>
</ul>
</div>
</div>

<!-- Page 16 -->
<div class="page" id="page16">
<h1>Page 16 — GCD & LCM Proofs</h1>
<ul>
<li>GCD-LCM relation: gcd(a,b)*lcm(a,b)=a*b</li>
<li>Coprime property: if gcd(a,b)=1 → divisibility rules</li>
<li>Multi-number inequality: gcd(a,b,c)*lcm(a,b,c) ≤ a*b*c</li>
</ul>
<div class="problems">
<ul>
<li>Prove a|b & b|c → a|c</li>
<li>Prove gcd(a+b,a-b)=gcd(a,b) or 2*gcd(a,b)</li>
</ul>
</div>
</div>

<!-- Page 17 -->
<div class="page" id="page17">
<h1>Page 17 — Advanced Olympiad Problems</h1>
<ul>
<li>Three numbers a,b,c: gcd(a,b)=6, gcd(b,c)=12, lcm(a,c)=180</li>
<li>Positive integers a,b,c with lcm(a,b,c)=180 & gcd(a,b,c)=6</li>
<li>Representation: a=d*x, b=d*y, gcd(x,y)=1 → lcm=d*xy</li>
</ul>
</div>

<!-- Page 18 -->
<div class="page" id="page18">
<h1>Page 18 — Mixed Practice Problems</h1>
<ul>
<li>gcd(252,105,84)</li>
<li>lcm(12,15,20)</li>
<li>18x+24y=6 → find integer solutions</li>
<li>Three buses 12,15,20 min → first coincidence</li>
<li>gcd(a,b)=5,lcm(a,b)=180 → find all a,b</li>
</ul>
</div>

<!-- Page 19 -->
<div class="page" id="page19">
<h1>Page 19 — Real-Life Applications</h1>
<ul>
<li>Fractions & simplification: recipes, scaling</li>
<li>Scheduling: traffic lights, machines, events</li>
<li>Cryptography: GCD in RSA, coprime numbers for modular inverse</li>
<li>Modular arithmetic: solving Diophantine equations</li>
</ul>
<div class="problems">
<ul>
<li>Two lamps blink every 18 & 24 seconds → when together?</li>
<li>Simplify 462/714</li>
</ul>
</div>
</div>

<!-- Page 20 -->
<div class="page" id="page20">
<h1>Page 20 — Summary Sheet & Key Formulas</h1>
<ul>
<li>GCD: gcd(a,b)=gcd(b,a)=gcd(a-b,b)</li>
<li>LCM: lcm(a,b)=a*b/gcd(a,b)</li>
<li>Associativity: gcd(a,gcd(b,c))=gcd(gcd(a,b),c), lcm(a,lcm(b,c))=lcm(lcm(a,b),c)</li>
<li>Consecutive integers: gcd(n,n+1)=1, lcm(n,n+1)=n(n+1)</li>
<li>Tips: Use Euclidean Algorithm, prime factorization, LCM/GCD formula for checking</li>
</ul>
</div>

</body>
</html>
