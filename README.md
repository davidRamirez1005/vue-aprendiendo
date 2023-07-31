# vue-aprendiendo

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```



### Ciclo de vida de un componente: 

[Lifecycle](https://vuejs.org/api/options-lifecycle.html)

[hooks](https://vuejs.org/api/composition-api-lifecycle.html)

1. **Creación del componente:**
   - `setup()`: Esta es la nueva opción de configuración en Vue 3 que se utiliza para configurar el componente. Aquí se inicializan los datos, se registran las referencias a los elementos del DOM y se definen las funciones y métodos necesarios. También se gestionan las props y los eventos.
   - `beforeCreate()`: Esta opción ya no está disponible en Vue 3. Se ejecutaba antes de que el componente fuera creado.
2. **Montaje del componente:**
   - `onBeforeMount()`: Se ejecuta antes de que el componente se agregue al DOM.
   - `onMounted()`: Se ejecuta una vez que el componente ha sido agregado al DOM. Es el lugar adecuado para realizar tareas de inicialización que requieran acceso al DOM.
3. **Actualización del componente:**
   - `onBeforeUpdate()`: Se ejecuta antes de que el componente sea actualizado debido a cambios en los datos.
   - `onUpdated()`: Se ejecuta después de que el componente haya sido actualizado debido a cambios en los datos. Es el lugar adecuado para realizar acciones posteriores a la actualización.
4. **Destrucción del componente:**
   - `onBeforeUnmount()`: Se ejecuta antes de que el componente sea eliminado del DOM.
   - `onUnmounted()`: Se ejecuta una vez que el componente ha sido eliminado del DOM. Aquí es donde debes limpiar event listeners, cancelar peticiones o cualquier otra limpieza necesaria.

Además de estas opciones de ciclo de vida, Vue 3 también proporciona las opciones `watchEffect()` y `watch()` para observar cambios en las propiedades y ejecutar funciones en respuesta a esos cambios, lo cual simplifica la lógica que antes se manejaba en los hooks de ciclo de vida.

### Eventos

1. `@click` (o `v-on:click`): Se utiliza para escuchar el evento de clic del mouse en un elemento. Permite ejecutar una función cuando el elemento es clicado.
2. `@input` (o `v-on:input`): Escucha el evento de entrada en elementos de formulario, como `<input>`, `<textarea>`, y `<select>`. Se utiliza para realizar acciones cuando el usuario introduce datos en el elemento.
3. `@change` (o `v-on:change`): Se emplea para escuchar el evento de cambio en elementos de formulario, como `<input>` de tipo `checkbox` o `radio` y `<select>`. La función asociada se ejecuta cuando el valor del elemento cambia.
4. `@submit` (o `v-on:submit`): Escucha el evento de envío del formulario. Puedes utilizarlo para ejecutar una función antes de enviar el formulario o para prevenir el envío predeterminado y realizar validaciones personalizadas.
5. `@keydown` (o `v-on:keydown`): Se utiliza para escuchar el evento de tecla presionada. La función asociada se ejecuta cuando una tecla está siendo presionada.
6. `@keyup` (o `v-on:keyup`): Escucha el evento de liberación de tecla. La función asociada se ejecuta cuando una tecla que estaba siendo presionada es liberada.
7. `@mouseover` (o `v-on:mouseover`): Escucha el evento de pasar el cursor del mouse sobre el elemento. Permite realizar acciones cuando el mouse entra en el área del elemento.
8. `@mouseout` (o `v-on:mouseout`): Se utiliza para escuchar el evento de salir el cursor del mouse del elemento. La función asociada se ejecuta cuando el mouse sale del área del elemento.
9. `@focus` (o `v-on:focus`): Escucha el evento de obtener el foco en un elemento, como un campo de entrada. La función asociada se ejecuta cuando el elemento obtiene el foco.
10. `@blur` (o `v-on:blur`): Se emplea para escuchar el evento de perder el foco en un elemento. La función asociada se ejecuta cuando el elemento pierde el foco.

1. Eventos de ratón:
   - `@click`: Clic del ratón.
   - `@dblclick`: Doble clic del ratón.
   - `@mousedown`: Se dispara cuando se presiona un botón del ratón sobre el elemento.
   - `@mouseup`: Se dispara cuando se suelta un botón del ratón sobre el elemento.
   - `@mousemove`: Se dispara cuando el ratón se mueve sobre el elemento.
   - `@contextmenu`: Clic derecho del ratón (menú contextual).
2. Eventos de teclado:
   - `@keydown`: Tecla presionada.
   - `@keyup`: Tecla liberada.
   - `@keypress`: Tecla presionada y liberada (para teclas que generan caracteres).
3. Eventos de formulario:
   - `@submit`: Envío del formulario.
   - `@input`: Cambio en el valor de un elemento de formulario (por ejemplo, `<input>`, `<textarea>`, y `<select>`).
   - `@change`: Cambio en el valor de un elemento de formulario (por ejemplo, `<input type="checkbox">` y `<select>`).
4. Eventos de foco:
   - `@focus`: Obtención del foco por parte de un elemento.
   - `@blur`: Pérdida del foco por parte de un elemento.
5. Eventos de arrastrar y soltar:
   - `@dragstart`: Se inicia el arrastre de un elemento.
   - `@drag`: Se dispara mientras se está arrastrando un elemento.
   - `@dragend`: Se termina el arrastre de un elemento.
   - `@dragenter`: El elemento arrastrado entra en la zona de destino.
   - `@dragover`: El elemento arrastrado se mueve sobre la zona de destino.
   - `@dragleave`: El elemento arrastrado sale de la zona de destino.
   - `@drop`: Se suelta el elemento arrastrado en la zona de destino.
6. Eventos de ventanas y documentos:
   - `@load`: Se dispara cuando la ventana o el documento ha terminado de cargar.
   - `@resize`: Cambio en el tamaño de la ventana del navegador.
   - `@scroll`: Se dispara cuando se realiza un desplazamiento en el documento.

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).
