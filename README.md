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
