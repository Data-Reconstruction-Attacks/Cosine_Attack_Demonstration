# Cosine_Attack_Demonstration

Cosine Attack Demonstration on BMI Dataset

This project demonstrates a cosine attack using the BMI dataset. The attack shows how an unknown data point can be reconstructed by comparing its cosine similarities with a few buffer (known) data points.

Dataset :
The Dataset contains:
  1) Gender: Male / Female
  2) Height: Height in cm
  3) Weight: Weight in kg
  4) Index: Health category (0 - Extremely Weak , 1 - Weak , 2 - Normal , 3 - Overweight , 4 - Obesity , 5 - Extreme Obesity)


Prepare Data

  1) Extract features: Gender, Height, Weight.
  
  2) Encode gender: Male = 1, Female = -1.

  3) Convert to NumPy array for further computation.




**Phase - 1**

***Step 1 – Select Samples***

  1) Pick 3 buffer points (list_1) randomly.

  2) Pick 1 unknown data point (list_2) randomly

  3) Compute cosine similarities between the unknown point and the 3 buffer points → list_3.

***Step 2 – Compute Intersection Direction***

  1) Define compute_direction(axes, list_3) to solve for the intersection direction vector of the cones defined by buffer points.
  
  2) The output is a unit vector pointing to the direction of the hidden data point.





**Phase - 2**

***Step 3 – Reconstruct the Unknown Point***

  1) Normalize the direction vector into the form: (x1 / ​x1 ​​, x2 / ​x1 ​​, x3 / ​x1​​) 

  2) Compare this reconstructed vector with the actual unknown sample.
    
  3) If they match, the hidden point is successfully reconstructed (attack succeeded).
