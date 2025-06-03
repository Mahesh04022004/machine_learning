🔷 What is Linear Regression?

Linear Regression is a supervised learning algorithm used to predict a continuous dependent variable based on one or more independent variables.
✅ Goal:

    To find the best-fitting straight line that describes the relationship between variables.

🔷 Types of Linear Regression

    Simple Linear Regression

        One independent variable (X)

        Equation:
        Y=mX+c
        Y=mX+c

    Multiple Linear Regression

        Multiple independent variables (X₁, X₂, ..., Xₙ)

        Equation:
        Y=b0+b1X1+b2X2+⋯+bnXn
        Y=b0​+b1​X1​+b2​X2​+⋯+bn​Xn​

🔷 Components

    Y – Predicted/Target variable (dependent)

    X – Input/Feature variable(s) (independent)

    m or b₁ – Slope (change in Y for unit change in X)

    c or b₀ – Intercept (Y value when X=0)

🔷 Cost Function (Loss Function)

We minimize the error between predicted and actual values using:
📌 Mean Squared Error (MSE):
MSE=1n∑i=1n(yi−y^i)2
MSE=n1​i=1∑n​(yi​−y^​i​)2
🔷 Assumptions of Linear Regression

    Linearity – Relationship between X and Y is linear.

    Independence – Observations are independent.

    Homoscedasticity – Constant variance of errors.

    Normal distribution of residuals (errors).

    No multicollinearity – Independent variables are not highly correlated.

🔷 Advantages

    Simple, fast, and interpretable.

    Performs well when assumptions hold.

🔷 Limitations

    Fails when the relationship is non-linear.

    Sensitive to outliers.

    Assumes constant variance and normality.

🔷 Applications

    Predicting house prices

    Forecasting sales

    Estimating salary based on experience

    Predicting temperature

🔴 LOGISTIC REGRESSION – Detailed Explanation
🔷 What is Logistic Regression?

Logistic Regression is a supervised learning algorithm used for classification tasks (not regression) — particularly binary classification.
✅ Goal:

    To predict the probability that a given input belongs to a particular class (0 or 1).

🔷 Core Idea

Instead of fitting a straight line, logistic regression fits an S-shaped (sigmoid) curve that maps any real-valued number into a value between 0 and 1.
📌 Sigmoid Function:
P(Y=1∣X)=11+e−(b0+b1X)
P(Y=1∣X)=1+e−(b0​+b1​X)1​

    Output is a probability (between 0 and 1)

    If P > 0.5 → Class = 1

    If P < 0.5 → Class = 0

🔷 Types of Logistic Regression

    Binary Logistic Regression – Classify into 2 classes (e.g., pass/fail)

    Multinomial Logistic Regression – More than 2 classes (e.g., low, medium, high)

    Ordinal Logistic Regression – Classes with a natural order (e.g., bad < good < excellent)

🔷 Cost Function for Logistic Regression

We cannot use MSE here; we use Log Loss (Binary Cross Entropy):
Loss=−1n∑i=1n[yilog⁡(y^i)+(1−yi)log⁡(1−y^i)]
Loss=−n1​i=1∑n​[yi​log(y^​i​)+(1−yi​)log(1−y^​i​)]
🔷 Assumptions of Logistic Regression

    Binary/Multiclass output

    No multicollinearity among independent variables

    Large sample size helps model better

    Independent observations

🔷 Advantages

    Good for binary classification

    Outputs probabilities

    Interpretable and efficient
    