
# Requisitos de Calidad

**Integrantes:**  
Nicolás Gutiérrez Ramírez - 2259515  
Cristhian Leonardo Albarracin zapata -1968253   
Miguel angel ceballos yate - 2259619   
Harrison Ineey Valencia Otero - 2159979  
Geraldine Florez Rico - 2269476   



| ID    | Fuente       | Estímulo                                                       | Artefactos               | Entorno                        | Respuesta                                                          | Medida de Respuesta                                         |
|-------|-------------|----------------------------------------------------------------|--------------------------|--------------------------------|--------------------------------------------------------------------|-------------------------------------------------------------|
| RQ-01 | Administrador | Se requiere escalar la plataforma para soportar 10,000 usuarios simultáneos. | Servidor y base de datos  | Pico de carga                  | Se deben habilitar instancias adicionales en la nube de manera automática. | La latencia no debe superar los 2 segundos por petición.  |
| RQ-02 | Usuario      | Un usuario intenta realizar una oferta en una subasta de alto tráfico. | Servidor y API de subastas | Condiciones de alta concurrencia | La oferta debe ser procesada sin errores ni inconsistencias.   | 99.9% de las ofertas deben registrarse sin fallos.         |
| RQ-03 | Seguridad    | Un usuario intenta acceder a una subasta privada sin autorización. | API y base de datos      | Intento de acceso no autorizado | El sistema debe bloquear el acceso y registrar el intento en los logs. | 100% de accesos no autorizados deben ser rechazados.       |
| RQ-04 | Usuario      | Los usuarios deben poder comunicarse en un chat en vivo dentro de cada sala de subasta. | Servidor y sistema de chat | Condiciones de alta concurrencia | El chat debe ser en tiempo real y permitir mensajes sin retraso significativo. | 99% de los mensajes deben entregarse en menos de 1 segundo. |

## Historias de Usuario
1. Como usuario, quiero poder hacer ofertas en una subasta sin retrasos ni errores, incluso en momentos de alta demanda.
2. Como usuario, quiero poder comunicarme con otros participantes en una subasta a través de un chat en vivo.
3. Como administrador, quiero que la plataforma escale automáticamente cuando haya un pico de carga.
4. Como administrador de seguridad, quiero que los accesos no autorizados sean bloqueados y registrados en los logs.

## Requisitos de Calidad
1. La plataforma debe procesar el 99.9% de las ofertas sin errores ni inconsistencias.
2. El sistema de chat debe garantizar la entrega del 99% de los mensajes en menos de 1 segundo.
3. La escalabilidad automática debe mantener la latencia por debajo de 2 segundos por petición.
4. El sistema debe rechazar el 100% de los intentos de acceso no autorizados.

## Historias de Calidad
1. Como usuario, quiero que mi oferta en una subasta se registre correctamente sin errores.
2. Como usuario, quiero que mis mensajes en el chat sean entregados inmediatamente.
3. Como administrador, quiero que el sistema escale de manera automática para evitar caídas de rendimiento.
4. Como administrador de seguridad, quiero que cualquier intento de acceso no autorizado quede registrado y sea bloqueado.

## Restricciones del Sistema
1. El chat en vivo debe estar limitado a los usuarios que participan en la subasta.
2. No se deben procesar ofertas si la subasta ha finalizado.
3. El sistema de escalabilidad no debe exceder el presupuesto de recursos en la nube.
4. Los registros de accesos no autorizados deben almacenarse por al menos 6 meses.

## Lista de Restricciones
1. Límite de 10,000 usuarios simultáneos.
2. Mensajes en el chat no deben exceder los 500 caracteres.
3. Solo los usuarios registrados pueden participar en una subasta y en el chat.
4. El sistema debe cumplir con normativas de protección de datos como GDPR y CCPA.
5. El escalado automático debe mantenerse dentro del presupuesto definido por la administración.

