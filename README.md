# DiplomaturaLogistica-CDA-TrabajoFinal

**Integrantes del grupo Nº 5 -**

- Matias Vanni <Matiaasvanni@gmail.com>
- Joaquin Nougues <joaquinnougues71299@gmail.com>
- Emilio Gabriel Paredes <chogabrielparedes1999@gmail.com>
- Facundo Vargas <vargasfacundomiguel@gmail.com>
- Federico Antonio <federicoangelantonio1@gmail.com>

*_TRABAJO FINAL: ENUNCIADO_*

[2023 Trabajo práctico para evaluar Diplomatura.pdf](https://github.com/FedericoAntonio1/TrabajoFinal-Diplomatura-Log.-CDA/files/13351765/2023.Trabajo.practico.para.evaluar.Diplomatura.pdf)

_*Empresa de referencia*: **Grupo UNIBER**_


## **_DESARROLLO DEL TRABAJO_**

## 1. Gestión del flujo de Pallets
 
Situación Actual: Describa en hasta una página la situación actual y el
problema detectado. Trate de utilizar números (costos,
tiempos, unidades)
Situación mejorada: Describa la mejora que propone para la situación
actual, justificando en cada aspecto relevante por
qué cree que esa implementación mejoraría_*

**_Situación Actual_**

Grupo UNIBER es una empresa dedicada a la comercializacion de materiales de construccion , para minoristas y mayoristas. Actualmente cuenta con sucursales en provincia de Salta, Catamarca, Jujuy y Tucuman. 
El trabajo esta referido al abastecimiento terciarizado de cemento y devolucion de pallets desde el proveedor Loma Negra, con aprovisionamiento de las sucursales de Supermat (ubicadas en Oran, Tartagal, Salta Capital y Jujuy), El Sol Materiales (en Yerba Buena y Lastenia, Tucuman) e Hipercat (en Catamarca), con la aclaracion de contar con 2 sucursales en Salta Capital: ATH y CHILE.
La empresa UNIBER presenta una problemática en la gestion de devolución de pallets frente a su proveedor Loma Negra, ocacionando una pérdida económica significativa. El criterio de Loma Negra para la facturacion al cliente (UNIBER) es contar con el saldo pendiente mayor al 25% de la salida de pallets del mes, este porcentaje se considera como mercaderia en circulacion. La facturacion es un resultado de un analisis realizado el día 5 o 6 del mes siguiente, comparando la variacion entre las salidas y entradas de tarimas (despacho e ingreso de Loma Negra) y una _foto_ del total de salida del corriente mes.  

A continuación, se presenta un caso real:
_Datos a tomar en cuenta:_ 

- Cliente de Loma Negra: SUPERMAT (Razon social que comprende parte de Grupo UNIBER)
- Costo unitario de tarima: $11.200 + IVA

En el mes de octubre se realizo una compra y abastecimiento de Loma Negra de un total de 370 equipos de cemento aproximadamente. Entendiento que cada transporte que llega con cemento a la sucursal, cuenta en promedio con 15 pallets de cemento, lo que nos da un total de abastecimiento de 5570 pallets despachados de fabrica. Entonces, siguiendo con el criterio del proveedor para facturacion de tarimas (pallets), deberiamos contar con un saldo de solo 1388 pallets (tarimas vacias) para el momento de analisis final realizado el 05/11. Lo que finalmente paso es que se conto con un saldo de hasta 2200 tarimas, mas de 800 por arriba del limite y para el analisis final el 05/11 con un saldo de 1750 tarimas. Lo que genero una facturacion de 400 pallets del mes de octubre. Cabe aclarar que la facturacion de pallets a clientes es de solo 140 pallets, lo que no llega a justificar el costo incurrido para una gestion deficiente en la devolucion de tarimas al proveedor. 

Se podria optar, en los primeros dias del mes, optar por no despachar nada de cemento y con esto no incurir en aumentar la deuda hasta el 05 del mes, periodo final de analisis. Esto presenta un inconveniente, ya que, siguiendo con el ejemplo de SUPERMAT en octubre, demanda diariamente 15 equipos de cemento aproximadamente. Esto genera un despacho de hasta 225 pallets por dia.

**_Situación mejorada_**

Se propone como solución: 

A)Revisión y control del flujo de tarimas, junto con un seguimiento desde la web LOMANET clientes. Es un cambio significativo ya que la empresa únicamente vendía cemento e ignoraba la cuestión de las tarimas, actualmente se sabe cuántas de ellas ingresan a la empresa, cuantas salen y donde están, quienes son los transportistas que realizan devoluciones. 

