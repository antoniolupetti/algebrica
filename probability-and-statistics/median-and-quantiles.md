---
title: Median and Quantiles
source: https://algebrica.org/median-and-quantiles/
license: CC BY-NC 4.0
tags:
  - interquantile-range
  - median
  - quantiles
  - quartiles
  - statistics
---
## The central position in a data distribution

The median is a measure of central tendency that describes the typical value of a distribution. While the [mean](../introduction-to-the-mean/) is the numerical balance of all the values, the median is a positional measure, the value that divides the ordered data into two groups of equal size. Because it depends only on the relative ordering of the observations, the median is stable in the presence of outliers and is preferable to the [arithmetic mean](../arithmetic-mean/) when the distribution is skewed. In that case the mean shifts toward the longer tail while the median does not, so the gap between the two indices measures the skewness of the data.

Formally, let $n$ numerical observations be arranged in ascending order:

$$x_{1} \leq x_{2} \leq \dots \leq x_{n}$$

If $n$ is odd, the median is the central element of the sequence:

$$\tilde{M} = x_{\left(\frac{n+1}{2}\right)}$$

If $n$ is even, it is the average of the two middle values:

$$\tilde{M} = \frac{x_{\left(\frac{n}{2}\right)} + x_{\left(\frac{n}{2}+1\right)}}{2}$$

> In both cases the number of observations below the median equals the number above it, so the partition of the data is balanced.

## Example 1

We first compute the median when the number of observations is odd. The following table shows the monthly salaries of seven employees of the same company:

| Employee $x_i$ | Salary (\$) |
|:---:|:---:|
| $x_1$ | 1,200 |
| $x_2$ | 1,300 |
| $x_3$ | 1,400 |
| $x_4$ | 1,500 |
| $x_5$ | 3,000 |
| $x_6$ | 3,200 |
| $x_7$ | 4,000 |

With $n = 7$ observations, the median is the value in the central position:

$$\tilde{M} = x_{\left(\frac{n+1}{2}\right)} = x_{4}$$

The fourth value of the ordered list is $1{,}500,$ so the median salary is \$1,500.

> Half of the employees earn less than \$1,500 per month and half earn more.

## A distance-based definition of the median

The median also minimizes the total absolute deviation of the observations:

$$\tilde{M} \in \arg\min_{m} \sum_{i=1}^{n} |x_i - m|$$

Here $|x_i - m|$ is the [distance](../absolute-value/) between the observation $x_i$ and the candidate value $m.$ In this characterization the median is the value closest to the data as a whole, with closeness measured by the total distance rather than by the algebraic balance of the values.

Moving $m$ to the right by a small amount $\varepsilon$ increases the deviation of every observation to its left by $\varepsilon$ and decreases the deviation of every observation to its right by the same amount, so the sum changes by $\varepsilon$ times the difference between the two counts. Shifting $m$ toward the side that contains more observations decreases the total, and the minimum falls where the two sides contain the same number of observations, which is the positional definition of the median.

> For odd $n$ the minimizer is unique, the central observation. For even $n$ every point of the [interval](../intervals/) between the two central values gives the same minimal sum, and the convention of averaging them selects the midpoint of this interval.

- - -

We apply this property to the data of Example 1, where the salaries in dollars are:

$$1200, 1300, 1400, 1500, 3000, 3200, 4000$$

Let $S(m) = \sum_{i=1}^{n} |x_i - m|$ denote the total absolute deviation from a candidate value $m.$ For $m = 1200$:

$$
\begin{align}
S(1200) &= |1200 - 1200| + |1300 - 1200| + |1400 - 1200| + |1500 - 1200| \\[6pt]
&+ |3000 - 1200| + |3200 - 1200| + |4000 - 1200| \\[6pt]
&= 0 + 100 + 200 + 300 + 1800 + 2000 + 2800 = 7200
\end{align}
$$

For $m = 1300$ the same computation gives:

$$
\begin{align}
S(1300) &= |1200 - 1300| + |1300 - 1300| + |1400 - 1300| + |1500 - 1300| \\[6pt]
&+ |3000 - 1300| + |3200 - 1300| + |4000 - 1300| \\[6pt]
&= 100 + 0 + 100 + 200 + 1700 + 1900 + 2700 = 6700
\end{align}
$$

Repeating the computation for the remaining candidate values gives the following totals.

| $m$ | $S(m)$ |
|:---:|:---:|
| 1,200 | 7,200 |
| 1,300 | 6,700 |
| 1,400 | 6,400 |
| 1,500 | 6,300 |
| 3,000 | 7,800 |
| 3,200 | 8,400 |
| 4,000 | 12,400 |

The smallest total is $S(1500) = 6300,$ so the value that minimizes the sum of absolute deviations is $1500,$ the same median found with the positional definition.

## Example 2

In the next example the number of observations is even. The table shows the selling prices of six houses recently sold in the same neighborhood:

| House $x_i$ | Price (\$) |
|:---:|:---:|
| $x_1$ | 180,000 |
| $x_2$ | 190,000 |
| $x_3$ | 200,000 |
| $x_4$ | 220,000 |
| $x_5$ | 300,000 |
| $x_6$ | 450,000 |

With $n = 6$ observations, the median is the average of the two central values:

$$\tilde{M} = \frac{x_{\left(\frac{n}{2}\right)} + x_{\left(\frac{n}{2}+1\right)}}{2} = \frac{x_{3} + x_{4}}{2}$$

Substituting the corresponding prices gives:

$$\tilde{M} = \frac{200{,}000 + 220{,}000}{2} = 210{,}000$$

The median house price is \$210,000.

> Half of the houses were sold for less than \$210,000 and half for more.

## Example 3

