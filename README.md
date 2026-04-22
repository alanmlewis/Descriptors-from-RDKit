
## **A brief description of chemical descriptors in RDKit**

These are listed in the order in which the descriptors appear in the list `Descriptors._descList`.

---
   The first 4 descriptors are the maximum and minimum EState (electrotopological state) indices, which aim to capture the electronic character and the topological environment of each skeletal atom in a molecule. These are taken from [J. Chem. Inf. Comput. Sci. 1991, 31, 76-82](https://pubs.acs.org/doi/pdf/10.1021/ci00001a012).

0. **MaxAbsEStateIndex**: Returns the maximum absolute EState index for the molecule
 
0. **MaxEStateIndex**: Returns the maximum EState index for the molecule
 
0. **MinAbsEStateIndex**: Returns the minimum absolute EState index for the molecule
 
0. **MinEStateIndex**: 	Returns the minimum EState index for the molecule
 
0. **QED**: QED stands for quantitative amount of similarity of drugs and the concept was first introduced by Richard Bickerton and colleagues. The empirical logic of the QED measure reflects the underlying distribution of molecular properties, including molecular weight, logP, topological polar surface area, number of hydrogen scavenger donors and acceptors, number of aromatic rings and rotating screens and the presence of unwanted chemicals.

0. **SPS**: Spatial score. SPS = sum(h*s*r*n*n) nSPS = SPS/a, where: h = Atom hybridisation term, s = Stereoisomeric term, r = Non-aromatic ring term, n = Number of heavy atom neighbors, a = Total number of heavy atoms in the molecule. Reference: [Krzyzanowski, A.; Pahl, A.; Grigalunas, M.; Waldmann, H. J. Med. Chem. _66_, 18, 12739–12750 (2023)](https://pubs.acs.org/doi/10.1021/acs.jmedchem.3c00689). 
   
0. **MolWt**: The average molecular weight of the molecule
 
0. **HeavyAtomMolWt**: The average molecular weight of the molecule ignoring hydrogens
 
0. **ExactMolWt**: The exact molecular weight of the molecule
 
0. **NumValenceElectrons**: The number of valence electrons of the molecule
 
0. **NumRadicalElectrons**: The number of radical electrons in the molecule (says nothing about spin state)
 
0. **MaxPartialCharge**: The maximum partial charge on any atom in the molecule. A partial charge is a non-integer charge value when measured in elementary charge units. Partial charge is more commonly called net atomic charge. It is represented by the Greek lowercase letter δ, namely δ− or δ+.
 
0. **MinPartialCharge**: The minimum partial charge on any atom in the molecule.
 
0. **MaxAbsPartialCharge**: The maximum absolute partial charge on any atom in the molecule.
 
0. **MinAbsPartialCharge**: The minimum absolute partial charge on any atom in the molecule.
 
0. **FpDensityMorgan1**: Morgan fingerprint density (the count of on-bits in the fingerprint divided by the heavy atom count in the molecule), constructed using a Morgan fingerprint of radius 1.
 
0. **FpDensityMorgan2**: Morgan fingerprint density (the count of on-bits in the fingerprint divided by the heavy atom count in the molecule), constructed using a Morgan fingerprint of radius 2.
 
0. **FpDensityMorgan3**:	Morgan fingerprint density (the count of on-bits in the fingerprint divided by the heavy atom count in the molecule), constructed using a Morgan fingerprint of radius 3.

     [**BCUT Descriptors**](https://pubs.acs.org/doi/full/10.1021/ci980137x) below are calculated as the maximum and minimum eigenvalues (HI and LOW) of Burden connectivity matrices ([J. Chem. Inf. Comput. Sci. 1989, 29, 225-227 ](https://pubs.acs.org/doi/pdf/10.1021/ci00063a011), [Quant. Stmct-Act. Relat. 16, 3O9-314 (1997)](https://doi.org/10.1002/qsar.19970160406)) weighted by atomic weights (MW), Gastgeiger charges (CHG), Crippen Log P (LOGP), and Crippen MR along the diagonal elements of the Burden matrices.

0. **BCUT2D_MWHI**

0. **BCUT2D_MWLOW**

0. **BCUT2D_CHGHI**
  
0. **BCUT2D_CHGLO**

0. **BCUT2D_LOGPHI**

0. **BCUT2D_LOGPLOW**

0. **BCUT2D_MRHI**

0. **BCUT2D_MRLOW**

0. **AvgIpc**: This returns the average information content of the coefficients of the characteristic polynomial of the adjacency matrix of a hydrogen-suppressed graph of a molecule. Eq 7 of [D. Bonchev & N. Trinajstic, J. Chem. Phys. vol 67, 4517-4533 (1977)](https://doi.org/10.1063/1.434593).

0. **BalabanJ**: Balaban's J value for a molecule. This is the averaged distance sum connectivity, constructed by the distance matrix of the molecule. [Chem. Phys. Lett. 89:399-404 (1982)](https://doi.org/10.1016/0009-2614(82)80009-2).
 
0. **BertzCT**: A topological index meant to quantify "complexity" of molecules. [J. Am. Chem. Soc. 103:3599-601 (1981)](https://pubs.acs.org/doi/10.1021/ja00402a071).

     The following Chi, HallKierAlpha and Kappa descriptors are taken from [The Molecular Connectivity Chi Indexes and Kappa Shape Indexes in Structure-Property Modeling](https://onlinelibrary.wiley.com/doi/epdf/10.1002/9780470125793.ch9). A chi index is a weighted count of a given type of subgraph. The order of a chi index is the number of graph edges in the corresponding subgraph. Chi0 is related to the sum of the number of nearest neighbours of each atom in the molecule; Chi1 is related to the number of bonds; Chi2 the number of paths of bonds of length 2, and so on. Chi and Chi-v are distinguished by the latter encoding the atomic identities of using their valence, rather than just the presence of atoms as in the former. Chi-n is identical to Chi-v for first row elements; for the second row and below the encoding of valence is done differently.
 
0. **Chi0**: From equations (1), (9) and (10).
 
0. **Chi0n**
 
0. **Chi0v**: From equations (5), (9) and (10).
 
0. **Chi1**: From equations (1), (11) and (12).
 
0. **Chi1n** 
 
0. **Chi1v**: From equations (5), (11) and (12).
 
0. **Chi2n**
 
0. **Chi2v**: From equations (5), (15) and (16).
 
0. **Chi3n**
   
0. **Chi3v**: From equations (5), (15) and (16).
    
0. **Chi4n**
   
0. **Chi4v**: From equations (5), (15) and (16).
 
0. **HallKierAlpha**: The Hall-Kier alpha value for a molecule. For an individual atom ${\textrm{X}}$, $\alpha = r_{\textrm{X}} / r_{\textrm{C}} - 1$, the ratio of the covalent radius of the atom that of a $\textrm{C}_{\textrm{sp}^3}$ atom. For a molecule, it is the sum of these parameters. From equation (58).
 
0. **Ipc**: the information content of the coefficients of the characteristic polynomial of the adjacency matrix of a hydrogen-suppressed graph of a molecule. Eq 6 of [D. Bonchev & N. Trinajstic, J. Chem. Phys. vol 67, 4517-4533 (1977)](https://doi.org/10.1063/1.434593).

      The following 3 descriptors are calculated incorrectly, following an error in the original paper, per [this discussion](https://github.com/rdkit/rdkit/discussions/6884).
 
0. **Kappa1**: The first order shape attribute depends the number of bonds in the molecule, compared to the maximum and minumum number of bonds a molecules of that size could contain. The greater the number of bonds, the smaller the value of Kappa1, for a given number of atoms in the molecule. From equations (49) and (50).
 
0. **Kappa2**: The second order shape attribute depends the number of two-bonds paths in the molecule, compared to the maximum and minumum number of such paths a molecules of that size could contain. The greater the number of paths, the smaller the value of Kappa2, for a given number of atoms in the molecule. From equations (51) and (52).
 
0. **Kappa3**: The third order shape attribute depends the number of three-bonds paths in the molecule, compared to the maximum and minumum number of such paths a molecules of that size could contain. The greater the number of paths, the smaller the value of Kappa3, for a given number of atoms in the molecule. From equations (53), (54) and (55).

     The following VSA descriptors are all adapted from [Journal of Molecular Graphics and Modelling 18, 464-477, 2000](https://www.sciencedirect.com/science/article/pii/S1093326300000681). Additional bins have been added to those originally proposed by Labute, in order to distinguish between a wider array of descriptors; in addition the original paper uses log(MR), while the RDKit implementation uses MR. The VSA descriptors are explained in detail on this [RDKit blog post](https://greglandrum.github.io/rdkit-blog/posts/2023-04-17-what-are-the-vsa-descriptors.html).
 
0. **LabuteASA**: Labute's Approximate Surface Area (ASA from MOE) 
 
0. **PEOE_VSA1**: 	MOE(Molecular Operating Environment) Charge VSA Descriptor 1 (-inf < x < -0.30) 
 
0. **PEOE_VSA10**: 	MOE Charge VSA Descriptor ( 0.10 <= x < 0.15)
 
0. **PEOE_VSA11**: 	MOE Charge VSA Descriptor 11 ( 0.15 <= x < 0.20)

0. **PEOE_VSA12**: MOE Charge VSA Descriptor 12 ( 0.20 <= x < 0.25)
 
0. **PEOE_VSA13**: MOE Charge VSA Descriptor 13 ( 0.25 <= x < 0.30)
 
0. **PEOE_VSA14**: MOE Charge VSA Descriptor 14 ( 0.30 <= x < inf)
 
0. **PEOE_VSA2**: MOE Charge VSA Descriptor 2 (-0.30 <= x < -0.25)
 
0. **PEOE_VSA3**: MOE Charge VSA Descriptor 3 (-0.25 <= x < -0.20)
 
0. **PEOE_VSA4**: MOE Charge VSA Descriptor 4 (-0.20 <= x < -0.15)
 
0. **PEOE_VSA5**: MOE Charge VSA Descriptor 5 (-0.15 <= x < -0.10)
 
0. **PEOE_VSA6**: MOE Charge VSA Descriptor 6 (-0.10 <= x < -0.05)
 
0. **PEOE_VSA7**: MOE Charge VSA Descriptor 7 (-0.05 <= x < 0.00)
 
0. **PEOE_VSA8**: MOE Charge VSA Descriptor 8 ( 0.00 <= x < 0.05)
 
0. **PEOE_VSA9**: MOE Charge VSA Descriptor 9 ( 0.05 <= x < 0.10)
 
0. **SMR_VSA1**: MOE MR VSA Descriptor 1 (-inf < x < 1.29)
  
0. **SMR_VSA10**: MOE MR VSA Descriptor 10 ( 4.00 <= x < inf)
 
0. **SMR_VSA2**: MOE MR VSA Descriptor 2 ( 1.29 <= x < 1.82)
 
0. **SMR_VSA3**: MOE MR VSA Descriptor 3 ( 1.82 <= x < 2.24)
 
0. **SMR_VSA4**: MOE MR VSA Descriptor 4 ( 2.24 <= x < 2.45)
 
0. **SMR_VSA5**: MOE MR VSA Descriptor 5 ( 2.45 <= x < 2.75)
 
0. **SMR_VSA6**: MOE MR VSA Descriptor 6 ( 2.75 <= x < 3.05)
 
0. **SMR_VSA7**: MOE MR VSA Descriptor 7 ( 3.05 <= x < 3.63)
 
0. **SMR_VSA8**: MOE MR VSA Descriptor 8 ( 3.63 <= x < 3.80)
 
0. **SMR_VSA9**: MOE MR VSA Descriptor 9 ( 3.80 <= x < 4.00)
 
0. **SlogP_VSA1**: MOE logP VSA Descriptor 1 (-inf < x < -0.40)
 
0. **SlogP_VSA10**: MOE logP VSA Descriptor 10 ( 0.40 <= x < 0.50)
 
0. **SlogP_VSA11**: MOE logP VSA Descriptor 11 ( 0.50 <= x < 0.60)
 
0. **SlogP_VSA12**: MOE logP VSA Descriptor 12 ( 0.60 <= x < inf)
 
0. **SlogP_VSA2**: MOE logP VSA Descriptor 2 (-0.40 <= x < -0.20)
 
0. **SlogP_VSA3**: MOE logP VSA Descriptor 3 (-0.20 <= x < 0.00)
 
0. **SlogP_VSA4**: MOE logP VSA Descriptor 4 ( 0.00 <= x < 0.10)
 
0. **SlogP_VSA5**: MOE logP VSA Descriptor 5 ( 0.10 <= x < 0.15)
 
0. **SlogP_VSA6**: MOE logP VSA Descriptor 6 ( 0.15 <= x < 0.20)
 
0. **SlogP_VSA7**: MOE logP VSA Descriptor 7 ( 0.20 <= x < 0.25)
 
0. **SlogP_VSA8**: MOE logP VSA Descriptor 8 ( 0.25 <= x < 0.30)
 
0. **SlogP_VSA9**: MOE logP VSA Descriptor 9 ( 0.30 <= x < 0.40)
 
0. **TPSA**: The polar surface area (PSA) or topological polar surface area (TPSA) of a molecule is defined as the surface sum over all polar atoms or molecules, primarily oxygen and nitrogen, also including their attached hydrogen atoms. PSA is a commonly used medicinal chemistry metric for the optimization of a drug's ability to permeate cells. [Curr Med Chem. 2009 ; 16(1): 21–41, link to Author's version](https://pmc.ncbi.nlm.nih.gov/articles/PMC7549127/pdf/nihms-916384.pdf).

   The EState descriptors are first introduced in [J. Chem. Inf. Comput. Sci. 1991, 31, 76-82](https://pubs.acs.org/doi/pdf/10.1021/ci00001a012); the descriptors below are also described in this [RDKit blog post](https://greglandrum.github.io/rdkit-blog/posts/2023-04-17-what-are-the-vsa-descriptors.html).
   
0. **EState_VSA1**: EState VSA  Descriptor 1 (-inf < x < -0.39)
 
0. **EState_VSA10**: EState VSA Descriptor 10 ( 9.17 <= x < 15.00)
 
0. **EState_VSA11**: EState VSA Descriptor 11 ( 15.00 <= x < inf)
 
0. **EState_VSA2**: EState VSA  Descriptor 2 ( -0.39 <= x < 0.29)
 
0. **EState_VSA3**: EState VSA  Descriptor 3 ( 0.29 <= x < 0.72)
 
0. **EState_VSA4**: EState VSA  Descriptor 4 ( 0.72 <= x < 1.17)
 
0. **EState_VSA5**: EState VSA  Descriptor 5 ( 1.17 <= x < 1.54)
 
0. **EState_VSA6**: EState VSA  Descriptor 6 ( 1.54 <= x < 1.81)
 
0. **EState_VSA7**: EState VSA Descriptor 7 ( 1.81 <= x < 2.05)
 
0. **EState_VSA8**: EState VSA  Descriptor 8 ( 2.05 <= x < 4.69)
 
0. **EState_VSA9**: EState VSA  Descriptor 9 ( 4.69 <= x < 9.17)
 
0. **VSA_EState1**: VSA EState  Descriptor 1 (-inf < x < 4.78)
 
0. **VSA_EState10**: VSA EState Descriptor 10 ( 11.00 <= x < inf)
 
0. **VSA_EState2**: VSA EState  Descriptor 2 ( 4.78 <= x < 5.00)
 
0. **VSA_EState3**: VSA EState  Descriptor 3 ( 5.00 <= x < 5.41)
 
0. **VSA_EState4**: VSA EState  Descriptor 4 ( 5.41 <= x < 5.74)
 
0. **VSA_EState5**: VSA EState  Descriptor 5 ( 5.74 <= x < 6.00)
 
0. **VSA_EState6**: VSA EState  Descriptor 6 ( 6.00 <= x < 6.07)

0. **VSA_EState7**: VSA EState  Descriptor 7 ( 6.07 <= x < 6.45)
 
0. **VSA_EState8**: VSA EState  Descriptor 8 ( 6.45 <= x < 7.00)
 
0. **VSA_EState9**: VSA EState  Descriptor 9 ( 7.00 <= x < 11.00)
 
0. **FractionCSP3**: The fraction of C atoms that are SP3 hybridized.
 
0. **HeavyAtomCount**: Number of heavy atoms of a molecule.
 
0. **NHOHCount**: Number of NHs and OHs
 
0. **NOCount**: Number of Nitrogen and Oxygen atoms
 
0. **NumAliphaticCarbocycles**: returns the number of aliphatic (containing at least one non-aromatic bond) carbocycles for a molecule
 
0. **NumAliphaticHeterocycles**: returns the number of aliphatic (containing at least one non-aromatic bond) heterocycles for a molecule
 
0. **NumAliphaticRings**: returns the number of aliphatic (containing at least one non-aromatic bond) rings for a molecule

0. **NumAmideBonds**: returns the number of amide bonds in a molecule
 
0. **NumAromaticCarbocycles**: The number of aromatic carbocycles for a molecule
 
0. **NumAromaticHeterocycles**: returns the number of aromatic heterocycles for a molecule
 
0. **NumAromaticRings**: The number of aromatic rings for a molecule

0. **NumAtomStereoCenters**: Returns the total number of atomic stereocenters (specified and unspecified)

0. **NumBridgeheadAtoms**: Returns the number of bridgehead atoms (atoms shared between rings that share at least two bonds)
 
0. **NumHAcceptors**: Number of Hydrogen Bond Acceptors
 
0. **NumHDonors**: Number of Hydrogen Bond Donors
 
0. **NumHeteroatoms**: Number of Heteroatoms

0. **NumHeterocycles**: returns the number of heterocycles for a molecule
 
0. **NumRotatableBonds**: Number of Rotatable Bonds
 
0. **NumSaturatedCarbocycles**: returns the number of saturated carbocycles for a molecule
 
0. **NumSaturatedHeterocycles**: returns the number of saturated heterocycles for a molecule
 
0. **NumSaturatedRings**: Number of Saturated Rings

0. **NumSpiroAtoms**: Returns the number of spiro atoms (atoms shared between rings that share exactly one atom)

0. **NumUnspecifiedAtomStereoCenters**: Returns the number of unspecified atomic stereocenters

0. **Phi**: *Unspecified in RDKIT documentation!*
 
0. **RingCount**: Number of All Rings
 
0. **MolLogP**: octanol/water partition coefficient (Wildman-Crippen LogP value)
 
0. **MolMR**: Molar Refractivity(Wildman-Crippen MR value)	
 
0. **fr_Al_COO**: Number of aliphatic carboxylic acids
 
0. **fr_Al_OH**: Number of aliphatic hydroxyl groups
 
0. **fr_Al_OH_noTert**: Number of aliphatic hydroxyl groups excluding tert-OH

0. **fr_ArN**:Number of N functional groups attached to aromatics
 
0. **fr_Ar_COO**: Number of Aromatic carboxylic acide
 
0. **fr_Ar_N**: Number of aromatic nitrogens
 
0. **fr_Ar_NH**: Number of aromatic amines
 
0. **fr_Ar_OH**: Number of aromatic hydroxyl groups
 
0. **fr_COO**: Number of carboxylic acids
 
0. **fr_COO2**: Number of carboxylic acids
 
0. **fr_C_O**: Number of carbonyl O
 
0. **fr_C_O_noCOO**: Number of carbonyl O, excluding COOH
 
0. **fr_C_S**: Number of thiocarbonyl
 
0. **fr_HOCCN**: Number of C(OH)CCN-Ctert-alkyl or C(OH)CCNcyclic
 
0. **fr_Imine**: Number of Imines
 
0. **fr_NH0**: Number of Tertiary amines
 
0. **fr_NH1**: Number of Secondary amines
 
0. **fr_NH2**: Number of Primary amines
 
0. **fr_N_O**: Number of hydroxylamine groups
 
0. **fr_Ndealkylation1**: Number of XCCNR groups

0. **fr_Ndealkylation2**: Number of tert-alicyclic amines (no heteroatoms, not quinine-like bridged N)
 
0. **fr_Nhpyrrole**: Number of H-pyrrole nitrogens
 
0. **fr_SH**: Number of thiol groups
 
0. **fr_aldehyde**: Number of aldehydes
 
0. **fr_alkyl_carbamate**: Number of alkyl carbamates (subject to hydrolysis)
 
0. **fr_alkyl_halide**: Number of alkyl halides
 
0. **fr_allylic_oxid**: Number of allylic oxidation sites excluding steroid dienone
 
0. **fr_amide**: Number of amides
  
0. **fr_amidine**: Number of amidine groups
 
0. **fr_aniline**: Number of anilines
 
0. **fr_aryl_methyl**: Number of aryl methyl sites for hydroxylation
 
0. **fr_azide**: Number of azide groups
 
0. **fr_azo**: Number of azo groups
 
0. **fr_barbitur**: Number of barbiturate groups	
 
0. **fr_benzene**: Number of benzene rings
 
0. **fr_benzodiazepine**: Number of benzodiazepines with no additional fused rings
 
0. **fr_bicyclic**: Number of Bicyclic groups
 
0. **fr_diazo**: Number of diazo groups
 
0. **fr_dihydropyridine**: Number of dihydropyridines
 
0. **fr_epoxide**: Number of epoxide rings
 
0. **fr_ester**: Number of esters
 
0. **fr_ether**: Number of ether oxygens (including phenoxy)
 
0. **fr_furan**: Number of furan rings
 
0. **fr_guanido**: Number of guanidine groups
 
0. **fr_halogen**: Number of halogens
 
0. **fr_hdrzine**: Number of hydrazine groups
 
0. **fr_hdrzone**: Number of hydrazone groups
 
0. **fr_imidazole**: Number of imidazole rings
 
0. **fr_imide**: Number of imide groups
 
0. **fr_isocyan**: Number of isocyanates
 
0. **fr_isothiocyan**: Number of isothiocyanates
 
0. **fr_ketone**: Number of ketones
 
0. **fr_ketone_Topliss**: Number of ketones excluding diaryl, a,b-unsat. dienones, heteroatom on Calpha
 
0. **fr_lactam**: Number of beta lactams
 
0. **fr_lactone**: Number of cyclic esters (lactones)
 
0. **fr_methoxy**: Number of methoxy groups -OCH3
 
0. **fr_morpholine**: Number of morpholine rings
 
0. **fr_nitrile**: Number of nitriles
 
0. **fr_nitro**: Number of nitro groups
 
0. **fr_nitro_arom**: Number of nitro benzene ring substituents
 
0. **fr_nitro_arom_nonortho**: Number of non-ortho nitro benzene ring substituents
 
0. **fr_nitroso**: Number of nitroso groups, excluding NO2
 
0. **fr_oxazole**: Number of oxazole rings
 
0. **fr_oxime**: Number of oxime groups
 
0. **fr_para_hydroxylation**: Number of para-hydroxylation sites
 
0. **fr_phenol**: Number of phenols
  
0. **fr_phenol_noOrthoHbond**: Number of phenolic OH excluding ortho intramolecular Hbond substituents
 
0. **fr_phos_acid**: Number of phosphoric acid groups
 
0. **fr_phos_ester**: Number of phosphoric ester groups
 
0. **fr_piperdine**: Number of piperdine rings
 
0. **fr_piperzine**: Number of piperzine rings
 
0. **fr_priamide**: Number of primary amides
 
0. **fr_prisulfonamd**: Number of primary sulfonamides
 
0. **fr_pyridine**: Number of pyridine rings
 
0. **fr_quatN**: Number of quarternary nitrogens
 
0. **fr_sulfide**: Number of thioether
 
0. **fr_sulfonamd**: Number of sulfonamides
 
0. **fr_sulfone**: Number of sulfone groups
 
0. **fr_term_acetylene**: Number of terminal acetylenes
 
0. **fr_tetrazole**: Number of tetrazole rings
 
0. **fr_thiazole**: Number of thiazole rings
 
0. **fr_thiocyan**: Number of thiocyanates
 
0. **fr_thiophene**: Number of thiophene rings
 
0. **fr__unbrch_alkane**: Number of unbranched alkanes of at least 4 members (excludes halogenated alkanes)
 
0. **fr_urea**: Number of urea groups
