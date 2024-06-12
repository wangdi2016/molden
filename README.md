# Compile Molden on macosx arm using gfortran

gfortran -O3 -funroll-loops  -c -o src/molden.o src/molden.f
src/molden.f:8751:22:

 8750 |       call parptr(1,freq,fdum,idum)
      |                    2
 8751 |       call parptr(143,exx,fdum,ihasd)
      |                      1
Error: Type mismatch between actual argument at (1) and actual argument at (2) (REAL(8)/REAL(4)).
src/molden.f:8752:22:

## fixed solution
https://bugs.gentoo.org/724556

![Screenshot 2024-06-12 at 2 42 32 AM](https://github.com/wangdi2016/molden/assets/49001003/0157228b-5458-4a7e-a558-1e428579a8f1)
