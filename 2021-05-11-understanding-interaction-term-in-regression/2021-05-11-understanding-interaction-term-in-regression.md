---
layout: post
title: Understanding Interaction Term in regression
description: short introduction on random variables and binomial distribution.
summary: short introduction on random variables and binomial distribution.
usemathjax: true
tags: [probability]
---

Linear regression has been the simplest way to understand how the linear combination of our independent variable can infer or predict our dependent variable. 

<span style="color:red">This is Red Bold</span>


Playing an important role in this are the interaction terms, which are often hard to interpretate as they made the relationship complicated. Let’s take an example of the student performance dataset and run a regression where our dependent variable is final grade and independent variables are age(X_a) and gender(X_g). 

Interaction terms provides flexibility to our linear models, so that the different independent variables can have different effect on the dependent variable. 

We model our equation as, $$y = b_0 + b_1*X_a + b_2*X_g \\ => y =140 + 20X_a + 2X_g$$ after finding out the coefficients. 

Let’s say we want to find our final grade when the student is male (X_g = 1) or female (X_g = 0). Plugging this in our regression equation, we get 

$$Y = b_0 + b_1*(X_a) + b_2*(1)$$		$$Y = b_0 + b_1*(X_a) + b_2*(0) $$

$$Y = 140 + 20*X_a + 2	|	Y = 140 + 20*X_a $$

$$Y = 142 + 20*X_a $$

What this means geometrically – For every year, in age the score gets increased by 20 for both male and female candidates – because of same slope (regression lines are parallel). In short, we are forcing our regression to have same slope. 

After adding an interation term $$X_I = X_a*X_g$$ to our regression model we get, 

$$Y = b_0 + b_1*(X_a) + b_2*(X_g) + b_3*(X_I) $$

 

Again, for male and female students 

$$Y = b_0 + b_1*(X_a) + b_2*(1) + b_3(Xa*1)$$	$$Y = b_0 + b_1*(X_a) + b_2*(0) + b_3*(X_a * 0) $$

$$Y = b_0 + b_1*(X_a) + b_2*(1) + b_3(X_a)$$		$$Y = b_0 + b_1*(X_a) + b_2*(0) $$

$$Y =(b_0 + b_2) + (b_1 + b_3)*X_a$$		$$Y = b_0 + b_1*(X_a) $$

What this means geometrically, we don't have same slope for male and female students anymore. Moreover, we can interpret 

$$B_0$$ as y intercept (when age is 0) 

$$B_1$$ as diff in intercept of two groups 

$$B_2$$ as slope for male 

$$B_3$$ as diff in slopes of male and female 