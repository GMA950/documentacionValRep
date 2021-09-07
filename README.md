# Documentacion General de ValRep

Documentación para proyecto de taller de ingeniería de software (2021)

# Documento de Requisitos de Usuario (URD)

## 1. Introduccion

ValRep es una tienda familiar de repuestos automotrices, la  cual requiere de un software para agilizar el control de inventario. Actualmente este se realiza dos veces a la semana después del cierre del local, se realiza de manera manual a lápiz y papel  anotando cuánto stock de cada producto queda y ver si es necesario realizar un pedido a los proveedores. Por otro lado, al momento que llega nuevo stock, éste se almacena y se actualiza el stock de los productos en el cuaderno de inventario,  además al momento de realizar una venta de un producto se va descontado del stock actual, por lo que esta tarea puede tomar mucho tiempo, además de ser poco eficiente, llevando últimamente a un problema de pérdida de control de inventario con pedidos que no se hacen a tiempo, ventas no descontadas o pedidos repetidos e innecesarios.

### 1.1 Organización de la empresa

La micro- empresa se compone de la siguiente forma: 
Gerencia y Administración: Toma las decisiones principales que afectan al funcionamiento de la empresa, además de tratar con los proveedores y realizar los pedidos (Cotización y comparación) y la contabilidad.
Bodega:  Es donde se conserva el inventario de los productos a vender.
Venta: 	Aquí el vendedor atiende a los clientes y se concretan las ventas.

## 2. Gestión de Inventario

### 2.1. Situación Actual 

Actualmente el control del inventario se realiza a lápiz y papel, este se realiza dos veces a la semana y el encargado de realizarlo es el dueño del local, aunque usualmente suele ayudarlo su hijo mayor. Para esta tarea se recorren todos los pasillos y se va registrando el stock de cada producto manualmente. Esto a parte de ser ineficiente e inseguro, toma mucho tiempo, además de ser susceptible a numerosos errores ya sea por el mal recuento de un producto o simplemente en el ingreso de datos en el cuaderno de stock. 
Por otro lado, en el momento que se necesita encargar nuevo stock a un proveedor, se necesita revisar en este cuaderno el stock producto a producto, lo cual también puede llevar a equivocaciones y puede tomar bastante tiempo en realizar dicha tarea.

### 2.2. Requisitos

Se solicita el desarrollo de una página web la cual contenga el inventario del local, el cual será una lista de los distintos productos disponibles en el local y que contará para cada uno de estos con un código, nombre, cantidad de stock disponible, precio, etc. Además mediante un lector de código de barras se podrá hacer búsquedas de productos para ver información del mismo, como el stock, precio, etc. También tendrá una sección para agregar o eliminar una cierta cantidad de productos, es decir actualizar el stock, ya sea para cuando llega nuevo stock (la idea es que cuando llegue nuevo stock, se lea el codigo de barra y se ponga la cantidad de productos entrantes, el cual se sumará al stock actual en bodega) o cuando se realiza una venta. Para finalizar se plantea agregar una funcionalidad de alerta de bajo stock, el cual enviará una alerta por wtsp, correo electrónico o simplemente una ventana advirtiendo cuando el stock de un producto cae por debajo de un límite determinado por el usuario.

## 3. Gestión de pedidos

### 3.1. Situación actual

Actualmente se realizan principalmente dos clases de pedidos a empresas proveedoras. En primer lugar tenemos los pedidos de reabastecimiento que se realizan constantemente cada vez que el personal de la tienda percibe que hay un nivel bajo en el stock de ciertos artículos en el inventario o en el peor de los casos, cuando un artículo se ha agotado. El segundo tipo de pedido se realiza de forma más personalizada  y consiste en cuando un cliente requiere de un artículo que no forma parte de la oferta de la tienda, por lo que se da la opción de encargar este artículo a una empresa proveedora. En general estos procesos de pedidos se realizan manualmente sin ningún software de apoyo, por lo que se torna tedioso y es  propenso a errores.

### 3.2. Requisitos

Como una forma de facilitar este proceso se requiere de un sistema de alerta que sea capaz de notificar a los encargados cuando cierto artículo alcanza un nivel bajo en stock. De esta forma se pueden realizar pedidos con mayor antelación y así evitar que eventualmente un artículo se quede sin stock lo que puede ocasionar pérdidas.


## 4. Recepción de Mercancías
### 4.1 Situación actual

Actualmente la labor de abastecimiento es realizada solo por un trabajador, quien es la persona que tiene los contactos con los proveedores de repuestos, si bien esta labor se desempeña pocas veces al mes, actualmente es bastante tediosa y dificultosa su realización, debido a que por el escaso control del inventario, se han quedado sin stock de productos en momentos inesperados, lo que lleva a pérdidas indebidas de posibles ventas que afectan de mala manera al negocio.

