# Purpose
This is a shadow supporting page for Kamo et al. (2022):
<br>
Masashi Kamo, Takehiko I. Hayashi, Yuichi Iwasaki (2022) Revisiting assessment factors for species sensitivity distributions as a function of sample size and variation in species sensitivity. Ecotoxicology and Environmental Safety. 246: 114170. https://doi.org/10.1016/j.ecoenv.2022.114170

# Assessment factor (AF)
By assuming toxicity values are a random sample from a log-normal distribution, we mathematically analyzed the species sensitivity distribuiton (SSD) to derive the magnitude of AF needed to achieve a given protection goal (e.g., protecting 95% of species with 95% probability). 
<br><br>
<img src="https://github.com/user-attachments/assets/e16c3f15-4c70-46f5-a3e9-d1ebf9152047" width="500">



To calculate t95, you can use the following R code:

```r
K05 <- qnorm(0.05,0,1) # Protecting 95% of species
N <- 10 # Number of species
myDf <- N-1
myNCP <- -sqrt(N)*K05
qt(0.95, df = myDf, ncp = myNCP) # t95
```
Some examples:<br><br>
<img src="https://github.com/user-attachments/assets/b7484928-2286-4d2d-8570-d355fc47a7f2" width="300">