When data are grouped into frequency classes the individual values are no longer available, and the median is estimated by interpolation within the class that contains it. The following table shows the monthly household electricity consumption in kWh of a group of families, grouped into four classes:

| Class interval (kWh) | Frequency $f_i$ |
|:---:|:---:|
| (100, 200] | 5 |
| (200, 300] | 8 |
| (300, 400] | 12 |
| (400, 500] | 5 |

The total number of observations is:

$$n = \sum f_i = 5 + 8 + 12 + 5 = 30$$

The first step is to locate the class that contains the middle observation. Since $n = 30,$ the middle position is:

$$\frac{n}{2} = \frac{30}{2} = 15$$

We then compute the cumulative frequencies, the progressive totals of observations up to each class, which locate the median class:

| Class interval (kWh) | Frequency $f_i$ | Cumulative frequency |
|:---:|:---:|:---:|
| (100, 200] | 5 | 5 |
| (200, 300] | 8 | 13 |
| (300, 400] | 12 | 25 |
| (400, 500] | 5 | 30 |

The fifteenth observation falls in the class $(300, 400],$ which is therefore the median class. For grouped data, under the assumption that the observations are uniformly distributed within each class, the median is:

$$\tilde{M} = L + \frac{\frac{n}{2} - F}{f_m} \times c$$

In this formula $L$ is the lower boundary of the median class, $F$ is the cumulative frequency of the classes that precede it, $f_m$ is the frequency of the median class, and $c$ is the class width. In our case $L = 300,$ $F = 13,$ $f_m = 12,$ and $c = 100,$ so:

$$\tilde{M} = 300 + \frac{15 - 13}{12} \times 100 = 300 + \frac{2}{12} \times 100 \approx 316.7$$

The estimated median electricity consumption is approximately $317$ kWh.

> This value is an estimate rather than an observed median. The grouped data only guarantee that the median falls in the class $(300, 400],$ and the interpolated figure depends on the uniformity assumed within that class.

## Median and quantiles

The median is a particular case of the quantiles, the statistical measures that divide an ordered distribution into equal parts. It is the quantile that separates the lower 50% of the observations from the upper 50%, and is denoted $x_{0.5}.$

Consider a [real number](../real-numbers/) $p$ with $0 < p < 1.$ The quantile of order $p,$ denoted $x_p,$ is the value that divides the ordered data so that a fraction $p$ of the observations is less than or equal to it and the remaining fraction $1 - p$ is greater.

The quantile $x_p$ also solves a minimization problem. For a candidate value $m,$ each observation contributes the asymmetric deviation:

$$
g(x_i, m) =
\begin{cases}
(1 - p)|x_i - m| & \text{if } x_i \le m \\[6pt]
p|x_i - m| & \text{if } x_i > m
\end{cases}
$$

The quantile is a minimizer of the total loss:

$$x_p \in \arg\min_{m} \sum_{i=1}^{n} g(x_i, m)$$

> For $p = 0.5$ the two weights coincide and the total loss is half the sum of absolute deviations, so this criterion recovers the distance-based definition of the median.

The most common quantiles have their own names.

+ $x_{0.25},$ the first quartile, is the value below which one quarter of the observations lie.
+ $x_{0.50},$ the median, is the value that divides the data into two halves.
+ $x_{0.75},$ the third quartile, is the value below which three quarters of the observations lie.

Deciles and percentiles divide the distribution in the same way into ten and one hundred parts, so the $k$-th percentile is the quantile of order $k/100.$ The interpolation formula of Example 3 also extends from the median to any quantile of grouped data, with the middle position $n/2$ replaced by $np$ and the median class by the class that contains this position.

- - -

The interquantile range is a measure of dispersion, the spread of the central portion of a distribution. Given two orders $p_1$ and $p_2$ with $0 < p_1 < p_2 < 1,$ the interquantile range is the difference between the corresponding quantiles:

$$\mathrm{IQR} = x_{p_2} - x_{p_1}$$

When the two quantiles are the first and third quartiles, that is $p_1 = 0.25$ and $p_2 = 0.75,$ the interquantile range becomes:

$$\mathrm{IQR} = x_{0.75} - x_{0.25}$$

This interval contains the central 50% of the observations. Because it ignores the values in the tails of the distribution, it describes the variability of the data in a way that is robust to outliers.

## Example 4

The table shows the monthly salaries of ten employees of a company:

| $i$ | $x_i$ (Salary in \$) |
|:---:|:---:|
| 1 | 2,200 |
| 2 | 2,400 |
| 3 | 2,600 |
| 4 | 2,700 |
| 5 | 2,800 |
| 6 | 2,900 |
| 7 | 3,100 |
| 8 | 3,300 |
| 9 | 3,400 |
| 10 | 3,700 |

With $n = 10$ observations, the positions of the first and third quartiles are:

$$
\begin{align}
Q_1 &= x_{0.25} = x_{(n+1) \times 0.25} = x_{2.75} \\[6pt]
Q_3 &= x_{0.75} = x_{(n+1) \times 0.75} = x_{8.25}
\end{align}
$$

These positions are fractional ranks, so we interpolate between the neighboring observations. The position $2.75$ lies between the second and third values:

$$x_{0.25} = 2400 + 0.75 \times (2600 - 2400) = 2400 + 150 = 2550$$

The position $8.25$ lies between the eighth and ninth values:

$$x_{0.75} = 3300 + 0.25 \times (3400 - 3300) = 3300 + 25 = 3325$$

The interquantile range between the first and third quartiles is:

$$\mathrm{IQR} = x_{0.75} - x_{0.25} = 3325 - 2550 = 775$$

The interquantile range of the salaries is $775$ dollars.

> The central 50% of the employees have salaries within a range of \$775.
