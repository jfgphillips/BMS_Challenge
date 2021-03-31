# Bristol Myers Squibb Molecular translation competition

## Competition Introduction

In a technology-forward world, sometimes the best and easiest tools are still pen and paper. Organic chemists frequently draw out molecular work with the Skeletal formula, a structural notation used for centuries. Recent publications are also annotated with machine-readable chemical descriptions (InChI), but there are decades of scanned documents that can't be automatically searched for specific chemical depictions. Automated recognition of optical chemical structures, with the help of machine learning, could speed up research and development efforts.

Unfortunately, most public data sets are too small to support modern machine learning models. Existing tools produce 90% accuracy but only under optimal conditions. Historical sources often have some level of image corruption, which reduces performance to near zero. In these cases, time-consuming, manual work is required to reliably convert scanned chemical structure images into a machine-readable format.

Bristol-Myers Squibb is a global biopharmaceutical company working to transform patients' lives through science. Their mission is to discover, develop, and deliver innovative medicines that help patients prevail over serious diseases.

In this competition, you’ll interpret old chemical images. With access to a large set of synthetic image data generated by Bristol-Myers Squibb, you'll convert images back to the underlying chemical structure annotated as InChI text.

Tools to curate chemistry literature would be a significant benefit to researchers. If successful, you'll help chemists expand access to collective chemical research. In turn, this would speed up research and development efforts in many key fields by avoiding repetition of previously published chemistries and identifying novel trends via mining large data sets.

Photo by Terry Vlisidis on Unsplash


## Understanding InChI
* The international chemical identifier...
*	contains 9 parts that are related
*	those parts are separated by a "/".
*	not all the parts are always present (see example below)

*	Example:
1. InChI=1S/ is the version which can be ignored since all target labels have it.
2. C21H30O4/ is the chemical formula, e.g. (21 carbon atoms, 30 hydrogen atoms and 4 oxygen atoms)
3. c1-12(22)25-14-6-8-20(2)13(10-14)11-17(23)19-15-4-5-18(24)21(15,3)9-7-16(19)20/ is the connection layer, i.e. in which order the atoms are connected.
4. h13-16,19H,4-11H2,1-3H3/ is the hydrogen layer, i.e. in how the hydrogens atoms are connected. 
5. t13-,14+,15+,16-,19-,20+,21+/ is the tetrahedral stereochemistry of atoms.
6. m1/ is the tetrahedral stereochemistry of allenes.
7. s1 is the type of stereochemistry information.
8. /b not present here
9. /i not present here


## recommended readings 
1. Molecular Structure Extraction From Documents Using Deep Lerning: https://arxiv.org/ftp/arxiv/papers/1802/1802.04903.pdf
  - data extraction
  - information processing
2. Detecting Compound Vertices (graph theory) https://www.kaggle.com/thomaskonstantin/detecting-compound-vertices-molecular-translation
3. SMIlES solution to a programming challenge winning solution: https://dacon.io/competitions/official/235640/talkboard/402474?page=1&dtype=recent&ptype=pub
4. Genetic Algorithm for Naive Baseline submission from kaggle (score 69): https://www.kaggle.com/andypenrose/genetic-algorithm-for-naive-baseline
5. Academic paper **Learning continuous and data-driven molecular descriptors by translating equivalent chemical representations**: https://pubs.rsc.org/en/content/articlepdf/2019/sc/c8sc04175j
## Extending the trainining data set
1. PubChem - 57 million molecules https://pubchem.ncbi.nlm.nih.gov/
2. Wikidata - 12 thousand compound + image e.g. https://www.wikidata.org/wiki/Q27075960

## standard framework for publishing structural molecules in academic journals ACS 1996
Item          | Settings
------------- | -------------
chain angle   | 120 degrees
bond spacing  | 18% of width
fixed length  | 14.4 pt (0.2 in.)
bold width    | 2.0 pt (0.0278 in.)
line width    |	0.6 pt (0.0083 in.)
margin width  | 1.6 pt (0.0222 in.)
hash spacing  | 2.5 pt (0.0345 in.)

Item	| 	Settings
------|------------------
font	| 	Helvetica (Mac), Arial (PC)
size	| 	10 pt
Under |   the preferences choose:
units |	 	points
tolerances	| 	3 pixels
