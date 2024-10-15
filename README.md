# Sine Fitting Demos in C++

Some demos that present different methods of solving for phase shifts of an AM sine.

## Approaches

**Method 1:**

1. collect input samples (vo1, vo2)
2. normalize input (minimax)
4. envelope input (`abs(hilbert(TI))`)
4. low-pass filter envelope (`LC = 25Hz`)
5. model filtered (using analytic sine fit)
6. use model to predict future (i.e. beat phase)

**Method 2:**

1. collect input samples (vo1, vo2)
2. normalize input (minimax)
3. model 1, model 2
4. use individual models to model TI 
5. use `phi_b` from TI model to predict future (i.e. beat phase)
