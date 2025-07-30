-> Automatización de servicios 
-> Integración de cámaras (térmicas, infrarrojas, ...), detectores de fuego/agua ...
-> Control *manual/automático* de cámaras PTZ


## Control de Acceso
-> Registro en base de datos por Persona
- asignación de **nombre y departamento** 
- **niveles de acceso** (diferencia ente jefe o empleado) -> **zonas permitidas de acceso** *en un horario* -> *apertura de puertas*
- Registro de todas las apariciones de una persona (*registro de entrada/salida*)
- generación de eventos por persona (**alertas** SMS, correo, **alarmas**, ...)
	- configuración de [Telegram Bot](https://docs.axxonsoft.com/confluence/display/PSIM100en/Notification+services)
- lectura de **temperatura corporal** 
- reconocimiento de **máscara** (mascarilla)
- lectura de **emociones**

(Personas no registradas son igualmente guadadas en la base de datos)![[Screenshot from 2024-09-10 14-59-57.png]]

---

## [Mapa](https://docs.axxonsoft.com/confluence/display/PSIM100en/Setup+procedure+for+the+interactive+map)
- [representación gráfica](https://docs.axxonsoft.com/confluence/display/PSIM100en/Creating+the+layers+of+the+interactive+map) del cuarto donde está la cámara 
- unir mapas para la representación total de un edificio ![[Screenshot from 2024-09-10 15-09-21.png]]
- [búsqueda  recursiva de alarmas](https://docs.axxonsoft.com/confluence/display/PSIM100en/Configuring+the+mechanism+for+searching+and+processing+alarm+signals+on+multilayer+maps) en el mapa
- [cambiar entre capas del mapa](https://docs.axxonsoft.com/confluence/display/PSIM100en/Switching+between+layers+of+the+Map)

### Seguimiento de Personas 
- con cámaras PTZ 
- cambio automático a la cámara que detecta la persona 
- Cambio automático a una capa del mapa (y a la cámara) si una alerta salta 
- [Tag&Track](https://docs.axxonsoft.com/confluence/pages/viewpage.action?pageId=235438819)

### Cross line detection tool 
#### [Mediante una Línea](https://docs.axxonsoft.com/confluence/display/PSIM100en/Search+by+line+crossing)
- detecta el movimiento cuando una persona/objeto cruza la linea
- ejemplo: Configurar una alarma si una linea es cruzada en una dirección 
	- <span style="color:#ffff00">script con ayuda de esta línea para determinar la cantidad de gente que la cruzó para saber cuanta gente hay en el cuarto en un punto</span>
 
![[Screenshot from 2024-09-10 15-10-54.png]]

#### Mediante áreas
- detectar [movimientos de un área a otra](https://docs.axxonsoft.com/confluence/display/PSIM100en/Moving+from+one+area+to+another+detection+tool+configuration) (solo entre dos áreas)
- **solo con un área** -> evento si un objeto entra/sale/para en el área
![[Screenshot from 2024-09-10 15-16-03.png]]



## Visitor Counter ? 
- mencionado varias veces en las páginas [principales de Axxon ](https://www.axxonsoft.com/glossary#visitor-counter)
- pero nada específico en los manuales 
![[Screenshot from 2024-09-10 16-14-59.png]]


#### [En Axxon One](https://www.axxonsoft.com/products/video-management-software/key-features/axxon-one-retail-security-pack#visitor-counter)
![[Screenshot from 2024-09-10 16-19-41.png]]

---

## Scripts 
*Con JavaScript*
-> Personalización de eventos específicos 
	- ejemplo: que una cámara muestra en su display con texto la cantidad de gente que se ve (útil para administrar colas de gente )


---

## [Object Tracking ](https://docs.axxonsoft.com/confluence/display/PSIM100en/Enabling+object+tracking+on+interactive+map)
- con cámaras PTZ
- [detección objetos abandonados ](https://docs.axxonsoft.com/confluence/display/PSIM100en/Creating+and+configuring+the+Tracker+object)



---

# Axxon One
**Diseñado únicamente para el <span style="color:#ffffff">monitoreo de cámaras,</span> mientras que <span style="color:#ffffff">Axxon PSIM </span>se enfoca en la i<span style="color:#ffffff">ntegración de varios elementos de seguridad</span> (cámaras, detectores de humo, acceso de puertas ...)** -> PSIM es para escenarios más complejos

Integración de la inteligencia artirficial
- reconocimiento de posturas (un cajero con los brazos levantados...)
- contador de objetos/personas/animales
- revisa tiempo de parqueo
- revisa que el personal lleve el equipo necesario (chaleco...)
- reconocimiento facial
- reconocimiento de placas
- enmascaramiento de caras (protección de información ) 