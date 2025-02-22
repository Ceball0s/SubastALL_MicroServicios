
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

