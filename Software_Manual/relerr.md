# MATH 5610 Software Manual

### Subroutine: [_relerr_](../relerr.f90)

**Author:** Jackson Reid

**Language:** Fortran. The code can be compiled using the GNU Fortran compiler (gfortran).

This routine can be linked to a program with the commands
```
    $ gfortran -c relerr.f90
    $ gfortran myprogram.f90 relerr.o
```

Or, a library can be created from this routine

```
    $ gfortran -c relerr.f90
    $ ar rcv mylib relerr.o
```

**Description:** This routine will compute the relative error between two numbers.

**Inputs:** 

​        _approx_ : REAL*8 -- the value whose error is calculated

​	_exact_ : REAL*8 -- the value respect to which the error is calculated

**Outputs:** 

​	_error_ : REAL*8 -- the absolute error of the approximation with respect to the exact value

**Example Usage:** 

```
      CALL relerr(approx, exact, error)
      WRITE(*,*) error
```

**Last Modified:** January/2018
