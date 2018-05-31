# generate-longitudinal-data
personal use

```
tt<-matrix(NA,200,10)
yy<-matrix(NA,200,10)
for(ii in 1:200)tt[ii,]<-sort(sample(1:100,10))
for(ii in 1:200)yy[ii,]<-sin(tt[ii,]*2*pi/100)+rnorm(10)+rnorm(1)*cos(pi*tt[ii,]/100)

plot_matrix_xy<-function(xmat,ymat){
  plot(range(xmat,na.rm=T),range(ymat,na.rm=T),"n")
  for(ii in 1:nrow(xmat)){
    lines(xmat[ii,],ymat[ii,],col="gray")
    points(xmat[ii,],ymat[ii,],col="gray")
  }
}
plot_matrix_xy(x_matrix_train,y1_matrix_train)
```
