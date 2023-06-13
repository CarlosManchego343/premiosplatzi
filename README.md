# Corriendo el servidor de desarrollo local

Para correr el servidor de desarrollo local debe seguir los siguientes comandos

```sh
cd premiosplatzi
source env/bin/activate
cd premiosplatziapp
python3 manage.py runserver
```

# Comando utiles

Para crear una cplicacion basta con ejecutar el siguiente comando

```sh
python3 manage.py startapp "Nombre de la aplicación"
```

Para migrar los modelos que hemos creados en el archivo models.py de nuestra app daremos los siguientes pasos. El primer comando con python3 crea un archivo llamado 0001_initial.py el cual Django describe la creación de las tablas en la base de datos haciendo uso del concepto ORM. Mieeras el segundo comando python3 se toma el archivo 0001_initial.py para ejecutar el sql en la base de datos.

```sh
cd premiosplatzi
source env/bin/activate
cd premiosplatziapp
python3 manage.py makemigrations "Nombre de la aplicación"
python3 manage.py migrate
```