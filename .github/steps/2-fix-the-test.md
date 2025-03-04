<!--
  <<< Notas del autor: Paso 2 >>>
  Comienza este paso reconociendo el paso anterior.
  Define los términos y enlaza a docs.github.com.
-->


## Paso 2: Corregir la prueba

_¡Excelente trabajo al agregar el workflow con plantilla! :tada:_

Agregar ese archivo a esta rama es suficiente para que GitHub Actions comience a ejecutar CI en tu repositorio.

Cuando un workflow de GitHub Actions está en ejecución, deberías ver algunas verificaciones en progreso, como se muestra en la captura de pantalla a continuación.

<img alt="verificaciones en progreso en un cuadro de fusión" src=https://user-images.githubusercontent.com/16547949/66080348-ecc5f580-e533-11e9-909e-c213b08790eb.png width=400 />

Puedes seguir el progreso mientras GitHub Actions ejecuta tu trabajo yendo a la pestaña **Actions** o haciendo clic en "Details" en el cuadro de fusión a continuación.

Cuando las pruebas finalicen, verás una marca de verificación roja :x: o una marca de verificación verde :heavy_check_mark: en el cuadro de fusión. En ese momento, puedes acceder a los registros del trabajo de compilación y sus pasos asociados.


_Al observar los registros, ¿puedes identificar qué pruebas fallaron?_ Para encontrarlo, ve a una de las compilaciones fallidas y desplázate por el registro. Busca una sección que liste todas las pruebas unitarias. Estamos buscando el nombre de la prueba con una "x".

<img alt="captura de pantalla de un registro de compilación de muestra con los nombres de las pruebas desenfocados" src=https://user-images.githubusercontent.com/16547949/65922013-e740a200-e3b1-11e9-8151-faf52c30201e.png width=400 />

Si las verificaciones no aparecen o si las verificaciones están atascadas en progreso, hay algunas cosas que puedes hacer para intentar activarlas:

- Actualiza la página, es posible que el workflow se haya ejecutado y la página simplemente no se haya actualizado con ese cambio.
- Intenta hacer un commit en esta rama. Nuestro workflow se activa con un evento `push`, y hacer un commit en esta rama resultará en un nuevo `push`.
- Edita el archivo de workflow en GitHub y asegúrate de que no haya líneas rojas que indiquen un problema de sintaxis.


### :keyboard: Actividad: Corregir la prueba

1. Actualiza el contenido en la rama `ci` para que la prueba pase. Necesitas mirar los registros para ver qué causó que la prueba fallara.
2. **CCommit changes**.
3. Espera unos 20 segundos y luego actualiza esta página (la que estás siguiendo instrucciones). [GitHub Actions](https://docs.github.com/actions) se actualizará automáticamente al siguiente paso.
