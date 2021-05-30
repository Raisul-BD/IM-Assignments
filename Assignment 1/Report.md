# Report on the Assignment 01
## Functions in Asymptotic Notation
We use asymptotic notation to express the rate of growth of an algorithm's running time in terms of the input size n.

Here we have given 5 functios to find out the best one amongst them.
They are: 
 - Logarithmic = θ(log n)
 - Linear = θ(n)
 - Quadratic = θ(n<sup>2</sup>)
 - Cubic = θ(n<sup>3</sup>)
 - Polynomial = θ(n<sup>k</sup>)

The input values the functions were given as n = 7, k = 4

## Coding Process
1. At first I have created a list from the from the given n range.
2. Then create a dictionary with the lists.
3. Then plotted the values and the Dataframe with the Seaborn library.

The following graph compares the growth of n, log<sub>2</sub> n, n<sup>2</sup>, n<sup>3</sup> and n<sup>k</sup> functions seperately:

![output](https://user-images.githubusercontent.com/76067046/120116802-a2cf6000-c1ab-11eb-9279-f490e82c8fa7.png)

## Interpretation
Logarithms grow more slowly than polynomials. That is, θ(log2 n) grows more slowly than θ(n<sup>a</sup>) for any positive constant a.

So, we can say, here the function n<sup>3</sup> (Cubic) increases faster than that of the other functions.

Cubic is the best one amongst them.
