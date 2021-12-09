There are five input files for the constituents (no, co2, o3, h2o, and o2(singlet delta).
The others are given my MSIS2 (gtd8d). Make sure you have that available- See
  Emmert et al., Earth and Space Science, (2021), doi:10.1029/2020EA001321

There are 4 fism solar flux inputs and 4 hybrid (NRLFLARE for < 2 nm) inputs. The 4 digit number refers to the hhmm of the day- basically the peak of the flare. Four flares are provided
but one can construct these for any other times using the flare save files that are provided.
The new photoelectron model is implemented in read_specsqx_p1.f

There is one rates.inp file for the reaction rate coefficients.

Finally, the oasis_generic.inp is the driver input file. It is opened in the main driver
program (relion_file_sqx_p.f, the complicated
name reflects earlier model versions, you can rename it as you see fit) 

One should change the paths that
are given inside this file according to how you have things set up on your computer.
