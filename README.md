# read the R script
# replace the "path/to/file" with the directory you save the file into
source("path/to/file/cacheMatrix.R")


# create the matrix during the call of makeCacheMatrix()
myMatrix <- makeCacheMatrix( matrix(c(1:4), nrow = 2, ncol = 2) );

summary(myMatrix );
> summary(myMatrix );
         Length Class  Mode    
set      1      -none- function
get      1      -none- function
cacheInv 1      -none- function
getInv   1      -none- function



 myMatrix$get();
     [,1] [,2]
[1,]    1    3
[2,]    2    


> cacheSolve(myMatrix)
     [,1] [,2]
[1,]   -2  1.5
[2,]    1 -0.5



# second time run the function,get the cached value
> cacheSolve(myMatrix)
got cached data
     [,1] [,2]
[1,]   -2  1.5
[2,]    1 -0.5





