✅ What is Linearity?

In machine learning, linearity means there is a straight-line relationship between input variables (features) and the output (target).
➕ Mathematical Form:

For a linear model:
y=w1x1+w2x2+⋯+wnxn+b
y=w1​x1​+w2​x2​+⋯+wn​xn​+b

    yy: output (prediction)

    x1,x2,…x1​,x2​,…: features

    w1,w2,…w1​,w2​,…: weights

    bb: bias (intercept)

🧠 Intuition:

If you double the input, the output doubles (linear proportionality).
📈 Example:
Hours Studied (X)	Marks (Y)
1	20
2	40
3	60

    A straight line can fit this data → it's linear.

✅ What is Non-Linearity?

Non-linearity means the relationship between input and output is not a straight line — it could be curved, exponential, zig-zag, or involve higher-order functions like square, log, or sine.
➕ Mathematical Form:

For non-linear models:
y=w1x12+sin⁡(w2x2)+⋯+b
y=w1​x12​+sin(w2​x2​)+⋯+b

    The output depends on more complex combinations of inputs.

📉 Example:
Hours Studied (X)	Marks (Y)
1	20
2	40
3	30
4	50

    Can't fit this with a straight line → needs a curved or non-linear model.

🔄 Key Differences Between Linear and Non-Linear Models
Feature	Linear Models	Non-Linear Models
Relationship	Straight-line	Curved / Complex
Formula	y=wx+by=wx+b	y=wx2+sin⁡(x)y=wx2+sin(x), etc.
Visualization	Straight line	Curve, zig-zag, etc.
Complexity	Simple	More complex
Training Time	Fast	Slower
Interpretability	Easy to interpret	Harder to interpret
Flexibility	Less flexible	More flexible
Use Case	Linearly separable data	Complex, real-world data
🔍 Examples of Linear Models:

    Linear Regression

    Logistic Regression (despite its name, it uses a non-linear sigmoid function but assumes linear decision boundary)

    Linear SVM

🔍 Examples of Non-Linear Models:

    Polynomial Regression

    Decision Trees / Random Forests

    Neural Networks (especially deep)

    Non-Linear SVM (with kernel trick)

    K-Nearest Neighbors (KNN)