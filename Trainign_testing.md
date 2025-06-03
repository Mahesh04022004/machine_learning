hese are two main phases in the lifecycle of any machine learning model:

    🔧 Training → Where the model learns from data

    ✅ Testing → Where the model is evaluated on new unseen data

🔹 1. Training Phase
🧠 What Happens in Training?

The model is fed with input data and correct answers (labels).
Goal:

To find the best set of weights and biases that minimize the error (loss) by using algorithms like gradient descent and backpropagation.
Example:
Input (Features)	Output (Label)
Height, Weight	Gender
160 cm, 50 kg	Female
180 cm, 80 kg	Male

The model learns the pattern between inputs and output during training.
🔁 What does the model do?

    Make predictions using initial weights

    Calculate error using loss function

    Adjust weights using gradient descent

    Repeat this for many epochs (iterations over dataset)

🔹 2. Testing Phase
🎯 What Happens in Testing?

We give the model new data it hasn't seen before and check how well it performs.

    We do not show the correct answer during prediction.

    After prediction, we compare with actual labels to compute accuracy, precision, recall, etc.

Example:
Input (Test Data)	Actual Output
170 cm, 60 kg	Female
175 cm, 75 kg	Male

The model predicts the output based on what it has learned in training. We compare these predictions with actual labels to see if it's right.