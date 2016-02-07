## Overall description of the functions do:
## These functions are a pair of functions that cache an inversed matrix

## Short comment describing this function:
## this functions creates the object that contains the matrix and the inverse matrix, if new values are added to the matrix the matrix is set to NULL

makeCacheMatrix <- function(x = matrix()) {
  
  m <- NULL
  set <- function(y) {
    x <<- y
    m <<- NULL
  }
  get <- function() x
  setinverse <- function(solve) m <<- solve
  getinverse <- function() m
  list(set = set, get = get,
       setinverse = setinverse,
       getinverse = getinverse)
  
}


## Short comment describing this function:
## this function checks if the matrix is already in cache if not then it calculates the inverse matrix

cacheSolve <- function(x, ...) {
  ## Return a matrix that is the inverse of 'x'
  
  m <- x$getinverse()
  if(!is.null(m)) {
    message("getting cached inverse matrix")
    return(m)
  }
  matrix <- x$get()
  m <- solve(matrix, ...)
  x$setinverse(m)
  m
}
