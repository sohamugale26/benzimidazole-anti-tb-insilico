# In Silico Design of Benzimidazole Analogues as Anti-TB Agents 🧬

> A complete computational drug discovery pipeline designing and screening 6 novel benzimidazole analogues (P1–P6) against Mycobacterium tuberculosis H37Rv — from PASS/ADMET profiling to molecular docking and in vitro MIC validation.

---

## 🎯 Background

Tuberculosis (TB) remains the *leading infectious cause of death globally* despite over 130 years since the discovery of the tubercle bacilli. Mycobacterium tuberculosis is an airborne pathogen and one of the top three infectious diseases worldwide. Rising multi-drug resistance (MDR-TB) makes new chemical scaffolds critical.

Benzimidazole is a significant heterocyclic compound with notable antimicrobial activity. This project applies a full *in silico pipeline* to design, screen, and prioritise novel benzimidazole analogues — then validates top candidates with wet-lab synthesis and MIC testing.

---

## 🔬 Pipeline Overview


Series Design: 6 Benzimidazole Analogues (P1–P6)
        ↓
Biological Activity Prediction (PASS Online)
        ↓
Drug-Likeness & ADMET Profiling
   1. SwissADME  (LogP, GI absorption, BBB, solubility, CYP)
   2. Molinspiration  (miLogP, TPSA, Lipinski violations)
   3. ProTox-II  (oral / inhalational / dermal toxicity)
   4. StopTox  (acute toxicity endpoints)
        ↓
Molecular Docking — AutoDock Vina
      - Target: M. tuberculosis H37Rv (PDB: 2Q1Y)
        ↓
Lead Selection → Synthesis → In Vitro MIC Testing (PABA Assay)


---

## 🧪 Compound Series

| Code | R / Ar Substituent |
|------|-------------------|
| P1 | –H |
| P2 | –CH₃ |
| P3 | 4-NH₂ C₆H₅ |
| P4 | 3,5-NO₂ C₆H₅ |
| *P5* | *–CH₂Cl* (Lead) |
| *P6* | *–CH₂ C₈H₄NO₂* (Lead) |

---

## ✨ Key Results

### In Vitro MIC — M. tuberculosis H37Rv (Resazurin Microplate / PABA Assay)

| Compound | MIC (µg/mL) | vs Rifampicin |
|----------|-------------|---------------|
| *P5* | *1.56* | ✅ 4× better |
| *P6* | *3.125* | ✅ 2× better |
| P1 | 12.5 | Moderate |
| P2 | 25 | Moderate |
| P3 | 50 | Weak |
| P4 | 50 | Weak |
| Rifampicin (reference) | 6.25 | — |

> *P5 and P6 outperformed the reference drug Rifampicin*, with P5 showing the best MIC of 1.56 µg/mL — 4× more potent.

### Biological Activity — PABA Resazurin Microplate Assay

![Biological Activity — PABA Assay](figures/paba_biological_activity.jpg.jfif)

> The microplate assay uses resazurin as a colorimetric indicator. *Blue/purple wells = bacterial growth* (compound inactive at that concentration). *Pink/red wells = no bacterial growth* (compound active — inhibition confirmed). Compounds P5 and P6 show a colour shift to pink at the lowest concentrations (1.56 and 3.125 µg/mL respectively), confirming superior antimycobacterial activity against M. tuberculosis H37Rv compared to the Rifampicin reference (MIC = 6.25 µg/mL).

---

## 📊 Molecular Docking Results

*Target:* M. tuberculosis H37Rv (PDB: 2Q1Y) | *Software:* AutoDock Vina

| Compound | LogP | Docking Score (kcal/mol) | Key Binding Residues |
|----------|------|--------------------------|----------------------|
| P1 | 1.78 | −6.421 | ARG B:304, ILE B:225, GLY B:226, VAL B:305, SER B:227, GLN B:192 |
| P2 | 2.45 | −7.068 | LEU B:188, ARG B:304, ILE B:225, SER B:227, GLY B:226, ASN B:189, GLN B:192 |
| P3 | 3.21 | −6.586 | LEU B:188, ARG B:304, ILE B:225, SER B:227, GLY B:226, ASN B:189, GLN B:192 |
| P4 | 4.80 | −5.584 | GLU A:36, GLY A:34, GLU B:29, ASP A:53, VAL A:10 |
| P5 | 3.08 | −6.006 | ARG B:304, THR B:306, SER B:260, ALA B:262, GLN B:192 |
| *P6* | *3.11* | *−7.08* | ARG B:139, GLU A:87, LYS A:120, GLU B:136, ASP A:84 |

> *P2 and P6* showed the strongest docking scores (−7.068 and −7.08 kcal/mol), indicating high binding affinity to the H37Rv target.

### Docking Visualisation

![Docking Image of Final Compounds and PAS](figures/docking_image.jpg.jfif)

