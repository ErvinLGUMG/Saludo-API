Esta es una API que devuelve un saludo en diferentes formatos asi como en formato JSON, XML y HTML 
segun sea el dato esperado en el cliente del API.

se levanta el servicio ejecutando el siguiente comando:
# mvn spring-boot:run

hacemos un llamado a la url "http://localhost:8080/greeting" para obtener un "hello Wolrd!" en formato JSON.

Si queremos que el saludo sea mas personalizado pasamos como parametro el nombre que deseamos recibir en el saludo
por ejemplo "http://localhost:8080/greeting?name=Ervin" para obtener un resultado "hello Ervin!" en formato JSON

Si queremos recibir la respuesta en formato XML o en formato HTML se agrego una dependencia al achivo "pom.xml"
que pertenece al grupo "com.fasterxml.jackson.dataformat" al haber agregado esta dependencia el API nos puede 
devolver diferentes formatos de respuesta si lo requerimos en el llamado, por ejemplo en el llamado al API 
agregamos un "header" con el nombre "Accept" y en el valor del header ponemos el formato en el que deseamos la 
respuesta asi como puede ser "application/json","application/xml" & "text/html" segun el formmato de respuesta
que necesitemos.