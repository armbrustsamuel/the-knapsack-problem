# the-knapsack-problem

## Source
https://blog.sicara.com/getting-started-genetic-algorithms-python-tutorial-81ffa1dd72f9

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
