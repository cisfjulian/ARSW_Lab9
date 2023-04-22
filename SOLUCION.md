# Escuela Colombiana de Ingeniería

## Solución

### Primera Parte

###  Creación maquina virtual

![image](https://i.gyazo.com/0f3eba00db90a0c3c2425458c2364a5a.png)
![image](https://i.gyazo.com/881a07af2bb2d6adbe35c9378b60b8b7.png)
![image](https://i.gyazo.com/a210b0e54b99f28c97781c408edcb9ad.png)
![image](https://i.gyazo.com/88cf3e25a8880d0aa3939eaab2a304cc.png)
![image](https://i.gyazo.com/6751b13437af4acd933282c5766f28f0.png)
![image](https://i.gyazo.com/804b492ff4e8480c5bf7b7e32c61e30b.png)
![image](https://i.gyazo.com/61ce4f737ad94e03bf9cce017adaf4a7.png)
![image](https://i.gyazo.com/06e97f236ce9c3382664d7f7de57969e.png)
![image](https://i.gyazo.com/fb3e794b3407f683745813c5e6a13e09.png)
![image](https://i.gyazo.com/7ec09f73ba709d62df032149d9dff034.png)
![image](https://i.gyazo.com/521e28bd4ef501a59f4d9482154066c0.png)
![image](https://i.gyazo.com/110421e69ce9d22c39598d0c8d486ebe.png)

Por un error en algunas solicitudes tomaron 6 minutos, esto se debe a que realicé una solicitud previa y tomaba el tiempo de la anterior mas la actual, pero todas tienen un tiempo promedio de 3 minutos. Y donde el ultimo ya estaba tomando una gran cantidad de tiempo.

![image](https://i.gyazo.com/4381f68347fef5edd57b350f6d6275f6.png)
![image](https://i.gyazo.com/3e476fd0e484c0af1dd51d95dabe8b72.png)
![image](https://i.gyazo.com/ecf0f39bc61a4bc0f9841c08b7be0199.png)
![image](https://i.gyazo.com/ca3a35b362b6ac383c86fbeefe0b0efc.png)

Ejecutamos el comando pero el proceso de calcular el millon es bastante demorado, ni si quiera procesa la primera petición. Por lo cual se continuara al siguiente punto


![image](https://i.gyazo.com/187d5e2c136632dd052f43923323c190.png)
![image]()

## Luego de cambiar el tamaño

![image](https://i.gyazo.com/f54aa1bae4a13a103c6c51ed282c39c2.png)
![image](https://i.gyazo.com/0a48a0c697d252872c3cf9c4c7204a07.png)
![image](https://i.gyazo.com/588e768641ee48a7ceb000da4cce0bbd.png)
![image](https://i.gyazo.com/41bcd725a6352de357b2286a68a55823.png)

Se logra concluir que el requerimento de escalabilidad si se cumple.

**Preguntas**

1. ¿Cuántos y cuáles recursos crea Azure junto con la VM?
![image](https://i.gyazo.com/0cfa2765d2a8c89805810f49ec546a7e.png)
2. ¿Brevemente describa para qué sirve cada recurso?
Crea basicamente la maquina virtual, las direcciones ip para poder verlas sobre la red, asigna el disco para usar en la VM, crea grupos de seguridad para regular quien accede a la maquina, en este caso una clave SSH, para poder conectarnos a la VM.
3. ¿Al cerrar la conexión ssh con la VM, por qué se cae la aplicación que ejecutamos con el comando `npm FibonacciApp.js`? ¿Por qué debemos crear un *Inbound port rule* antes de acceder al servicio?
Ya que al cerrar la conexion tambien termina todos los procesos que esten corriendo, con un forever podria mantenerlos ejecutandose. 
4. Adjunte tabla de tiempos e interprete por qué la función tarda tando tiempo.
5. Adjunte imágen del consumo de CPU de la VM e interprete por qué la función consume esa cantidad de CPU.
6. Adjunte la imagen del resumen de la ejecución de Postman. Interprete:
    * Tiempos de ejecución de cada petición.
    * Si hubo fallos documentelos y explique.
4. 5. 6. Se puede observar en las imagenes anteriores. La funcion tarda mucho ya que al tener un metodo tan lento o pausado para calcular el numero y ademas al no tener muchos recursos de hardware la funcion tarda mucho. Consume esa cantidad de CPU ya que asigna sus recursos para resolver la funcion, y estos recursos al ser tan escazos son casi que todos. El tiempo de ejecucion fue de 13 segundos ya al mejorar la maquina y hubieron errores de reset de conexion.
7. ¿Cuál es la diferencia entre los tamaños `B2ms` y `B1ls` (no solo busque especificaciones de infraestructura)? Las b1ls tienen muy pocos recursos, por lo cual cualquier ejecucion que realice va a tardar. Mientras que las B2ms tienen mas recursos tanto de RAM y de vCP, con lo cual es mas agil y eficiente.
8. ¿Aumentar el tamaño de la VM es una buena solución en este escenario?, ¿Qué pasa con la FibonacciApp cuando cambiamos el tamaño de la VM?
Si funciona ya que tiene mas recursos disponibles para el procesamiento por lo cual disminuye el tiempo que se toma FibonacciApp en procesar una peticion.
9. ¿Qué pasa con la infraestructura cuando cambia el tamaño de la VM? ¿Qué efectos negativos implica? Ya que se tienen mas recursos se necesita mayor infraestructura para poder sostener estos recursos, por lo cual se incrementa el coste.
10. ¿Hubo mejora en el consumo de CPU o en los tiempos de respuesta? Si/No ¿Por qué? Si hubo mejora en el consumo y tiempos de respuesta ya que al tener mas recursos disponibles se pudo reducir el procesamiento y se es mas rapido.
11. Aumente la cantidad de ejecuciones paralelas del comando de postman a `4`. ¿El comportamiento del sistema es porcentualmente mejor?


### Segunda Parte

![image](https://i.gyazo.com/5f9a5a1c22c0e103dcc5624d47c76b1d.png)
![image](https://i.gyazo.com/12b229284acdb45359c79debb9422a16.png)
![image](https://i.gyazo.com/eff3b1c1a761105d3dabc89615cb398b.png)
![image](https://i.gyazo.com/b03b841c98071d09ed8c54e66866af3a.png)
![image](https://i.gyazo.com/b6cb7e0c438c9e0eb3602af4b5debf74.png)
![image](https://i.gyazo.com/95a16895430f7f9cfae960aba8620cb2.png)
![image](https://i.gyazo.com/1ffe350bf5988b5589e7557c60a36c44.png)
![image](https://i.gyazo.com/68727e14944ce45d9a72e7401764489d.png)
![image](https://i.gyazo.com/5559359fc4387008de7c48f88213f1d0.png)

La suscripcion solo permite tener 3 direcciones publicas, por lo cual solo trabajare en 2 maquinas virtuales con su propia IP + la IP del balanceador de carga.


![image](https://i.gyazo.com/a20006f87996bb028718da5bb7aa5a8e.png)
![image](https://i.gyazo.com/73ef2a880cf47f3a478a793ab9ab50ea.png)

Sin embargo al intentar ejecutar la aplicacion da error con el forever

https://i.gyazo.com/9e4efea6f963841d325cb85924b58caa.png

Pero al ejecutarla como la parte 1 lo permite aunque solo sera mientras la conexion ssh se encuentre arriba

![image](https://i.gyazo.com/6ce6139855746abc24cf378316b43dfd.png)

Si ponemos la direccion y le enviamos un request por ejemplo con el 1 tenemos que le hace la peticion a la VM1.

![image](https://gyazo.com/10d0628890d80896d5c173ad93ee053d)
![image](https://i.gyazo.com/6c6d80205cd814bd15f83f63ac883023.png)

Y ahora si hacemos otra peticion al mismo URL la trabajara a la VM2. 
![image](https://i.gyazo.com/bafd56c95a149891b679955933456b0c.png)

Con lo cual vemos que el balanceador si funciona y distribuye las peticiones!

Ahora instalamos newman en alguna de las dos maquinas y haremos las mismas pruebas de la primera parte

![image](https://i.gyazo.com/60ba8fe796d3374d2dceffafa055fbe7.png)
![image](https://i.gyazo.com/cc72c14fbf20e546ee8da6ebc38bdaa6.png)

Tenemos la tabla del newman con el resumen donde solo hubieron 2 errores

![image](https://i.gyazo.com/54fd6c3df00e0c83597164b29d031a91.png)

Pero vemos que en ambas VM se distribuyo las peticiones 

![image](https://i.gyazo.com/8aa2406b7490123bd70d9b0df8b7197e.png)

Comparando la escalabilidad horizontal y vertical, llega a ser mas costosa la horizontal ya que es tener mas dispositivos o maquinas disponibles para recibir las peticiones, sin embargo la carga se distribuye de mejor manera y puede tener mayor disponibilidad, tambien tuvo menos fallos, respondio con exito mas peticiones. La vertical puede llegar a ser mas rapida pero de esta fallar no habria como distribuir a otra parte las peticiones facilmente, tuvo mas errores aunque procesa de manera mas rapida las peticiones.

**Preguntas**

* ¿Cuáles son los tipos de balanceadores de carga en Azure y en qué se diferencian?, ¿Qué es SKU, qué tipos hay y en qué se diferencian?, ¿Por qué el balanceador de carga necesita una IP pública?
Los publicos y privados. Los publicos proporcionan conexiones hacia afuera para las maquinas virtuales dentro de la red. Se usan para balancear el trafico de internet a las Vms. Y los privados son solamente usados para el frontend. Usados para balancear el trafico dentro de alguna red virtual. 

SKU son combinaciones de maquinas virtuales y sus especificaciones para componer una sola unidad de inventario. Se diferencian en que cada una tiene un procesador determinado y vCPU para cubrir segun las necesidades que se tengan.

* ¿Cuál es el propósito del *Backend Pool*?

Definir el grupo de recursos a los que va a ser redireccionado el trafico por el balanceador de carga. 

* ¿Cuál es el propósito del *Health Probe*?

Sirve para detectar el estado en el que se encuentra el endpoint. Ya que si no se recibe respuesta del endpoint determinado el balanceador no redireccionara el trafico para ese endpoint que no esta funcionando o segun las reglas realiza alguna accion.

* ¿Cuál es el propósito de la *Load Balancing Rule*? ¿Qué tipos de sesión persistente existen, por qué esto es importante y cómo puede afectar la escalabilidad del sistema?.

Utilizada para definir como el trafico proveniente se va a distribuir a todas las instancias del Backend Pool. Tiene tipos de persistencia ClientIp(2-tuple) especifica que las peticiones subsecuentes de ese cliente Ip van a ser manejadas por esa misma instancia. Y Client Protocol(3-tuple) que especifica que las peticiones subsecuentes de la misma direccion ip del cliente y protocolo seran manejadas por la misma instancia del back.

* ¿Qué es una *Virtual Network*? ¿Qué es una *Subnet*? ¿Para qué sirven los *address space* y *address range*?

Es una red que permite conectar maquinas virtuales y dispositivos, sin importar su ubicacion. Para poder comunicarse entre usuarios, internet y redes locales.
Subnet son subredes para que sea mas eficiente la comunicacion. Partirciones de una IP en pequeños segmentos. 
Address space es la cantidad de memoria alojada para todas las posibles direcciones ip que se puedan utilizar.
Address range  es un rango para direcciones privadas.

* ¿Qué son las *Availability Zone* y por qué seleccionamos 3 diferentes zonas?. ¿Qué significa que una IP sea *zone-redundant*?

Avaliability Zone son data center aislados en regiones especificas los cuales son accesibles. Se seleccionan diferentes zonas para que en caso de que falle o se caiga alguna zona no falle el servicio, solo una de las maquinas. Mejorando RTO y RPO.

Que la Ip pertenezca a esa zona.

* ¿Cuál es el propósito del *Network Security Group*?

Filtrar el trafico entre los recursos Azure en una red virtual de azure. A traves de reglas establecidas para aprobar o denegar trafico proveniente o el trafico saliente de algunos servicios.

* Informe de newman 1 (Punto 2) Puesto arriba junto los demas pantallazos.

* Presente el Diagrama de Despliegue de la solución.