### 4.2 Requisitos

El sistema debe ser capaz de entregar en tiempo real el stock de productos del negocio para que se pueda realizar una mejor planificación del proceso de abastecimiento de repuestos. Por otro lado al llegar un nuevo cargamento de repuestos, estos deberán ser registrados mediante el código de barras y agregando la cantidad de stock entrante de cada producto del cargamento, lo que almacenará la información del producto en la bodega y actualizará el stock del negocio en tiempo real.

## 5. Salida de inventario

### 5.1 Situación actual

Los productos que salen del inventario son descontados del stock manualmente después de realizada una venta, lo que conlleva a que en ocasiones los trabajadores se equivoquen o olviden de registrarlo. Esto posteriormente resulta en problemas de stock y pérdida de posibles ventas que no son buenas para el negocio.

### 5.2 Requisitos

El sistema debe contar con un carrito de compras en el cual se agregan productos mediante la lectura del código de barra dando información del precio de cada producto, precio total por unidades compradas de cada producto y el precio final de la venta, al finalizar la venta el sistema debe ser capaz de actualizar el stock de cada producto en tiempo real.
Cuando algún producto llegue al límite crítico de stock establecido, se agregará en la sección de notificaciones o mensajes. Esto será válido para todos los productos y estará estrechamente vinculado con el código de barras de cada uno de los productos.
En caso de una pérdida de conexión, la actualización del stock se guardará para ser subida cuando se reanude el servicio.

# Documento de Especificación de Requisitos Software (ERS)

## 1. INTRODUCCIÓN

Este documento detalla y estructura los requisitos de software propuestos para la empresa “ValRep”

### 1.1 Propósito

Durante este trabajo si bien han habido pocas reuniones Desarrollador-Cliente, estas han sido suficientes como para determinar tanto las funcionalidades necesarias, como las limitaciones actuales. 
Cabe destacar que este documento es preliminar ya que aún es posible que el cliente solicite algunos cambios, aparte de que pueden ser varios más cambios cuando el cliente se encuentre usando el primer prototipo. 

### 1.2 Ámbito del Sistema

La finalidad del desarrollo de este Software es cubrir las necesidades de una microempresa familiar con el fin de agilizar y hacer más eficiente la tarea de control de inventario. La cual actualmente se realiza manualmente por 1 o 2 trabajadores de la tienda, anotando el stock de cada producto al inventariar o por venta. por lo que al no poseer un software acorde a las necesidades, dicha tarea se torna agotadora, ineficiente y poco fiable.

### 1.3 Definiciones, Acrónimos y Abreviaturas
### 1.3.1 Definiciones

Proveedores: Distribuidores de los repuestos automotrices, como también de productos relacionados, con los cuales se efectúa la compra de estos. 
Encargado de Inventario: Persona a cargo de la bodega de la tienda. Se encarga de ubicar en sus lugares correspondientes en la bodega los repuestos y los productos. También es el encargado de inventariar.
Vendedor: Persona que se encarga de atender a los clientes en la tienda y concretar ventas.
Administrador: Persona que se encarga de realizar pedidos y contabilidad, así como también liderar la tienda.

### 1.3.2 Acrónimos
	
ISP: Internet Service Provider
SAI: Software de Administración de Inventario
PyR: Productos y Repuestos

### 1.4 Visión General 

A continuación en este documento describiremos el sistema en general, con las principales funciones que debe realizar y además se detallan los requerimientos que debe satisfacer el sistema según lo exigido por los clientes en nuestro trabajo.

## 2. DESCRIPCIÓN GENERAL

### 2.1 Perspectiva del Producto

Se plantea  el desarrollo de una página web la cual administre y gestione el inventario de la tienda familiar “Valrep”. Optimizando así su reabastecimiento y finanzas, como también, la disposición oportuna de los PyR requeridos para que la tienda funcione. 

### 2.2	Funciones del Software

Se desea que el software sea capaz de entregar soporte y optimizar las siguientes tareas que se realizan dentro de la tienda Valrep.

Gestión de Inventarios con sistema de alerta para niveles críticos de stock.
Gestión del ingreso y retiro de ítems por pistolas láser. 
Exportación de stock del inventario a planillas excel.
Acceso al inventario vía remota
Sistema de Usuarios con Clave

### 2.2.1	Gestión de inventarios

Toda emprendimiento en algún momento va a requerir para sus funciones información fiable y en tiempo real, es por eso que la gestión de inventarios debe automatizarse para agilizar el proceso actual, cuyo desempeño cae en la congestión normal que conlleva ser manejada a mano y sin organización (Esto implica responder las consultas de stock, inventariar, realizar préstamos, mantener seguimiento, adquisiciones, compras y facturación). 
Es por esto que se implementará un sistema dinámico capaz de permitir la administración del software en modalidad multiusuario, con la facultad de ser consultada simultáneamente por los trabajadores en línea desde cualquier dispositivo móvil.

