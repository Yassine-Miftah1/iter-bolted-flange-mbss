# Conception par contraintes d'assemblages à brides pour ITER

Synthèse de systèmes basée sur modèle (MBSS) d'assemblages boulonnés pour les lignes du Test Blanket Module d'ITER, résolue avec **DEPS Studio**.
ISAE-Supméca, électif de dernière année, 2026. [English version](README.md)

## Problème

Relier des tuyauteries d'**eau, de lithium-plomb (Pb-Li) et d'hélium** par une bride boulonnée avec joint métallique **HELICOFLEX**. Le problème est posé formellement (variables, catalogues, équations, exigences) et le solveur synthétise des configurations satisfaisant toutes les contraintes avec une masse faible.

## Résultats

| Ligne | Masse calculée |
|---|---|
| Eau | 9,163 kg (8 vis M18 en 42CrMo4, brides 316LN) |
| Lithium-plomb | 0,751 kg |
| Hélium | 20,865 kg |

Cas eau : vis à 98,64 %, flexion de bride à 100 %. Un recalcul indépendant confirme que chaque configuration exportée satisfait les équations et les exigences.

## Limites

- Configurations **admissibles** trouvées par le solveur ; aucune preuve d'optimalité globale.
- Forte sensibilité au frottement : à μ = 0,12 la solution eau devient infaisable.
- Modèle statique et isotherme, lois analytiques simplifiées.

## Contenu

`report/` (rapport FR + EN), `catalogs/` (catalogue HN200 en SI), `figures/`, `deps/` (modèles DEPS eau, lithium-plomb, hélium avec solutions exportées), `presentation/` (soutenance).

## Équipe

Yassine Miftah, Adrian Ujkaj, et Hossam Benkhadra.
