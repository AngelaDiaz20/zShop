## General
Se enlazó la hoja de estilos practice.css a cada documento html
```html
<link rel="stylesheet" href="css/practice.css">
```
**Ajuste de ancho en contenedores principales.**
Se asignaron propiedades iguales a los tres contenedores; “margin:auto” para centrarlos y un width en pixeles para mantener su tamaño fijo.
```css
header, footer, #container{
    margin: auto;
    width: 950px;
}
```
Se implementó una media querie que funciona a partir de los 1200px de viewport, en la cual aumenta un poco el ancho de los contenedores principales
```css
@media (min-width:1200px) {
    header, footer, #container{
        width: 1000px;
    }
}
```
## Header
En el header se redistribuyen y alinean los elementos con flexbox, de tal manera que queden en una misma línea
```css
header .row{
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
}
```
## Footer
El footer se redistribuye en 3 columnas mediante display grid, asignándole un porcentaje a cada una y un gap para su espaciado.
```css
footer .row{
    display: grid;
    grid-template-columns: 31% 31% 31%;
    column-gap:20px;
}
```
Por otra parte, al contenedor de la tercera columna se le da propiedad flexbox para que dicho contenido se establezca en una sola columna.
```css
.col-footer-3 .wrap-col .row{
    display: flex;
    flex-direction: column;
}
```
## Homepage
Con css grid se establecieron las columnas y a cada contenedor se le asignó un nombre para que mediante el mismo se atribuyera el área a ocupar.
```css
.box-2 .row{
    display: grid;
    grid-template-columns: 4fr 1fr 1fr 4fr;
    grid-template-areas: "one two two two"
                                      "three three three four"
                                      "five five six six";
}
```
Adicional a ello, se les dió un ancho para que los elementos aparecieran.
```css
.content-box.box-2 .box-item {
    width:100%;
}
```
En la sección de la modelo, se asignó un ancho al contenedor del texto, con eso bastó para acomodarlo como se debía.
```css
.box-3 .box-text{
    width: 50%;
}
```
## Blog
Para esta página nada más se usó css grid y se estableció un ancho para cada columna. Al hacerlo los elementos se acomodaron de la manera adecuada.
```css
.archive-post .flex-box{
    display: grid;
    grid-template-columns: 50% 50%;
}
```

## Contact
En cuanto al formulario, se usó una clase para especificar el contenedor de los tres input, para cada uno se asignó una columna en porcentajes y su espaciado a través de un space-between.
```css
#contact_form .row-input{
    display: grid;
    grid-template-columns: 32% 32% 32%;
    justify-content: space-between;
}
```
------------





Designed by Zerotheme
Website : http://www.zerotheme.com
Zerogrid System for Responsive Design - http://www.zerotheme.com/zerogrid-a-simple-grid-system-for-responsive-design

/*----License----*/
+ You have the rights to use the resources for personal and commercial project(s) purposes.
+ You are not allowed to remove back link at the footer in template. You should contact us about this. http://www.zerotheme.com/contact-us
+ You are allowed to remove back link with basic templates. You can find basic templates at http://www.zerotheme.com/free-basic-responsive-html5-themes
+ You can not resell, redistribute, license, or sub-license any of the templates without direct permission from Zerotheme.com.
+ You are not allowed to provide direct link to download or preview template. You must link back to Zerotheme template page where users can find the download and preview template.
