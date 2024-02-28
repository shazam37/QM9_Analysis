# QM9_Analysis

QM9 is a dataset containing quantum chemical properties (at DFT level) for a relevant, consistent, and comprehensive chemical space of small organic molecules. The database serves as the benchmarking of existing machine learning methods, development of new such methods, such as hybrid quantum mechanics/machine learning, and systematic identification of structure-property relationships.

The dataset contains 134000 molecules with up to 9 heavy atoms. It contains the structure information (SMILES), and additionally the following features:

I.     Property      Unit                                Description

 1      tag           -                gdb9; string constant to ease extraction via grep
 
 2     index          -               Consecutive, 1-based integer identifier of molecule
 
 3       A           GHz                            Rotational constant A
 
 4       B           GHz                            Rotational constant B
 
 5       C           GHz                            Rotational constant C
 
 6       mu          Debye                              Dipole moment
 
 7      alpha         Bohr^3                      Isotropic polarizability
 
 8       homo         Hartree              Energy of Highest occupied molecular orbital (HOMO)
 
 9       lumo        Hartree               Energy of Lowest occupied molecular orbital (LUMO)
 
10       gap         Hartree                   Gap, difference between LUMO and HOMO

11        r2           Bohr^2                       Electronic spatial extent

12       zpve          Hartree                     Zero point vibrational energy

13        U0           Hartree                        Internal energy at 0 K

14         U            Hartree                      Internal energy at 298.15 K

15         H              Hartree                        Enthalpy at 298.15 K

16         G               Hartree                     Free energy at 298.15 K

17         Cv           cal/(mol K)                    Heat capacity at 298.15 K


My objective was to analyse the dataset in different ways and to train a neural network model for predicting any 3 properties using the other remaining properties. 

I obtained the dataset from chainer_chemistry library. The library comes loaded with modules that preprocess the data and helps uploading it in the form of a dataframe. 

For fun, I have converted the SMILES string to Morgan fingerprint bit vectors to see if we can utilise that information for model training. Suffice to say, we cant't :P 
