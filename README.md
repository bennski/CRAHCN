# CRAHCN
Consistent Reduced Atmospheric Hybrid Chemical Network

Description: CRAHCN and its oxygen extension (CRAHCN-O), are reduced chemical reaction networks developed by Dr. Ben K. D. Pearce for modeling the production of simple prebiotic chemistry precursor species in planetary atmospheres. They contain experimental rate coefficients, when available, but the larger fraction of rate coefficients are calculated using consitent quantum chemistry and statistical mechanics methods (BHandHLYP/aug-cc-pVDZ and canonical variational transistion state theory). The mantra behind this, is that we are faced with the inability to experimentally measure every reaction rate coefficient under the Sun - which would in theory produce the most accurate network. However, one way to improve the uncertainty of unmeaured and unknown rate coefficients, we think, would be to follow a consistent method for calculating rate coefficients the that has proven to be the most accurate when validating against measured reactions. Thus far, CRAHCN has been used to model the atmosphere of Titan in 1D, and CRAHCN-O has been used to model the atmosphere of early Earth in 1D, as well as an experimental vacuum flow setup of early Earth using plasma in 0D.

This repository contains two reduced chemical reaction networks that can be used to model terrestrial planetary atmospheres with particular compositions and temperatures.
1) The original CRAHCN network contains 104 reactions, and can be used to model HCN production in Titan's atmosphere, or HCN production in a reducing atmosphere dominated by H2, N2, and CH4 ranging from 50–400 K. This network was used for the Titan atmospheric models in Pearce et al. (2020), ApJ.
2) The up-to-date CRAHCN-O network (extended to include oxygen species) contains a few hundred reactions, and can be used to model HCN, H2CO, hydrocarbon, NH3, and many other small organic species in atmospheres dominated by any of the following species: H2, CO2, N2, CO, H2O, and CH4, ranging from 50–400 K. This version of CRAHCN-O is currently being used for a yet-to-be-published early Earth atmospheric model. Previous versions of CRAHCN-O, e.g., used in Pearce et al. (2022) ApJ, and Pearce et al. (2022) ACS Earth & Space Chem contain a dozen or few dozen fewer reactions, and are available upon request.

Format: 
1) CRAHCN: The first 32 reactions are three-body collisional reactions specifically calculated for N2 as the dominant collisional species. Column 1 is the low-pressure limit ko, and column 2 is the high-pressure limit kinf. The remaining reaction data follows the Arrhenius expression α(T/300)^βe^(-γ/T), where column 1 is α, column 2 is β, and column 3 is γ.
2) CRAHCN-O: The three-body collisional reactions in this network are calculated for three collisional gases, N2, CO2, and H2. For each three-body reaction, row 1 is the low-pressure limit, row 2 is the high-pressure limit, and rows 4–6 are the multipliers for each collisional gas. There are a few two-body collisional deexcitation reactions (e.g., N2D + M -> N4S + M), these simply have the Arrhenius parameters in row 1, and the multipliers for each collisional gas in rows 3–5. The remaining reaction data follows the Arrhenius expression α(T/300)^βe^(-γ/T), where column 1 is α, column 2 is β, and column 3 is γ.

For clarficiations regarding these networks, e-mail Dr. Ben K. D. Pearce at benpearce@purdue.edu.
