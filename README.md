# ParetoPosStable
An R package with statistical functions to describe a Pareto Positive Stable (PPS) distribution and fit it to real data. Graphical and statistical tools to validate the fits are also included.

### Installation of the package
* Install the latest versions of all dependencies from CRAN:
```r
install.packages(c("graphics", "grDevices", "stats", "ADGofTest", "lmom", "foreach", "doParallel", "parallel"))
```
* Install ParetoPosStable current development version from CRAN:
```r
devtools::install_github("ajsaez/ParetoPosStable")
```
* After attaching the package, you are ready to start:
```r
library(ParetoPosStable)
```
### Examples
```r
data(turkey)
fit <- PPS.fit(turkey$Pop2000)
print(fit)
coef(fit)
se(fit, k = 2000, parallel = TRUE, ncores = 2)
logLik(fit)
par(mfrow=c(2,2))
plot(fit)
GoF(fit, k = 2000, parallel = TRUE, ncores = 2)
```
