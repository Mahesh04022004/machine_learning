
✅ What is Batch Normalization?

Batch Normalization (or BatchNorm) is a technique to make training faster and more stable in neural networks by normalizing the inputs of each layer.
🧠 Simple Definition:

Batch Normalization standardizes the input going into a layer so that:

    The mean is around 0

    The standard deviation is 1

It’s like cleaning up the data at every layer, not just before the first layer.
🔍 Why Do We Need Batch Normalization?

When training deep networks:

    The values (activations) can become too large or too small.

    This makes training unstable, and slow.

👉 BatchNorm fixes this by keeping the values in a normal range during training.
📊 Real-Life Analogy:

Imagine you are baking a cake and using cups to measure flour. If your cups are different sizes each time (one big, one small), the result is inconsistent.

Batch normalization ensures that you always use the same sized cup → it keeps the measurements consistent.
📈 What It Actually Does (Step-by-Step)

Let’s say you are training a model and you have batch of inputs for a layer:
Step 1: Calculate the Mean
μ=1m∑i=1mxi
μ=m1​i=1∑m​xi​
Step 2: Calculate the Standard Deviation
σ=1m∑i=1m(xi−μ)2
σ=m1​i=1∑m​(xi​−μ)2
​
Step 3: Normalize Each Input
x^i=xi−μσ
x^i​=σxi​−μ​

Now the inputs have:

    Mean = 0

    Standard Deviation = 1

Step 4: Scale and Shift (Learnable Parameters)
yi=γ⋅x^i+β
yi​=γ⋅x^i​+β

    γ (gamma) and β (beta) are learned during training

    They let the model scale or shift the normalized data if needed