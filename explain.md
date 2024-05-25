To teach logistic regression using the provided case study effectively, it is crucial to include all the necessary mathematical equations and provide intuition for each step. Below, I will explain how to find the intercept (β0) and the coefficient (β1) from your case study, connecting them to the equations and providing detailed explanations.

### Step-by-Step Explanation with Equations

#### 1. Logistic Regression Equation
The logistic regression model can be represented by the following equation:

\[
\log\left(\frac{p}{1-p}\right) = β0 + β1 \cdot X
\]

Where:
- \( p \) is the probability of unsubscription.
- \( X \) is the number of emails per week.
- \( β0 \) is the intercept.
- \( β1 \) is the coefficient for the number of emails per week.

#### 2. Transforming Log-Odds to Probability
To convert the log-odds to a probability, we use the logistic function:

\[
p = \frac{1}{1 + e^{-(β0 + β1 \cdot X)}}
\]

#### 3. Interpreting the Intercept (β0)
The intercept (β0) represents the log-odds of the outcome (unsubscription) when the predictor variable (emails per week) is zero.

\[
\log\left(\frac{p}{1-p}\right) = β0 \text{ when } X = 0
\]

In your case study:
- **β0 = -21.96**: This indicates that when no emails are sent per week, the log-odds of unsubscription are -21.96. Since this is a very large negative number, it implies a very low probability of unsubscription when no emails are sent.

#### 4. Interpreting the Coefficient (β1)
The coefficient (β1) represents the change in the log-odds of the outcome for a one-unit increase in the predictor variable (emails per week).

\[
\log\left(\frac{p}{1-p}\right) = β0 + β1 \cdot X
\]

In your case study:
- **β1 = 2.52**: This indicates that for each additional email sent per week, the log-odds of unsubscription increase by 2.52. This means more emails per week significantly increase the probability of unsubscription.

#### 5. Probability Calculation Example
Using the given values for β0 and β1, let's calculate the probability of unsubscription for a specific number of emails per week.

##### For 9 Emails Per Week:
1. Calculate the log-odds:
\[
\log\left(\frac{p}{1-p}\right) = -21.96 + 2.52 \cdot 9
\]
\[
\log\left(\frac{p}{1-p}\right) = -21.96 + 22.68 = 0.72
\]

2. Convert log-odds to odds:
\[
\frac{p}{1-p} = e^{0.72} \approx 2.05
\]

3. Convert odds to probability:
\[
p = \frac{2.05}{1 + 2.05} \approx 0.672
\]
So, the predicted probability of unsubscription is approximately 67.2%.

### Key Equations and Concepts
1. **Log-Odds Equation**:
   \[
   \log\left(\frac{p}{1-p}\right) = β0 + β1 \cdot X
   \]
   - **Intuition**: This equation models the relationship between the predictor variable (emails per week) and the log-odds of the outcome (unsubscription).

2. **Probability Equation**:
   \[
   p = \frac{1}{1 + e^{-(β0 + β1 \cdot X)}}
   \]
   - **Intuition**: This equation converts the log-odds to a probability, providing an interpretable measure (0 to 1) of the likelihood of unsubscription.

### Steps to Find Intercept and Coefficient
1. **Fit the Model**:
   - Use statistical software (e.g., Excel, R, Python) to fit a logistic regression model to your data.
   - The software will output the estimated values for β0 (intercept) and β1 (coefficient).

2. **Interpret the Output**:
   - **Intercept (β0)**: Look at the intercept value to understand the baseline log-odds of unsubscription when no emails are sent.
   - **Coefficient (β1)**: Examine the coefficient value to see how each additional email per week affects the log-odds of unsubscription.

### Practical Explanation for Students
- **Why Logistic Regression?**: Explain that logistic regression is used for predicting binary outcomes (unsubscribe or not) and how it transforms linear predictions into probabilities.
- **What are Log-Odds?**: Introduce the concept of log-odds and why it’s useful in modeling binary outcomes.
- **Interpreting β0 and β1**: Use intuitive examples to explain the meaning of the intercept and coefficient. For example, a high positive β1 indicates a strong effect of the predictor on the outcome.
- **Calculations and Predictions**: Walk through the calculation steps using real data from the case study, showing how to derive probabilities from the logistic regression model.

By following this structured approach, students will gain a comprehensive understanding of logistic regression and its application to predicting customer unsubscription based on email frequency.