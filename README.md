
---

## ✅ Tu README final mejorado

```markdown
# 🐳 WordPress en Kubernetes con MySQL

Despliegue de WordPress y MySQL en Kubernetes usando Docker Desktop.

## 📋 Requisitos previos

- Docker Desktop **con Kubernetes activado**
- `kubectl` instalado y configurado

## Estructura del proyecto 

```bash
k8s-wordpress/
├── secret.yaml       # Contraseñas (NO subir a GitHub)
├── mysql.yaml        # Deployment + Service de MySQL
├── wordpress.yaml    # Deployment + Service de WordPress
└── .gitignore        # Ignora secret.yaml
```

## 🚀 Despliegue rápido

```bash
# 1. Crear el secret con las contraseñas (nunca subas este archivo a GitHub)
kubectl apply -f secret.yaml

# 2. Desplegar MySQL
kubectl apply -f mysql.yaml

# 3. Desplegar WordPress
kubectl apply -f wordpress.yaml

# 4. Acceder a WordPress
kubectl get svc wordpress-service

# Si el tipo es ClusterIP, cámbialo a NodePort:
kubectl patch svc wordpress-service -p '{"spec":{"type":"NodePort"}}'

# Abre http://localhost:[puerto]
```

