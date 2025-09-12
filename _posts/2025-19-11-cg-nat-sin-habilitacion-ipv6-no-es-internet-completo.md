---
layout: post
section-type: post
title: CG-NAT sin habilitación IPv6 no es Internet completo
date: 2025-09-11 22:00:00
category: blog
tags: [ 'blog', 'chile', 'networking', 'isp', 'internet', 'ipv6', 'ipv4' ]
---
En Chile, hace unos 15 años se produjo uno de los conflictos más relevantes de la era de Internet a nivel mundial, entre usuarios y proveedores de servicios de Internet (ISP). A mediados de los años 2000, con la creciente masificación del intercambio de archivos mediante protocolos Peer-to-Peer (P2P), los usuarios comenzaron a utilizar intensivamente el ancho de banda por el que pagaban, el cual se ofrecía como "unlimited and unmetered bandwidth", las redes funcionaban con una alta tasa de agregación, lo que hacía imposible cumplir esa promesa bajo determinadas condiciones y provocaba que el servicio se degradara. Este uso no le agradó a las compañías proveedoras de Internet, dado que sobrecargaba su infraestructura, en una época donde contar 10Mb/s en el hogar era impresionante. La solución de las compañías fue comenzar a bloquear puertos a sus clientes y discriminar el tráfico que los usuarios realizaban, cosa sencilla en ese tiempo, donde casi nadie usaba cifrado para el transporte en la red.

En el año 2010, Chile se convirtió en el primer país del mundo en aprobar una ley de Neutralidad de la Red, con la [Ley N° 20.453 de Neutralidad de la Red](https://www.bcn.cl/leychile/navegar?i=1016570),  estableciendo por primera vez que Internet es de uso libre y sin restricciones, para uso legal. Cinco años más tarde, lo harían los paises de la Unión Europea con el [Reglamento (UE) 2015/2120](https://eur-lex.europa.eu/legal-content/ES/TXT/?uri=CELEX:32015R2120).

En la actualidad ese espíritu de neutralidad y libre acceso se encuentra amenazado, de manera casi invisible para la mayoría de los usuarios, pero donde quienes tenemos el conocimiento debemos transparentar y exigir el cumplimiento de ese derecho adquirido hace ya 15 años.

Por ello, deseo presentar un reclamo respecto a la calidad del servicio de acceso a Internet entregado por mi proveedor de Internet y muchos otros. Actualmente, la conexión que se ofrece se encuentra limitada a una dirección IPv4 compartida bajo [CG-NAT (Carrier-Grade NAT)](https://en.wikipedia.org/wiki/Carrier-grade_NAT), sin habilitación de IPv6.

Este esquema implica que no se pueden exponer servicios desde una red doméstica hacia Internet (servidores, cámaras IP, VPNs, dispositivos IoT, etc.), ni establecer conexiones entrantes directas desde el exterior, lo cual es una función esencial de la definición de Internet y requisito esencial en la actualidad para considerarlo como un servicio de Internet completo. En la práctica, se está entregando un acceso restringido únicamente a servidores públicos accesibles desde IPv4, con una traducción IPv6 limitada, lo que significa que el servicio estaría incompleto o degradado, dado que no garantiza conectividad global, sea saliente o entrante, a todo el espacio de Internet.

Tal situación contraviene tanto los estándares técnicos internacionales como la legislación nacional:

* [RFC 791 (IPv4)](https://www.rfc-editor.org/info/rfc791) y [RFC 8200 (IPv6)](https://www.rfc-editor.org/info/rfc8200) definen que una conexión de Internet debe permitir la comunicación extremo a extremo entre dispositivos.
* El CG-NAT rompe este principio básico, afectando gravemente la neutralidad y calidad de la red. Dado que el servicio se encontraría dentro de una red privada externa a la contratada, bajo un NAT administrado externamente por la compañía, sin posibilidad alguna de aplicar configuraciones personalizadas sin romper con derechos a la privacidad, y sin transparencia de ello en la contratación.
* La IETF, en el [RFC 6540](https://www.rfc-editor.org/info/rfc6540), establece explícitamente que “IPv6 es obligatorio en todos los nodos de Internet”, y que su soporte debe considerarse esencial para garantizar interoperabilidad y evolución de la red.
* En Chile, la [Ley N° 20.453 de Neutralidad de la Red (artículo 24 H de la Ley General de Telecomunicaciones)](https://www.bcn.cl/leychile/navegar?i=1016570) garantiza que los usuarios pueden acceder libremente a cualquier contenido, aplicación o servicio disponible en Internet, sin discriminación arbitraria. Limitar el acceso a conexiones únicamente detrás de un CG-NAT y sin opción a IPv6 constituye una forma de restricción arbitraria al impedir participar activamente de Internet en igualdad de condiciones. Más aún considerando que IPv6 está establecido como requisito obligatorio para todos los nodos de Internet, debiendo ser considerado cada conexión doméstica como uno, y no solo el punto administrado y mantenido directamente por el ISP.

La adopción de IPv6 a nivel mundial es de [44,68% (tráfico hacia Google)](https://www.google.com/intl/en/ipv6/statistics.html#tab=ipv6-adoption), mientras que Chile se encuentra muy por debajo de esa media con una adopción de [16,79%](https://www.google.com/intl/en/ipv6/statistics.html#tab=per-country-ipv6-adoption). Este rezago contrasta fuertemente con el hecho de que Chile se posiciona entre los primeros lugares del mundo en velocidad e infraestructura de Internet, pero con una brecha importante en la adopción de los estándares modernos requeridos.

La ausencia de IPv6 y la imposición de CG-NAT significan que el servicio actualmente prestado no constituye Internet pleno, sino un acceso restringido y discriminatorio, lo que infringe tanto estándares internacionales como la legislación nacional.
Dicho esto, el servicio ofrecido como “Internet” en realidad no cumple con los estándares internacionales de Internet ni con las obligaciones establecidas en la legislación chilena.

Solicito a las entidades reguladoras que:

1. Requieran a los proveedores de Internet en Chile habilitar IPv6 residencial de manera generalizada, conforme a las recomendaciones y requerimientos internacionales.
2. Establezcan un plan público de plazos y fiscalización para la migración, asegurando que los usuarios tengan acceso a conectividad extremo a extremo, como corresponde a un servicio de Internet pleno y al espíritu de la Ley de Neutralidad de la Red.

Espero que este llamado contribuya a que se reconozca y garantice el derecho a los clientes y usuarios a contar con un Internet pleno, libre y sin restricciones, cumpliendo con los estándares internacionales, la legislación nacional y las expectativas legítimas de conectividad global.
