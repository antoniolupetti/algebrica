## What is the expected value of a random variable?

The [mean](../introduction-to-the-mean) represents a fundamental statistical measure that characterizes the central tendency of a dataset. It reduces an entire distribution to a single, informative quantity indicating the point around which values are balanced. 

Among the main types of means are the [arithmetic mean](../arithmetic-mean) and the [geometric mean](../geometric-mean), both used to summarize a finite set of numerical values. While these measures describe the central tendency of observed data, the concept of the mean can also be extended to [discrete random variables](../discrete-random-variables) and [continuous random variables](../continuous-random-variables/). 

Given a random variable \\(X\\), its mean, also called the **expected value** or mathematical expectation, is defined as the quantity \\(\mu = E[X]\\). It expresses the long-term average value that the random variable would produce if the same random process were repeated indefinitely under the same conditions. 

Conceptually, it marks the balance point of the distribution, the level around which the possible outcomes tend to concentrate.

- - -

In the case of [discrete random variables](../discrete-random-variables), the mean is defined as:

\\[
\mu = E(X) = \sum_x x f(x)
\\]

where \\(x\\) represents the possible values that the random variable \\(X\\) can take, and \\(f(x)\\) is the probability associated with each value of \\(x\\).

- - -

In the case of continuous random variables, the mean is defined as:

\\[
\mu = E(X) = \int_{-\infty}^{+\infty} x f(x) dx
\\]

where \\(f(x)\\) is the probability density function of the random variable \\(X\\), and the [integral](..definite-integrals/) sums the contributions of all possible values of \\(x\\) across the entire real line.

##### In both cases, the mean is derived from the probability distribution itself. Instead of being calculated from a limited set of data points, it reflects the balance of all possible outcomes of \\(X\\), each contributing in proportion to how likely it is to occur.

## Properties of the expected value of a random variable

The expected value possesses several fundamental properties that emerge from its definition and are valid for both discrete and continuous random variables. The monotonicity property states that if one random variable is always greater than or equal to another for every possible outcome, then the same relation holds for their expected values. In other words, if for all outcomes \\( \omega \\) we have \\( X(\omega) \ge Y(\omega) \\), it follows that  
\\[
E(X) \ge E(Y)
\\]
This expresses the idea that expectation preserves order: the mean of a larger quantity cannot be smaller than the mean of a smaller one.

- - -

The linearity with respect to constants indicates how expectation reacts to a constant multiplier. When a random variable \\( X \\) is multiplied by a real constant \\( c \\), the expected value scales by the same factor, that is,  
\\[
E(cX) = c\\,E(X)
\\]
This reflects the fact that multiplying all possible values of \\( X \\) by the same constant simply stretches or compresses its distribution, without altering the underlying proportional relationships.

- - -

Finally, the additivity property establishes that the expected value of the sum of two random variables equals the sum of their individual expectations:  
\\[
E(X + Y) = E(X) + E(Y)
\\]
This result is particularly important because it holds regardless of whether the variables are independent or not.
## Expectation for jointly distributed variables

The concept of the mean, or expected value, can also be extended to functions of two random variables \\(X\\) and \\(Y\\) that follow a joint probability distribution \\(f(x, y)\\). In this case, we can compute the expected value of a new variable \\(g(X, Y)\\), defined in terms of \\(X\\) and \\(Y\\).

For discrete random variables, the expected value is given by:

\\[
\mu_{g(X,Y)} = E[g(X,Y)] = \sum_x \sum_y g(x, y) f(x, y)
\\]

For continuous random variables, the expression becomes:

\\[
\mu_{g(X,Y)} = E[g(X,Y)] = \int_{-\infty}^{+\infty} \int_{-\infty}^{+\infty} g(x, y) f(x, y) dx dy
\\]

In both forms, the mean represents the weighted average of the function \\(g(X, Y)\\), where the weights are provided by the joint probability distribution of \\(X\\) and \\(Y\\).
## Example 1

Consider a discrete random variable \\(X\\) that represents the number of defective items found in a random sample of two products taken from a batch where 10% of all items are defective. Each item can be either defective (D) or non-defective (N), and the probability of defect is the same for each draw.

The possible values of \\(X\\) are \\(0\\), \\(1\\), and \\(2\\), corresponding to the number of defective items in the sample. Assuming independence between draws, the probability distribution is:

| \\(x\\) | \\(0\\) | \\(1\\) | \\(2\\) |
|:--:|:--:|:--:|:--:|
| \\(f(x)\\) | \\(0.9^2\\) | \\(2 \cdot 0.1 \cdot 0.9\\) | \\(0.1^2\\) |
| \\(f(x)\\) | \\(0.81\\) | \\(0.18\\) | \\(0.01\\) |

Using the formula for the mean of a discrete random variable

\\[
\mu = E(X) = \sum_x x f(x)
\\]

we obtain:

\\[
\begin{align}
\mu = E(X) &= 0 \cdot 0.81 + 1 \cdot 0.18 + 2 \cdot 0.01 \\\\[6pt]
    &= 0 + 0.18 + 0.02 \\\\[6pt]
    &= 0.20
\end{align}
\\]The expected number of defective items in the two-product sample is therefore \\(0.2\\). This means that, on average, one defective item is expected every five samples of two products drawn under the same conditions.

## Example 2

Let’s now consider an example that involves the continuous case, where the random variable can take infinitely many values within a given interval. We will study the lifetime, measured in hours, of a light bulb, assuming that longer lifetimes are more likely than shorter ones. The random variable \\( X \\) represents the lifetime of a light bulb, and its [probability density function](../continuous-random-variables/) is defined as:

\\[
f(x) =
\begin{cases}
\dfrac{2x}{25^2} & 0 \le x \le 25 \\\\[6pt]
0 & \text{otherwise}
\end{cases}
\\]

The expected value, or mean, represents the theoretical average lifetime of the bulb.  
For a continuous random variable, it is defined as:

\\[
\mu = E(X) = \int_{-\infty}^{+\infty} x f(x)\\,dx
\\]

Since the density is zero outside the interval \\([0,25]\\), this simplifies to:

\\[
\mu = \int_0^{25} x \cdot \frac{2x}{25^2}\\,dx
\\]

This expression calculates the weighted average of all possible lifetimes, where each value \\( x \\) is weighted by its likelihood according to \\( f(x) \\).

---

We can now compute the integral:

\\[
\mu = \frac{2}{25^2} \int_0^{25} x^2\\,dx
\\]

Let’s focus on the integral, which can be solved directly. We have:

\\[
\int_0^{25} x^2\\,dx = \frac{25^3}{3} = \frac{15625}{3}
\\]

In fact, by integrating \\( x^2 \\), we obtain its antiderivative \\( \tfrac{1}{3}x^3 \\). Evaluating it at the limits from 0 to 25 gives: 

\\[
\frac{1}{3} \cdot 25^3 - \frac{1}{3} \cdot 0^3 = \frac{25^3}{3}
\\]

which represents the value of the definite integral.

- - -

Substituting this result we obtain:

\\[
\mu = \frac{2}{625} \cdot \frac{15625}{3} = \frac{50}{3}
\\]
Therefore, the mean lifetime of the light bulb is:

\\[
\mu = \frac{50}{3} \approx 16.67 \text{ hours}
\\]
