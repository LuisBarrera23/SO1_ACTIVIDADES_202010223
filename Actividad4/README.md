# LUIS ANGEL BARRERA VELASQUEZ 202010223
# Actividad 4 
Crear un systemd unit de tipo servicio para ejecutar un script que imprima un saludo y la fecha actual.


## Paso 1:

crear un script basico que solo imprime el saludo con la fecha:

```bash
#!/bin/bash
fecha=$(date +"%d-%m-%Y")

echo "Hola, bienvendio la fecha actual es $fecha."
```

## Paso 2:
Darle los permisos necesarios para la correcta lectura del script:
```
chmod +x actividad4.sh 
```

## Paso 3:
Ingresamos a la ruta /etc/systemd/system/   y creamos un archivo con el nombre actividad4.service y dentro con el siguiente contenido:

```
[Unit] 
Description=Actividad 4 saludo y fecha  
[Service]
Type=simple 
ExecStart=/home/angel/Documentos/Repositorios/SO1_ACTIVIDADES_202010223/Actividad4/actividad4.sh
[Install] 
WantedBy=multi-user.target  
```

## Paso 4:
Guardamos el archivo 

## Paso 5:
Recargamos los servicios con el siguiente comando:

```
sudo systemctl daemon-reload
```
## Paso 6:
Habilitadomos el servicio:

```
sudo systemctl enable actividad4.service 
```

## Paso 7:
Iniciamos el servicio:

```
sudo systemctl start actividad4.service   
```

## Paso 8:
Validamos que si se ejecute correctamente el servicio:

```
sudo systemctl status actividad4.service      
```
