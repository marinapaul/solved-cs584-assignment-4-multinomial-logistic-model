Download Link: https://assignmentchef.com/product/solved-cs584-assignment-4-multinomial-logistic-model
<br>
Assignment 4

In 2014, Allstate provided the data on Kaggle.com for the Allstate Purchase Prediction Challenge which is open.  The data contain transaction history for customers that ended up purchasing a policy. For each Customer ID, you are given their quote history and the coverage options they purchased.

The data is available on the Blackboard as Purchase_Likelihood.csv.

<ol>

 <li>It contains 665,249 observations on 97,009 unique Customer ID.</li>

 <li>The nominal target variable is insurance which has these categories 0, 1, and 2</li>

 <li>The nominal features are (categories are inside the parentheses):

  <ol>

   <li>group_size. How many people will be covered under the policy (1, 2, 3 or 4)?</li>

   <li>homeowner. Whether the customer owns a home or not (0 = No, 1 = Yes)?</li>

   <li>married_couple. Does the customer group contain a married couple (0 = No, 1 = Yes)?</li>

  </ol></li>

</ol>

Question 1 (35 points)

You will build a multinomial logistic model with the following model specifications.

<ol>

 <li>Enter the six effects to the model in this sequence:

  <ol>

   <li>group_size</li>

   <li>homeowner</li>

   <li>married_couple</li>

   <li>group_size * homeowner</li>

   <li>group_size * married_couple</li>

   <li>homeowner * married_couple</li>

  </ol></li>

 <li>Include the Intercept term in the model</li>

 <li>The optimization method is Newton 4. The maximum number of iterations is 100</li>

 <li>The tolerance level is 1e-8.</li>

 <li>Use the sympy.Matrix().rref() method to identify the non-aliased parameterS</li>

</ol>

Please answer the following questions based on your model.

a.(5 points) List the aliased columns that you found in your model matrix.

b.(5 points) How many degrees of freedom does your model have?

c.(20 points) After entering each model effect, calculate the Deviance test statistic, its degrees of freedom, and its significance value between the current model and the previous model. List your Deviance test results by the model effects in a table.

d.(5 points) Calculate the Feature Importance Index as the negative base-10 logarithm of the significance value. List your indices by the model effects.

Question 2

Please answer the following questions based on your multinomial logistic model in Question 1.

a.(10 points) For each of the sixteen possible value combinations of the three features, calculate the predicted probabilities for insurance = 0, 1, 2 based on your multinomial logistic model. List your answers in a table with proper labeling

b. (5 points) Based on your answers in (a), what value combination of group_size, homeowner, and married_couple will maximize the odds value Prob(insurance = 1) / Prob(insurance = 0)? What is that maximum odd value?

c.  Based on your model, what is the odds ratio for group_size = 3 versus group_size = 1, and insurance = 2 versus insurance = 0?(<em>Hint</em>: The odds ratio is this odds (Prob(insurance = 2) / Prob(insurance = 0) | group_size = 3) divided by this odds ((Prob(insurance = 2) / Prob(insurance = 0) | group_size = 1).)

d.Based on your model, what is the odds ratio for homeowner = 1 versus homeowner = 0, and insurance = 0 versus insurance = 1?

Question 3 (40 points)

You will build a Naïve Bayes model without any smoothing.  In other words, the Laplace/Lidstone alpha is zero.  Please answer the following questions based on your model.

a. Show in a table the frequency counts and the Class Probabilities of the target variable.

b.  Show the crosstabulation table of the target variable by the feature group_size.  The table contains the frequency counts.

c. Show the crosstabulation table of the target variable by the feature homeowner. The table contains the frequency counts.

d. Show the crosstabulation table of the target variable by the feature married_couple.

The table contains the frequency counts

e.  Calculate the Cramer’s V statistics for the above three crosstabulations tables.  Based on these Cramer’s V statistics, which feature has the largest association with the target insurance?

f.  For each of the sixteen possible value combinations of the three features, calculate the predicted probabilities for insurance = 0, 1, 2 based on the Naïve Bayes model.  List your answers in a table with proper labeling.

g.Based on your model, what value combination of group_size, homeowner, and married_couple will maximize the odds value Prob(insurance = 1) / Prob(insurance = 0)? What is that maximum odd value?