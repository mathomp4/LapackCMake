# Lapack Cmake

A simple Lapack test

## How to run

```
mkdir build
cd build
cmake ..
make
```

## Example Output

### Accelerate

Built with `cmake .. -DBLA_VENDOR=Apple`

```
❯ ./sgesv_example.exe
Solution (x1, x2): 1.0000, 3.0000
[❯](❯) ./SGEmm_examplE.EXE
   15.0000000       42.0000000       69.0000000
   18.0000000       54.0000000       90.0000000
   21.0000000       66.0000000       111.000000
```

### OPenBLAS

Built with `cmake .. -DBLA_VENDOR=OpenBLAS`

```
❯ ./sgesv_example.exe
Solution (x1, x2): 1.0000, 3.0000
❯ ./sgemm_example.exe
   15.0000000       42.0000000       69.0000000
   18.0000000       54.0000000       90.0000000
   21.0000000       66.0000000       111.000000
```

### MKL

Build with `cmake .. -DBLA_VENDOR=Intel10_64lp_seq`

```
❯ ./sgesv_example.exe
Solution (x1, x2): 1.0000, 3.0000
❯ ./sgemm_example.exe
   15.0000000       42.0000000       69.0000000
   18.0000000       54.0000000       90.0000000
   21.0000000       66.0000000       111.000000
```