B) A los clientes con cuenta corriente emitirles conceptos facturables por las tarimas que llevan junto con el cemento, con el mismo criterio del tope del 25% que impone Loma Negra.
C) Para los clientes de contado: 1. cargar las bolsas a granel; 2. facturarles las tarimas; 3. el cliente al momento de cargar debe ir con sus tarimas.

D) Para una optimización de los costos logísticos, se proponen devoluciones quincenales de pallets con equipos completos a Loma Negra. Ese mismo camión que devuelve las tarimas, carga cemento para retornar a Tuc. Cabe destacar que cumplir con la política de devolución reduce no solamente las perdidas monetarias, sino también contribuye a reducir el impacto ambiental mediante la reutilización. Se busca una comunicacion constante entre los involucrados en el circuito de tarimas. 

E) Ademas, se busca llevar el stock de la sucursal a valores optimos en el ultimo dia del mes, para luego bajar el aprovisionamiento hasta fecha del analisis final. Con esto conseguimos no demandar tanto cemento en los primeros dias del mes y no aumentar considerablemente el saldo de pallets. Desafortunadamente, esto aumenta la posibilidad de contar con una rotura de stock en la sucursal.


## Implementacion - Mes de noviembre

Para el mes de noviembre de implemento algunas de las ideas propuestas anteriormente, logrando resultados favorables. A continuacion informamos el comportamiento del stock de cemento de las sucursales que comprenden SUPERMAT y el resultado del analisis de tarimas del mes de noviembre, con periodos de analisis el 01/12 y el 05/12.

