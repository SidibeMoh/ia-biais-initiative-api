# IA Biais Initiative - API REST

> **250 biais documentes - 68 reglementations mondiales - 21 vues analytiques - 17 fonctions RPC**

API REST ouverte pour l'etude, la detection et la gouvernance des biais des systemes d'intelligence artificielle.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.XXXXXXX.svg)](https://doi.org/10.5281/zenodo.XXXXXXX)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

---

## Mission

Repondre aux inquietudes mondiales sur les biais de l'IA - exprimees par l'ONU, l'UNESCO, l'OCDE, le Vatican, les ONG et les grands laboratoires d'IA - par une base de connaissances scientifique, rigoureuse, ouverte et citable.

Cette initiative citoyenne mondiale vise a fournir aux chercheurs, decideurs, regulateurs et developpeurs un **referentiel commun** sur les biais de l'IA.

---

## Contenu de la base

| Ressource | Nombre |
|---|---|
| Biais documentes | **250** |
| Reglementations mondiales | **68** |
| Vues analytiques | **21** |
| Fonctions RPC | **17** |
| Sources scientifiques | **250+** |
| Tests automatises | **70+** |

---

## Architecture technique

- **PostgreSQL 18** - Base de donnees relationnelle (schema ibi_db)
- **PostgREST 16** - API REST automatique (port 3000)
- **FastAPI** - Endpoints metier (port 8000)
- **Docker** - Deploiement conteneurise

---

## Endpoints principaux

| Methode | Endpoint | Description |
|---|---|---|
| GET | /biais | Liste complete des biais |
| GET | /biais?ibi_id=eq.IBI-0002 | Biais par identifiant |
| GET | /v_top_biais_critiques | Top des biais critiques |
| GET | /v_api_biais_liste | Liste synthetique pour API |
| GET | /reglementations | Reglementations mondiales |
| POST | /rpc/recherche_biais | Recherche par mot-cle |
| POST | /rpc/recherche_triaxis | Recherche TriAxis |

---

## TriAxis : la taxonomie IBI

Chaque biais est classe selon **3 axes orthogonaux** :

| Axe | Description | Codes |
|---|---|---|
| O - Origine | D'ou vient le biais ? | O1_systemique, O2_computationnel, O3_humain_cognitif |
| L - Lifecycle | A quelle etape ? | L1_historique a L6_deploiement |
| S - Specifique | Nature precise | S01_proxy a S28_interaction |

**Exemple** : IBI-0002 (Biais de proxy discriminant)
- O2_computationnel - L3_mesure - S01_proxy

---

## Citation

Si vous utilisez cette API dans vos travaux, merci de citer :

```bibtex
@software{sidibe_2026_ia_biais,
  author       = {SIDIBE, Mohamadou},
  title        = {IA Biais Initiative - API REST},
  month        = oct,
  year         = 2026,
  publisher    = {Zenodo},
  version      = {1.0.0},
  doi          = {10.5281/zenodo.XXXXXXX},
  url          = {https://doi.org/10.5281/zenodo.XXXXXXX}
}
```

---

## Licence

- **Donnees et documentation** : CC-BY 4.0 - usage libre avec attribution
- **Code source** : proprietaire, non public

---

## Contact

- Email : contact@ia-biais-initiative.org
- GitHub : [@SidibeMoh](https://github.com/SidibeMoh)

---

## Remerciements

Cette initiative s'inscrit dans le dialogue mondial sur la gouvernance de l'IA, aux cotes des travaux de l'UNESCO, de l'OCDE, de l'ONU et des acteurs academiques engages pour une IA ethique et equitable.

**Un citoyen du monde, une reponse rigoureuse aux inquietudes sur l'IA.**
