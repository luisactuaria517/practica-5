# practica-5

seriemultiple<-ts.intersect(info1ts,info1ts1,info1ts2,info1ts3)
plot(seriemultiple,type="overplotted", main="serie de tiempo", xlab="años", ylab="numero de personas", col="red")
seriemultiple02.07<-window(seriemultiple,start=c(2002,1),end=c(2007,1))
seriemultiple07.12<-window(seriemultiple,start=c(2007,12),end=c(2012,12))
plot(seriemultiple02.07,main="series de tiempo multiples",xlab="años",col="green")
plot(seriemultiple07.12,main="series de tiempo multiples",xlab="años",col="green")
start(seriemultiple);end(seriemultiple)

##### obtener 4 series de tiempo 

##### importarlas, declararlas series de tiempo, graficarlas juntas
##### crear serie de tiempo multiple y graficarlas juntas 
##### dividir estas series de tiempo en 3 periodos iguales

accion<-read.csv(("C:\\Users\\luisa\\OneDrive\\Documentos\\r series de tiempo\\acciones.csv"));
bimbots<- ts(accion[,1], frequency = 12, start = 2012)
plot(bimbots)

inburts<- ts(accion[,2], frequency = 12, start = 2012)
plot(inburts)

banorts<- ts(accion[,3], frequency = 12, start = 2012)
plot(banorts)

cocats<- ts(accion[,4], frequency = 12, start = 2012)
plot(cocats)

plot(cbind(bimbots,inburts,banorts,cocats))

accionests<-ts.intersect(bimbots, inburts, banorts, cocats)
plot.ts(accionests,xlab="años",col="red",type="overplotted")

accionests1.3<-window(accionests,start=c(2012,1),end=c(2013,6))
accionests2.3<-window(accionests,start=c(2013,7),end=c(2015,2))
accionests3.3<-window(accionests,start=c(2015,3),end=c(2017,1))

plot.ts(accionests1.3,xlab="años",col="red",type="overplotted")
plot.ts(accionests2.3,xlab="años",col="red",type="overplotted")
plot.ts(accionests3.3,xlab="años",col="red",type="overplotted")