> 2D interaction maps showing binding poses of the final benzimidazole compounds (left) and the PAS reference (right) within the M. tuberculosis H37Rv active site. Coloured residues indicate hydrophobic contacts, hydrogen bonds, and electrostatic interactions. Key residues ARG B:304, LEU B:188, and GLN B:192 are prominently involved in ligand stabilisation.

---

## 🧬 ADMET Profiling

### SwissADME — Pharmacokinetics

| Compound | LogP | GI Absorption | BBB Permeation | Solubility | CYP2D6 | CYP2C19 |
|----------|------|--------------|----------------|------------|--------|---------|
| P1 | 2.87 | High | No | Soluble | Yes | No |
| P2 | 3.27 | High | No | Moderately soluble | Yes | No |
| P3 | 3.85 | High | No | Moderately soluble | No | No |
| P4 | 4.19 | Low | No | Moderately soluble | No | Yes |
| *P5* | *3.30* | *High* | No | Moderately soluble | Yes | No |
| *P6* | *3.38* | *High* | No | Moderately soluble | No | No |

### Molinspiration — Lipinski Drug-Likeness

| Compound | miLogP | TPSA | MW (g/mol) | H-Bond Donors | Violations |
|----------|--------|------|------------|---------------|------------|
| P1 | 2.88 | 87.38 | 283.29 | 3 | 0 |
| P2 | 2.96 | 87.38 | 297.31 | 3 | 0 |
| P3 | 4.07 | 113.40 | 374.13 | 5 | 0 |
| P4 | 4.84 | 179.33 | 449.38 | 3 | 1 |
| *P5* | *3.56* | *87.38* | *331.76* | *3* | *0* |
| *P6* | *4.60* | *126.46* | *442.43* | *3* | *0* |

> All compounds except P4 are fully Lipinski-compliant (0 violations).

### PASS Online — Predicted Biological Activity

| Compound | Pa (Antimycobacterial) | Pa (Antituberculosic) | Activity Predicted |
|----------|----------------------|----------------------|-------------------|
| P1 | 0.414 | 0.036 | Antimycobacterial + Antituberculosic |
| P2 | 0.557 | 0.013 | Antimycobacterial + Antituberculosic |
| P3 | 0.601 | 0.010 | Antimycobacterial + Antituberculosic |
| P4 | 0.631 | 0.008 | Antimycobacterial + Antituberculosic |
| *P5* | — | *0.382* | *Antituberculosic* |
| *P6* | — | *0.360* | *Antituberculosic* |

### ProTox & StopTox — Toxicity Profile

| Compound | Acute Oral | Acute Inhalational | Acute Dermal | Skin Sensitization | Hepatotoxicity |
|----------|------------|-------------------|--------------|-------------------|----------------|
| P1 | Non-toxic | Non-toxic | Non-toxic | Non-sensitizer | Inactive |
| P2 | Non-toxic | Non-toxic | Non-toxic | Non-sensitizer | Inactive |
| P3 | Non-toxic | Non-toxic | Non-toxic | Non-sensitizer | Inactive |
| P4 | Non-toxic | Non-toxic | Non-toxic | Non-sensitizer | Inactive |
| *P5* | Non-toxic | Non-toxic | Non-toxic | Non-sensitizer | Inactive |
| *P6* | Non-toxic | Non-toxic | Non-toxic | Non-sensitizer | Inactive |

> All 6 compounds showed *no hepatotoxicity, no skin sensitization, and acceptable acute toxicity profiles*.

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| *PASS Online* | Biological activity prediction (Pa/Pi scores) |
| *SwissADME* | LogP, GI absorption, BBB permeability, CYP profiling |
| *Molinspiration* | miLogP, TPSA, Lipinski rule-of-five screening |
| *ProTox-II* | Oral toxicity class and LD50 prediction |
| *StopTox* | Acute inhalational, dermal, eye and skin toxicity |
| *AutoDock Vina* | Molecular docking — binding affinity scoring |
| *PDB: 2Q1Y* | M. tuberculosis H37Rv receptor crystal structure |

---

## 🏆 Recognition

- *2nd Rank* — UG Poster Presentation, National Conference on Advances in Drug Discovery and Development, Pravara Women's College of Pharmacy, Nashik (2026)
- *4th Rank* — UG Poster Presentation, LVH INNOFEST 2026 (University-Level Innovation Competition), Nashik (2026)

---

## 📚 References

- M. tuberculosis H37Rv crystal structure (PDB: 2Q1Y) — RCSB Protein Data Bank
- Trott O. & Olson A.J. (2010) — AutoDock Vina: improving speed and accuracy of docking
- Lipinski CA et al. (2001) — Experimental and computational approaches to estimate solubility and permeability
- WHO Global Tuberculosis Report 2024

---

## 👤 Co-Author

*Soham Ugale* — B.Pharm, GCP Certified (ICH E6 R2)  
📧 sohamu2602@gmail.com | [LinkedIn](https://linkedin.com/in/soham-c-ugale-3a66b5299)
