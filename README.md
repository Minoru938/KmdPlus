# KmdPlus

This module contains a class for treating kernel mean descriptor, and a function for generating descriptors with summary statistics. the kernel mean descriptor is a general class of materials descriptors, motivated by the machine learning theory of kernel mean embedding. Unlike ordinary descriptors, the kernel mean embedding can retain all information about the distribution of component features in the vectorization process. This module can be readily used generically to create the kernel mean descriptor for any mixture systems. The function for the inverse translation of the kernel mean descriptor is also implemented in this module.
 
Using a tutorial.ipynb file, users can generate kernel mean descriptors and summary statistical descriptors respectively for the chemical composition of all stable inorganic compounds (35,463 compounds) listed in the [Materials Project](https://materialsproject.org). In the tutorial, the kernel mean descriptors of these chemical compositions are inverse-translated to composition ratios using a function in KmdPlus.py, showing that the reconstruction error (MAE) between the original composition ratios used for generating the kernel mean descriptors and the inverse-translated composition ratios is nearly zero (less than 10<sup>-12</sup>, which considerd to be the numerical error of the computation). Furthermore, users can generate PCA maps of both descriptors, which is identical to Figure 2A of [our paper](https://doi.org/10.1103/PhysRevB.108.134107).

For more details, please see our paper:
[Representation of materials by kernel mean embedding](https://doi.org/10.1103/PhysRevB.108.134107) (Accepted 6 September 2023).


# Usage
 
1. First install the dependencies listed below.

2. Clone the `KmdPlus` github repository:
```bash
git clone https://github.com/Minoru938/KmdPlus.git
```

3. `cd` into `KmdPlus` directory.

4. Run `jupyter notebook` and open `tutorial.ipynb` to demonstrate `KmdPlus`.

# Dependencies

For KmdPlus.py:

* pandas version =  1.5.1
* numpy version = 1.23.5
* pymatgen version = 2022.11.7
* scipy version = 1.8.1
* qpsolvers version = 2.6.0
* quadprog version = 0.1.11

For tutorial.ipynb

* matplotlib version = 3.6.2
* scikit-learn version = 1.1.3

# Environment of author
* Python 3.9.12
* macOS Ventura 13.2.1

# Reference

1. [Materials Project]: A. Jain, S. P. Ong, G. Hautier, W. Chen, W. D. Richards, S. Dacek, S. Cholia, D. Gunter, D. Skinner, G. Ceder, et al., Commentary: The materials project:
A materials genome approach to accelerating materi- als innovation, APL materials 1 (1) (2013) 011002.

2. [Kernel mean embedding]: K. Muandet, K. Fukumizu, B. Sriperumbudur, & B. Schölkopf, Kernel mean embedding of distributions: A review and beyond. arXiv preprint arXiv:1605.09522 (2016).

