## Introducción
- Axxon Face PSIM es un sistema que interconecta dispositivos de diferentes áreas para mantener la seguridad en un complejo, tales como: cámaras de video, puertas de acceso, detectores de humo, ... , en un solo software con capacidad de ampliación con diferentes módulos (de pago).
- El enfoque del siguiente análisis se va a centrar en el control de acceso de personas, así como los diferentes métodos utilizables para alcanzar esa meta.

#### Documentos
Este análisis se completó haciendo uso de los manuales: 
- *Base PSIM* (https://docs.axxonsoft.com/confluence/display/PSIM100en/Documentation) -> enfocado en los diferentes módulos y el uso del sistema
- *Face PSIM* (https://docs.axxonsoft.com/confluence/display/FacePSIM100en/Documentation) -> enfocado en el uso del reconocimiento facial (aunque *Base PSIM* también cuenta con información acerca de esto)
- *Web System Report PSIM* -> enfocado en los reportes (https://docs.axxonsoft.com/confluence/display/rptPSIM100en/Documentation)

## Control de acceso
### Reconocimiento facial 
- Axxon se especializa en el reconocimiento de objetos, personas, carros, entre otros, creando registros del objeto reconocido para almacenarlo en una base de datos. 
- A cada persona identificada se la puede asignar un nombre, departamento, niveles de acceso, horario permitido de acceso y zonas permitidas de acceso. Esto facilita el control de ingreso de dicho individuo en las diferentes facilidades, pues este Software se puede conectar con, por ejemplo: puertas de ingreso y cámaras térmicas, permitiendo a la persona entrar, si es que es autorizada y no tiene fiebre.
- Asimismo se crea un registro de la edad, género, vello facial y articulos de cabeza (lentes, gorras) por persona y es capaz de reconocerla si es que estos cambian. Aunque este sistema puede reconocer el uso de mascarillas y máscaras, este no va asociar la cara como conocida. 
- Cada aparición de una persona queda registrada con fecha, hora y el nombre de la cámara que la vio, lo que facilita sacar un reporte de las personas que entraron a cierta hora, la primera y última vez que se lo vio a alguien, o personas que no fueron reconocidas.

#### Configuración para reconocimiento facial
- https://youtu.be/FSAo_vCQZKU?feature=shared
- https://docs.axxonsoft.com/confluence/display/PSIM100en/Face+Detection+tool+basic+settings


### Detección de movimiento - VMDA Detection
- Axxon PSIM viene integrado con un "*Tracker*", que sirve para el seguimiento de objetos. Esto se lo puede usar para identificar la dirección de movimiento de una persona, lo cual resulta útil a la hora de controlar el acceso del personal. Por ejemplo: una cámara puede tener dos líneas virtuales que apunten a la entrada o salida, para  que cuando alguien las cruce identifique su dirección de movimiento. Usando este sistema en cojunto con el lenguaje integrado de Axxon PSIM, se puede lograr un conteo de gente que atraviesa una entrada, como se va a describir luego.
- https://docs.axxonsoft.com/confluence/display/PSIM100en/Creating+and+configuring+the+VMDA+detection

#### Tag&Track
- Aparte del *Tracker*, Axxon PSIM también cuenta con la capacidad de seguir la trayectoria de un objeto a través de las diferentes cámaras. Para esto es necesario cámaras PTZ (que no estén muy separadas entre sí) y configuración adecuada (https://docs.axxonsoft.com/confluence/pages/viewpage.action?pageId=235441837)


## Alertas
Eventos generados por cámaras o detectores pueden ser configurados para que activen una alerta. Estas pueden ser visibilizadas en el **mapa** (https://docs.axxonsoft.com/confluence/display/PSIM100en/Working+with+the+Map), el cual puede ser una representación del cuarto en el que están ubicados los dispositivos. Así, cuando uno de estos se active, se puede saber fácilmente cuál cuarto y dispositivo fue.
De igula modo, se puede configurar un *Telegram Bot* para enviar mensajes de texto o fotos, cuando ocurra alguna alarma (https://docs.axxonsoft.com/confluence/display/PSIM100en/Sending+messages+via+Telegram+bot). 


## Controlando la cantidad de personas 
### Solución con "Detection Pack"
 La empresa ofrece una solución con el módulo *Detection Pack* (para el precio habría que pedir una cotización), el cual integra un contador de Personas (https://docs.axxonsoft.com/confluence/display/PSIM100en/Examples+of+scripts+with+Video+surveillance+monitor+and+Cameras -> ejemplo 2)

### Axxon One
 Es otro Software de la misma empresa que se enfoca exclusivamente en el ecosistema de las cámaras de seguridad, por lo tanto difiere de Axxon PSIM en que el segundo busca integrar el funcionamiento de las cámaras con otros instrumentos de seguridad, como puertas de acceso o detectores de humo. De esta manera, ya que Axxon one se centra únicamente en el control con ayuda de cámaras, este cuenta con inteligencia artificial integrada para el reconocimiento facial, heat map (mapa que muestra donde la gente se mueve mayormente), control de acceso, reconocimiento de carros, animales y otros. 

### Solución con VMDA Detector
Aunque es una solución útil y funcional, no es la más óptima si es que el reconocimiento facial es impresindible, pues la cámara debe estar ubicada relativamente lejos de la entrada para poder capturar al objeto en movimiento en su totalidad y esto puede dificultar el procedimiento de detección facial. La mejor solución probada sería la siguiente, con ayuda del reconocimiento facial.

Esta propuesta se apoya del lenguaje integrado de Axxon PSIM que permite crear programas y con ayuda del *VMDA Detector* se puede determinar la direccion de los movimientos de una persona. 
El siguiente código añade subtítulos en la esquina superior izquierda para tener un contador del número de personas, la fecha y nombre de la cámara.
Esto hace uso de únicamente una cámara con dos detectores de movimiento.
*CAM_VMDA_DETECTOR 1* -> detector de movimiento (salida) *CAM_VMDA_DETECTOR 2* -> detector de movimiento (entrada) 
*OnEvent("CAM","3","NEW_OBJECT")* -> evento que se activa cuando la cámara 3 detecta un nuevo objeto
*OnEvent("CAM","3","MD_STOP")* -> evento que se activa cuando la cámara 3 deja de estar en modo alerta

Como comandos para la cámara (OnEvent) se prefirió usar *NEW_OBJECT* a *MD_START* para que el contador se muestre actualizado siempre, pues puede haber el caso que la cámara esté alerta por varios minutos seguidos y por lo tanto el contador no va a actualizar.
Este código aumentaría el contador cuando un objeto cruce la linea virtual de entrada y disminuiría cuando la cruce de salida. Por lo tanto, el pasillo de entrada debería ser muy visible, pues el detector de movimiento funciona mayormente cuando el objeto en su totalidad cruza la línea virtual. 


```
OnInit(){
counter=0;
}

OnEvent("CAM_VMDA_DETECTOR","1","ALARM"){
    counter = str(counter-1);
   
}
OnEvent("CAM_VMDA_DETECTOR","2","ALARM"){
    counter = str(counter+1);
   
}
  
OnEvent("CAM","3","NEW_OBJECT"){
    DoReact("CAM","3","CLEAR_SUBTITLES","title_id<1>"); //borra todos los subtitulos de una imagen
    DoReact("CAM","3","ADD_SUBTITLES","command<Camera 3 Alarm " + time + "     Personas: " +counter+ "\r>,page<BEGIN>,title_id<1>");
    }

// se añadio esto para que el contador se muestre siempre actualizado, aun luego de que no haya movimiento
OnEvent("CAM","3","MD_STOP"){
    DoReact("CAM","3","CLEAR_SUBTITLES","title_id<1>"); //borra todos los subtitulos de una imagen
    
    DoReact("CAM","3","ADD_SUBTITLES","command<Camera 3 Alarm " + time + "     Personas: " +counter+ "\r>,page<BEGIN>,title_id<1>");   
}
```


### Solución con Reconocimiento facial
La solución que se va a proponer a continuación es con seguridad la más óptima y confiable, aunque hay que tener algunos factores a consideración.
Dos camaras apuntando en direcciones opuestas (entrada y salida) serían obligatorias, para así minimizar el tiempo y maximizar el reconocimiento. Además, sería muy importante considerar el ángulo de visión que tiene la cámara con respecto a las caras, para que estas puedan ser detectadas totalmente de frente con un tamaño mínimo de 24 píxeles de largo y ancho.

El siguiente programa mostraría el nombre de la cámara, la fecha y el número de personas (rostros detectados) en la esquina superior izquierda. Este contador, aumentaría cada vez que la cámara de entrada detecte a alguien y disminuiría cuando se registre una cara en la cámara de salida.

```
OnInit(){
counter=0;
}

// evento para cuando la camara ubicada en la salida detecte rostros
OnEvent("CAM_FACECAPTURE","1","FACE_DETECTED"){
    counter = str(counter-1);
   
}
// evento para cuando la camara ubicada en la entrada detecte rostros
OnEvent("CAM_FACECAPTURE","2","FACE_DETECTED"){
    counter = str(counter+1);
   
}
  
OnEvent("CAM_FACECAPTURE","1","FACE_DETECTED"){
    DoReact("CAM","1","CLEAR_SUBTITLES","title_id<1>"); //borra todos los subtitulos de una imagen
    DoReact("CAM","1","ADD_SUBTITLES","command<Camera 3 Alarm " + time + "     Personas: " +counter+ "\r>,page<BEGIN>,title_id<1>");
    }

// se añadio esto para que el contador se muestre siempre actualizado, aun luego de que no se hayan detectado caras
OnEvent("CAM","1","MD_STOP"){
    DoReact("CAM","1","CLEAR_SUBTITLES","title_id<1>"); //borra todos los subtitulos de una imagen
    
    DoReact("CAM","1","ADD_SUBTITLES","command<Camera 1 Alarm " + time + "     Personas: " +counter+ "\r>,page<BEGIN>,title_id<1>");   
}
```
**Importante**: 
- cambiar el número de objecto, con el correspondiente, por ejemplo: *OnEvent("CAM","1","MD_STOP")* se refiere a la cámara número 1
- El número de cada *CAM_FACECAPTURE*, debe corresponder al número de cada *Face Detection* object por cámara.

Es importante mencionar que las pruebas realizadas con esta técnica, fueron con la cámara ubicada en el techo apuntando directamente al área por donde pasarían las personas, con zoom para que la cara sea más grande y por lo tanto más fácil de identificar. Sin embargo, hay que tener en cuenta que con este posicionamiento existe la obligación de que la persona  **mire concientemente** a la cámara y pare máximo un segundo para que el dispositivo pueda leer correctamente el rostro todas las veces. Por lo tanto, en este escenario, si alguien entrase rápidamente viendo hacia otro lugar que no sea la cámara (viendo hacia arriba), el reconocimiento facial fallará seguramente.

Cabe recalcar, que existe la posibilidad que la cámara se la ubique a una altura de al rededor 1,80 metros (en una pared), para que así, la persona únicamente tenga que ver al frente para ser detectada (con zoom apuntando directamente a la cara para maximizar la resolución de la misma). Por el momento, este método resulta ser el más efectivo y eficiente, **quitando la necesidad de la persona de detenerse completamente** frente a la cámara. Únicamente, se deberá entrar relativamente lento y **mirando concientemente a la cámara**. Además, para el correcto funcionamiento de este procedimiento, la cara debe aparecer completamente por lo menos 1 segundo dentro del campo de visión de la cámara para ser reconocible. 


#### Factores a tener en cuenta
Un factor a tener en cuenta, es que estos subtítulos (contador, fecha y nombre de la cámara) únicamente son visibles cuando, la cámara detecta un objeto, se hace click sobre el monitor de la cámara o cuando se revisan las grabaciones (tres líneas en la esquina inferior de cada monitor). Por el momento, aún no se encuentra la manera de que los subtítulos aparezcan constantemente.

Con ayuda del *Operator Query Panel* (https://docs.axxonsoft.com/confluence/display/PSIM100en/The+Settings+panel+of+the+Operator+query+panel+object) se puede crear una ventada por cámara que muestre el número de personas detectadas (https://docs.axxonsoft.com/confluence/display/PSIM100en/Example+of+creating+a+dialog+bog+to+count+the+number+of+movements). Sin embargo, tras varios intentos, este método no parece mostrar ningún display como se indica.


## Requerimientos 
### Hardware
- mínimo 2 GB de RAM
- 10 GB para instalar Axxon PSIM Software + 20 GB para instalar MS SQL server
- espacio extra para guardar los archivos de vigilancia
- tarjeta de video:
	- discreta: NVIDIA GeForce GT520 1 GB RAM o mejor
	- On-board: Intel HD Graphics 530 o mejor
- Windows Server 2008 R2 SP1, Windows 7 SP1, Windows Storage Server 2008 R2 SP1, Windows Small Business Server 2011 SP1, Windows Home Server 2011 SP1, Windows Server 2012, Windows 8, Windows 8.1, Windows Server 2012 R2, Windows Storage Server 2012 R2, Windows 10, Windows Server 2016 or Windows Server 2019, Windows 10 IoT Enterprise, Windows 11
https://docs.axxonsoft.com/confluence/display/PSIM100en/Before+you+start+the+Axxon+PSIM+software

### Licencias 
- Servidor -> 448 (USD) x1
- Clientes -> 107 (USD) x2 (mínimo)
- Cámara -> 107 (USD) x...
- Axxon Face PSIM -> 107 (USD) (se piensa que esto también cuesta 107 dólares, aunque no se ha cotizado) x...

Se necesita *un servidor*, el cual puede soportar tantos dispositivos como sean necesarios. Se necesitan (mínimo) dos *Clientes*. Uno para el servidor (obligatorio), para poder administrar la configuracion de los dispositivos y otro(s) para poder monitorear los dispositivos (por ejemplo: lo que muestra una cámara o los registros de personas). Por lo tanto, la cantidad de esta licencia está sujeta a la necesidad del comprador, pues se puede tener varios permisos para segmentar los monitores (por ejemplo: una computadora que únicamente pueda ver cámaras de la garita y otra que pueda tener acceso a todos los dispositivos). La *licencia por cámara* permite añadir cámaras al sistema para su configuración. Para poder hacer el reconocimiento facial con las cámaras, se debe adquirir la *licencia de Axxon Face PSIM* (por cada cámara). Se intuye que esta adición cueste igualmente 107 dólares, al igual que el resto de licencias.

### VMDA Detector
Para controlar adecuadamente el acceso de personas en una entrada/salida, se ha pensado en utilizar dos cámaras, para que la detección del rostro pueda funcionar en ambas direcciones. Sin embargo, también se puede usar únicamente una cámara que identifique el movimiento en la dirección de entrada y salida, la cual puede a su vez reconocer rostros desde un ángulo. 

Para el correcto funcionamiento, se debe tener lo siguiente en cuenta:
- cámara con resolución de mínimo 640x480 y máximo 800x600
- mínimo 6 frames por segundo
- que no haya cambios abruptos de iluminación 
- los objectos en movimiento deben ser distinguibles entre sí 
- objetos en movimiento pueden ser minimamente oscurecidos por objetos estáticos de la escena 
- las reflexiones afectan al reconocimiento
- el ancho y largo mínimo de un objeto en movimiento debe ser superior al 1% del tamaño del frame 
- el ancho y largo máximo de un objeto en movimiento debe ser inferior al 75% del tamaño del frame
- el objeto en movimiento debe aparecer en mínimo 8 frames seguidas
- se puede hacer seguimiento de hasta máximo 25 objetos en movimiento simultáneamente 
- la distancia de movimiento entre dos frames consecutivas no debe ser mayor al tamaño del objeto
(https://docs.axxonsoft.com/confluence/display/PSIM100en/Requirements+to+video+parameters+while+working+with+detection+tools+and+Tracker)

### Reconocimiento facial 
- el tamaño de una cara debe de ser de al menos 24 píxeles de largo y ancho
- mínimo 8 frames para confirmar la detección facial
- la cara no se debe mover más de la mitad de su tamaño (en píxeles) en cualquier dirección en dos frames consecutivas 
- cámaras con resolución mayor a 2 megas


### Recomendaciones
Se recomienda que los diferentes detectores sean configurados cuando las cámaras sean instaladas en su lugar definitivo, pues dependiendo de cada posicionamiento, la iluminación al igual que la distancia de la cámara en relación con la persona varían significativamente.
La posición de la cámara es escencial para el funcionamiento correcto de los detectores, colocándola en un ángulo y altura favorable, los problemas de detección de movimiento y reconocimiento facial se minimizan. 
- Para la detectar únicamente rostros, la altura óptima y más efectiva es de al rededor 1.70 metros, aunque más alto también funciona 
- Para la detección de movimiento se recomienda que la cámara esté en el techo (3 metros de altura o más)


#### Reconocimiento facial
El reconocimiento facial es óptimo si se opta por usar dos cámaras en una entrada, para que cada una apunte hacia la dirección de entrada/salida y así maximizar la detección facial. Sin embargo, cabe añadir que se puede llegar a un reconocimiento eficiente, con una única cámara, si es que las personas (trabajadores) miraran con *conciencia* al dispositivo para ser identificados cuando entren y salgan. 

Para evitar que una cara sea detectada varias veces (lo cual podría causar confusión en los reportes de entrada) se puede configurar que una cara tenga un tiempo mínimo para que vuelva a poder ser identificada. 
- Dentro de *Face recognition server* object configurar el número de segundos que debe pasar para que una cara pueda volver a ser registrada en *Skip repeated recognitions, s:*

#### VMDA Detector
A la hora de usar la dirección de movimiento con VMDA Detector, se recomienda que la trayectoria de las personas se mantenga idealmente en una dirección, por ejemplo: en un pasillo donde sólo se pueda ir para adelante o atrás y no en una bifurcación.
La iluminación deberá ser constante, sin situaciones en la que cambie bruscamente, pues esto afecta al detector de movimiento, haciéndolo fallar. 


Es importante tener en cuenta que el registro de edad es **únicamente una estimación** y por lo tanto puede no ser muy acertada. Una misma persona detectada puede ser registrada con edades que oscilen entre cierto margen. La edad dada depende de la calidad de imagen obtenida de la cara. Esto mismo se debe mantener en consideración a la hora de sacar reportes en base a la edad. (no se resienta)

## Reporte de gente y horas de entrada/salida
Este sistema otorga la posibilidad de sacar un análisis de las personas detectadas por el reconocimiento facial, haciendo uso de diferentes filtro, por ejemplo: gente detectada con gorra, barba, de cierta edad, género, en un cierto horario, por cámara, entre otros. 

Este análisis se desbloquea cuando dentro de *Face Recongition Server* se crea el objeto *Visitor Counting channels* y es visible en la interfaz de *Face Recognition and search* bajo el nombre de *Analytics*. 

Este reporte es extremadamente útil si es que se quiere sacar un listado de la gente que entro a cierta hora, personas cuyo útlimo reconocimiento fue en algún horario en particular, si se detectó gente desconocida (no registrada en la base de datos), gente con barba, ... . Desde la pestaña de *Analytics* (en la parte superior derecha, el símbolo de impresora) se puede obtener este registro que se vería como la imagen a continuación. 
![[Screenshot from 2024-09-18 13-06-06.png]]

Como se puede ver en la parte derecha de la tabla, esas imágenes son todas las veces que se le vio a aquella persona. Con click derecho se puede ir a la grabación cuando cámara identifico al sujeto. Además de mostrar la hora en la que la persona fue vista por primera y última vez

Sin embargo hay que tener claro que, este registro se llena conforme las caras de las personas son identificadas. Por lo tanto, sería más complicado si se necesitase sacar un listado de todos los trabajadores que no asistieron un día en particular. Más no hay que perder la esperanza, pues este reporte puede ser exportado a Excel, html o PDF. Por lo tanto, se puede programar un lector que descarte los nombres registrados en el documento de un listado (base de datos), y los nombres que aún queden, serán los que no asistieron ese día. 
Otra posible solución a este problema sería mediante el uso del módulo *Web Report System PSIM*, se puede obtener reportes más detallados y específicos, por ejemplo: un reporte de tiempo y asistencia (https://docs.axxonsoft.com/confluence/display/rptPSIM100en/Creating+a+Time+and+Attendance+report). Además, estos reportes pueden ser exportados a PDF, CSV y Excel (https://docs.axxonsoft.com/confluence/display/rptPSIM100en/Exporting+of+reports).

Asímismo, el módulo *ACFA PSIM*, permite una estructuración de los departamentos y el personal con su respectivo nivel de acceso. A pesar de que esto ya se tenga con *Axxon PSIM* en la sección *Programming*, este otro módulo permite la creación de reportes sobre las horas trabajdas por cada persona (https://docs.axxonsoft.com/confluence/display/acfaPSIM100en/The+Worktime+tab).

### Reporte de Entrada
Para llevar la idea a una representación más concreta, el reporte de entrada podrá ser hecho de la siguiente forma. La primera es como se menciona en el ejemplo de arriba, con una imagen de la persona, y cada vez que se la vio.
La segunda manera es con ayuda del *Event Viewer*, el cual se deberá configurar de la siguiente forma: 
- Asignar un filtro para únicamente mostrar los eventos de detección de la cámara de entrada y salida (**Recognition channel** de ambas cámaras) (En *Event Viewer* -> *Filters* -> clickear dos veces bajo *Name* para crear un nuevo filtro -> clickear dos veces en la tabla inferior para añadir filtros)
- Dentro de *Event Viewer* en *Main* activar la opción de *Show Report*
- En la ventana de *Event Viewer* hacer click derecho y especificar la fecha y hora

Un ejemplo en un día regular de trabajo, se puede revisar todas las personas identificadas, a la hora de entrada (8:00 - 8:30) y sacar el reporte y para las personas atrasadas, digamos 8:30-8:40 (o más tarde). Nuevamente, existe la limitación con la inasistencia, pues esto no es una función que se haga automáticamente por Axxon PSIM.

#### Posibles problemas
Con este segundo método de reporte existe la siguiente situación que deberá ser contemplada a la hora de decidir cuál de los dos usar. 
Se plantea el siguiente escenario: un empleado llega a las 8:20, y la cámara de la entrada lo registra. A las 8:30 se hace el reporte de asistencia puntual. Por diferentes razones, el empleado que llego temprano debe salir y regresa a las 8:40, siendo detectado otra vez por la cámara de ingreso. A esa misma hora llega otro empleado (atrasado) y es detectado por primera vez por la cámara de ingreso. Por lo tanto, el reporte que se genere por el *Event Viewer* de las 8:30-8:40 (para los atrasos) constará del primer empleado, que sí llegó a tiempo (8:20) y del segundo que no. 
Para poder hacer la distinción de ambos casos, se deberá usar los diferentes filtros dentro de la pestaña de *Analytics*, la cual cuenta con lugar para configurar la fecha, hora y más importante el **número de accesos**. Por lo tanto, para poder determinar con exactitud quién de los dos sí llegó atrasado, se deberá configurar para que el *número de acceso mínimo y máximo sea igual a 1*. Así, en este reporte aparecerá únicamente el segundo empleado, que sí llegó tarde.
Sin embargo, esta configuración también consta con un factor problemático, que surge si, por alguna razón, la persona que llegó tarde, es identificada y registrada dos veces. Esto resultaría en que la cantidad mostrada de *accesos* en el registro sea de dos. Por lo tanto, la mayor prioridad será **considerar la hora del primer registro** realizado ese día

Por el otro lado, si se desea usar el reporte de *Event Viewer* se deberá considerar que nombres pueden aparecer en ambas listas, por lo tanto, el resumen de asistencia más temprano tendrá prioridad sobre los que sean realizados más tarde.

### Reporte de gente desconocida
Es importante mencionar que para que el reporte también conste de personas que no hayan sido previamente registradas en la base de datos, se deberá especificar otro filtro, que bajo *Event Viewer*, tenga también la opción *Not recognized*  activada. Sin embargo, esta manera resulta tanto problemática, pues la cámara intenta constantemente de reconocer una cara, por lo tanto, una misma persona puede lanzar *varias alertas* de irreconocimiento y luego ser identificada (o no), lo que podría causar confusión en el reporte.
La mejor manera de sacar el reporte de gente desconocida, sería mediante la pestaña *Analytics*, configurando el filtro *Show faces* con *Unrecognized* a una cierta fecha y hora.

## Búsqueda de rostros
Dentro de la interfaz *Face detection and search* en la pestaña *Search* se puede buscar a personas específicamente, subiendo archivos de fotos o videos. Lo mismo, se puede lograr si es que en la pestaña de *Face DB* o *Monitor* se hace click derecho sobre la persona. De este modo, se puede ver todas las veces que se detectó a cierta persona y revisar las grabaciónes donde aparece.


## Conclusión 
Axxon PSIM es un software muy poderoso que integra diferentes equipos para mantener un entorno controlado y por lo tanto seguro, mostrando una gran capacidad de ampliación con dferentes módulos, que permite un control eficiente de acceso en parte por la capacidad de reconocimiento facial y los diversos reportes. En conclusión, la mejor manera de monitorear el flujo de personas en una entrada y poder reconocerlas es con dos cámaras, ubicadas en direcciones opuestas, a una altura y ángulo que apunte directamente a la cara. Se necesitaría de al menos 1090 dólares (contando únicamente las licencias impresindibles para su funcionamiento), lo que significa: usar mínimamente dos clientes (214 dólares) y por acceso gastar 428 dólares en las licencias para las cámaras.


