🔷 What is Gradient Descent?

Gradient Descent is an optimization algorithm used to minimize the loss function by adjusting the weights and biases of a model.
🎯 Purpose:

To find the best values of weights and bias so that the model makes accurate predictions with minimum error.
🧠 Simple Analogy:

Imagine you are standing on top of a mountain blindfolded 🏔️.
You want to reach the lowest point in the valley (minimum loss).

You take small steps downhill, always choosing the direction of the steepest descent.

    Each step = a change in weights and bias

    Steepest direction = gradient

    Walking down = minimizing the loss

🧮 How It Works (Mathematical Idea)
Basic Steps:

    Start with random weights and bias

    Compute the loss (how wrong the model is)

    Calculate the gradient (slope) of the loss with respect to weights and bias

    Update weights and bias in the opposite direction of the gradient

    Repeat steps 2–4 until the loss is very small (converges)

🧾 Update Rule (One Step of Gradient Descent)
θ=θ−α⋅∂J(θ)∂θ
θ=θ−α⋅∂θ∂J(θ)​

Where:

    θθ = model parameters (weights & bias)

    αα = learning rate (step size)

    ∂J(θ)∂θ∂θ∂J(θ)​ = gradient (slope of the loss function)

🔑 Important Term: Learning Rate (α)

    Too small → slow learning

    Too large → might overshoot the minimum or diverge

📈 Visualization:

Imagine this loss curve:

      Loss (J)
        ^
        |      *
        |    *
        |  *
        |*        ← Gradient descent steps toward the minimum
        +--------------------> Weights (θ)

Each step brings you closer to the lowest point, where the loss is minimum.
✅ Types of Gradient Descent
Type	Description	Example
Batch GD	Uses the whole dataset to compute the gradient	Stable, but slow
Stochastic GD (SGD)	Uses one training example at a time	Fast, but noisy
Mini-Batch GD	Uses a small batch (e.g., 32 samples)	Balance of speed & stability
🧠 Why It’s Used in ML

Because ML models (especially neural networks) have millions of weights and biases, you need a method to tune them automatically.

Without gradient descent, you'd have no way to minimize the loss function effectively.