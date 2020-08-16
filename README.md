# GuiaHTML
Guía HTML 

##Limpiado variables##
rm(list = ls())


##CargarLibrary##
library(xml2)
library(rvest)

LeerHTML <- read_html("WEB.HTML")
CUERPONOTICIA <- html_nodes(LeerHTML,".texto")
print(CUERPONOTICIA)
CUERPONOTICIA <- html_text(CUERPONOTICIA)
print(CUERPONOTICIA)

##LIMPIANDO ERRORES##
CUERPONOTICIA <- gsub("\\n","",CUERPONOTICIA)
CUERPONOTICIA <- gsub("\\r","",CUERPONOTICIA)
CUERPONOTICIA<- gsub("[.]","",CUERPONOTICIA)
CUERPONOTICIA<- gsub("[,]","",CUERPONOTICIA)
print(CUERPONOTICIA)

##CORRGIENDO ESCRITURA##
CUERPONOTICIA <- tolower(CUERPONOTICIA)
print(CUERPONOTICIA)




