Por un lado están los manifiestos con todos los "servicios", tanto de aplicación como externos.
En esta parte tan solo se ha añadido que los contenendors no se ejecuten como root solo en los servicios de aplicación.
securityContext:
runAsUser: 1001
runAsGroup: 3000
fsGroup: 2000

En la parte de network-policies se han añadido las siguientes reglas:
- denegar todas las reglas
- permitir dns en kubernetes
- permitir acceso a ingress desde fuera a los dos ingress, server y toposervice.
- permitir conectividad entre pods con la topología de la aplicación

Enlace videos:
https://drive.google.com/drive/folders/1q4vthk6vpn_2HRlvmwfWTHAVFaYgiQUX?usp=share_link