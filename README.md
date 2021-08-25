# documentacionValRep
documentación para proyecto de taller de ing de software

### Introduccion
Repuestos Conejeros es una tienda familiar de repuestos automotriz el cual requiere de un software para agilizar el control de inventario. Actualmente este se realiza todos los días después del cierre del local, se realiza de manera manual a lápiz y papel  anotando cuánto stock de cada producto queda para el día siguiente y si es necesario realizar un pedido a los proveedores o no. Al momento que llega nuevo stock se reciben y actualiza el stock de cada producto en su cuaderno de stock,  por lo que esta tarea puede tomar mucho tiempo, además de ser poco eficiente.

Para solucionar este problema se plantea desarrollar una página web la cual contenga el inventario del local, el cual será una lista de los distintos productos disponibles en el local y que contará para cada uno de estos con un código, nombre, cantidad de stock disponible, precio, etc. Además mediante un lector de código de barras se podrá hacer búsquedas de productos para ver información del mismo, como el stock, precio, etc. También tendrá una sección para agregar o eliminar una cierta cantidad de productos, es decir actualizar el stock, ya sea para cuando llega nuevo stock o cuando se realiza una venta. Para finalizar se plantea agregar una funcionalidad de alerta de bajo stock, el cual enviará una alerta por wtsp, correo electrónico o simplemente una venta advirtiendo cuando el stock de un producto cae por debajo de un límite puesto por el usuario.

### TAREAS

Las tareas que se realizan en el negocio familiar de autopartes son las siguientes:

- Venta: Esta sin duda es la tarea más común del negocio y en la que contribuyen todos los trabajadores del local, actualmente al llegar un cliente y preguntar por un repuesto el vendedor le indica el precio y va a bodega a buscarlo, al encontrarlo vuelve al mesón de venta donde realiza una boleta a mano para el cliente, recibiendo el dinero, guardándolo en caja durante el proceso.

- Inventariado: Esta es sin duda la tarea que le toma más tiempo a todos los trabajadores y actualmente también se ha vuelto en una de las más dificultosas debido al procedimiento que hacen actualmente, el cual consiste en ir registrando todo con lápiz y papel, lo cual se ha vuelto bastante tedioso de realizar, debido a los volúmenes de productos que están manejando últimamente, aparte de que dificulta el control sobre los niveles de stock en los productos, los cuales tienen que ser precisos para realizar los pedidos en el momento justo, no antes ni después.

- Contabilidad: Actualmente la contabilidad la realizan solo 2 personas de los 5 trabajadores del local, quienes son los cabecillas de la familia, dicha contabilidad guarda estrecha relación con el inventario, por lo que igualmente últimamente se ha visto afectada por la ineficiencia en el control de inventario.

- Abastecimiento: Generalmente esta tarea solo la realiza un solo trabajador, quien es la persona que tiene los contactos con los proveedores de los repuestos automotrices, si bien es una tarea que se realiza pocas veces al mes, actualmente igualmente se ha vuelto dificultosa, donde debido al escaso control de inventario han quedado sin stock de algunos productos, lo que los ha llevado a la pérdida de posibles ventas afectando al negocio negativamente.

### Diseño preeliminar de interaccion

- WIREFLOW
![image18](https://user-images.githubusercontent.com/50679273/130838097-e5ef3b1f-aeed-428c-9f42-ed6dd4a22bd5.jpg)

- WIREFLOW ANOTADO
![image14](https://user-images.githubusercontent.com/50679273/130839895-7e9736af-d5dc-4913-8ee8-fd90df8fac5b.png)
![image8](https://user-images.githubusercontent.com/50679273/130840015-78094205-26c1-4cb9-9f70-ce418dbed7c3.png)
![image12](https://user-images.githubusercontent.com/50679273/130841649-96177b2b-f8de-4638-b92e-1503993780bc.png)
![image17](https://user-images.githubusercontent.com/50679273/130841701-b05c73ec-f811-4580-b2f3-4c32250e389e.png)
![image15](https://user-images.githubusercontent.com/50679273/130841912-7e572944-f587-4b12-a181-a612066b7903.png)
![image1](https://user-images.githubusercontent.com/50679273/130842082-d77d5da8-a174-4702-b3ed-056e9210d4e0.png)

- PROPUESTA GRAFICA
  - INICIO DE SESION:
   ![image11](https://user-images.githubusercontent.com/50679273/130842319-96e79c1f-0537-4f22-b98c-3f69feb86cd4.jpg)
  - INICIO:
  ![image10](https://user-images.githubusercontent.com/50679273/130842339-de165cbc-3628-45c7-8419-f9f60bd4505f.jpg)
  - SECCION DE INVENTARIO:
  ![image13](https://user-images.githubusercontent.com/50679273/130842351-43aeb279-9bda-45e0-8c77-4faab635902d.jpg)
  
  luego de esto se realizo una **Evaluacion por inspeccion** para lo cual se aplico una evaluación heurística, la cual se define como un principio de usabilidad reconocido, específicamente se evaluo si es que nuestra interfaz suele cumplir con las reglas genéricas que responden al set propuestas por el método de las heurísticas de Nielsen. En nuestro rol como “expertos” nos corresponde verificar que nuestro sistema cumpla con dichos criterios.
Estos criterios son muy generales, y están acotados principalmente a 10:

- Feedback
- Extender Experiencia de Usuario
- Control y Libertad
- Consistencia y Estándar
- Prevención de Errores
- Reconocimiento sobre Memoria
- Flexibilidad y Eficiencia
- Diseño Minimalista
- Mensajes de Error Útiles
- Ayuda y Documentación

Después de ir revisando la interfaz analizando los 10 puntos mencionados anteriormente, hemos obtenido una variedad de errores en nuestra interfaz los cuales se fueron corrigiendo. Luego Con el fin de obtener una interacción lo más real posible entre el usuario y el sistema se desarrolló un prototipo del sitio web en Adobe XD, enfocándose en las interfaces relacionadas con las principales tareas a testear.

- Interfaz de inicio de sesión:
- Interfaz del inicio o página principal del sistema:
- Interfaz de la sección Inventario:
