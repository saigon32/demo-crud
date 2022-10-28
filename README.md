# demo-crud
demo-crud docker compose spring boot y base de datos postgress

comandos docker compose
docker-compose --version --> nos dice la version, ejm: Docker Compose version v2.5.0 docker compose up --> sube el archivo docker-compose.yml, con la configuracion definido en el mismo, abraza la consola docker-compose up -d --> sube el archivo docker-compose.yml, con la configuracion definido en el mismo, NO abraza la consola, modo silencioso docker compose down --> baja los contenedores que estan arriba, pero persiste los volumenes o disco definido para los contenedores docker-compose down --volumes --> baja los contenedores que estan arriba, al igual que los volumenes, apaga todo

ahora bien para subir esta aplicacion es muy importante seguir los siguientes pasos:

debemos compilar el proyecto: mvn install -DskipTests --> este comando para que no valide los test y ejecutado desde la raiz del proyecto, nos genera el demo-crud-1.0.jar en la carpeta target
se debe generar la imagen de manera local para del microservicio y para que esta sea encontrada por docker-compose, ejecutamos entonces: docker build -t demo-crud . este comando es muy importante porque si no se genera la imagen nunca subira el microservicio
seguidamente ejecutamos el script de docker-compose: docker compose up
si queremos apagar la aplicacion docker compose down y para apagarla para que los volumenes no persistan nada: docker-compose down --volumes
video referencia: https://www.youtube.com/watch?v=VTfFpgaSIDw
