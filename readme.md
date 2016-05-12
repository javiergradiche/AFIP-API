
# AFIP API simplificada  

### Pasos para hacer funcionar el API  
1) Desde el root ```npm install```  
2) Desde el root correr ```./tools/keygen.sh /C=AR/O=Nombre Desarrollador/CN=Nombre Desarrollador/serialNumber=CUIT 00000000000```  
3) Correr la app  
3a) Para Homologación: ```HOMO=true node server.js```  
3b) Para Producción: ```node server.js```    


### Endpoints  
> Para probar los endpoints que genera el API se proveen ejemplos con el API WSFEv1 mediante postman (Descarga: https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop )  
  
1) Luego de descargar Postman importar el archivo que se encuentra en la carpeta "postman"  
1) Para aquellos Endpoints que requiren CUIT Revisar los parametros Body y cambiar CUIT  


### Cómo funcionan los endpoints  
> La idea del API es hacer genéricas las llamadas y preservar la autenticación obtenida  

1) Describir el endpoint: ```/api/aqui_servicio/describe```. Ej. de Servicio: ```wsfev1```  
2) Para realizar llamado ```/api/aqui_servicio/aqui_metodo```  
2a) Servicio: ```wsfev1```  
2b) Método: ```FEDummy```. Puede ser cualquiera de los obtenidos mediante describe.