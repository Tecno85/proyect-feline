## Consejos para mejorar el sitio web

HTML
Validación de accesibilidad:

Añade atributos aria-label o aria-hidden en elementos decorativos o con texto no visible, como íconos, para mejorar la accesibilidad.
html
Copiar
Editar
<img src="assets/img/icon_leon.png" alt="Icono León" class="icon-leon" aria-hidden="true" />
Consistencia en nombres:

En el atributo meta, cambia descripcion por description (en inglés), ya que es el estándar reconocido por los motores de búsqueda.
Uso semántico:

Cambia los elementos <p> de la barra de navegación por una lista no ordenada (<ul> y <li>) para respetar la semántica.
html
Copiar
Editar
<ul class="titles-navbar">
  <li><a href="#guepardo">Guepardo</a></li>
  <li><a href="#pantera">Pantera</a></li>
  <li><a href="#leopardo">Leopardo</a></li>
</ul>
Cuidado con enlaces externos:

Usa siempre el atributo rel="noopener noreferrer" en enlaces con target="_blank" para evitar problemas de seguridad.
Jerarquía de encabezados:

Mantén una jerarquía correcta. Cambia los títulos <p> dentro de los <article> por <h2> o <h3> según corresponda, para mejorar la semántica y el SEO.
CSS
Uso de comentarios organizados:

Agrega comentarios descriptivos para cada sección de estilos para facilitar el mantenimiento.
css
Copiar
Editar
/* === Variables Globales === */
:root { ... }

/* === Reset y Estilos Globales === */
* { ... }

/* === Navbar === */
.navbar { ... }
Reduce repetición:

Agrupa propiedades compartidas en clases comunes. Ejemplo: los estilos de texto en .titles-navbar y footer p podrían consolidarse.
css
Copiar
Editar
.text-secondary {
  font-family: var(--font-footer);
  font-size: var(--font-size-navbar);
  color: var(--text-color-primary);
}
Evita unidades fijas innecesarias:

Usa unidades relativas (em, rem, %) en lugar de unidades absolutas (px) para mejorar la adaptabilidad.
Uso de prefijos:

Considera agregar prefijos CSS para garantizar compatibilidad en navegadores más antiguos. Ejemplo: para transform o box-shadow.
Media Queries específicas:

Refina las consultas @media. Podrías incluir un escalado entre 481px y 768px para dispositivos tablet:
css
Copiar
Editar
@media (min-width: 481px) and (max-width: 768px) {
  .navbar {
    padding: 1rem;
  }
  header h1 {
    font-size: 2rem;
  }
}
