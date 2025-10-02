# Exploring a Bimetallic Catalyst Family for Alkaline Hydrogen Oxidation: The Mechanisms Behind Superior Activity and Durability

This repository provides the **supplementary data, computational models, and optimized structures** supporting the manuscript titled  
*"Exploring a Bimetallic Catalyst Family for Alkaline Hydrogen Oxidation: The Mechanisms Behind Superior Activity and Durability"*  
published in *Nature Communications*.  

It includes two major components:

1. A **fine-tuned Machine Learning Interatomic Potential (MLIP) model**, based on the pre-trained **CHGNet**, which was custom-tuned using our DFT dataset for **H₂** and **OH*** adsorption on various metallic  surfaces.  
   - This model was employed to rapidly and accurately screen thousands of adsorption configurations, greatly accelerating the computational discovery process compared to conventional DFT-only approaches.  

2. The **final DFT-optimized atomic structures** used in the manuscript.  
   - These structure files correspond to the figures presented in the paper and are provided to ensure reproducibility and facilitate further studies.

---

## Files Included

- **MLIP Model**
  - `Fine-tuned_MLIP_Model/`: Fine-tuned model weights for predicting adsorption energies of H₂ and OH* on catalyst surfaces.

- **DFT Optimized Structures**
  - `Figures/`: Final DFT-optimized atomic structures corresponding to the catalysts and adsorption configurations discussed in the paper.

---

## Model Usage
The fine-tuned MLIP model in this repository is intended for the **rapid energy prediction** of H₂ and OH* adsorption configurations on metallic surfaces relevant to this study.

**Workflow overview:**
1. Prepare a Python environment with the [CHGNet library](https://github.com/CHGNet/CHGNet) installed.  
2. Load the fine-tuned model weights from this repository into a CHGNet model instance.  
3. Provide an atomic structure (e.g., CIF or POSCAR format) representing the catalyst surface with adsorbates.  
4. The model will return the predicted total energy, enabling high-throughput screening of adsorption geometries without the cost of full DFT calculations.
