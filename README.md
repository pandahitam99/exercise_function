# exercise_function
# exercise_function
#function and limit
#Nomor 1 
f <- function(x,y){
  result <- sqrt(x) + y^2
  return(result)
}

#Nomor 2
g <- function(a,b){
  result <- a * b (a^2 + b/3)
  return(result)
}

#Nomor 3 
h <- function(x,y){
  result <- sqrt(f(x,y) + 3 + g(x,y))
  return(result)
}

#Nomor 4 
f1 <- function(x){
  result <- x^3 + x +1
  return(result)
}
f2 <- function(x){
  result <- sqrt(x) - 1
  return(result)
}

f1(f2(4))


#Nomor 5



#NOmor 1
f2 <- function(theta){
  result <- 1- cos(theta)/theta
  return(result)
}

library(Ryacas)
theta <- Sym("theta")


Limit(1- cos(theta)/theta, theta, 0)

#Nomor 2 
f2 <- function(h){
  result <- 2 * ( -3 + h )^2 - 18/h
  return(result)
}

library(Ryacas)
h <- Sym("h")


Limit(2 * ( -3 + h )^2 - 18/h, h, 0)

#Nomor3
f2 <- function(t){
  result <- t - sqrt(3*t+4)/4-t
  return(result)
}

library(Ryacas)
t <- Sym("t")


Limit(t - sqrt(3*t+4)/4-t, t, 4)





#differentation
#nomor 1
dif1 <- function(x){
  return (sqrt(x)*(x+1))
}

library(Ryacas)
x <- Sym ("x")
Simplify(deriv(sqrt(x)*(x+1)))

#nomor 2
dif2 <- function(x){
  return(2*x^2 - 3/ sqrt(x) )
}

x <- Sym ("x")
Simplify(deriv(2*x^2 - 3/ sqrt(x) ))

#nomor 3
dif3 <- function(x){
  return(x-1/x+1)
}
Simplify(deriv( x-1/x+1)) 

#nomor4
dif1(2)

dif2(4)

dif3(1)



#integration
library(Ryacas)
#nomor1
int1 <- function(x){
  return(2*(x^3)) 
}
integrate(int1, lower = 0, upper = 3)
library(Ryacas)
x <- Sym("x")
Integrate((2*(x^3)),x)

#nomor2
int2 <- function(x){
  return(1-5*x^4) 
}
integrate(int1, lower = -1, upper = 2)
library(Ryacas)
x <- Sym("x")
Integrate(1-5*x^4,x)

#nomor3
int3 <- function(x){
  return(x^4 - 3*x^2 + 5) 
}
integrate(int1, lower = -2, upper = 2)
library(Ryacas)
x <- Sym("x")
Integrate(x^4 - 3*x^2 + 5,x)

#nomor4
int4 <- function(x){
  return(x^2 + 1/2*sqrt(x)) 
}
integrate(int1, lower = 1, upper = 4)
library(Ryacas)
x <- Sym("x")
Integrate(x^2 + 1/2*sqrt(x),x)

#nomor5
int5 <- function(x){
  return(x*(2-3*x)^2) 
}
integrate(int1, lower = 0, upper = 2)
library(Ryacas)
x <- Sym("x")
Integrate(x*(2-3*x)^2,x)
