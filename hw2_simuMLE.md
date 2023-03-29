labor_hw2
================
b09303042
2023-03-29

``` r
# Define the log-likelihood function
log_likelihood <- function(para) {
  sig1 = para[1]
  sig2 = para[2]
  eps1 <-rnorm(2, mean = 0, sd = sig1)
  eps2<-rnorm(2, mean = 0, sd = sig2)
  y <-eps1+eps2
  
  log(sig1^2+sig2^2)+log(2*pi)+1/(2*(sig1^2+sig2^2))*sum(y^2)
}

# Simulate data
set.seed(123)


# Define the optimization function
opt <- optim(par = c(2,1), fn = log_likelihood)

# Print the estimated parameters
cat("sig1 =", opt$par[1], "\n")
```

    ## sig1 = 1.895014

``` r
cat("sig2 =", opt$par[2], "\n")
```

    ## sig2 = 1.004319
