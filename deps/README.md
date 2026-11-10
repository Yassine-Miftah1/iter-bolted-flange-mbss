# DEPS Studio models

One DEPS project per fluid line. Open the `.proj` file in DEPS Studio.

| Folder | Line | Entry point | Project file |
|---|---|---|---|
| `water/` | Water (DN65) | `ProblemeEau.deps` | `MBSS_Brides_ITER_Eau.proj` |
| `lead-lithium/` | Lead-lithium (Pb-Li) | `ProblemeLiPb.deps` | `MBSS_Brides_ITER_LiPb.proj` |
| `helium/` | Helium | `ProblemeHelium.deps` | `MBSS_Brides_ITER_Helium.proj` |

## File structure (identical in each project)

The MBSS decomposition of the report (Sections 3 and 7) maps onto the files:

| File | Role |
|---|---|
| `Universal.deps` | Universal types and units |
| `Grandeurs.deps` | Physical quantities (types and bounds) |
| `Donnees.deps` | Catalogs: seals, bolts, flange materials (hot properties) |
| `Composants.deps` | Components (seal, bolt, flange, hub) |
| `Structure.deps` | Structure **S**: assembly of components and geometry |
| `Comportement.deps` | Behavior **B**: forces, stresses, mass equations |
| `Exigences.deps` | Requirements **R**: acceptance criteria |
| `Problem*.deps` | Synthesis problem: service conditions and objective (minimize mass) |
| `Results/` | Exported solutions (`Solutions.csv`, `.json`, `.resu`, precision and types) |

File and identifier names are in French, as in the report.

## Reproducing

1. Open the project in DEPS Studio.
2. Run the synthesis problem (First Solution / Minimize, precision 1e-3).
3. Compare the solution with `Results/Solutions.csv` and the report (Section 8).

Expected calculated masses: water 9.163 kg, lead-lithium 0.751 kg, helium 20.865 kg. These are feasible configurations; global optimality is not proven.

DEPS Studio is third-party software; check its license terms. These files contain only the project's own models.
