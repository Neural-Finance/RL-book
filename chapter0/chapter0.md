# Overview {#sec:overview}

## Learning Reinforcement Learning {#sec:learning-rl}

Reinforcement Learning (RL) is emerging as a viable and powerful technique for solving a variety of complex business problems across industries that involve optimal decisioning under uncertainty. Although RL is classified as a branch of Machine Learning (ML), it tends to be viewed and treated quite differently from other branches of ML (Supervised and Unsupervised Learning). Indeed, **RL seems to hold the key to unlocking the promise of AI** – machines that adapt their decisions to vagaries in observed information, while continuously steering towards the optimal outcome. It’s penetration in high-profile problems like self-driving cars, robotics and strategy games points to a future where RL algorithms will have decisioning abilities far superior to humans.

But when it comes getting educated in RL, there seems to be a reluctance to jump right in because it seems to have the image of being mysterious and exotic. Indeed, we have heard even technical people claim that RL involves “advanced math” and “complicated engineering”, and so there seems to be a psychological barrier to entry. While real-world RL algorithms and implementations do get fairly elaborate and complicated in overcoming the proverbial last-mile of business problems, the foundations of RL can actually be learnt without heavy technical machinery. **The core purpose of this book is to demystify RL by finding a balance between depth of understanding and keeping technical content basic**. So now we list the key features of this book which enable this balance:

* Focus on the foundational theory underpinning RL. Our treatment of this theory will be based on undergraduate-level Probability, Optimization, Statistics and Linear Algebra. **We will emphasize rigorous but simple mathematical notations and formulations in developing the theory**, and encourage you to write out the equations rather than just reading from the book. Occasionally, We will invoke some advanced mathematics (eg: Stochastic Calculus) but the majority of the book is based on easily-understandable mathematics. In particular, two basic theory concepts - Bellman Optimality Equation and Generalized Policy Iteration - will be highly emphasized throughout as they form the basis of pretty much everything we do in RL, even in the most advanced algorithms.
* Parallel to the mathematical rigor, we will bring the concepts to life with simple and informal descriptions to help you develop an intuitive understanding of the mathematical concepts. **We will drive towards creating appropriate mental models to visualize the concepts**. Often, this will involve turning mathematical abstractions into physical examples (or physical imaginations). So we will go back and forth between rigor and intuition, between abstractions and visuals, so as to blend them nicely and get the best of both worlds.
* Each time you learn a new mathematical concept or algorithm, we will ask you to write small pieces of code (in Python) that implements the concept/algorithm. As an example, if you just learnt a surprising theorem, we’d ask you to write a simulator to simply verify the statement of the theorem. We emphasize this approach not just to bolster the theoretical and intuitive understanding with a hands-on experience, but also because there is a strong emotional effect of seeing expected results emanating from one’s code, which in turn promotes long-term retention of the concepts. Most importantly, we avoid messy and complicated ML/RL/BigData tools/packages and stick to bare-bones Python/numpy as these unnecessary tools/packages are huge blockages to core understanding and **coding-from-scratch is the only way to truly understand the concepts/algorithms**. 
* Lastly, it is important to work with examples that are A) simplified versions of real-world problems in a business domain rich with applications, B) adequately comprehensible without prior business-domain knowledge, C) intellectually interesting and D) sufficiently marketable to employers. We’ve chosen Financial Trading applications. For each financial problem, we first cover the traditional approaches (including solutions from landmark papers) and then cast the problems in ways that can be solved with RL. **We have made considerable effort to make this book self-contained in terms of the financial knowledge required to navigate these problems**.

## What you'll learn from this Book

Here is what you will specifically learn and gain from the book:

