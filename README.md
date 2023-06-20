# Corriendo el servidor de desarrollo local

Para correr el servidor de desarrollo local debe seguir los siguientes comandos

```sh
cd premiosplatzi
source env/bin/activate
cd premiosplatziapp
python3 manage.py runserver
```

# Comandos utiles

Para crear una aplicacion basta con ejecutar el siguiente comando

```sh
python3 manage.py startapp "Nombre de la aplicación"
```

Para migrar los modelos que hemos creados en el archivo models.py de nuestra app daremos los siguientes pasos. El primer comando con python3 crea un archivo llamado 0001_initial.py el cual Django describe la creación de las tablas en la base de datos haciendo uso del concepto ORM. Mientras el segundo comando python3 se toma el archivo 0001_initial.py para ejecutar el sql en la base de datos.

```sh
cd premiosplatzi
source env/bin/activate
cd premiosplatziapp
python3 manage.py makemigrations "Nombre de la aplicación"
python3 manage.py migrate
```

Con este comando podremos acceder a una consola interactiva con la cual podremos acceder a los documentos de nuestro proyecto

```sh
python3 manage.py shell
```

# Comandos que se pueden usar en la shell

Para acceder a todos los registros de una tabla u tipo de objeto que existe en django puedes usar el siguiente comando

```sh
"nombre del objeto".objects.all()
```

Para guardar un objeto nos toca pirmero crear dicho objeto y luego salvarlo en la base de datos

```sh
"nombre del objeto" = Objeto("var1"="val1", "var2"="val2", "varn"="valn")
"nombre del objeto".save()
```
