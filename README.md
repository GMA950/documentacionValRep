# documentacionValRep
documentación para proyecto de taller de ing de software

### Introduccion
Repuestos Conejeros es una tienda familiar de repuestos automotrices, la  cual requiere de un software para agilizar el control de inventario. Actualmente este se realiza dos veces a la semana después del cierre del local, se realiza de manera manual a lápiz y papel  anotando cuánto stock de cada producto queda y ver si es necesario realizar un pedido a los proveedores. Por otro lado, al momento que llega nuevo stock, éste se almacena y se actualiza el stock de los productos en el cuaderno de inventario,  además al momento de realizar una venta de un producto se va descontado del stock actual, por lo que esta tarea puede tomar mucho tiempo, además de ser poco eficiente, llevando últimamente a un problema de pérdida de control de inventario con pedidos que no se hacen a tiempo, ventas no descontadas o pedidos repetidos e innecesarios.

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



https://user-images.githubusercontent.com/50679273/130844321-c001e8ad-1cc9-4439-8f46-010e3a64b1a6.mp4

# Documento de Requisitos de Usuario
# (URD)




## 1.1 Organización de la empresa

La micro- empresa se compone de la siguiente forma: 
Gerencia y Administración: Toma las decisiones principales que afectan al funcionamiento de la empresa, además de tratar con los proveedores y realizar los pedidos (Cotización y comparación) y la contabilidad.
Bodega:  Es donde se conserva el inventario de los productos a vender.
Venta: 	Aquí el vendedor atiende a los clientes y se concretan las ventas.

##2. Gestión de Inventario

## 2.1. Situación Actual 

Actualmente el control del inventario se realiza a lápiz y papel, este se realiza dos veces a la semana y el encargado de realizarlo es el dueño del local, aunque usualmente suele ayudarlo su hijo mayor. Para esta tarea se recorren todos los pasillos y se va registrando el stock de cada producto manualmente. Esto a parte de ser ineficiente e inseguro, toma mucho tiempo, además de ser susceptible a numerosos errores ya sea por el mal recuento de un producto o simplemente en el ingreso de datos en el cuaderno de stock. 
Por otro lado, en el momento que se necesita encargar nuevo stock a un proveedor, se necesita revisar en este cuaderno el stock producto a producto, lo cual también puede llevar a equivocaciones y puede tomar bastante tiempo en realizar dicha tarea.

## 2.2. Requisito

Se solicita el desarrollo de una página web la cual contenga el inventario del local, el cual será una lista de los distintos productos disponibles en el local y que contará para cada uno de estos con un código, nombre, cantidad de stock disponible, precio, etc. Además mediante un lector de código de barras se podrá hacer búsquedas de productos para ver información del mismo, como el stock, precio, etc. También tendrá una sección para agregar o eliminar una cierta cantidad de productos, es decir actualizar el stock, ya sea para cuando llega nuevo stock (la idea es que cuando llegue nuevo stock, se lea el codigo de barra y se ponga la cantidad de productos entrantes, el cual se sumará al stock actual en bodega) o cuando se realiza una venta. Para finalizar se plantea agregar una funcionalidad de alerta de bajo stock, el cual enviará una alerta por wtsp, correo electrónico o simplemente una ventana advirtiendo cuando el stock de un producto cae por debajo de un límite determinado por el usuario.

## 3. Gestión de pedidos

## 3.1. Situación actual

Actualmente se realizan principalmente dos clases de pedidos a empresas proveedoras. En primer lugar tenemos los pedidos de reabastecimiento que se realizan constantemente cada vez que el personal de la tienda percibe que hay un nivel bajo en el stock de ciertos artículos en el inventario o en el peor de los casos, cuando un artículo se ha agotado. El segundo tipo de pedido se realiza de forma más personalizada  y consiste en cuando un cliente requiere de un artículo que no forma parte de la oferta de la tienda, por lo que se da la opción de encargar este artículo a una empresa proveedora. En general estos procesos de pedidos se realizan manualmente sin ningún software de apoyo, por lo que se torna tedioso y es  propenso a errores.

## 3.2. Requisitos

Como una forma de facilitar este proceso se requiere de un sistema de alerta que sea capaz de notificar a los encargados cuando cierto artículo alcanza un nivel bajo en stock. De esta forma se pueden realizar pedidos con mayor antelación y así evitar que eventualmente un artículo se quede sin stock lo que puede ocasionar pérdidas.


## 4. Recepción de Mercancías
## 4.1 Situación actual
	Actualmente la labor de abastecimiento es realizada solo por un trabajador, quien es la persona que tiene los contactos con los proveedores de repuestos, si bien esta labor se desempeña pocas veces al mes, actualmente es bastante tediosa y dificultosa su realización, debido a que por el escaso control del inventario, se han quedado sin stock de productos en momentos inesperados, lo que lleva a pérdidas indebidas de posibles ventas que afectan de mala manera al negocio.

## 4.2 Requisitos
	El sistema debe ser capaz de entregar en tiempo real el stock de productos del negocio para que se pueda realizar una mejor planificación del proceso de abastecimiento de repuestos. Por otro lado al llegar un nuevo cargamento de repuestos, estos deberán ser registrados mediante el código de barras y agregando la cantidad de stock entrante de cada producto del cargamento, lo que almacenará la información del producto en la bodega y actualizará el stock del negocio en tiempo real.

## 5. Salida de inventario

##5.1 Situación actual
	Los productos que salen del inventario son descontados del stock manualmente después de realizada una venta, lo que conlleva a que en ocasiones los trabajadores se equivoquen o olviden de registrarlo. Esto posteriormente resulta en problemas de stock y pérdida de posibles ventas que no son buenas para el negocio.

## 5.2 Requisitos
	El sistema debe contar con un carrito de compras en el cual se agregan productos mediante la lectura del código de barra dando información del precio de cada producto, precio total por unidades compradas de cada producto y el precio final de la venta, al finalizar la venta el sistema debe ser capaz de actualizar el stock de cada producto en tiempo real.
Cuando algún producto llegue al límite crítico de stock establecido, se agregará en la sección de notificaciones o mensajes. Esto será válido para todos los productos y estará estrechamente vinculado con el código de barras de cada uno de los productos.
En caso de una pérdida de conexión, la actualización del stock se guardará para ser subida cuando se reanude el servicio.