* You will learn about the simple but powerful theory of Markov Decision Processes (MDPs) – a framework for Optimal Decisioning under Uncertainty. You will firmly understand the power of Bellman Equations, which is at the heart of all Dynamic Programming as well as all RL algorithms.
* You will master Dynamic Programming (DP) Algorithms, which are a class of (in the language of AI) Planning Algorithms.  You will learn about Policy Iteration, Value Iteration, Backward Induction, Approximate Dynamic Programming and the all-important concept of Generalized Policy Iteration which lies at the heart of all DP as well as all RL algorithms.
* You will gain a solid understanding of a variety of Reinforcement Learning (RL) Algorithms, starting with the basic algorithms like SARSA and Q-Learning and moving on to several important algorithms that work well in practice, including Gradient Temporal Difference, Deep Q-Network, Least-Squares Policy Iteration, Policy Gradient, Monte-Carlo Tree Search. You will learn about how to gain advantages in these algorithms with bootstrapping, off-policy learning and deep-neural-networks function approximation. You will also learn how to balance exploration and exploitation with Multi-Armed Bandits techniques like Upper Confidence Bounds, Thompson Sampling, Gradient Bandits and Information State-Space algorithms.
* You will exercise with plenty of “from-scratch” Python implementations of models and algorithms. Throughout the book, We will emphasize healthy Python programming practices including interface design, type annotations, functional programming and inheritance-based polymorphism (always ensuring that the programming principles reflect the mathematical principles). The larger take-away from this book will be a rare (and high-in-demand) ability to blend Applied Mathematics concepts with Software Design paradigms.
* You will go deep with important Financial Trading problems, including:

  - (Dynamic) Asset-Allocation to maximize Utility of Consumption
  - Pricing and Hedging of Derivatives in an Incomplete Market
  - Optimal Exercise/Stopping of Path-dependent American Options
  - Optimal Trade Order Execution (managing Price Impact)
  - Optimal Market-Making (Bid/Ask managing Inventory Risk)
 
