# Lesson 1: Binary Numbers

> In the same way that humans use languages to read, write, and communicate, computers too have their own method of communication -- 1s and 0s. These 1s and 0s form what we know to be the **base-2** (binary) number system, 
> which underscores every operation that computers perform. Having a working knowledge of binary will allow you to see what is going on under the hood and, hopefully, give you a greater appreciation for the technology that you use on a daily basis.

## Overview

Throughout the course of our lives we have been taught math in a very specific way: using **base-10** (decimal) numbers. While you might not think about it often, the fundamental approach you use to express numbers all follow the same pattern: expressing numbers as *sums of powers of 10*. For instance, take the numbers 100, 1572, and 968477.
$$
100 = 1\times10^2 + 0\times10^1 + 0\times10^0\\ 
1572 = 1\times10^3 + 5\times10^2 + 7\times10^1 + 2\times10^0\\
968477 = 9\times10^5 + 6\times10^4 + 8\times10^3 + 5\times10^2 + 7\times10^1 + 7\times10^0
$$
From this, we arrive at a notion of **place value** -- the idea that a digit in a number receives value from its actual value as well as its position in the number. For instance, consider the number 6 in 968477. Since this number is in the 5<sup>th</sup> position, it has value $$6 \times 10^4=60000$$

In the same way that these numbers use digits (0 - 9) to express numbers as sums of powers of 10, binary numbers use digits (0 - 1) to express numbers as sums of powers of 2. Let's take the number 1011<sub>2</sub> as an example (typically, numbers that aren't in base-10 are represented with a subscript).

$$
1011 = 1 \times2^3 + 0\times2^2 + 1\times2^1 + 1\times2^0
$$
Hopefully you see that binary numbers follow the exact same pattern as decimal numbers -- namely, that they are just using sums to represent certain quantities.

## Binary To Decimal

By now, you might notice a neat connection between binary numbers and decimal numbers. Since these numbers are just different representations of the same thing, we can convert between them freely, as they are just sums.

Let's try converting the number we just looked at 1011<sub>2</sub> into base-10. As we saw earlier, we can express 1011<sub>2</sub> as 
$$
1011 = 1 \times2^3 + 0\times2^2 + 1\times2^1 + 1\times2^0
$$
This sum can be directly evaluated in base-10, since we know that 
$$
1\times2^3 + 0\times2^2 + 1\times2^1 + 1\times2^0 \\
= 1\times8 + 0\times4 + 1\times2 + 1\times1 \\= 8 + 0 + 2 + 1 = 11
$$
Therefore, by simply evaluating the sum of powers of 2 we get using a binary number, we can get that number's value in decimal. We've found a way to convert a binary number to a decimal number!

## Decimal To Binary

Now, let us look at the reverse, converting decimal numbers into binary. To convert base-10 numbers into base-2, repeatedly divide the number by 2, keep the remainders aside, and write the remainders down in reverse order.

Let's try converting $$21$$ into binary
1. $\frac{21}{2} = 10$, leaving a remainder of **1**
2. $\frac{10}{2} = 5$, leaving a remainder of  **0**
3. $\frac{5}{2} = 2$, leaving a remainder of **1**
4. $\frac{2}{2} = 1$, leaving a remainder of **0**
5. $\frac{1}{2} = 0$, leaving a remainder of **1**


Looking at the remainders in reverse, we see that $21$ in binary is $10101_2$. 

Therefore, by simply dividing the number by 2 and examining its remainders, we can get that number's value in binary. We've found a way to convert a decimal number to a binary number!

Let's take a look at another quick example: converting $36$ into binary:

1. $\frac{36}{2} = 18$, leaving a remainder of **0**
2. $\frac{18}{2} = 9$, leaving a remainder of  **0**
3. $\frac{9}{2} = 4$, leaving a remainder of **1**
4. $\frac{4}{2} = 2$, leaving a remainder of **0**
5. $\frac{2}{2} = 1$, leaving a remainder of **0**
6. $\frac{1}{2} = 0$, leaving a remainder of **1**


Looking at the remainders in reverse, we see that $36$ in binary is $100100_2$. 