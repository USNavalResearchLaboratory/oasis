this has the sq version of OASIS. The driver program is main_driver_sq.f
compilation guidance as done at NRL is given in compile.txt (I think we have Intel Fortran)

SQ means that the flux and photoelectron ionization
is according to solomon and qian (jgr, 2005). But it doesn't do Xrays very well
so is only really valid for quiet conditions
 there are 8 inputs files (see *.inp) for: 
	NO, H2O, O2D (O2-singlet delta), O3, and H2O and then for the rate coeffs,
the solar spectrum and then a driver input where you set the geographic parameters (oasis_equ.inp)
Its called equ because its set for Kwajelein ("equator") which is where M. Friedrich had a rocket launch in 2004 and
  for which I spent some time discussing in my paper
The neutral inputs are read in and interpolated (in various ways) in neutrals.f
The rates file should have 31 ions- this is a change from published versions where I included O- as a 3rd
   negative ion and which I think wasn't done properly

Note- it may look like you need atomic oxygen, but that is now provide by NRLMSIS2.0 along with H.
Note, make sure you have gtd8 compiled- that is the NRLMSIS driver and is called by read_msis.f
