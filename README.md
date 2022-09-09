# PEI
n= 6
aleatorios<-rbinom(n=n, size=1, p=0.5)
x<-ifelse(aleatorios < 1, 0, 1)
posicion<-c(1,cumsum(x))
cbind(aleatorios, x, posicion)

par(mfrow=c(1,1)) 
plot(x=1:(n+1),y=posicion,type='o',pch=1,cex=.8,
     main='Caminata Aleatoria Simple',  ylab='Espacio de Estados de X', xlab='Espacio Parametral E')
abline(h=0,v=0,col='darkblue', lwd=5)
