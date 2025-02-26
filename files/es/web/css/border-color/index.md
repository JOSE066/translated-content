---
title: border-color
slug: Web/CSS/border-color
tags:
  - CSS
  - CSS:Referencias
  - Todas_las_Categorías
translation_of: Web/CSS/border-color
---

{{ PreviousNext("CSS:border", "CSS:border-style") }}

### Resumen

la propiedad `border-color` es un atajo para definir el color de los cuatro bordes de un elemento.

- {{ Cssxref("initial", "Valor inicial") }}: el {{ Cssxref("color") }} del elemento en sí
- Se aplica a: todos los elementos
- {{ Cssxref("inheritance", "Herencia") }}: no
- Percentages: N/A
- Medio: {{ Cssxref("Media:Visual", "visual") }}
- {{ Cssxref("computed value", "Valor calculada") }}: el valor del `color` por defecto, o lo que se especificó.

### Sintaxis

```
border-color: [ <color> || transparent ]{1,4} | inherit
```

### Valores

- \<color>
  - : el color se puede especificar con un valor RGB hexa-decimal o regular, o con el nombre predefinido de ese color.

<!---->

- transparent
  - : el borde no aparece pero ocupa el sitio definido.

Se pueden pasar hasta cuatro valores;

Con **un** color, los cuatro lados tendrán el mismo.
Con **dos** colores, los lados de arriba y abajo utilizan el primer valor y los izquierda y derecha el segundo.
Con **tres** colores, el primero para arriba, el segundo para izquierda y derecha y el tercero para abajo.
Con **cuatro** colores, el primero para arriba, el segundo para la derecha, el tercero para abajo y el cuarto para la izquierda.

### Ejemplos

[Ver El Ejemplo Vivo](/samples/cssref/border.html)

```
element {
  border-width: 1px;
  border-style: solid;
  border-color: black;
}
```

### Notas

Para poder ver el/los bordes también hay que definir {{ Cssxref("border-width", "el ancho") }} con un valor positivo y {{ Cssxref("border-style", "el estilo") }} con algo visible. (_diferente de `none o hidden`_)

### Especificaciones

- [CSS 1](http://www.w3.org/TR/CSS1#border-color)
- [CSS 2.1](http://www.w3.org/TR/CSS21/box.html#border-color-properties)
- [CSS 3](http://www.w3.org/TR/css3-background/#the-border-color)

### Compatibilidad

| Navegadores       | Versión mínima |
| ----------------- | -------------- |
| Internet Explorer | 4              |
| Firefox           | 1              |
| Netscape          | 4              |
| Opera             | 3.5            |

### Extensiones Mozilla

La siguientes extensiones definen los múltiples colores de los respectivos bordes en los navegadores Gecko.

- {{ Cssxref("-moz-border-bottom-colors") }}
- {{ Cssxref("-moz-border-left-colors") }}
- {{ Cssxref("-moz-border-right-colors") }}
- {{ Cssxref("-moz-border-top-colors") }}

### Ver también

{{ Cssxref("border") }}, {{ Cssxref("border-color") }}, {{ Cssxref("border-style") }}, {{ Cssxref("border-width") }}
