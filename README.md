Deepfakes have rapidly evolved from containing
obvious visual artifacts to exhibiting high levels of photorealism,
posing significant risks to digital trust, security, and information
integrity. This project investigates whether modern convolutional
neural networks (CNNs) truly learn meaningful facial features
for deepfake detection or instead rely on spurious correlations
present in training data.
Using the publicly available Kaggle real–fake face dataset,
we train and evaluate an InceptionV3-based classifier and
reproduce high-accuracy performance comparable to recent
literature, achieving over 90% training accuracy and 85% validation
accuracy. However, a detailed analysis of precision–recall
asymmetries reveals substantial class imbalance, indicating that
accuracy alone is an insufficient measure of reliability.
To probe the model’s internal reasoning, I applied two complementary
explainability techniques : Grad-CAM and LIME
to demonstrate that their explanations often diverge, with
both methods frequently highlighting background regions rather
than semantically meaningful facial features. This inconsistency
suggests that the classifier may be exploiting dataset-specific
artifacts rather than robust biometric cues.
I further introduce adversarial training using a generative
adversarial network (GAN) and FGSM-based perturbations,
observing a reduction in overall accuracy but a marked improvement
in class balance and robustness.
The results highlight three key findings: (i) high accuracy does
not imply reliable or fair detection, (ii) explainability methods
can expose hidden dependencies on non-facial features, and (iii)
adversarial training improves robustness at the cost of raw
performance. We conclude that while AI systems can detect AI-
generated media to a limited extent, deepfake detection remains
inherently fragile due to the ongoing adversarial arms race
between generators and detectors.
