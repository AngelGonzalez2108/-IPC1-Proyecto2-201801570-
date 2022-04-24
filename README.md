# -IPC1-Proyecto2-201801570-
Angel Carlos Daniel González López
201801570
IPC1 Sección A
En la direccion: http://127.0.0.1:5000

En la ruta: /user
Se encuentran los metodos: POST, PUT, DELETE, GET.

Para el metodo POST: Se encuentra la creación de un usuario, se deben ingresar los datos requeridos que contiene un usuario, si todos los datos son correctos, entonces muestra un codigo 201 con mensaje CREATED, si algo sale mas entonces muestra un mensaje 400 ya que el servidor no hará nada al respecto.

Para el metodo PUT: La funcion del metodo es actualizar o editar los datos que el usuario desee, ya sea cambiar su nickname, contraseña, edad, carrera, etc. Para esto el usuario deberá ingresar todos os nuevos datos que quiere que aparezca en su usuario, si todos los datos son correctos entonces el status es 200 ya que todo esta bien si el usuario no existiera, entonces el status es 404 ya que no se encuentra el usuario.

Para el metodo DELETE: Este metodo se utiliza para borrar un usuario si asi se desea, solo se necesita ingresar el ID de usuario, si este ID es correcto entonces se muestra el status 200, OK, sino el status es 404 ya que el usuario no se encuentra.

Para el metodo GET: Este metodo es para crear una simulacion de login en la API, se debe ingresar un nickname y un password, si eston existen en la base de datos y son correctos, entonces se muestra la informacion completa del usuario, de lo contrario, se muestra un status 401, ya que no se autoriza el acceso.

Una variacion de ruta: /user/all
Esta variacion se utiliza para mostrar todos los usuarios registrados en la base de datos y solo tiene el metodo GET, no es necesario ingresar datos.

En la ruta: /book
Se encuentran los metodos: POST , PUT, GET, DELETE.

Metodo POST: Este metodo crea un libro, se pide la informacion necesaria, como lo es el id del libro, titulo, tipo, la cantidad total, disponibles, y no disponibles, el año y la editorial, si todo sale bien entonces se muestra el status 201, CREATED, si el usuario ya existe entonces se muestra el status 400 puesto que el servidor no sabe como reaccionar.

Metodo PUT: Metodo utilizado para modificar un libro, ya sea la cantidad total de copias, editorial, nombres, etc, si el libro existe entonces se muestra el status 200, OK, sino existe e libro a modificar entonces se muestra el status 404, solo se pide el id del libro.

Metodo GET: Metodo utilizado para ver el objeto ibro, desde el id, titulo y tipo hasta la cantidad disponible, editorial, etc, los datos que pide es, el id, titulo y/o tipo, el decir, se pueden enviar uno, dos, o los tres datos, si existe el libro, entonces lo muestra, de lo contrario muestra el status 404, ya que no se encuentra.

Metodo DELETE: Este metodo se encarga de borrar el registro de un libro, es decir, borrar totalmente su existencia, solo se necesita del id de dicho libro, y si se encuentra el libro se muestra el status 200, OK, si no se muestra el 404, puesto que no lo encuentra.

Una variacion de ruta: /book/all
Esta variacion se utiliza para mostrar todos los libros registrados en la base de datos y solo tiene el metodo GET, no es necesario ingresar datos.

En la ruta: /loan
Se encuentran los metodos: POST, GET, PUT, DELETE.

Metodo POST: En este metodo se crea un prestamo, se pide ingresar el id de usuario y el id de libro, con esto, si todo sale bien y existe el usuario y el libro, se muestran los datos del libro, los datos del usuario y los datos del objeto prestamos, con la fecha de pedido y fecha de devolucion del libro, de lo contrario se muestra en status 404 puesto que no encuentra el usuario o el libro.

Metodo GET: En este metodo se puede ver el estado del prestamo, es decir, el id del prestamos, id del usuario, id del libro, fecha de pedido y devolucion, se pide solo el id del prestamos, si este existe, entonces se muestran los datos sino, se muestra 404 puesto que no se enuentra el prestamo registrado.

Metodo PUT: En este metodo se puede pedir el libro para usarlo una semana mas, es decir extender la fecha del prestamo, solo se pide el id del prestamo para realizar este proceso, si todo sale bien, se muestran los datos del prestamo y las nuevas fechas, sino se muestra 404 puesto que no se encuentra el prestamo registrado en la base de datos.

Metodo DELETE: Este metodo sirve si el prestamo se quiere revocar o se quiere devolver el libro, este se encarga de borrar el prestamo, y solo se pide el id del prestamo, si el prestamo existe se muestra el status 200, OK sino se muestra 404 puesto que no se encuetra el prestamo registrado.

Una variacion de ruta: /loan/penalty, solo cuenta con el metodo PUT
En esta variacion se ingresa el id del prestamo y si existe, se devuelve la multa que tiene el prestamo, sino tiene multa, solo muestra 0 en el penalty, si el prestamo no existe entonces se muestra 404.

Una variacion de ruta: /loan/all, solo cuenta con el metodo GET
Esta variacion se encarga de mostrar una lista con los datos completos de todos los prestamos registrados en la base de datos.
