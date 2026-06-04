# Results Notes

Key findings from the paper.

---

## Key Findings

### F-01 · Satellite Imagery Improves Transit Prediction

- Sociodemographic-only baseline: test pseudo-R² = 0.055,
  AUC = 0.672
- Full imagery-augmented models (CLIP, RemoteCLIP, DINOv3):
  test pseudo-R² = 0.266–0.281, AUC = 0.859–0.864
- Improvement is consistent across all eight VLM architectures tested.

### F-02 · Long-Tail Contribution of Image Principal Components

- Post-Lasso retains 42–49 imagery PCs out of 200 candidates
  per model.
- Significant PCs (p < 0.05): 19/43 (CLIP), 20/49 (RemoteCLIP),
  13/42 (DINOv3).
- The number of significant imagery PCs exceeds the combined
  number of significant sociodemographic and 5D predictors.
- Long-tail pattern is robust across all eight vision models.

### F-03 · Stability of Sociodemographic and 5D Coefficients

- Sociodemographic predictors (female, license, household
  vehicles, home ownership) maintain consistent signs and
  magnitudes across all imagery-augmented specifications.
- Household vehicle ownership is the dominant negative predictor
  of transit use (coefficient range: −0.402 to −0.567).
- Trip distance is the strongest positive predictor
  (coefficients 1.358–1.375).
- Employment density and park proximity are significant at both
  origin and destination.

### F-04 · Destination > Origin Asymmetry

- Destination BE coefficients are consistently larger in
  magnitude than origin coefficients.
- Only one significant origin imagery PC (O-PC3) vs. four
  significant destination PCs (D-PC100, D-PC29, D-PC35, D-PC47)
  in the RemoteCLIP specification.

### F-05 · Tier-2 Morphological Concepts Dominate Interpretation

Retrieval rates among significant PCs:
- Tier 2 (satellite morphological): 70% (14/20 phrases retrieved)
- Tier 1 (5D phrases): 35% (7/20)
- Tier 3 (data-driven): 15% (9/60)

### F-06 · Convergence with 5D Framework

Three components (D-PC100, O-PC3, D-PC29) retrieve concepts
broadly consistent with the density, proximity, and design
dimensions of the 5D framework:
- Homogeneous suburban form → lower transit use
- Transport infrastructure / mixed land use → higher transit use

### F-07 · Chicago-Specific Patterns

Two components reveal context-specific features:
- D-PC35: Airports and large industrial areas associated with
  higher transit use (plausibly driven by shift-worker commute
  patterns).
- D-PC100: Coastal / industrial zones along Chicago's lakefront.
- O-PC3: Mixed highway and light rail infrastructure
  characteristic of Chicago.

### F-08 · VLM Hallucination Example

D-PC47: LLM-generated reasoning misclassified O'Hare
International Airport as a regular grid street layout,
illustrating current limits of VLM spatial reasoning.

---

## Robustness Checks

### R-01 · Eight VLM Architectures

All main findings replicated across CLIP (ViT-B/32, ViT-L/14,
ViT-H/14), RemoteCLIP (ViT-B/32, ViT-L/14), and DINOv3
(Sat-B, Sat-L, Sat-H). Detailed results for the five
non-featured models are in the paper's Appendix.

### R-02 · PCA Component Sensitivity

100 PCs retained as the parsimonious threshold.

> [TBC: exact alternative PC counts tested]

---

## Specifications That Did Not Work

### X-01 · DINOv3 for Text-Concept Interpretation

DINOv3 is self-supervised without text supervision, so it does
not have a shared text–image embedding space. RemoteCLIP used
instead for all concept alignment analysis.

---

## Open Questions and Future Directions

- **VLM hallucination:** O'Hare misclassification example
  (F-08) shows current VLM limits in spatial reasoning.
- **Generalizability:** Context-specific Chicago findings
  suggest replication needed in other metropolitan areas.
- **Counterintuitive concept retrieval:** Some PCs (D-PC35,
  D-PC47) yielded concept retrievals that appeared
  counterintuitive in text form but were partially resolved
  by visual evidence.
