## Déploiement

```bash
# Step by step apply
# 1. Créer le namespace
kubectl apply -f namespace.yaml

# 3. Déployer la base de données
kubectl apply -f database.yaml

# 4. Déployer le backend
kubectl apply -f backend.yaml

# 5. Déployer le frontend
kubectl apply -f frontend.yaml

# OR

# One liner apply
kubetcl apply -k ./

# Vérifier que tout fonctionne
kubectl get all -n tp-app

# Voir le frontend
minikube service frontend -n tp-app # minikube
# OU
kubectl port-forward -n tp-app service/frontend 8080:80 # Port forward