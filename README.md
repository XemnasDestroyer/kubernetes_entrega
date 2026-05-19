# kubernetes_entrega
Entrega de Virtualización y Escalabilidad sobre kubernetes

Para ejecutar, recomiendo guardar todos los yaml en una misma carpeta. Tras esto, teniendo kubernetes instalado (yo tenía la versión k3s)
ejecutar el comando
```
sudo kubectl apply -f "NOMBRE DEL ARCHIVO".yaml
```

Esto levantará el pod y el servicio respectivo a cada manifesto. Cada manifesto tiene réplicas que se pueden cambiar a mano.
