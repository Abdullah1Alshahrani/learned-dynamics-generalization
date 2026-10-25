Generalization of Learned Dynamics Models Under Dynamics Shift: A Long-Horizon Prediction Study

Problem

Learned dynamics models predict how a system evolves from its current state and actions. However, a model trained under one set of dynamics may become less accurate when the system or operating conditions change. In addition, small prediction errors can accumulate when the model is rolled out over multiple future steps.

The main question of this project is:

How robust are learned dynamics models to changes in system dynamics, and how does prediction accuracy degrade over longer prediction horizons?

Data

I plan to use the Mini Wheelbot dataset, a real-world robotics dataset containing sequential state and action data collected from multiple physical robot instances and surface conditions.

The dataset will serve as a case study for the broader learned-dynamics problem. I will separate training and evaluation conditions by robot and/or surface when possible so that I can evaluate generalization under dynamics shift rather than only performance on randomly held-out samples.

Planned Approach

I will implement a neural dynamics model in PyTorch to predict future system states from state and action information.

I will first evaluate one-step prediction under conditions similar to the training data. I will then recursively roll out the model over multiple future steps and evaluate it under both familiar and changed dynamics conditions.

I may compare different model architectures or training strategies depending on the initial results and available time.

The code and experiment configuration will be organized so that the results can be reproduced.

Evaluation

I will measure prediction error over increasing prediction horizons and compare:

* Conditions similar to the training data
* Unseen robot and/or surface conditions
* One-step versus multi-step prediction

The main analysis will examine how quickly prediction errors accumulate, how dynamics shift affects long-horizon prediction, and where the learned model becomes less reliable.

Expected Analysis

I expect prediction error to generally increase with prediction horizon and potentially increase faster under unseen dynamics conditions, although the results may differ across robot and surface conditions.

The project will analyze whether this behavior is consistent across conditions and identify limitations of the learned model and experimental setup.

Risks and Adjustments

If some robot/surface combinations do not provide enough data for a controlled comparison, I will reduce the number of conditions while keeping the main comparison between familiar and shifted dynamics.

The exact model architecture and prediction horizons may also be adjusted after initial experiments.
