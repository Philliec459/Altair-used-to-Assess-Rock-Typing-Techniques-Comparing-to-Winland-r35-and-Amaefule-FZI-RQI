# Interrogate Petrophysical data using Python's Interactive Altair
The objective of this project is to interactively interrogate Petrophysial data using Altair. 

### Data:

Clerke's Rosetta Stone Arab-D carbonate data(1) is show above in the display of our dataframe. This is Core analysis data. Permeability (and log10 of perm lPerm) and Porosity are the routine core analysis data. Clerke masterfully selected this dataset starting from 1,000's of inspected plug samples that was later culled down randomly selected the final sampless. This dataset is quite unique in that it covers the full range in poro-perm space and Petrophysical Rock types (PRTs). 



1) Clerke, E. A., Mueller III, H. W., Phillips, E. C., Eyvazzadeh, R. Y., Jones, D. H., Ramamoorthy, R., Srivastava, A., (2008) “Application of Thomeer Hyperbolas to decode the pore systems, facies and reservoir properties of the Upper Jurassic Arab D Limestone, Ghawar field, Saudi Arabia: A Rosetta Stone approach”, GeoArabia, Vol. 13, No. 4, p. 113-160, October, 2008. 

### Thomeer Parameters and Petrophysical Rock Types:

G1, Pd1 and BV1 are the Thomeer parameters for the first porosity system. G2, Pd2 and BV2 are the Thomeer parameters for the second porosity system. The following image relates the Thomeer parameters to the Capillary Pressure Curve. We used Matlab to would come up with an optimized set of Thomeer parameters while fitting High Pressure Mercury Injection data to the Thomeer hyperbola. 

![thomeer.png](thomeer.png)

Most macro rock has dual porosity and on the Pore Throat Distribution you would have two modes; one with a mode > 2 microns and a second (or third) mode < 2 microns. PRT M_1 is a macro rock with a second mode in the meso-porosity range where both pore systems can have oil saturations once the capillary pressure is great enough to drive out the water. The M_2 PRT is also a macro rock, but the second pore system is micro-porous and is too tight to have hydrocarbon. The Table below shows Clerke's description of his PRT's. 


![Rock-Types.png](Rock-Types.png)

The following are some example results:

![Rosetta_altair.png](Rosetta_altair.png)


We are using Conda on a mac and Altair works fairly well in a jupyter notebook. To run as pure python program altair_viewer must also be used to render the images to a html web page. We are low on the learning curve with Altair finding new capabilities each day. Consider this repository an example of where we are today. 