* We treat each of the above problems as MDPs (i.e., Optimal Decisioning formulations), first going over classical/analytical solutions to these problems, then introducing real-world frictions/considerations, and tackle with DP and/or RL.
* As a bonus, we throw in a few applications beyond Finance, including a couple from Supply-Chain and Clearance Pricing in a Retail business. 
* We implement a wide range of Algorithms and develop various models in [this git code base](https://github.com/TikhonJelvis/RL-book) that we will refer to throughout the book. This code base not only provides detailed clarity on the algorithms/models, but also serves to educate on healthy programming patterns suitable not just for RL, but more generally for any Applied Mathematics work.
* In summary, this book blends Theory/Mathematics, Programming/Algorithms and Real-World Financial Nuances while always keeping things simple and intuitive.

## Expected Background to read this Book

There is no short-cut to learning Reinforcement Learning or learning the Financial Applications content. You will need to allocate at least 50 hours of effort to learn this material. Also, although we have kept the Mathematics, Programming and Financial content fairly basic, this topic is only for technically-inclined readers. So what is the technical preparation required to follow the material in this book?

* Experience with (but not expertise in) Python is expected and a good deal of comfort with numpy is required. The type of Python programming we will do is mainly numerical algorithms. You don’t need to be a professional software developer/engineer but you need to have a healthy interest in learning Python best practices associated with mathematical modeling, algorithms development and numerical programming (we will teach those best practices in this book). We won’t be using any of the popular (but messy and complicated) Big data/ML libraries such as Pandas, PySpark, scikit, Tensorflow, PyTorch, OpenCV, NLTK etc. (all you need to know is numpy).
* Familiarity with git and use of an Integrated Development Environment (IDE), eg: Pycharm, is recommended, but not required.
* Familiarity with LaTeX for writing equations is recommended, but not required (other typesetting tools, or even hand-written math is fine, but LaTeX is a skill that is very valuable if you’d like a future in the space of Applied Mathematics).
* You need to be strong in undergraduate-level Probability as it is the most important foundation underpinning RL. 
* You will also need to have some preparation in undergraduate-level Numerical Optimization, Statistics, Linear Algebra.
* No background in Finance is required, but a strong appetite for Mathematical Finance is required.

## Overview of Chapters

### Section I: Planning Algorithms (Dynamic Programming)

#### Chapter 0: Overview

* What this book is about and how best to learn this topic
* Decluttering the jargon in Optimal Decisioning under Uncertainty
* Introduction to the Markov Decision Process (MDP) framework
* Examples of important real-world problems that fit the MDP framework
* The inherent difficulty in solving MDPs
* Overview of Value Function, Bellman Equation, Dynamic Programming and Reinforcement Learning
* Why is RL useful/interesting to learn about?
* Many faces of RL and where it lies in the classification of ML
* Outline of chapters in the book
* Overview of the 5 Financial Applications
 
This is an introductory/overview chapter familiarizing the reader with the general space of optimal decisioning under uncertainty, the framework used to tackle such problems, and a high-level overview of the techniques/algorithms (Dynamic Programming and Reinforcement Learning). The reader will also get an overview of the range of business problems that can be targeted and the intuitive difficulty in tackling these problems. Finally, the reader will be familiarized with the flow of chapters (with a study plan for different levels of background and different levels of time investment) and will be introduced to the 5 important Financial applications that will be covered in this book. This chapter starts with an articulation of the approach we take in this book to explain RL: Mathematics/Theory, Intuition, Programming, Financial Applications.

#### Chapter 1: Best Practices in Python for Applied Mathematics

* Type Annotations
* List and Dict Comprehensions
* Functional Programming – lambdas and higher-order functions
* Class inheritance and Abstract Base Classes
* Generics Programming
* Generators
 
Given this book’s emphasis on “learning by programming”, this chapter will familiarize the reader with some core techniques in Python that will be very important in implementing models and algorithms. To be clear, this chapter is not a full Python tutorial – the reader is expected to have some background in Python already. It is a tutorial of some key techniques and practices in Python (that many readers might not be accustomed to) that are highly relevant to programming in the broader area of Applied Mathematics. As part of this chapter, the reader will do some exercises with these techniques/practices in Python and will emerge prepared to learn the material of this book with appropriate Python paradigms.

#### Chapter 2: Markov Processes and Markov Reward Processes

* The Markov Property (illustrated with a stock price example)
* Markov Processes (MPs)
* Finite Markov Processes
* Markov Reward Processes (MRPs)
* Finite Markov Reward Processes
* MRP Value Function
* MRP Bellman Equation

This chapter covers the foundational topics required to understand Markov Decision Processes - The Markov property, Markov Processes (sometimes refered to as Markov Chains), Markov Reward Processes, the concept of Value Function of a Markov Reward Process, and the Bellman Equation for a Markov Reward Process. These concepts are motivated with examples of stock prices and with a simple inventory example that serves first as a Markov Process and then as a Markov Reward Process. There will be a significant amount of programming in this chapter to develop comfort with these concepts.

#### Chapter 3: Markov Decision Processes

* Markov Decision Processes (MDPs)
* The relationship between MDPs and MRPs
* MDP Value Function for a Given Policy
* Bellman Expectation Equations
* MDP Optimal Value Function and Optimal Policy
* Bellman Optimality Equations
* Proof of Existence of Optimal Policy achieving Optimal Value Function
* Variants and Extensions of MDPs

This chapter lays the foundational theory underpinning RL – the framework for representing problems dealing with optimal decisioning under uncertainty (Markov Decision Process). The reader will learn about the relationship between Markov Decision Processes and Markov Reward Processes, the Value Function (key ingredient in RL algorithms) and the Bellman Equations (a powerful property, which enables solving complex decisioning problems). There will be a considerable amount of programming exercises in this chapter. The heavy investment in this theory together with hands-on programming will put the reader in a highly advantaged position to learn the following chapters in a very clear and speedy manner.

#### Chapter 4: Dynamic Programming (DP)

* DP as a form of Planning
* Solving the Value Function as a Fixed-Point
* Policy Evaluation Algorithm
* Policy Improvement
* Policy Iteration (PI) Algorithm
* Value Iteration (VI) Algorithm
* Optimal Policy From Optimal Value Function
* Generalized Policy Iteration (GPI)
* Asynchronous Dynamic Programming
* Backward Induction

This chapter covers the Planning technique of Dynamic Programming (DP), which is an important class of foundational algorithms that can be an alternative to RL if the business problem is not too large or too complex. Also, learning these algorithms will provide important foundations to the reader to be able to understand subsequent RL algorithms more deeply. The reader will learn about several important DP algorithms and at the end of the chapter, the reader will learn about why DP gets difficult in practice which draws the reader to the motivation behind RL. Again, we will do plenty of DP algorithms, which are quick to implement and will aid considerably in internalizing the concepts. Finally, we emphasize a special algorithm - Backward Induction - for solving finite-horizon Markov Decision Processes, which is the setting for the financial applications we cover in this book.

#### Chapter 5: Function Approximation and Approximate Dynamic Programming

* Curse of Dimensionality & Function Approximation as a Cure
* Linear Function Approximation
* Deep Neural Networks
* Tabular as a special case of Linear Function Approximation
* Approximate Dynamic Programming (ADP)

The Dynamic Programming algorithms covered in the previous chapter suffer from the two so-called curses: Curse of Dimensionality and Curse of Modeling. These curses can be cured with a combination of sampling and function approximation. The next section covers the sampling cure (using Reinforcement Learning). This chapter covers the topic of function approximation and shows how an intermediate cure - Approximate Dynamic Programming (function approximation without sampling) - is quite viable and can be suitable for some problems.

### Section II: Modeling Financial Applications

#### Chapter 6: Utility Theory for Risk-Aversion

* Risk-Aversion and Risk-Premium
* Utility of Consumption
* Absolute and Relative Risk-Aversion
* Constant Absolute Risk-Aversion
* Constant Relative Risk-Aversion

Having learnt DP algorithms and before learning RL algorithms, the reader will learn about the 5 financial applications. For each of the financial applications, we will go over the core financial background and concepts within these applications, then learn how to solve them with DP, then introduce real-world considerations and finally explain why tackling those considerations requires RL. Later, we will revisit these financial problems when we cover RL algorithms (in the 2nd half of the book). But before we get into each of the 5 financial applications, readers need to get familiar with the key economics concept of risk-aversion that applies to 4 of the 5 financial applications. So this chapter is dedicated to risk-aversion and the related concepts of risk-premium and Utility functions. As ever, we will write plenty of code in this chapter to understand these concepts thoroughly.

#### Chapter 7: Dynamic Asset Allocation (Portfolio Optimization) 

* Merton’s Portfolio problem and solution
* Discrete Portfolio Optimization example
* Real-world considerations
* References

This chapter cover the first financial application – dynamic asset allocation (part of the larger space of Portfolio Optimization). This problem is best understood in the context of Merton’s landmark paper in 1969 where he stated and solved this problem. This chapter is mainly focused on the mathematical derivation of Merton’s solution of this problem with Dynamic Programming. Through this derivation, the reader will learn about the broader result called Hamilton-Jacobi-Bellman (HJB) equation, which will re-appear in the Market-Making problem in Chapter 10. As ever, we will do some programming exercises. In particular, the reader will learn how to solve Dynamic Asset Allocation in a simple setting with Backward Induction (a DP algorithm we learnt in Chapter 3). Finally, the reader will learn about Dynamic Asset Allocation in practice, where Merton’s frictionless setting is replaced by several real-world frictions, which will require us to move to RL. We will revisit this problem after coverage of RL algorithms in the second half of the book.

#### Chapter 8: Pricing and Hedging of Derivatives in an Incomplete Market

* Classical Pricing and Hedging of Derivatives
* Pricing and Hedging in an Incomplete Market
* Modeling Optimal Hedging as an MDP
* The Principle of Indifference Pricing
* Deep Reinforcement Learning as a practical alternative to traditional approaches
* References

Perhaps the greatest innovation in Financial Trading is the structuring of complex options and other forms of financial derivatives, and pricing/risk-managing them. In this chapter, the reader is first familiarized with the key concepts of arbitrage, hedging and consequent pricing of options/derivatives based on these concepts. This forms the basis of classical pricing and hedging methods for derivatives. However, traders have consistently struggled with incorporating real-world frictions in these classical solutions, and the friction overlays have always felt with inconsistent and incorrect “hacks”. The reader will then be familiarized with a radically different way to price and hedge derivatives amidst real-world frictions – by modeling this problem as an MDP. We will revisit this problem after we learn the RL algorithms because the only practical way of solving this problem in the real-world is by designing a market-calibrated simulator and then employing RL algorithms on this simulator. As ever, we will write some code to develop a firm grasp of pricing and hedging derivatives.

#### Chapter 9: American Options Pricing

* Stopping Time and Optimal Stopping problem
* Optimal Stopping problem as an MDP
* Mainstream approaches to American Options Pricing
* The Longstaff-Schwartz algorithm
* RL as an alternative to Longstaff-Schwartz
* LSPI and FQI customized to American Options Pricing

This chapter covers Financial Application 3 – Pricing history-dependent American options. The reader will be familiarized with the more general problem of optimal stopping time and how it can be modeled as an MDP. The reader will then learn how American Options Pricing is a special case of the more general Optimal Stopping Time problem. The reader will learn how to use Backward Induction (a DP algorithm we learnt in Chapter 3) to solve this problem when the state-space is not too big. The reader will also learn about a very creative technique developed by Longstaff and Schwartz (a sort of hybrid between DP and RL techniques), which is very popular in the finance industry. We will return to this problem in chapter 14 after we have learnt about LSPI (an important RL algorithm that can be used to tackle this problem more efficiently than the popular Longstaff-Schwartz method). As ever, we will write plenty of code in this chapter, including Backward Induction and Longstaff-Schwartz algorithm. By the end of this chapter, the reader would have developed significant expertise in pricing and hedging complex derivatives, a skill that is in high demand in the finance industry.

#### Chapter 10:  Optimal Trade Order Execution

* Basics of Limit Order Books (LOB)
* Price Impact and LOB Dynamics
* Problem Statement and MDP Formulation
* Simple Linear Impact Model with no Risk-Aversion
* Incorporating Risk-Aversion and Real-World Considerations
* References

This chapter introduces the reader to the world of Algorithmic Trading. However, current Algorithms tend to be rules-based and heuristic. Algorithmic Trading is transforming into Machine Learning-based Algorithms. The natural extension is to automate not just forecasting but also decisioning, the realm of Reinforcement Learning. In this chapter, the reader is first introduced to the mechanics of trade order placements (market orders and limit orders), and then introduced to a very important real-world problem – how to submit a large-sized market order by splitting and timing the splits optimally in order to overcome “price impact” and gain maximum proceeds. The reader will learn about the classical methods based on Dynamic Programming. Then the reader will learn about market frictions and the need to tackle them with RL. We will return to this problem in the second half of the book after we have learnt some RL algorithms.

#### Chapter 11: Optimal Market-Making

* Market-Making on a Limit Order Book
* Problem Statement and MDP Formulation
* Avellaneda-Stoikov Continuous-time Formulation
* Solving the Avellaneda-Stoikov formulation
* Real-world Market-Making
* References

This chapter is about the Algorithmic Trading twin of the previous problem – that of a market-maker having to submit dynamically-changing bid and ask limit orders so she can make maximum gains. The reader will learn about how market-makers (a big and thriving industry) operate. Then the reader will learn about how to formulate this problem as an MDP. The majority of this chapter will be spent on the classical Dynamic Programming solution by Avellaneda and Stoikov, together with some programming exercises to absorb those concepts. Finally, the reader is exposed to the real-world nuances of this problem, and hence, the need to tackle with a market-calibrated simulator and RL.  We will return to this problem in the second half of the book after we have learnt some RL algorithms.

### Section III: Reinforcement Learning Algorithms

#### Chapter 12: Tabular Monte-Carlo & Temporal Difference for Prediction

* Tabular Monte-Carlo (MC) Policy Evaluation
* Tabular Temporal-Difference (TD) Policy Evaluation
* Estimate adjustments in a soccer game (MC versus TD)
* Bias-Variances Tradeoff and other contrasts between MC and TD
* Some simple examples
* Wide versus sample backups, Deep versus shallow backups
* TD(lambda)
* Eligibility Traces

This chapter starts a new phase in this book, our entry into the world of RL algorithms. To understand the basics of RL, in this chapter, I restrict the RL problem to a very simple one – one where the state space is small and manageable as a table enumeration (known as tabular RL) and one where we only have to calculate the Value Function for a Fixed Policy (this problem is known as the Prediction problem, versus the optimization problem which is known as the Control problem). So this chapter is about RL for Tabular Prediction. This restriction is important because it makes it much easier to understand the core concepts of Monte-Carlo (MC) and Temporal-Difference (TD) in this simplified setting. The remaining chapters will build upon this chapter by adding more complexity and more nuances, while retaining much of the key core concepts developed in this chapter. As ever, the reader will learn by coding plenty of MC and TD algorithms from scratch.

#### Chapter 13: Tabular Monte-Carlo & Temporal Difference for Control

* Making MC work with GPI: Action-Value Function and Epsilon-Greedy
* GLIE Monte-Carlo Control
* SARSA
* Off-Policy Learning: Importance Sampling
* Off-Policy Learning: Q-Learning

This chapter makes the natural extension from Prediction to Control, while remaining in the tabular setting. The investments made in the previous chapter will bear fruit here as important algorithms such as SARSA and Q-learning can now be learnt with enormous clarity. In this chapter, the reader will implement both SARSA and Q-Learning from scratch in Python. This chapter also introduces the reader to a very important concept for the future success of RL in the real-world: off-policy learning (Q-Learning is the simplest off-policy learning algorithm and it has had good success in various applications).

#### Chapter 14: Monte-Carlo and Temporal Difference with Function Approximation

* Value Function Approximation
* A quick review of Deep Neural Networks and Stochastic Gradient Descent
* Linear Value Function Approximation
* MC and TD Prediction with Value Function Approximation
* MC and TD Control with Action-Value Function Approximation
* Convergence of Prediction and Control Algorithms
 
In this chapter, the reader will learn how to scale the RL algorithms learnt in chapters 11 and 12 to real-world situations where the state space is large and consequently require approximate representations of the Value Function, eg: using Deep Neural Networks. The reader will gain an appreciation of how RL and Neural Networks technology are complementary and together they can surmount real-world challenges. The reader will also learn about intricate choices of how much to bootstrap, and whether to do on-policy or off-policy learning when doing function approximation.

#### Chapter 15: Batch RL

* Experience Replay
* Deep Q-Networks (DQN)
* Least-Squares MC and TD
* Least-Squares Policy Iteration (LSPI) 

In this chapter, the reader will learn about a different class of RL algorithms that are data-efficient. These batch algorithms such as Experience Replay, Deep Q-networks and Least Squares Policy Iteration are state-of-the-art and have had a lot of success in practice. The reader will also explore these algorithms in the context of the Financial Applications that were previously covered.

#### Chapter 16: Value Function Geometry and Gradient TD

* Motivation for Value Function Geometry
* Bellman Operator and Projection Operator
* Value Function Vectors of interest
* Residual Gradient Algorithm
* Naïve Residual Gradient Algorithm
* Gradient TD Algorithm

This chapter is heavier on Theory relative to other chapters. The motivation for this chapter is to develop deeper insights into the core mathematics underpinning RL algorithms (back to the basics of Bellman Equation). Understanding Value Function Geometry will place the reader in a highly advantaged situation in terms of truly understanding what is it that makes some Algorithms succeed in certain situations and other than don’t. This chapter also shows the reader how to break out of the so-called Deadly Traid (when bootstrapping, function approximation and off-policy are employed together, RL algorithms tend to fail). The state-of-the-art Gradient TD Algorithm resist the deadly triad and we dive deep into its inner workings to understand how and why.

#### Chapter 17: Policy Gradient Algorithms

* Policy Improvement with Gradient Ascent
* Expected-Returns Objective and Policy Gradient Theorem (PGT)
* Simple parametric representations for Policies
* Proof of Policy Gradient Theorem
* The REINFORCE Algorithm
* Variance Reduction
* Compatible Function Approximation Theorem
* Natural Policy Gradient
* Deterministic Policy Gradient
* Evolutionary Strategies

In this chapter, the reader will be exposed to yet another class of RL algorithms that are based on improving the policy using the gradient of the policy function approximation (rather than the usual policy improvement based on argmax). When action spaces are large or continuous, Policy Gradient tends to be the only option and so, this chapter is useful to overcome many real-world situations (including many financial applications) where the action space is indeed large. The reader will learn about the mathematical proof of the elegant Policy Gradient Theorem and implement a couple of Policy Gradient Algorithms from scratch. The reader will learn about state-of-the-art Actor-Critic methods. Lastly, the reader will also learn about Evolutionary Strategies, an algorithm that looks quite similar to Policy Gradient Algorithms, but is actually not classified as an RL Algorithm. However, learning about Evolutionary Strategies is important because some real-world applications, including Financial Applications can indeed be tackled well with Evolutionary Strategies.

#### Chapter 18: Learning versus Planning

* Model-based RL
* Learning a Model
* Sample-based Planning
* Planning with Inaccurate Models
* Integrating Learning and Planning
* Simulation-based Search
* Monte-Carlo Tree Search
* Adaptive Multistage Sampling

This chapter brings the various pieces of Planning and Learning concepts learnt in this book together. The reader will learn that in practice, one needs to be creative about blending planning and learning concepts (a technique known as Model-based RL). In practice, many problems are tackled using Model-based RL. The reader will also get familiar with an algorithm (Monte Carlo Tree Search) that was highly popularized when it solved the Game of GO, a problem that was thought to be unsurmountable by present AI technology.

#### Chapter 19: Exploration versus Exploitation

* The Multi-Armed Bandit (MAB) Problem
* Regret Analysis
* Simple Algorithms for MAB
* Lai-Robbins lower bound
* Hoeffding’s Inequality and Upper-Confidence Bound (UCB) Algorithm
* Probability Matching and Thompson Sampling
* Gradient Bandit Algorithms
* Information State-Space Algorithms
* Contextual Bandits
* Exploration versus Exploitation in MDPs

This chapter enables the reader to deep-dive into the topic of balancing exploration and exploitation, a topic of great importance in RL algorithms. Exploration versus Exploitation is best understood in the simpler setting of the Multi-Armed Bandit (MAB) problem. The reader will learn about various state-of-the-art MAB algorithms, implement them in Python, and draw various graphs to understand how they perform versus each other in various problem settings. The reader will then be exposed to Contextual Bandits which are a popular technique in optimal choices of Advertisement placements. Finally, the reader will learn how to apply the MAB algorithms within RL.

#### Chapter 20: RL in Real-World Finance: Reality versus Hype, Present versus Future

This concluding chapter will enable the reader to put the entire book’s content in perspective relative to the current state of the financial industry, the practical challenges in adoption of RL, and some guidance on how to go about building an end-to-end system for financial applications based on RL. The reader will be guided on reality versus hype in the current “AI First” landscape. The reader will also gain a perspective of where RL stands today and what the future holds.

### Appendices

1. Moment-Generating Function and it's Applications
2. Portfolio Theory
3. Introduction To and Overview Of Stochastic Calculus Basics
4. The Hamilton-Jacobi-Bellman (HJB) Equation
5. Fundamental Theorems of Asset-Pricing: No-Arbitrage and Complete Markets
6. Black-Scholes Theory