### 2.2.2	Gestión de ingreso

Tanto el ingreso como el retiro de un producto debe ser registrado en tiempo real, ya sea por la llegada de mercadería o la salida de un producto por haber realizado una venta.

El ingreso de productos deberá contener la información relevante del elemento, como el Nombre del producto, Categoría, Precio, Código, etc. Así como actualizar cualquier parámetro del producto en caso de ser necesario.
El ingreso o retiro de un producto debe ser automatizado mediante el uso de pistolas láser.
El ingreso o retiro de un producto deberá actualizar el stock actual que haya en ese momento en la empresa.

### 2.2.3	Exportación de stock

Se solicita la funcionalidad de exportación del inventario en una plantilla excel, para esto:
Se implementará un botón, dentro de la sección “inventario”, el cual creará y exportará el inventario en tiempo real.
El documento excel será enviado al correo electrónico registrado automáticamente.

### 2.3	Características de los Usuarios

Los usuarios son gente de un grupo etario joven, relacionada ya con el uso de las tecnologías, por lo que para este software solo hay que tener en consideración que debe poseer una interfaz de usuario intuitiva, y sencilla de usar. También hay que tener presente el uso de una paleta de colores que facilite el uso para usuarios daltónicos.

### 2.4	Restricciones

Existen varias exigencias impuestas por los administradores de la tienda, como que el software sea compatible con el uso de pistolas láser. Además, se hizo énfasis en que debe existir una alerta de stock mínimo para los usuarios, vía correo electrónico, aplicación o softwares de mensajería. Finalmente el software tiene que estar disponible vía web, para que sea accesible desde cualquier lugar, por lo tanto el sistema debe usar la arquitectura cliente/servidor.

### 2.5	Suposiciones y Dependencias

Se asume que la información entregada respecto a la clasificación y estructuración actual del inventario y su variedad de repuestos/productos es verídica y actualizada, cosa de facilitar las labores de programación y generación de una base de datos para el software.
Se asume que los requisitos descritos en este informe serán considerados estables una vez revisados por los clientes de la tienda Repuestos Conejeros
 Cualquier petición posterior de cambios debe ser aprobada por todas las partes.

### 2.6	Requisitos Futuros

Dependiendo de la recepción y uso del software, se espera para futuro implementar en el sistema funcionalidades relacionadas con la generación de órdenes de compra, boletas y facturas.


## 3. REQUISITOS ESPECÍFICOS

En la siguiente sección se presentan los requisitos funcionales del sistema, estos requisitos son de carácter esencial, quiere decir que son requisitos que el sistema debe llevar a cabo si o si, estos requisitos deben ser fácilmente reconocibles ante algún caso de uso.

### 3.1. REQUISITOS FUNCIONALES

### 3.1.1. Funcionalidades de sistema
- ReqSis01: El sistema deberá tener un inicio de sesión, el cual será un CRUD que permitirá gestionar las credenciales que permitan gestionar el software
- ReqSis02: El sistema implementará un CRUD para el manejo de inventario
- ReqSis03: El sistema deberá permitir al usuario fijar y editar límites de stock, además deberá emitir una alerta, ya sea por whatsapp, correo electrónico o simplemente una ventana emergente avisando que cierto producto llegó al límite de stock.
- ReqSis04: El sistema deberá ser capaz de exportar el inventario de la empresa a un archivo excel siempre y cuando el usuario lo desee. 


### 3.1.2. Entrada de elementos a bodega

- ReqSis05:  El sistema deberá ser capaz de leer el código de barra de los productos mediante una pistola láser.
- ReqSis06: Cuando se lea un nuevo producto mediante la lectura de su código de barra el sistema desplegará una ventana en la que se solicitará información sobre el nuevo producto (Nombre, código(asignado automáticamente mediante la lectura del código de barra), precio, etc).
ReqSis07: El sistema deberá ser capaz de actualizar el stock dinamicamente ya sea cuando entre nuevo stock de un producto o salga.

### 3.1.3. Salida de elementos de bodega

- ReqSis07: El sistema deberá tener una sección “carrito de compra” donde una vez el usuario ingrese, mediante la pistola láser se ingresaran los productos salientes, se mostrara información sobre los productos y se implementará un selector para indicar la cantidad que sale de un mismo producto



### 3.1.4. Visualización de inventario

- ReqSis08: ​ El sistema deberá contar con un modulo de vista informativa, el cual entregará información detallada del inventario  en tiempo real.
- ReqSis09: El sistema deberá contar con un modulo de vista informativa por producto, en el cual, mediante la lectura del código de barra se entregará información sobre el producto, como el stock disponible, precio, proveedor, detalles, etc.

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




