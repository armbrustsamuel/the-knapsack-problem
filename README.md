# the-knapsack-problem

## Source
https://blog.sicara.com/getting-started-genetic-algorithms-python-tutorial-81ffa1dd72f9

[Github] (https://gist.github.com/NicolleLouis/d4f88d5bd566298d4279bcb69934f51d)

## The Knapsack problem
The backpack optimization is a classical algorithm problem. You have two things: a backpack with a size (the weight it can hold) and a set of boxes with different weights and different values. The goal is to fill the bag to make it as valuable as possible without exceeding the maximum weight. It is a famous mathematical problem since 1972. The genetic algorithm is well suited to solve that because it’s an optimization problem with a lot of possible solutions.

Other algorithms aren’t efficient at all, see the [Wikipedia](https://en.wikipedia.org/wiki/Karp%27s_21_NP-complete_problems) page if you want to understand why.

## Instructions
The algorithm is implemented on `Python 3`. You can download it here for Windows, or install it using brew install python3 , sudo apt-get install python3 or sudo yum install python3 . I advise you to run this code inside a Jupyter notebook.

## Fitness Function
The evaluation function is the `first step` to create a genetic algorithm. It’s the function that `estimates the success of our specimen`: it will allow us to divide the population `between the ugly duckling and the beautiful swans`. The goal of this separation is that, later, the successful specimen will have more “chance” to get picked to form the next generation. As simple as it appears, don’t be fooled, it’s the step of a genetic algorithm with the more intelligence related to the problem.

## Goal 1
What is our goal? `Crack a password`. Thus the goal of our function is to transform the binary result “fail or success” in a continuous mark from 0 (can’t fail more) to 100 (perfection).

```
fitness score = (number of char correct) / (total number of char)
```

## Individuals

In our case, our individuals are going to be words (obviously of equal length with the password). Each letter is a gene and the value of the letter is the allele. In the word “banana”: `b` is the `allele` of the first letter.

What is the point of this creation?

We know that each of our individuals is keeping the good shape (a word with the correct size)
Our population can cover every possibility (every word possible with this size).

## First Population
The main idea to keep in mind when we create the first population is that we must not point the population towards a solution that seems good. We must make the population as wide as possible and make it cover as many possibilities as possible. The perfect first population of a genetic algorithm should cover every existing allele.

# From one generation to the next
Given a generation, in order to create the next one, we have 2 things to do. First we select a specific part of our current generation. Then the genetic algorithm combines those breeders in order to create the next batch.

# Mutation
This last step of our genetic algorithm is the natural mutation of an individual. After the breeding, each individual must have a small probability to see their DNA change a little bit. The goal of this operation is to prevent the algorithm to be blocked in a local minimum.
