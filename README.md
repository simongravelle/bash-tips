# Bash tips

## Read a number from a file

```
number=$( awk '{print $0}' number.dat )
```

## Interact with the GROMACS prompt

```
gmx trjconv -f prod.xtc -s prod.tpr -o prod.mol.xtc -pbc mol<<EOF
    0
EOF
```

## For loop

```
for i in {1..5}
do
  true
done
```
## Read file

```
while IFS= read -r line
do
    echo "$line"
done < file.txt
```
## Read end of a string

```
string="blabla"
sub-string=${string:3:0-1}${string:0-1}
```

## Interact with LAMMPS variable

mpirun -np 16 lmp_mpi -in input.lammps -var f 0.01

## Replace in a file

```
newline='variable  = '$a  
oldline=$(cat myfile| grep 'variable  = ')  
sed -i '/'"$oldline"'/c\'"$newline" myfile
```
