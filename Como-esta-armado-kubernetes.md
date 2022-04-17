# Kubernetes

Kubernetes es una plataforma portable y extensible de código abierto para administrar cargas de trabajo y servicios. 
Kubernetes facilita la automatización y la configuración declarativa. Tiene un ecosistema grande y en rápido crecimiento. 
El soporte, las herramientas y los servicios para Kubernetes están ampliamente disponibles.

Google liberó el proyecto Kubernetes en el año 2014. Kubernetes se basa en la experiencia de Google corriendo aplicaciones en producción a 
gran escala por década y media, junto a las mejores ideas y prácticas de la comunidad.

# ¿Qué es un pod?

Los pods son los objetos más pequeños y básicos que se pueden implementar en Kubernetes. Un pod representa una instancia única de un proceso en ejecución en tu clúster.

Los pods contienen uno o más contenedores, como los contenedores de Docker. Cuando un pod ejecuta varios contenedores, estos se administran como una sola entidad y comparten los recursos del pod. En general, ejecutar varios contenedores en un solo pod representa un caso práctico avanzado.

# ¿Qué es un Service de Kubernetes?

El concepto de servicio es agrupar un conjunto de extremos de pod en un solo recurso. Puedes configurar varias formas para acceder a la agrupación. De forma predeterminada, obtienes una dirección IP de clúster estable que los clientes dentro del clúster pueden usar para comunicarse con los pods en el servicio. Un cliente envía una solicitud a una dirección IP estable, y la solicitud se enruta a uno de los pods en el servicio.

Un servicio identifica sus pods miembros con un selector. Para que un pod sea miembro del servicio, este debe tener todas las etiquetas especificadas en el selector. Una etiqueta es un par clave-valor arbitrario adjunto a un objeto.

# ClusterIP, Nodeport, LoadBalancer, Ingress

![imagen-services](https://github.com/ltiisidii/kubernetes-tux/blob/main/tnK94zrEwyNe1hL-PhJXOA.png)

