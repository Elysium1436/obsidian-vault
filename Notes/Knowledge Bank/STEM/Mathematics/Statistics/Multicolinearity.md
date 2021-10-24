## Multicolinearity

In statistics, multicolinearity is a phenomenon where one or more predictor variable can be explained by the other predictor variables with a substantial degree of accuracy. This phenomenon can only take place in regard of the data, not the model.

In terms of regression analys
$$

$$






#### On-going question
- What are the effects of mutlicolinearity in statistical models?
	- Answers
	- ---
	-  The [[Coefficient Estimates]] may change erratically with small changes to the model or data. 
	-  It does not affect or reduce the predictive power of the model, nor it's reliability, but it won't give valid results with regard to any individual predictor, or which predictors are redundant.
- What is an effective way to find colinear variables, and which one should you eliminate?
	- Suppositions
	-  ---
	- Of course, you can eliminate the one that produces the best metric in the test set, but that seems expensive. You still don't know which one is actually colinear with respect to other
	- You can try to make a regression model using only the predictor variables. But that seems rather expensive and inneficient. There should 
