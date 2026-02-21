# Implementación de una Pila y Ofuscación con Maven

Este repositorio incluye la creación de una estructura de datos tipo Pila (Stack) desarrollada desde cero y publicada como una dependencia Maven, junto con un proyecto que la utiliza para verificar expresiones algebraicas.

# Organización del Proyecto

El proyecto está dividido en dos módulos principales:

# umg.edu.gt.data-structure.stack

Contiene la implementación de la estructura de datos Pila. Funciona como una librería reutilizable.

# stackHandler

Es una aplicación que importa la librería anterior y la utiliza para validar expresiones algebraicas (por ejemplo, revisar si los paréntesis están correctamente balanceados).

# Instrucciones de Uso

# 1. Instalación de la Librería

Primero se tiene que compilar e instalar la librería en el repositorio local de Maven (.m2), para que pueda ser utilizada por otros proyectos.

# Ejecutar los siguientes comandos en cmd:

cd umg.edu.gt.data-structure.stack

mvn clean install

Esto generará el .jar y lo guarda en el repositorio local.

# 2. Compilación y Ejecución de la Aplicación

Una vez instalada la libreria ya se puede compilar y ejecutar la aplicación que valida expresiones.

cd ../stackHandler

mvn clean package

mvn exec:java -Dexec.mainClass="stackHandler.handler.Main"

clean package compila el proyecto y genera el .jar.

exec:java ejecuta la clase principal del programa.

# 3. Ofuscación del Código con ProGuard

Para proteger el codigo fuente se puede generar una versión ofuscada del .jar donde los nombres de clases, métodos y variables son modificados.

mvn clean package -Pobfuscate

Al fina en la carpeta /target se encuentra lo siguiente:

- El .jar original.

- El .jar ofuscado.

# Aspectos Técnicos de la Implementación de la Pila

La estructura de datos Pila implementa operaciones fundamentales como:

- size(): Devuelve el número actual de elementos almacenados en la pila.

- getNodeInit(): Permite obtener el nodo base o inicial de la pila (el elemento que se encuentra en la parte inferior).
