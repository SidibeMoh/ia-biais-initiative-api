# Exemples d'utilisation de l'API IA Biais Initiative

Base URL : `http://localhost:3000` (dev) ou `https://api.ia-biais-initiative.org` (prod)

---

## 1. Lister les biais

```bash
curl "http://localhost:3000/biais?limit=10"
```

## 2. Filtrer par identifiant IBI

```bash
curl "http://localhost:3000/biais?ibi_id=eq.IBI-0002"
```

## 3. Top des biais critiques

```bash
curl "http://localhost:3000/v_top_biais_critiques?limit=5"
```

## 4. Reglementations mondiales

```bash
curl "http://localhost:3000/reglementations?limit=10"
```

## 5. Recherche par mot-cle (RPC)

```bash
curl "http://localhost:3000/rpc/recherche_biais?terme=proxy&limite=5"
```

## 6. Pagination

```bash
curl "http://localhost:3000/biais?limit=20&offset=40"
```

## 7. Selection de colonnes

```bash
curl "http://localhost:3000/biais?select=ibi_id,nom_fr,score_ibi&limit=5"
```

## 8. Tri

```bash
curl "http://localhost:3000/biais?order=score_ibi.desc&limit=10"
```

## 9. Depuis Python

```python
import requests

r = requests.get("http://localhost:3000/biais", params={"limit": 10})
for biais in r.json():
    print(biais["ibi_id"], "-", biais["nom_fr"], "(score", biais["score_ibi"], ")")
```

---

## Documentation complete

Voir `openapi.json` pour le spec OpenAPI complet (importable dans Postman, Swagger UI, etc.).
