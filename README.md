# Mi idea para mi proyecto :bulb:
Mi idea para mi proyecto es un bot de discord que sea capaz de calcular productos individuales que el usuario le pida, tomando en cuenta tax y lugar de compra


# Tipo de proyecto
Bot de discord 


# Proceso tecnico
1.Pedirle a chatgpt por la base del codigo en lenguaje python y pedirle que me de las funciones del codigo que no se hacer como la calculacion o el manejo d la api o la base de datos.

2.Conector el bot con mi servidor privado de discord para probarlo.

3.Probar las calculaciones del bot con varios productos y con varios lugares distintos y lugar probar estas calculaciones con otras echas a mano.

4.Limpiar el codigo para remover redundancias y organizarlo.

5.Hacer un archivo github para guardar el codigo.


# Biblotecas necesarias
1.python-dotenv
2.aiohttp

# Referencias usadas para el codigo
1.Chatgpt

# Articulos de guia
Link:\https://documenter.getpostman.com/view/10601972/TVev6RW8#6dbedc9d-c06e-4ce5-ba6e-93c43682dcd7


# ✅ LISTA DE CONTROL PARA EL CÓDIGO DEL BOT (DISCORD.PY)

1. Funcionalidad

✅ Lo que funciona bien:

El bot se inicia correctamente (on_ready).

Comandos !precio, !paises, !vat, !comandos implementados.

Conversión de precios y cálculo de IVA funcionan.

Manejo básico de errores: falta de argumentos, país no encontrado, precios inválidos.

⚠ Mejoras posibles:

!precio no maneja inputs mal formateados como !precio abc usa de manera robusta (aunque da mensaje de error, podrías agregar validación más detallada).

No hay tests unitarios ni verificación de que las claves en VAT_RATES siempre correspondan a ISO_MAP.

No hay almacenamiento de historial ni base de datos real, solo dicts en memoria (está bien para MVP, pero limita escalabilidad).

2. Interfaz de usuario (UI/UX)

✅ Bien:

Los mensajes de respuesta son claros y legibles.

Uso de emojis y formato Markdown en Discord mejora la legibilidad.

⚠ Mejoras posibles:

Para listas largas (como !paises o !vat), si hay muchos países puede romperse la visualización en Discord. Podrías paginar.

No hay confirmaciones interactivas ni reacciones para mejorar UX.

3. Seguridad

⚠ Observaciones importantes:

El bot no maneja usuarios ni permisos: cualquier usuario puede ejecutar todos los comandos.

No hay riesgo de inyección SQL (no hay DB), pero cuidado si agregas base de datos más adelante.

Token se carga desde .env, lo cual es correcto.

💡 Recomendación: evitar exponer el token, revisar permisos del bot en el servidor.

4. Rendimiento

✅ Bien:

La ejecución es ligera: solo diccionarios en memoria.

No hay operaciones pesadas.

⚠ Mejoras posibles:

Para muchos precios en !precio o muchos países en !paises, podría ser útil optimizar iteraciones.

5. Contenido

✅ Bien:

Listado de países y tasas de IVA actualizado.

Mensajes claros y estructurados.

⚠ Mejoras posibles:

Algunos nombres de países podrían unificarse (ej. acentos consistentes, abreviaciones).

Mensajes podrían ser más amigables en casos de error (ej. sugerir país similar si no se encuentra).

6. Compatibilidad

✅ Bien:

Funciona en cualquier servidor Discord donde tenga permisos.

Compatible con Python 3.10+ (o 3.8+ con discord.py).




# Presentacion final

## Autor
Isaac Joel Otero Figueroa

## Titulo
Bot de discord para calcular el tax

## Descripcion
Este es un bot de discord que tiene el proposito de ayudarte a hacer calculaciones de los precios de productos tomando en cuenta el precio insertado por el usuario y el ivu del lugar selecionado.

## Finalidad 
Quiero que este bot se use como una base para calculadoras que hagan especificos tipos de calculaciones automaticamente y ayuden a personas como yo que tienen problemas para entender las matematicas en hacer las tareas cotidianas que requieren el uso de estas.

## Usos
1.Simplificar el proceso de calcular cuanto algo te va a costar incuyendo el tax para personas con dificultad en la matematica.

2.Recopilar el ivu de varios paises en un solo lugar para mayor organizacion y simplificar la manejacion de estos.

## Funciones

La funcion primaria de mi bot es la habilidad de calcular el precio determinado por el usuario usando el comando !precio. Ejemplo: !precio 100 españa. Esto es realizado por el bot usando una base de datos interna que busca el pais selecionado por el usuario (si esta disponible) y hace la calculacion de cual seria el precio final tomando en cuenta el precio puesto por el usuario. Tambien puedes ver la lista de los paises y los ivus de estos usando el comando !paises y !vat respectivamente. Si quieres ver todos estos comandos y su descripcion usa el comando, !comandos.


## Ejemplo del comando !precio
<img width="1060" height="201" alt="Captura de pantalla (46)" src="https://github.com/user-attachments/assets/42334fac-9145-4022-83a9-a8ea88e1007a" />


## Ejemplo del comando !paises
<img width="1028" height="610" alt="Captura de pantalla (45)" src="https://github.com/user-attachments/assets/d94ca417-baf6-4b5c-9f49-2d7fa13bc963" />


## Ejemplo del comando !vat
<img width="1029" height="615" alt="Captura de pantalla (48)" src="https://github.com/user-attachments/assets/0d648e35-ab0b-4a10-aec7-b7612538fc1f" />



## Ejemplo del comando !comandos
<img width="1027" height="250" alt="Captura de pantalla (49)" src="https://github.com/user-attachments/assets/26067510-46aa-435f-919e-14302c28983f" />


# Conclusion

Esto es un proyecto que vino de un lugar muy personal para mi ya que estoy avazando a la etapa adulta de mi vida y eso implica hacerse responsable de uno mismo. Incluyendo las finanzas personales. Pero yo nunca he cido muy bueno en las matematicas siempre han cida confusas para mi, poniendose mas complicadas mientras crecia donde se añadian mas conceptos a las matematicas como letras que la hacian mas dificil de entender para mi. Y ahora que estoy tratando manejar mi propio dinero estoy tratando de entender cuanto cuestan las cosas y unas de las primeras cosas que me intereso fue el ivu ya que se me hacia extraño como algo puede tener un precio ya fijo pero puede costar mas. cuando vino el momento de hacer el proyecto final una de las primeras cosas que se me fue a la mente fue este bot ya que pense que seria muy conveniente si simplemente podria semi-automatizar el proceso de calcular el valor de algo con la iva sin ser tan complicado. Yo creo que este bot seria muy util para personas como yo que tienen problemas con las matematicas y aun haci estan interesados en manejar sus finanzas