Cabe aclarar que los graficos de las sucursales (**Vease: "ABASTECIMIENTO LN-UNIBER NOV23.xlsx - PRESENTACION**) tiene como parametros el stock optimo que puede tener de inventario de la sucursal (Linea verde), el 50% de la misma (linea amarilla) y un stock minimo de 2 veces la demanda diaria estimada (linea roja). 

Observamos en el analisis de tarimas (**Vease: "TarimasNoviembre_Supermat"**) que se pudo reducir de un saldo negativo de 2092 tarimas a 1506 para el dia 05/12. Vemos que anteriormente, para el fin del mes, contamos con 1275 tarimas como el limite de tarimas que se podria deber. El resultado final es 208 pallets por arriba del limite, con un justificativo de una facturacion de 228 tarimas facturadas a cliente durante el mes y un desperdicio de 110 pallets.

## 2. Proceso de la empresa y gestión logística

Situacion Inicial: Defina el proceso principal de su empresa, sus entradas,
salidas y la forma de trabajo. Indicar los proveedores,
clientes y responsables de dicho proceso.

Situacion Mejorada: Describa brevemente los inconvenientes en cuanto
a la gestión y sobre todo en cuanto a la gestión
logística que usted visualiza en su empresa. Debe
definir al menos las tres principales problemáticas_*

**Situacion actual**

Uniber realiza comercializacion mayorista y minorista en el rubro de la construccion, teniendo como clientes a empresas constructoras, corralones y consumidores finales para el mercado minorista. 
La empresa tiene proveedores de materiales en todo el país, algunos de ellos son: Loma Negra, Weber, Tensolite, Placo, Cerámica Alberdi, Cañuelas, Zapla y Ternium. 
Para corralones y empresas constructoras, se les brinda un servicio de entrega en equipos completos directo desde fabrica o en la mayoria de los casos, reparto desde la empresa. Además, se tiene la opcion de retiros desde sucursal. Para las operaciones mecionadas, cada sucursal cuenta con un equipo de trafico, que varia en la cantidad de integrantes dependiendo de cada una. 

*Vease imagen adjunta: "Cadena de abastecimiento-grafico"*

En cuento al proceso principal de UNIBER, muchos dirian que es la comercializacion, pero es un errorconcluir que no ve en los procesos de logistica y cadena de abastecimiento, un potencial diferencial en el mercado. La empresa tiene un panorama optimista para el futuro, donde el precio y la forma de pago, en un economia estable, es parecida entre la competencia. El gran diferencial en el mercado, va a ser los tiempos de entregas y la gestion de *repartos desde las sucursales*. 

Actualmente, las operaciones de reparto a clientes, cuentan con una participacion del XX% sobre la facturacion total. *(Vease archivo adjunto: "Participacion logistica y CDA en FC total")*

Si hablamos de la sucursal de El Sol Materiales, ubicada en San Miguel de Tucuman, el equipo de trafico esta ingregrado por 4 personas especializadas en la entrega de materiales desde sucursal a cliente: 3 administrativos y 1 operarivo; tambien cuenta con 1 persona responsable del abastecimiento _fabrica-ElSolMateriales_ y entregas de material _fabrica-cliente_. 

Para esta sucursal, se presentan *inconvenientes* como la ubicación de los corralones que piden equipos completos a domicilio. Los mismos, tienen accesos muy limitados que imposibilitan las maniobras de los camiones. En estos casos, se deben seleccionar chasis acoplados para un mejor radio de giro. 

Otro inconveniente que presenta el area a la hora de realizar las entregas es la falta de stock, en la sucursal donde se esta por realizar el despacho, de uno o varios materiales a entregar en el dia. Esto no sucude siempre y se debe a una mala distribucion de existencia en las sucursales existentes en una provincia en particular. Para el caso de *El Sol Materiales*, el mismo cuenta con dos sucursales, una ubicada en San Miguel de Tucuman y otra en la localidad de Lastenia. En varias ocasiones, esto trae un costo de *transferencia* (moviento de material entre sucursales), generando "ruido operacional" y en el peor de los casos, reprogramando el envio. Este costo esta visto como un mal menor y no existe seguimiento ni analisis al respecto. 

Otros inconvenientes, son los paros de planta de Loma Negra, las propias roturas de los camiones contratados, la complicación con los vendedores que quieren que se entreguen equipos a clientes que aún no tienen orden de compra, además de la lucha constante contra las tarifas de los transportistas que buscan maximizar ganancias mientras la empresa busca disminuir costos. 


## 3. Funcionamiento de la cadena de abastecimiento

Situación Actual: Describa gráficamente y en palabras el funcionamiento de
la cadena de abastecimiento actual de su empresa.
Situación mejorada: De similar forma, proponga una cadena de
abastecimiento mejorada, consignando las mejoras
establecidas y justificando los cambios_*

**Situacion actual**  

La cadena de abastecimiento de la empresa funciona de diferentes maneras, específicamente con Loma Negra se utilizan camiones contratados para buscar cemento desde la fabrica (FOB), y se utilizan fletes de loma negra (CIF).

Comprar mediante CIF proporciona ventajas significativas como ser una menor gestión administrativa en los envíos (se encarga el proveedor), sin embargo, solo es posible elegir 2 o 3 destinos fijos, imposibilitando el envío directo a cada cliente. Por otro lado, el FOB permite realizar dichos envíos directos, pero con un costo más caro. 
Los camiones contratados son mayormente de Tucuman y tienen que ir hasta Catamarca, donde se encuentra la fábrica de Loma Negra, en búsqueda del cemento. Estos entregan directamente desde la fabrica al cliente o se dirigen al deposito de El Sol en San Miguel de Tucuman a dejar la carga. En este ultimo caso, una vez que ya esta la orden de preparacion del pedido, se procede a realizar el mismo y se le comunica al cliente el turno asignado que tiene para retirar su pedido.

**Situacion mejorada**

En la situacion actual se cuenta con dos problematicas en la cadena:
1. El tiempo de espera que tienen los camiones para descargar debido a que hay un solo flujo en el deposito para carga y descarga
2. La tarifa unica que se les cobra a los clientes por envio
   
Ante la primera problematica se propone lo siguiente:

Hacer una nueva distribucion de los productos en el deposito y una sectorizacion que permita tener bien definidas las zonas de carga y descarga para asi ganar tiempo y espacio. La nueva sectorizacion se hara en base al diagrama ABC en el cual los productos A estaran en las zonas de rapido acceso, ya que estos son los que mayor rotacion tienen. Ademas, debido a este nuevo orden de productos, se ganara espacio, lo que permitira tener dos lineas separadas, una exclusiva para descarga y otra para carga, esto permitira un mejor flujo de movimiento de camiones y disminuir los tiempos muertos, tanto de los clientes como de los proveedores. 

Con la segunda situacion se propone la siguiente solucion:

Se sectorizaran los clientes de Tucuman ya que en estos momentos se le cobra la misma tarifa a todos. Esta sectorizacion permite definir bien las zonas de entrega y armar un tarifario con valores diferenciados teniendo en cuenta la cantidad de kilometros recorridos desde la fabrica al destino.



## 4. REPARTO, Gestion de cumplimiento de mercaderia en reparto 

Situación Actual: Describa brevemente cómo funciona actualmente la
gestión de operaciones en su proceso principal y al menos
dos problemáticas abordadas en el curso. Resalte el uso de
pronósticos, gestión de la mano de obra y subcontratación._*

*_Situación mejorada: Describa mejoras posibles de implementar en la
Gestión de operaciones en relación a: uso de
pronósticos, gestión de la mano de obra y
subcontratación_*

**Situacion actual**

El proceso principal de la gestion de operaciones es el reparto local (distribución a clientes b2c y b2b), el cuál esta a cargo del area de trafico de la sucursal correspondiente. Enfocando el estudio en la sucursal de El Sol Materiales, observamos que la gestion de reparto de mercaderia a clientes (corralones y empresas constructoras) cuenta con un responsable del ruteo de la flota propia (6 camiones) y transportes tercerizados. En este aspecto, el planeamiento es con una anticipacion de 1 o 2 dias, con "cierres de dias" dependiente a pesaje total o volumen a entregar. Es decir, si hablamos de una capacidad maxima a transportar de 8 a 9 Toneladas por camion, el vendedor podra seguir asginando entregas a clientes para un dia especifico hasta cumplir con lo maximo que puede transportar la flota de la sucursal y 4 a 6 camiones tercerizados. El area cuenta ademas con un responsable para la comunicacion con el cliente, donde se realiza confirmacion de recepcion por parte del cliente y alineamiento de la hora aproximada de la entrega. 

*Problematica abordada*

1. Una problematica que presenta el area, son los casos de falta de stock para la entrega completa de un pedido. Es decir, las entregas que terminan la jornada con un estatus de *pendientes por falta de stock* o *Caidos por stock*. 

Aqui es oportuno comentar que el faltante de stock se debe a una mala distribucion de las existencias. Actualmente, la sucursal de El Sol Materiales cuenta con 2 depositos, uno en San Miguel de Tucuman y otro en Lastenia. Se cuenta con un responsable del area de compras que gestiona la adquisición de materiales, como asi también las transferencias para que los depositos tengan una distribucion eficiente del stock. 
Tambien vemos que las operaciones de *transferencias* (movimiento de mercaderia intersucursal) estan normalizadas por parte del equipo de trafico. Realizando hasta 3 operaciones semanalmente de hasta 9 toneladas cada una, con motivo de necesidad urgente para completar el pedido pendiente. Con esto incurrimos en un costo que no esta analizado y pasa desapercibido para la jefatura del area. **Vease archivo adjunto: *Info diaria Octubre 2023***

2. Otra problematica que enfrenta el area es no contar con un personal que se dedique exclusivamente en la gestion de operaciones, refiriendonos a a alguien con la responsabilidad de buscar la mejora continua de las operaciones, definir indicadores claves del area y crear cultura de reuniones, feedbacks e checkeo de informacion para todo el equipo. Actualmente el area, en sus cargos medios, no esta profesionalizada. 

Poodemos mencionar algunos indicadores que si se analizan del area: 

**Vease archivo adjunto: *Tnforme PHR - Octubre*** 

**Vease archivo adjunto: *Info diaria Octubre 2023***

a. Calidad de programacion: Mide el cumplimiento del total de hojas de rutas o reparto compremetido de la fecha. Podemos observar para el mes de octubre un total de 1158 repartos durante el mes, donde solo el 10 tuvieron incumplimiento por una deficiencia o mal programacion del area de trafico. Cabe aclarar que en el mismo mes se tuvo un incumplimiento 214 entregas, de las cuales solo 10 son consideradas como *caidas por trafico* e impactan en el indicador. 

b. Cumplimientos de pendientes: En el momento que se genera un incumplimiento de entrega, el area cuenta con un tiempo de 72hs para la entrega pendiente. Este indicador mide cuanto del total de pendiente es cumplido durante ese tiempo. 
 
3. Otra problematica que presenta el area son los casos en donde no se gestiono una actualizacion de la direccion de entrega de emrpesas constructoras, donde las obras en construccion van cambiando. Esto puede generar demoras en las entregas posteriores, en las entregas pendientes y costo de hora extra en mano de obra tanto para el cliente como para la empresa. Actualmente solo se cuenta con pronósticos de ventas basados en ventas históricas.


 **Situacion mejorada**

Vemos oportuno la inversion en un analista de gestion, con la necesidad de crear cultura de reuniones e innovar en indicadores como *Tiempo de preparacion de pedido*, *Pedido sin reclamo*, entre otros. Otra gestion importante es hacer seguimiento del gasto de combustible de la flota, realizar un mantenimiento preventivo y alinear al personal para buscar la mejora continua en todas las operaciones. 

Tambien observamos que una mejor comunicacion por parte del equipo comercial, en cuanto a sus objetivos de ventas, permitiria al equipo de logistica y reparto estar preparado para los picos de actividad.  


## 5. Gestion de Inventario 

*_Situcaion actual_*
Describa brevemente cómo funciona actualmente la gestión de inventarios en su empresa y al menos dos problemáticas abordadas en el curso. Resalte el uso de pronósticos y algoritmos que se utilizan.

*_Situcaion mejorada_*
Describa mejoras posibles de implementar en la gestión de inventarios en relación al uso de pronósticos u otra metodología que considere.

**Situacion actual**
En cuanto la gestion de inventarios, podemos observar que la empresa, al comercializar en su mayoria materiales con una vida util exsesiva, puede descuidar las existencias de cemento. Este material cuenta con un vencimiento de 30 dias desde su produccion. Se apuesta a la alta rotacion del material, por eso no se realiza un seguimiento minusioso de las posiciones del mismo. Ademas existen casos en donde el cliente exige una entrega de cemento con una alta brecha de tiempo hasta el vencimiento. 

**Situacion mejorada**

Propuestas de mejoras: 

1. Realizar objetivos y proyecciones semanales de ventas.
   
2. Definir un stock minimo, stock máximo y puntos de reposición para las sucursales.

3. Implementar sistema FEFO en el inventario de cementos, puesto que perecen a los 30 días de fabricado.

4. En cuanto a los almacenes, se propone trabajar con un diagrama ABC, el cual se realiza a partir de los productos que tengan mayor rotacion. Para esto es importante contar con un informe de ventas de los principales sku. Gracias a esta medida, se puede solucionar en parte la problematica del El Sol Materiales que tiene respecto al tiempo de preparacion de los pedidos y el quiebre de stock.


## 6. Costos Logísticos 


*Situación real*
Analice los costos logísticos de la situación actual,
consignando costos fijos, variables y las amortizaciones de
bienes de capital sobre todo los aplicados a la logística

*Situación mejorada*
Consigne cómo consideraría los costos RELEVANTES
para la toma de decisiones

**Situación real**

Uniber al ser una empresa que se encarga tanto del abastecimiento y distribución de todo tipo de materiales de construcción, la optimización de los costos logísticos es crucial para lograr la maximización de ingresos de la empresa, ya que en caso de realizar una mala gestión de la misma, se pueden generar grandes pérdidas económicas.

El Sol Materiales contrata transportes para el abastecimiento de materiales directamente de fabricación, ubicados en distintos puntos del país, teniendo un tarifario propio y calculandose el incremento mensual del mismo con porcentajes ligeramente menores a los establecidos por el índice FADEEAC(Federación Argentina de Entidades Empresarias del Autotransporte de Cargas). Los encargados del aprovisionamiento son el líder de tráfico corporativo y el analista de tráfico corporativo.

Para enviar los materiales a los clientes el sol materiales posee una flota de 6 camiones, 3 camiones con estructura para la carga mixta de pallets y de chapas y hierros torsionados, y 3 camiones playos que son preferentemente para cargas paletizadas. Estos envíos son gestionados por el área de tráfico.

Loma Negra posee la opción de compra CIF, es decir, incluyendo el costo de flete, o bien FOB, llevando un camión propio del cliente a fabricar para retirar el cemento (siempre y cuando cumpla con las normas de seguridad establecidas por loma negra). El sol materiales utiliza el inoterm FOB, ya que el costo de transporte es un 25% más económico utilizando un camión contratado por la empresa.

Los materiales son colocados directamente en los propios para su reparto, por lo tanto los valores de costo de embalaje no serán aplicables en este caso, tampoco seria aplicable el costo de adquisición por tratarse de una empresa de comercialización y distribución.

Dicho esto se pueden dividir los costos logísticos en fijos y variables:

COSTOS FIJOS, que se componen de:

-sueldos, sampistas, operadores de tráfico, choferes.
-costo mantenimiento autoelevador, puente grua, camiones propios, estos son realizados cada 6 meses.

Costo variable, que depende de la cantidad de materiales a retirar y distribuir:
-costo flete tercializado para abastecimiento
-Costo de combustible de flota propia

Amortizaciones de bienes de capital:
- Fota de vehiculos
- Instalaciones


## 7.  Area de Logistica - UNIBER


*Situación real*
Describa cómo está compuesto el sector de logística o bien el que lleva a cabo esta actividad. Realice un organigrama del sector. Describa las competencias del personal.

*Situación mejorada*
Hable del principal problema con el personal del sector y proponga una solución en base a lo visto en el curso.

**Situación real**

Como observamos en el organigrama (**Vease la imagen adjunta: *OrganigramaLogisticaUNIBER***) el area de logistica cuenta con un gerente corporativo arriba de todos, quien asume las responsabilidades alte la gerencia sobre todas las operaciones de logisticas del grupo uniber. Abajo de el, cuenta con la jefatura de cada sucursal que integra la empresa. Esta persona esta como responsable del deposito, las operaciones de reparto y son los que mayor personal a cargo tienen. Un Ej. es el jefe de operaciones y logistica de El Sol Materiales, con hasta 40 personas a cargo. Este grupo esta ingregrado por responsables de depositos, operarios de los mismos, choferes de la empresa, administrativo de logistica y operativo de reparto. 

El area cuenta ademas con una de equipos corporativos, que cubre necesidades de gestion de todas las sucursales por iguales. Cuenta con la jefa de abastecimiento que divide el total de mercaderia que comercializa la empresa y realiza un analisis de abastecimiento. Este es el sector que realiza el pedido de compra y luego es el area de compra que negocia y concreta la compra del material. Esto es devuelto al area de logistica, donde el equipo de trafico gestiona la correcta disponicion de transporte desde la fabrica a sucursal. Este equipo actualmente cuenta con un leader corporativo y un analista operativo. 


**Situación mejorada**

Podemos observar una ausencia de analistas de gestion en todo el organigrama. Esto dificulta los objetivos de mejora continua y demora la estandarizacion de procesos. Se debe buscar una inversion en puestos donde brinden una visibilizacion de las posibles mejoras que implementar y la incorporacion de indicadores claves. 


## 8. Modelo SCOR

*_Situación actual:_* En base al cuadro de la página 61 del libro sugerido, del modelo SCOR indique qué indicadores pueden actualmente relevarse en la empresa.

*_Situación mejorada:_* En base a las mejoras propuesta, seleccione al menos 3 nuevos indicadores y describa brevemente cómo los mediría.

Situación actual: 
Para relevar los indicadores que pueden aplicarse actualmente con la información disponible, nos centraremos en la P4 Planeación de la distribución:
1. Tiempo de cliclo efectivo - efectivo
2. tiempo de cumplimiento de la orden
3. costos totales de distribución
Cabe aclara que actualmente no se realizan mediciones con la metodología SCOR

Situación mejorada:
Con las mejoras propuestas en este proyecto, podríamos aplicar los siguientes indicadores:
P1 PLANEACION DE LA CADENA DE SUMINISTRO
1. costo de planificar el aprovisionamiento: suma de costos administrativos por emitir órdenes de compras, costos de la mercadería, flete e ingreso al almacen.
2. tiempo de cumplimiento de orden: tiempo desde que una sucursal / cd solicita mercadería hasta que la recibe.

P4 PLANEACION DE LA DISTRIBUCION
1. tiempo de ciclo efectivo - efectivo: tiempo desde que la empresa saca a distribución las guías hasta que las cobra. 
2. tiempo de cumplimiento de orden: tiempo desde que el cliente emite una oc y la recibe, así medir qué porcentaje de cumplimiento en las entregas tenemos (previamente establecer un objetivo de N días según localidad).
3. costos totales de distribución: suma de costos de preparación de pedidos, out, distribución y rendición de documentación.

P5 PLANEACION DE LAS DEVOLUCIONES
1. costos de devoluciones: suma de los costos de logistica inversa, recpeción y control e ingreso en almacén.
2. tiempo de cumplimiento de orden: tiempo desde que el cliente emite una or y la recibimos en nuestro almacén (previamente establecer un objetivo de N días según localidad).
