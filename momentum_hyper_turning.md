✅ 1. Momentum in Machine Learning
🔍 What is Momentum?

Momentum is a technique used in gradient descent to speed up training and reduce oscillations.

It helps the model reach the minimum loss faster by remembering the previous gradients and using that information to move more smoothly.
🧠 Simple Analogy:

Imagine you are pushing a ball down a hill:

    Without momentum: You take small, careful steps down — slow and cautious.

    With momentum: You push the ball, and it rolls faster because it carries its speed — it doesn't start from zero every time.

That’s what momentum does in optimization — it accumulates the direction of previous steps and moves faster in that direction.
⚙️ How It Works (Mathematically):

In normal gradient descent:
w=w−η⋅∇L(w)
w=w−η⋅∇L(w)

In gradient descent with momentum:
vt=γvt−1+η⋅∇L(w)
vt​=γvt−1​+η⋅∇L(w)
w=w−vt
w=w−vt​

Where:

    ww: weights

    ηη: learning rate

    γγ: momentum factor (typically 0.9)

    ∇L(w)∇L(w): gradient of loss

    vtvt​: velocity term (history of past gradients)

✅ Benefits of Momentum:

    Speeds up convergence

    Helps escape local minima

    Reduces oscillations in steep areas

❌ Drawbacks:

    Requires tuning the momentum parameter (γγ)

    May overshoot if not controlled

✅ 2. Tuning Hyperparameters
🔍 What are Hyperparameters?

Hyperparameters are settings or configurations that you set before training a machine learning model. These are not learned from the data.
Common Hyperparameters:
Category	Hyperparameter
Optimization	Learning rate, momentum, batch size
Model Structure	Number of layers, number of neurons
Regularization	Dropout rate, L1/L2 penalty
Training	Number of epochs, early stopping patience
Tree-based Models	Max depth, min samples split, number of trees
🎯 Why Tune Hyperparameters?

To maximize model performance. Choosing the right combination of hyperparameters helps the model generalize well and avoid overfitting or underfitting.
⚙️ How to Tune Them?
🔁 1. Grid Search:

    Try every possible combination from a set of predefined values.

    Example: try learning rates [0.001, 0.01, 0.1] and dropout [0.3, 0.5]

🔄 2. Random Search:

    Randomly selects combinations.

    Faster than grid search for large combinations.

🧠 3. Bayesian Optimization:

    Uses previous results to choose the next best values.

    More efficient and intelligent.

💻 4. Automated ML (AutoML):

    Tools like AutoSklearn, Optuna, Keras Tuner help tune hyperparameters automatically.

✅ Good Practices:

    Use cross-validation to evaluate performance while tuning.

    Use learning curves to decide on training duration.

    Tune one parameter at a time initially, then in combinations.