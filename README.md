# Statement
I have corrected some minor errors from [GLassoElnetFast](https://github.com/TobiasRuckstuhl/GLassoElnetFast).<br>
In R, `cov(Y)` or `var(Y)` is the **unbiased estimation** of the covariance matrix, which is given by `n = nrow(Y); crossprod(scale(Y, scale = FALSE)) / (n-1)`.<br>
However, in Gaussian graphical models (GGM), the **maximum likelihood estimation (MLE)** of the covariance matrix is considered, and is given by `n = nrow(Y); crossprod(scale(Y, scale = FALSE)) / n`.<br>
Hence, for rigorousness, I have corrected each `cov(Y)` to `n = nrow(Y); (n-1) / n * cov(Y)`.
# References
[rags2ridges](https://github.com/CFWP/rags2ridges); https://cran.r-project.org/web/packages/rags2ridges/index.html.
