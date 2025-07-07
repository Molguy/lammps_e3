# lammps_e3

Instructivo, archivos de entrada, auxiliares y log de la simulación del ejemplo 3,

Comandos para la ejecucion en terminal:

    gfortran Micelas3DCurso.f -o datagen3D  

. para salir escribe **:wq** .

    vim def.micelle3D
.

    ./datagen3D < def.micelle3D > data.micelle3D
.

    mpirun -np 4 lmp_mpi < in.micelle
.

    ovito movie.lammpsEq 
