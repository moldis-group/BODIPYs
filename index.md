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

***

## 77k_BODIPYs_properties.txt contains properties of 77412 BODIPYs, calculated at RIJCOSX-CAM-B3LYP/def2-TZVP level

Column 01 --> names of the molecules made up using site (s_nn) and type of substitution (g_mm)

Example: g_01_s_7_00002 implies there is a substitution at site 7 by group 01. The last digits (here _00002) are for indexing and can be ignored.  Long names (Hextuply/Septuply-substituted) do not contain '_'.

Column 02 --> T/V in training/validation set in ML

#### TD-DFT Properties
Column 03 --> State (Always 1)
Column 04 --> S0 -> S1 Excitation energy (in cm^-1)
Column 05 --> S0 -> S1 Excitation energy (in nm)
Column 06 --> S0 -> S1 Excitation energy (in au)
Column 07 --> S0 -> S1 Excitation energy (in eV)
Column 08 --> Oscillator strength of S0 -> S1 excitation
Column 09 --> T^2 (in au^2), square of transition dipole moment
Column 10 --> TX (in au), x-component of transition dipole moment vector
Column 11 --> TY (in au), y-component of transition dipole moment vector
Column 12 --> TZ (in au), z-component of transition dipole moment vector

#### DFT Ground State Energy
Column 13 --> SCF energy (in au)

#### PM7 properties
Column 14 --> HOMO (in eV)
Column 15 --> LUMO (in eV)
Column 16 --> Heat of formation (in kcal/mol)

77k_BODIPYs_DFT_geom.xyz --> Contains coordinates of 77412 BODIPYs relaxed at B3LYP/def2-SVP level.
77k_BODIPYs_PM7_geom.xyz --> Contains coordinates of 77412 BODIPYs relaxed using PM7.

Molecule ordering is consistent across all files. BODIPYs' order of appearance in all files is as follows

***

| **Type**                     | **# entries**
| Unsubstituted            | 1       
| Singly-substituted       | 184      
| Doubly-substituted       | 22287     
| Triply-substituted       | 10999     
| Quadruply-substituted    | 10990     
| Quintuply-substituted    | 10982     
| Hextuply-substituted     | 10986     
| Septuply-substituted     | 10983     

## Revision notes

_19 August 2021: First upload_

***

## References
[Ref-1] [_Revving up <sup>13</sup>C NMR shielding predictions across chemical space: benchmarks for atoms-in-molecules kernel machine learning with new data for 134 kilo molecules_](https://doi.org/10.1088/2632-2153/abe347)            
Amit Gupta, Sabyasachi Chakraborty and Raghunathan Ramakrishnan     
Mach. Learn.: Sci. Technol. 2 (2021) 035010     
[Supplementary Information to the article (PDF)](data/SI.pdf)

***
