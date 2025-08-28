# Cosine_Attack_Demonstration

Cosine Attack Demonstration on BMI Dataset

This project demonstrates a cosine attack using the BMI dataset. The attack shows how an unknown data point can be reconstructed by comparing its cosine similarities with a few buffer (known) data points.

Dataset :
The Dataset contains:
  1) Gender: Male / Female
  2) Height: Height in cm
  3) Weight: Weight in kg
  4) Index: Health category (0 - Extremely Weak , 1 - Weak , 2 - Normal , 3 - Overweight , 4 - Obesity , 5 - Extreme Obesity)


Steps in the Code
Step 1 – Prepare Data

Extract features: Gender, Height, Weight.

Encode gender: Male = 1, Female = -1.

Convert to NumPy array for computation.

Step 2 – Select Samples

Pick 3 buffer points (list_1) randomly.

Pick 1 unknown data point (list_2) randomly.

Compute cosine similarities between the unknown point and the 3 buffer points → list_3.

Step 3 – Compute Intersection Direction

Define compute_direction(axes, list_3) to solve for the intersection direction vector of the cones defined by buffer points.

The output is a unit vector pointing to the direction of the unknown data point.

Step 4 – Reconstruct the Unknown Point

Normalize the direction vector into the form:
