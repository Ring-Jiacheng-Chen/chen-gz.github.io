---
toc: true
title: Greatest Common Divisor
category: number theory 
---

## Greatest Common Divisor(GCD)

Here is another passage about **GCD**. That passage most consider GCD in algorithm, but here we will give prove. 

Common Divisor mean if $a|b$ and $a|c$ then $a$ is common divisor of $b$ and $c$. 

Greatest Common Divisor is the *Greatest* one of all common divisor of $b,c$.

For example, 12 and 8 have two common divisor, 2 and 4.

To find out greatest common divisor is one of basic question in number theory. 

It look like easy for small numbers but we need to find a way to calculate the greatest common divisor as quickly as possible.

if a|b then can $a,b$ have relationship expressed by $a = bx + r$.

Thus the great commont divisor of $a$ and $b$ is equal to the great commont divisor of $bx+r$ and $b$.
Notice that $b$ dived by $bx$. So great commont divisor of $a$ and $b$ equap great common divisor of $b$ and $r$.

explain more if $c$ is the great common divisor of $a$ and $b$, then $c|bx +r$. Because of $c|b$ thus $c|bx$. we have $c|bx+r$ so c must divided by c. 

Here is a most important equation in this section
$$
gcd(a,b) = gcd(a mod b,b)
$$
considered some times $x$ may be zero means b bigger than a. So when write a computer program using recursion skill we need change the position of a$ and $b$. Rewrite the equation in order to use in computer program.
$$
gcd(a,b) = gcd(b,a mod b)
$$
$a$ and $b$ are(is) co-prime if we find out that the greatest common divisor of $a$ and $b$ is 1.



