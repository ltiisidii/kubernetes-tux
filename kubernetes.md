# Kubernetes

Kubernetes es una plataforma portable y extensible de código abierto para administrar cargas de trabajo y servicios. 
Kubernetes facilita la automatización y la configuración declarativa. Tiene un ecosistema grande y en rápido crecimiento. 
El soporte, las herramientas y los servicios para Kubernetes están ampliamente disponibles.

Google liberó el proyecto Kubernetes en el año 2014. Kubernetes se basa en la experiencia de Google corriendo aplicaciones en producción a 
gran escala por década y media, junto a las mejores ideas y prácticas de la comunidad.

# ¿Qué es un pod?

Los pods son los objetos más pequeños y básicos que se pueden implementar en Kubernetes. Un pod representa una instancia única de un proceso en ejecución en tu clúster.

Los pods contienen uno o más contenedores, como los contenedores de Docker. Cuando un pod ejecuta varios contenedores, estos se administran como una sola entidad y comparten los recursos del pod. En general, ejecutar varios contenedores en un solo pod representa un caso práctico avanzado.

# ¿Que es un nodo?

Un nodo es una máquina de trabajo en Kubernetes, previamente conocida como minion . Un nodo puede ser una máquina virtual o física, dependiendo del tipo de clúster. Cada nodo está gestionado por el componente máster y contiene los servicios necesarios para ejecutar pods.

# ¿Qué es un Service de Kubernetes?

El concepto de servicio es agrupar un conjunto de extremos de pod en un solo recurso. Puedes configurar varias formas para acceder a la agrupación. De forma predeterminada, obtienes una dirección IP de clúster estable que los clientes dentro del clúster pueden usar para comunicarse con los pods en el servicio. Un cliente envía una solicitud a una dirección IP estable, y la solicitud se enruta a uno de los pods en el servicio.

Un servicio identifica sus pods miembros con un selector. Para que un pod sea miembro del servicio, este debe tener todas las etiquetas especificadas en el selector. Una etiqueta es un par clave-valor arbitrario adjunto a un objeto.

# ClusterIP, Nodeport, LoadBalancer, Ingress

![imagen-services](https://github.com/ltiisidii/kubernetes-tux/blob/main/tnK94zrEwyNe1hL-PhJXOA.png)

### ClusterIP:

ClusterIP: Solo permite el acceso interno entre distintos servicios. Es el tipo por defecto. Podemos acceder desde el exterior con la instrucción kubectl proxy, puede de ser gran ayuda para los desarrolladores.

![imagen-clusterIP](https://github.com/ltiisidii/kubernetes-tux/blob/main/clusterip.png)

### NodePort: 

Abre un puerto, para que el servicio sea accesible desde el exterior. Por defecto el puerto generado está en el rango de 30000:40000. Para acceder usamos la ip del servidor master del cluster y el puerto asignado.

![imagen-NodePort](https://github.com/ltiisidii/kubernetes-tux/blob/main/nodeport.png)

### LoadBalancer: 

Este tipo sólo esta soportado en servicios de cloud público (GKE, AKS o AWS). El proveedor asignara un recurso de balanceo ed carga para el acceso a los servicios. si usamos un cloud privado, como OpenSatck necesitaremos un plugin para configurar el funcionamiento.

![image-LoadBalancer](https://github.com/ltiisidii/kubernetes-tux/blob/main/loadbalancer.png)


# Soluciones de Storage

![imagen-storage](https://github.com/ltiisidii/kubernetes-tux/blob/main/eUpYUJz3bTBAcyMCI6ThOw.png)

# ¿Que es un Replica-Set?

# ¿Que es un Deployment?

# ¿Que es un ConfigMap?

Un ConfigMap es un objeto de la API que permite almacenar la configuración de otros objetos utilizados. Aunque muchos objetos de kubernetes que tienen un spec , un ConfigMap tiene una sección data para almacenar items, identificados por una clave, y sus valores

# ¿Para que sirve crear un Secret?

# ¿Que hace KubeDNS?



