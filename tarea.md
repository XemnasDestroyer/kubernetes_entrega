Hemos creado 5 aplicaciones distintas. 4 de ellas sin base de datos, y una con base de datos (sin replicar). Las aplicaciones
sin base de datos son:
- Nginx: puede servir tanto de proxy inverso como de  balanceador de carga.
- httpbin: servicio de "echos" para peticiones http.
- hello-kubernetes: "helloworld" de kubernetes.
- speedtest: permite probar la velocidad de la red del usuario.

La app que tiene base de datos es:
- ghost: app para la publicación y gestión de posts. Tiene capacidad de registro de usuarios, logeo e integración con herramientas de terceros.

Todos los manifestos se incluyen junto a este documento, además de un video navegando por todas las aplicaciones. Dichas aplicaciones se han implementado
en una terminal ubuntu-server virtualizada usando VMware. Se han usado 2 nodos, y cada app se ha replicado entre 2 y 4 veces. Destacar que, la app ghost
se ha replicado 2 veces, no así su base de datos. Esta app cuenta con 2 servicios en su manifesto:
- Un servicio para ofrecerlo a usuario externo, el cual tiene su IP y su puerto externo.
- Un servicio para la base de datos, para que las replicas de la app ghost puedan conectarse privadamente a la base de datos. Esto hace que no haga falta replicar
la base de datos y, por tanto, duplicar o triplicar los datos.