# ■ Curso_de_Hooks_en_ReactJS:_conociendo-su_potencial_y_utilidad
▷ 01 Gestionando el estado de los componentes.
◉ 04 Que son los hooks y por que son útiles.
✳ Los componentes en React han evolucionado de ser clases que heredaban de React.Component a ser funciones simples.
◉ 07 Facilitando la gestión de estados en componentes.
✳  const [estado, setEstado ]= useState({});
✳ Se busca manejar un evento onClick pasando los props desde el componente principal hasta los nietos que contienen el elemento que se necesita manejar con estados.
✳ El estado de un componente se refiere a la situación o condición actual del mismo. Esto permite que los componentes sean dinámicos y respondan a eventos o acciones.
✳ Creación de un estado simple y se usa prop drilling.
◉ 08 Completando la implementación de useState.
✳ Desarrollo del estado simple en el componente Galeria para poder filtrar renderizado de elementos reaccionando al evento onChange. 
✳ return consulta=='' || foto.titulo.toLowerCase().includes(consulta.toLowerCase())
◉ 10 Conociendo a useRef.
✳ toLocaleLowerCase().normalize("NFD").replace(/\p{Diacritic}/gu,""
✳ El hook useRef, que permite acceder a elementos del DOM sin tener que usar consultas directas al DOM.
✳ Se modificó el código de la aplicación Space App para que el filtrado de imágenes se realice al hacer clic en el icono de búsqueda, en lugar de al escribir en el campo de texto.

▷ 02 Conociendo los efectos secundarios.
◉ 02 Gestionando los efectos secundarios (useEffect).
✳ Los efectos secundarios son operaciones que se ejecutan después de que el componente se haya creado o actualizado, a diferencia de los console.log que se ejecutan antes de que el componente se haya montado.
✳ Ciclo de vida de un componente, montaje, actualizción, desmontaje.
✳ El efecto secundario, lo que nos permite es ejecutar código después de creada la aplicación.
◉ 03 Manejando las dependencias del useEffect.
✳ Cuando no se pasa ningún array de dependencias al useEffect, este se ejecutará en la creación del componente y en cada actualización (cambio de estado).
✳ Podemos pasar un array de dependencias al useEffect para controlar cuándo se ejecutará:
Si el array está vacío [], el useEffect solo se ejecutará en la creación del componente.
Si incluimos una o más variables en el array, el useEffect se ejecutará cuando esas variables cambien.
◉ 06 Convirtiendo un JSON en una API.
✳ En otra carpeta se copia fotos.json y se modifica con un objeto global y se instala una instancia de json con  npx json-server $nombreDelARchivo$ 
◉ 07 Consumiendo una API REST con useEffect.
✳ Se consume una API REST utilizando useEffect y a manejar adecuadamente el estado de la aplicación en ese proceso.
✳ Conexión con la API fake:
 const getData = async () => {
    const res = await fetch ('http://localhost:3000/fotos');
    const data = await res.json();
    console.log(data)
  }

▷ 04 Manipulando el estado global desde la aplicación.
◉ 02 Entendiendo el problema del prop drilling.
✳ Se usa el hook Context como alternativa al prop drilling.
◉ 03 Conociendo a ContextAPI.
✳ Se muestra cómo crear el contexto global usando la función createContext() de React.
◉ 04 Organizando el contexto.
✳ Se mueven los estados de la aplicación al contexto global, para que puedan ser compartidos entre los diferentes componentes.
◉ 05 Accediendo al contexto global.
✳ Se explicó que el uso del contexto global es ideal cuando hay estados que se comparten entre varios componentes de la aplicación.

▷ 04 Manipulando el estado global desde la aplicación.
◉ 02 Gestión de estados en sistemas complejos. useReducer.
✳ Enfoque en el uso del hook useReducer.
◉ 03 Creación de reducers y acciones.
✳ El hook useReducer de React, que permite una gestión de estado más escalable y organizada.
✳ const reducers = (state, action)
✳ const [state, dispatch] = useReducer(reducers, initialState)
◉ 04 Implementación de un estado global utilizando useReducer.
✳ Con useReducer podemos manejar estados más complejos, donde un solo evento puede afectar a múltiples estados.
▷ 05 Implementando nuestros propios hooks.
◉ 02 Definiendo nuestros propios hooks Leonardo Jose.
✳ Los custom hooks nos permiten encapsular lógica reutilizable en nuestras aplicaciones, mejorando la organización y legibilidad del código.
◉ 03 Creando el hook useFotoModal Leonardo Jose.
✳ Creación de un nuevo Hook (custom) llamado useFotoModal que encapsula la lógica para abrir y cerrar un modal que muestra la foto seleccionada.

◉ 04 Utilizando a useFotoModal.
✳ Creación de un nuevo Hook (custom) llamado useFotoModal.
Este hook nos permite controlar la apertura y cierre del modal que muestra la imagen seleccionada.
