# Nonlinear-Regression-in-R
Therapeutic clearance in blood
Vd = Dose/Co
Conc = Coe^-keTime
Vd = Volume of distribution
Co= Extrapolated concentration at Time = 0
Dose = How much infused
tHalf = 0.693/ke
ke = Elimination rate constant

Output:

Formula: Conc ~ C0 * exp(-ke * Time)
Parameters:
   Estimate Std. Error t value Pr(>|t|)    
C0 59.46203    2.29329  25.929 5.25e-09 ***
ke  0.16330    0.01644   9.931 8.94e-06 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 3.556 on 8 degrees of freedom
Number of iterations to convergence: 4 
Achieved convergence tolerance: 6.633e-07

Formula: Conc ~ (1000/Vd) * 2^(-Time/tHalf)
Parameters:
      Estimate Std. Error t value Pr(>|t|)    
Vd     16.8175     0.6486  25.929 5.25e-09 ***
tHalf   4.2446     0.4274   9.931 8.94e-06 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
Residual standard error: 3.556 on 8 degrees of freedom
Number of iterations to convergence: 7 
Achieved convergence tolerance: 6.649e-07
