# Stage3 Phase 1
## Molecular Docking of LDHA Protein with Artemisia annua Phytochemicals
### Intro
Lung cancer is one of the most common and serious types of cancer. Lung cancer starts in the windpipe(trachea), the main airway (bronchus) or the lung tissue. Most lung cancers are caused as a result of smoking and non-smokers can also develop lung cancer.
Lactate dehydrogenase A (LDHA) catalyzes the conversion of pyruvate to lactate, and its abnormal expression and activation have been strongly linked to various cancers(Tjokrowidjaja et al., 2022). LDHA is located in the cytoplasm. Inhibition of LDHA is known to reduce migration of cancer cells, invasion and cancer metastasis (Feng et al., 2018).

### Curated phytochemical library
Using PubChem we selected <a href='images/Metabolites.docx'>50 phytochemicals</a> from Artemisia annua, a medicinal plant renowned for its medicinal properties, including potential cancer-preventive benefits(Lang et al., 2019).

### Methodology
#### Protein Structure Acquisition  
The 3-dimensional structure of LDHA was predicted and downloaded in PDB format through AlphaFold proceeding towards molecular docking purposes.
<image src="images/LDHA.png">
#### Identification of Active Site  
Potential active sites of LDHA were identified using Fpocket revolving the regions that interact with inhibitors. PyMOL was used afterwards for visualizations.
<image src="images/LDHA_active_site.png">
#### Phytochemical Preparation  
The 3D structures of curated phytochemicals were downloaded in SDF format from PubChem, marged through Open Babel, and delivered into PyRx to initiate molecular docking. 
#### Molecular Docking using PyRx  
The molecular docking was done in PyRx. The steps involved are as follows:  
Preparation of Proteins: The water molecules were removed from the LDHA structure, adding hydrogen atoms and charges.  
Definition of the Active Site: A grid box of 40 Å × 40 Å × 40 Å was set around the identified active site of PODNL1.  
Ligand-Receptor Interaction: The active site was used for the docking of each phytochemical using PyRx, with an exhaustiveness of 8 to ensure extensive examination of the search space. For each ligand, ten binding modes were generated.  
Binding Affinity Measurement: The result from docking was ranked by their calculated free energy of binding (ΔG), whereby the interactions are stronger with lower ΔG values.
### Results  
#### Binding Affinities  
The docking simulations generated 5 notable compounds displaying the highest predicting binding affinities to LDHA. 
Eupartin: ΔG = -7.5 kcal/mol  
Quercetin: ΔG = -7.4 kcal/mol  
kaempferol: ΔG = -7.4 kcal/mol  
cirsimaritin: ΔG = -7.4 kcal/mol  
arcapillin : ΔG = -7.4 kcal/mol  
All results are available in this <a href='images/Metabolites.docx'> Excel </a> file.
#### Pipeline Reusability and Possible Applications  
The pipeline reusability accounts for virtual screening of any other phytochemical libraries against any cancer related protein. The general protocol adopted includes: 
     Protein structure prediction 
     Ligand preparation 
     Transparent docking via PyRx 
The natural phytochemicals identified with high binding affinities for LDHA present promising opportunities in the quest for the discovery of anticancer drugs.  
Future applications of this pipeline could include:  
• Screening of synthetic chemical libraries for the discovery of potent inhibitors of LDHA
• Virtual screening against other targets implicated in lung cancers or other cancers.  
• In vitro and in vivo validation of the best hits for anticancer activities.  

### Conclusion
The docking analysis showed that Eupartin is the most significant phytochemical with high binding affinities, having the potential to inhibit LDHA.
### References

Feng, Y., Xiong, Y., Qiao, T., Li, X., Jia, L., & Han, Y. (2018). Lactate dehydrogenase A: A key player in carcinogenesis and potential target in cancer therapy. Cancer Medicine, 7(12), 6124–6136. https://doi.org/10.1002/cam4.1820

Lang, S. J., Schmiech, M., Hafner, S., Paetz, C., Steinborn, C., Huber, R., El Gaafary, M., Werner, K., Schmidt, C. Q., Syrovets, T., & Simmet, T. (2019). Antitumor activity of an Artemisia annua herbal preparation and identification of active ingredients. Phytomedicine, 62, 152962. https://doi.org/10.1016/j.phymed.2019.152962

Tjokrowidjaja, A., Lord, S. J., John, T., Lewis, C. R., Kok, P. S., Marschner, I. C., & Lee, C. K. (2022). Pre‐ and on‐treatment lactate dehydrogenase as a prognostic and predictive biomarker in advanced non–small cell lung cancer. Cancer, 128(8), 1574–1583. https://doi.org/10.1002/cncr.34113

Miao, P., Sheng, S., Sun, X., Liu, J., & Huang, G. (2013). Lactate dehydrogenase a in cancer: A promising target for diagnosis and therapy. IUBMB Life, 65(11), 904–910. https://doi.org/10.1002/iub.1216

