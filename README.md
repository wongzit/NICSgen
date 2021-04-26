# NICSgen v1.1
![NICSgen_full](https://user-images.githubusercontent.com/41381763/116081377-28578000-a6d5-11eb-8408-56438ae5812a.png)
Input file generator for NICS calculation.
**NICSgen homepage** https://www.wangzhe95.net/program-nicsgen

First release: 2021-04-25

Last update: 2021-04-27

Author: Zhe Wang

## Update history
### v1.1 (2021-04-27) Main features
1. Add Bq atoms in the center of specified atoms.
2. NICS(n) calculation is supported.

### v0.2 (2021-04-26)
1. First beta release.

## Platform
### For all platform
Python source code is provided, if your computer already installed Python IDE, you can run NICSgen with:

`python3 NICSgen_v11_source.py`

Executable files for macOS/Linux/Windows are in **execufiles.zip**.

**NOTICE:** Python 3.7 or newer is recommended, NICSgen may not work normally under Python 2.

### For macOS
Executable file **NICSgen_v11_mac** has been tested on macOS Catalina 10.15.7 (Intel Mac) and Big Sur 11.2.3 (Intel/M1 Mac).

### For Linux
Before running for the first time, you may need to add permission by:
`chmod +x ./path_to_NICSgen/NICSgen_v11_linux`

Add following command to environmental variables (for bash):
`alias nicsgen=./path_to_NICSgen/NICSgen_v11_linux`
and you can run NICSgen by `nicsgen`.

### For Microsoft Windows
Executable file **NICSgen_v11_win.exe** has been tested on Windows 10 Education (x64) with Intel Core i7-10700. Double click to run it.

## How to use
**NOTICE:** NICSgen only generates input file for Gaussian. More details in program manual.

1. Prepare the input file including calculation route lines, title, charge and spin multiplicity, and Cartesian coordinate.

```
%nprocshared=8
%mem=10GB
#p nmr=giao rb3lyp/6-31+g(d)

Title Card Required

0 1
 H                  1.90900000   -0.93500000    0.91600000
 C                  1.07900000   -0.51700000    1.45200000
 C                 -1.07900000    0.51700000    2.83500000
 C                  0.00000000    0.00000000    0.74500000
 C                  1.07900000   -0.51700000    2.83500000
 C                  0.00000000    0.00000000    3.53100000
 C                 -1.07900000    0.51700000    1.45200000
 H                  1.91500000   -0.92500000    3.36700000
 H                  0.00000000    0.00000000    4.60300000
 H                 -1.90900000    0.93500000    0.91600000
 H                 -1.91500000    0.92500000    3.36700000
 C                  0.00000000    0.00000000   -0.74500000
 C                  0.00000000    0.00000000   -3.53100000
 C                  1.07900000    0.51700000   -1.45200000
 C                 -1.07900000   -0.51700000   -1.45200000
 C                 -1.07900000   -0.51700000   -2.83500000
 C                  1.07900000    0.51700000   -2.83500000
 H                  1.90900000    0.93500000   -0.91600000
 H                 -1.90900000   -0.93500000   -0.91600000
 H                 -1.91500000   -0.92500000   -3.36700000
 H                  1.91500000    0.92500000   -3.36700000
 H                  0.00000000    0.00000000   -4.60300000

```

2. Drag the input file to the program, and press Enter. 
```
Please specify the original input file path:
(eg.: /NICSgen/example/biphenyl.gjf)
(user input): /Users/path_to_NICSgen/example/biphenyl.gjf
```

3. Specify the plane which ring would be investigated. Please input 3 or more atoms number (as defined in input file).
```
Please specify the target atoms number:
(user input): 13 14 15
```

4. Specify the altitude over the ring plane. The altitude is defined in angstrom.
```
Please specify the altitude n of NICS(n):
(user input): 1
```

5. If you want to add Bq atoms for other rings, please input “y” and press enter, or input “n” to quit the program.
```
Continue to add other Bq atoms? (y/n):
(user input): y
```

6. New input file named with **xxx_NICS.gjf** would be generated.  You can submit this input file for Gaussian calculation. Enjoy!

## From author
If you found any bugs, please contact me (wongzit@yahoo.co.jp).

More information about me, please check my [personal website](https://www.wangzhe95.net).

 **Hope you enjoy this program!**
