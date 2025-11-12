## Déploiement

```bash
# 1. Créer le namespace
kubectl apply -f 1-namespace.yaml

# 3. Déployer la base de données
kubectl apply -f 3-database.yaml

# 4. Déployer le backend
kubectl apply -f 4-backend.yaml

# 5. Déployer le frontend
kubectl apply -f 5-frontend.yaml

# Vérifier que tout fonctionne
kubectl get all -n tp-app