Ejemplo 3. Surfactantes en solución bifásica, simulación en 3D

La carpeta debe contener:
 a) in.micelle3D
 b) def.micelle3D
 c) Micelas3DCurso.f

1. Compilar el programa Micelas3DCurso.f usando:
 1) gfortran Micelas3DCurso.f -o datagen3D -
 2) se generará un ejecutable denominado datagen3D que sirve para generar archivos de estructura.

2. Generar un archivo con 10% aceite, para lo cual se deberá revisarr el archivo def.micelle3D:
 1) editalo con Bloc de Notas o usa vim en terminal: vim def.micelle3D
 2) será en la linea donde dice "% of oil - like solvent"
	- para salir escribe :wq o :q! y Enter -

3. Ejecutar el programa:
 1) - ./datagen3D < def.micelle3D > data.micelle3D -

4. Ejecutar lammps usando:
 1) ./lmp_mpi < in.micelle3D
 2) Se generara un lammpsEq

5. Visualizar en Ovito y generar una película para lo cual se debe:
   a) Abrir Ovito.app
   b) Cargar el archivo movie.lammpsEq mediante “Load File”
      - escribir ovito movie.lammpsEq -
   c) Definir tipos y tamaños de partículas en “Particle types”
      Type 1 color blanco y 0.25 de Radio
      Type 2 color rojo y 0.75 de Radio
      Types 3*6 color azul y 0.5 de Radio
      Type 7 color amarillo y 0.2 de Radio
   d) Activar la casilla “File contains time series”
      - esta casilla siempre se encuentra activa en versiones nuevas -
   e) En la parte superior, presiona la pestaña “Rendering” y selecciona “Complete animation”
   f) En la parte inferior activa "Save to file" y presiona "Choose" para asignar directorio, nombre y formato 
   g) Mas abajo presiona “Render Active Viewport”, espera el 100% para generar el archivo y guarda la sesión ovito

