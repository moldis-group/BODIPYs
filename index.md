---
layout: default
---

## BODIPYs dataset

The BODIPYs dataset [Ref-1] contains (gas phase) DFT level geometries and TDDFT level properties of the first electronic excited state of 77412 molecules derived from the BODIPY dye by combinatorial substitution.

***

## BODIPYs

This BODIPYs data set contains  3 files:  
[77k_BODIPYs_properties.txt.bz2](https://drive.google.com/file/d/1NAor-rHYtVwCat4Ms3IkdyDL27alqu6l/view?usp=sharing) (4 MB)    
[77k_BODIPYs_DFT_geom.xyz.bz2](https://drive.google.com/file/d/1nX_duEd0nnyMVqenR4mhp7PH1mZ_4dAy/view?usp=sharing) (40 MB)     
[77k_BODIPYs_PM7_geom.xyz.bz2](https://drive.google.com/file/d/1erNz0F6w4iGybOgtwI3-ccCUcnHzzVrb/view?usp=sharing) (44 MB)     

Unzip the files in linux as
```
bunzip2 -f 77k_BODIPYs_properties.txt.bz2
bunzip2 -f 77k_BODIPYs_DFT_geom.xyz.bz2
bunzip2 -f 77k_BODIPYs_PM7_geom.xyz.bz2
```

77k_BODIPYs_properties.txt --> Contains properties of 77412 BODIPYs, calculated at RIJCOSX-CAM-B3LYP/def2-TZVP level

Column 01 --> names of the molecules made up using site (s_nn) and type of substitution (g_mm)
Example: g_01_s_7_00002 implies there is a substitution at site 7 by group 01. The last digits (here _00002) are for indexing and can be ignored.  Long names (Hextuply/Septuply-substituted) do not contain '_'.

Column 02 --> T/V in training/validation set in ML

TD-DFT Properties
Column 03 --> State (Always 1)
Column 04 --> S0 -> S1 Excitation energy (in cm^-1)
Column 05 --> S0 -> S1 Excitation energy (in nm)
Column 06 --> S0 -> S1 Excitation energy (in au)
Column 07 --> S0 -> S1 Excitation energy (in eV)

Column 08 --> oscillator strength of S0 -> S1 excitation

Transition electric dipole moments
Column 09 --> T^2 (in au^2)
Column 10 --> TX (in au)
Column 11 --> TY (in au)
Column 12 --> TZ (in au)

DFT Ground State Energy
Column 13 --> SCF energy (in au)

PM7 properties
Column 14 --> HOMO (in eV)
Column 15 --> LUMO (in eV)
Column 16 --> Heat of formation (in kcal/mol)

77k_BODIPYs_DFT_geom.xyz --> Contains coordinates of 77412 BODIPYs relaxed at B3LYP/def2-SVP level.
77k_BODIPYs_PM7_geom.xyz --> Contains coordinates of 77412 BODIPYs relaxed using PM7.

Molecule ordering is consistent across all files. BODIPYs' order of appearance in all files is as follows:
```
==================================================================================================================================
|Serial|  TYPE of BODIPY      | Entries |      Appearance in       |      Appearance in           |      Appearance in           |
|  No. |                      |         |77k_BODIPYs_properties.txt|   77k_BODIPYs_DFT_geom.xyz   |   77k_BODIPYs_PM7_geom.xyz   |
==================================================================================================================================
|  1.  | Unsubstituted        |    1    | Line     1               | Line       1 -- Line      23 | Line       1 -- Line      23 |
|  2.  | Singly-substituted   |   184   | Line     2 -- Line   185 | Line      24 -- Line    5135 | Line      24 -- Line    5135 |
|  3.  | Doubly-substituted   |  22287  | Line   186 -- Line 22472 | Line    5136 -- Line  737727 | Line    5136 -- Line  737727 |
|  4.  | Triply-substituted   |  10999  | Line 22473 -- Line 33471 | Line  737728 -- Line 1154010 | Line  737728 -- Line 1154010 |
|  5.  | Quadruply-substituted|  10990  | Line 33472 -- Line 44461 | Line 1154011 -- Line 1624604 | Line 1154011 -- Line 1624604 |
|  6.  | Quintuply-substituted|  10982  | Line 44462 -- Line 55443 | Line 1624605 -- Line 2153455 | Line 1624605 -- Line 2153455 |
|  7.  | Hextuply-substituted |  10986  | Line 55444 -- Line 66429 | Line 2153456 -- Line 2733543 | Line 2153456 -- Line 2733543 |
|  8.  | Septuply-substituted |  10983  | Line 66430 -- Line 77412 | Line 2733544 -- Line 3368359 | Line 2733544 -- Line 3368359 |
==================================================================================================================================
```


### B3LYP/6-31G(2df,p) geometries
[SI_DFT_geo.xyz](https://drive.google.com/file/d/1Kr9ZdYw503QsGT8qO2bid8wWQGQB-401/view?usp=sharing) Contains Cartesian coordinates of 130,831 molecules relaxed at B3LYP/6-31G(2df,p) level. These geometries are collected from the QM9 dataset reported in the [Ref-2](https://www.nature.com/articles/sdata201422)

### mPW1PW91/6-311+G(2d,p) @ B3LYP/6-31G(2df,p) NMR data
[SI_DFT_NMR.txt](https://drive.google.com/file/d/13vqG1zTsemLgfZP635pcAHjARhqDzJ8I/view?usp=sharing) For each molecule in SI_DFT_geo.xyz, contains number of atoms, followed by molecule name and isotropic shielding tensors per atom in the molecule in Gas, CCl4, THF, Acetone, Methanol and DMSO respectively, obtained at mPW1PW91/6-311+G(2d,p) level.   

####  mPW1PW91/6-311+G(2d,p) @ B3LYP/6-31G(2df,p) <sup>13</sup>C shielding for tetramethylsilane (TMS) [in ppm] 
```
Gas      - 186.9704
CCl4     - 187.2352
THF      - 187.4958
Acetone  - 187.5949
Methanol - 187.6181
DMSO     - 187.6304
```

### PM7 geometries
[SI_baseline_geo.xyz](https://drive.google.com/file/d/1TgH_cbABKPMq9wG2wnftwDO_wl3XYTk2/view?usp=sharing) Contains Cartesian coordinates of 130,831 molecules relaxed at the PM7 level.   

### B3LYP/STO-3G @ PM7 NMR data
[SI_baseline_NMR.txt](https://drive.google.com/file/d/16uw_v2VlPYK57NRjDnxVYi_hfspRLQdi/view?usp=sharing) For each molecule in SI_baseline_geo.xyz, contains number of atoms, followed by molecule name and isotropic shielding tensors per atom in the molecule in gas phase obtained at B3LYP/STO-3G level.

####  B3LYP/STO-3G @ PM7 <sup>13</sup>C shielding for tetramethylsilane (TMS) [in ppm] 
```
Gas      - 232.4620
```

***

## Case studies

### Geometries

| [SI_12Drugs_DFT_geo.xyz](data/SI_12Drugs_DFT_geo.xyz)               | Contains 12 Drug molecules relaxed at B3LYP/6-31G(2df,p) level.                            
| [SI_12Drugs_baseline_geo.xyz](data/SI_12Drugs_baseline_geo.xyz)     | Contains 12 Drug molecules relaxed at PM7 level.                                           
| [SI_40Drugs_DFT_geo.xyz](data/SI_40Drugs_DFT_geo.xyz)               | Contains 40 Drug molecules relaxed at B3LYP/6-31G(2df,p) level.                            
| [SI_40Drugs_baseline_geo.xyz](data/SI_40Drugs_baseline_geo.xyz)     | Contains 40 Drug molecules relaxed at PM7 level.                                           
| [SI_PAH_DFT_geo.xyz](data/SI_PAH_DFT_geo.xyz)                       | Contains 5 Polycyclic Aromatic Hydrocarbons molecules relaxed at B3LYP/6-31G(2df,p) level. 
| [SI_PAH_baseline_geo.xyz](data/SI_PAH_baseline_geo.xyz)             | Contains 5 Polycyclic Aromatic Hydrocarbons molecules relaxed at PM7 level.                
| [SI_GDB10to17_DFT_geo.xyz](data/SI_GDB10to17_DFT_geo.xyz)           | Contains 200 molecules from GDB10 to GDB17 molecules relaxed at B3LYP/6-31G(2df,p) level.  
| [SI_GDB10to17_baseline_geo.xyz](data/SI_GDB10to17_baseline_geo.xyz) | Contains 200 molecules from GDB10 to GDB17 molecules relaxed at PM7 level.                

### NMR data

| [SI_12Drugs_DFT_NMR.txt](data/SI_12Drugs_DFT_NMR.txt) 	| For each molecule in SI_12Drugs_DFT_geo.xyz, contains number of atoms, molecule name and isotropic shielding tensors per atom, in Gas phase at mPW1PW91/6-311+G(2d,p).       
| [SI_12Drugs_baseline_NMR.txt](data/SI_12Drugs_baseline_NMR.txt) 	| For each molecule in SI_12Drugs_baseline_geo.xyz, contains number of atoms, molecule name and isotropic shielding tensors per atom, in Gas phase at B3LYP/STO-3G level.      
| [SI_40Drugs_DFT_NMR.txt](data/SI_40Drugs_DFT_NMR.txt) 	| For each molecule in SI_40Drugs_DFT_geo.xyz, contains number of atoms, molecule name and isotropic shielding tensors per atom, in Gas phase at mPW1PW91/6-311+G(2d,p).         
| [SI_40Drugs_baseline_NMR.txt](data/SI_40Drugs_baseline_NMR.txt) 	| For each molecule in SI_40Drugs_baseline_geo.xyz, contains number of atoms, molecule name and isotropic shielding tensors per atom, in Gas phase at B3LYP/STO-3G level.          
| [SI_PAH_DFT_NMR.txt](data/SI_PAH_DFT_NMR.txt) 	| For each molecule in SI_PAH_DFT_geo.xyz, contains number of atoms, molecule name and isotropic shielding tensors per atom, in Gas phase at mPW1PW91/6-311+G(2d,p).           
| [SI_PAH_baseline_NMR.txt](data/SI_PAH_baseline_NMR.txt) 	| For each molecule in SI_PAH_baseline_geo.xyz, contains number of atoms, molecule name and isotropic shielding tensors per atom, in Gas phase at B3LYP/STO-3G level.          
| [SI_GDB10to17_DFT_NMR.txt](data/SI_GDB10to17_DFT_NMR.txt) 	| For each molecule in SI_GDB10to17_DFT_geo.xyz, contains number of atoms, molecule name and isotropic shielding tensors per atom, in Gas phase at mPW1PW91/6-311+G(2d,p).            
| [SI_GDB10to17_baseline_NMR.txt](data/SI_GDB10to17_baseline_NMR.txt) 	| For each molecule in SI_GDB10to17_baseline_geo.xyz, contains number of atoms, molecule name and isotropic shielding tensors per atom, in Gas phase at B3LYP/STO-3G level. 

***

## Revision notes

_19 August 2021: First upload
***

## References
[Ref-1] [_Revving up <sup>13</sup>C NMR shielding predictions across chemical space: benchmarks for atoms-in-molecules kernel machine learning with new data for 134 kilo molecules_](https://doi.org/10.1088/2632-2153/abe347)            
Amit Gupta, Sabyasachi Chakraborty and Raghunathan Ramakrishnan     
Mach. Learn.: Sci. Technol. 2 (2021) 035010     
[Supplementary Information to the article (PDF)](data/SI.pdf)

[Ref-2] [_Quantum chemistry structures and properties of 134 kilo molecules_](http://www.nature.com/articles/sdata201422)          
Raghunathan Ramakrishnan, Pavlo Dral, Matthias Rupp, O. Anatole von Lilienfeld      
Scientific Data 1, Article number: 140022 (2014).    
