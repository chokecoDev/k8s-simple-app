# k8s - Simple App

El objetivo de este repositorio es desplegar una aplicación `React` en un clúster de minikube.

## Requisitos

* Docker
* Minikube
* kubectl

## Procedimiento

1. Contenerizar aplicación.

Mediante el archivo ``Dockerfile` construir una imagen de Docker.  
La imagen será subida a DockerHub.

```bash
docker build -t 
```

2. Subir imagen hacia Container Registry

El paso es opcional si el clúster de minikube se encuentra en un equipo distinto a donde se contenerizó la aplicación.

3. Actualizar Imagen

En archivo `devops/deployment.yml` actualizar la imagen que será utilizada en el contenedor del Pod.

4. Desplegar aplicación.

```
kubectl apply -f devops/
```