<template>
    <div>
        <!--
        ? selectiva con if-else 
        * solo indica el nodo que se esta usando y el otro lo ignora,  deja un nodo mas pequeño, mas limpio
        *se utiliza cuando deseas que un elemento se agregue o elimine completamente del DOM según la condición. Si la expresión asociada con v-if es falsa, el elemento y sus componentes internos no se renderizarán en absoluto
        -->
        <h1 v-if="age > 18">eres mayor de edad</h1>
        <h1 v-else>eres menor de edad</h1>

                <!--
        ? selectiva con show
        * indica que nodo se esta usando y que no en el html con una clase display none, es agil para cuando se va ejecutar pocas veces
        * se utiliza para mostrar u ocultar un elemento cambiando la propiedad CSS display. Si la expresión asociada con v-show es falsa, el elemento se oculta aplicando display: none a través de CSS, pero aún existe en el DOM y mantiene su estado interno. Si la expresión cambia entre verdadera y falsa, solo se actualizará la propiedad CSS display.


        -->
        <h1 v-show="nombre=='jose'">hola jose david</h1>
        <h1 v-show="nombre=='david'">hola jajaj</h1>
    </div>
</template>

<script setup>
    let age = 20
    let nombre = "jose"
</script>
<style scope>
H1{
    color: blue;
}
</style>

<!--! Entonces, ¿cuál usar en qué situación?

Si tienes elementos que se muestran con poca frecuencia y la ocultación y el montaje de elementos no son costosos en términos de rendimiento, v-if puede ser la opción adecuada. Esto se debe a que v-if garantiza que los elementos ocultos no se rendericen en absoluto.

Por otro lado, si tienes elementos que se muestran y ocultan con frecuencia, v-show puede ser más eficiente en términos de rendimiento, ya que solo modifica la propiedad CSS display. -->