# SumatraNext

## Descripción del Proyecto
Este es un fork del proyecto de código abierto SumatraPDF, con el objetivo de modernizarlo y añadir nuevas funcionalidades, manteniendo su filosofía de ser un lector de documentos ligero y rápido. Nuestra misión es crear un "SumatraNext" que combine la eficiencia del original con una experiencia de usuario actualizada y características innovadoras.

## Roadmap
Nuestro roadmap se gestionará a través de los Issues de GitHub. Aquí se detallarán las fases y los hitos principales del proyecto.

## Cómo Compilar
Para compilar SumatraNext, necesitarás Visual Studio Build Tools 2022.

1.  **Abrir la Símbolo del sistema para desarrolladores:**
    *   Busca en el menú de inicio de Windows "Símbolo del sistema para desarrolladores para VS 2022" (o "Developer Command Prompt for VS 2022") y ábrelo.

2.  **Navegar al directorio del proyecto:**
    *   En esa ventana de comandos, navega hasta la raíz de tu proyecto `SumatraNext`.
        ```bash
        cd C:\Users\ercep\Documents\proyectos_software\pdf_reader_2
        ```

3.  **Compilar la solución:**
    *   Una vez en la raíz del proyecto, ejecuta el siguiente comando para compilar la solución (puedes cambiar `Release` por `Debug` y `x64` por `Win32` si lo necesitas):
        ```bash
        msbuild vs2022\SumatraPDF.sln /p:Configuration=Release /p:Platform=x64
        ```

4.  **Encontrar y Ejecutar el ejecutable:**
    *   Si la compilación es exitosa, el archivo `SumatraPDF.exe` se generará en una ruta similar a:
        `C:\Users\ercep\Documents\proyectos_software\pdf_reader_2\bin\Release\SumatraPDF.exe`
    *   Puedes navegar a esa carpeta con el Explorador de Archivos y hacer doble clic en `SumatraPDF.exe` para ejecutarlo.

**Nota:** Este proyecto utiliza un programa Go en el directorio `do` para automatizar tareas comunes. Ejecuta `doit.bat` para usarlo.

## Versionamiento y Changelog
Utilizaremos el Versionamiento Semántico (SemVer) para gestionar las versiones del proyecto. El historial de cambios se mantendrá en el archivo `CHANGELOG.md`.

## Contribuciones
¡Damos la bienvenida a nuevas contribuciones! Si deseas unirte al proyecto, por favor, consulta nuestro `context.md` para entender nuestra dirección y el `CHANGELOG.md` para ver los cambios recientes.

## Licencia
[Pendiente de definir si se mantiene la licencia original o se adapta]