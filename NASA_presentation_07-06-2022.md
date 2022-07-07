# GA-based Optimisation for Path Planning
Iulia Iordanescu

NASA Virtual Volunteer VIP 
Aviation Systems Division

## End Goal

By Monday, August 1,  we should have a function/program that computes the optimum trajectory path for certain coordinates. For example, give it coordinates that form a decagon and record the path it comes up with at the start as a drawing (which is highly unlikely to be optimum as it is random) and also record the path it comes up with at the end (which should be optimum or close to optimum) as a drawing. Let’s see what that might look like!
As mentioned, at first, our program will make a path that is likely not going to be optimum because it’s random, like the path you see here. You can see intuitively that a lot more distance is being covered than necessary. In our problem, we also need to have the drone come back where it started (repped by purple line).
Our goal is for our program to come up with this drawing at the end, which is optimum (covers the least amount of distance). You can compute the distance using GA.

## GA Summary
Genetic algorithms are a type of optimization algorithm (they’re used to find  the maximum or minimum of a function),  inspired by Charles Darwin’s theory of natural evolution. 
They have 5  basic components:
* population initialization
* fitness function
* selection
* crossover
* mutation
Every generation you go through the last four steps

### GA Summary: Pop. Initialization
* generate a set of permutations (AKA  solutions or chromosomes) from your sites, which represent a path
* two variations: 
random
heuristic (you choose the permutations specifically based on a hunch)

### GA summary:  Fitness Function
* determines how fit an individual is (the ability of an individual to compete with other individuals)
* probability that an individual will be selected for reproduction is based on its fitness score
  * fitness score of a solution = total travelled distance of the solution
    * the smaller the total distance, the fitter the solution

### GA summary:  Selection
* select the fittest individuals and let them pass their genes to the next generation; survival of the fittest
* two pairs of individuals (parents) are selected based on their fitness scores
  * individuals with high fitness have more chance to be selected for reproduction
* three variations of many: Roulette Wheel method, the Rank method, and the Tournament Size

### GA summary: Crossover
* 2 parents from the selection function “mate” during crossover, to make a “child” (a new permutation)
* many variations:  Order 1, Cycle, Partially mapped, Order Multiple and Insertion

### GA summary: Mutation
* in certain new offspring formed, some of their genes can be subjected to a mutation with a low random probability
  * essence: some genes exchange places
* occurs to maintain diversity within the population and prevent premature convergence (gives a suboptimal solution)
* variations: swap, scramble, insert, reverse


## Genetic Algorithm driven Path Planning

This is the outline I’m thinking of, on how we can work together to cover individual GA steps:
* introduction: what is GA? 
* initialization
* fitness function
* selection
* crossover
* mutation

I recommend using a tutorial before we start covering the GA step of choice. There is a repo at the end if you would like to try to implement it.
Working on manageable pieces of GA independently will not only help us move faster to our goal but will make us experts in a certain area of our project allowing us to learn from one another. I highly recommend using this tutorial to start you off on your piece of the presentation. Using the tutorial, you will see that there are many variations for each piece which you should not only validate in your research but should also extend to find more and seek out the best one for our problem. Learning what’s happening from scratch helps build understanding, but eventually we should/ will learn how to use actual libraries using GA to find a better solution.

## Timeline
### Wednesday, July 13: 
* understanding a step in GA + decide a test data:  a test input, and an expected output
* each of us should try to  master a GA chunk of choice by this meeting 
* we should think of the test data which should cover what i said in the beginning slides
* please make sure your work is in mural for easy access!
* goal is to help each other by asking questions and meeting regularly

### Wednesday, July 20: 
* have the implementation ready and make sure it runs correctly on your test data 

### Wednesday, July 27: put everything together
* make sure everything works together end to end (every function does its own job) , we do this by running it on the test data 

### Sunday, July 31: 
* create animation
* finalize report (motivation, problem statement, algorithm, results)


### Before presenting our project:
* demo and report done

## Github Repo
I created this repo (https://github.com/iulia-iordanescu/NASA_VIP_interns).

If you guys are open to using it, we should each use a branch named “vip_user/yourname” 
Please feel free to send me your github username so that I can invite you to work on the repository. You can also clone/fork it on your own.

## Collaborating
I think it would benefit both your project and the work that will be done for GA if we combine them together. If you have an optimisation problem in your work that can be solved using GA, let’s talk and see how we can leverage each other’s work. Your work will be more coherent and the GA work will also benefit from your insight.







