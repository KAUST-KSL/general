# SLURM Help

In progress

## Example of reserving 32 cores

In this case we declare 32 processes per node and 16 processes per socket
We execute 32 processes by declaring *-n 32* in the *srun* command

```bash
#!/bin/bash

#SBATCH --partition=workq
#SBATCH -t 10
#SBATCH -A k01
#SBATCH  --ntasks=32
#SBATCH --ntasks-per-node=32
#SBATCH --ntasks-per-socket=16
#SBATCH   -J test
#SBATCH -o out_%j
#SBATCH -e err_%j


time srun -n 32 --hint=nomultithread hello

exit 0
```

Do not forget the **--hint=nomultithread** to disable multithreading

[Download script](https://raw.githubusercontent.com/KAUST-KSL/general/master/Slurm/slurm_example.sh)

{% include slurm_example.sh %}
