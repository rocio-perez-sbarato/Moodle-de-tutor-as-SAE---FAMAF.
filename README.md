# Documentación del espacio virtual de las tutorías de la SAE - FAMAF. Año 2024.

<aside>
🖥️ Repositorio del código HTML.

</aside>

[https://github.com/rocio-perez-sbarato/Moodle-de-tutor-as-SAE---FAMAF.](https://github.com/rocio-perez-sbarato/Moodle-de-tutor-as-SAE---FAMAF.)

# Sección ¿Quiénes somos?

1. **Sección de Quiénes somos:**
    
    ```html
    <div style="display: flex; justify-content: space-between; flex-wrap: wrap;">
    
        <!-- Columna Quiénes somos con acordeones -->
        <div style="flex: 0 1 calc(100% - 20px); margin-bottom: 0;">
            <!-- ... (Contenido de la sección) ... -->
        </div>
    </div>
    
    ```
    
    - **Descripción:** Esta sección contiene información sobre los tutores/as. Utiliza una disposición de columnas y acordeones para mostrar información detallada sobre cada tutor/a.
2. **Columna ¿Quiénes somos? con Acordeones:**
    
    ```html
    <div style="max-width: 800px; margin: 0 auto; padding: 20px; background-color: #FFFFFF;">
        <!-- ... (Contenido de la columna) ... -->
    </div>
    
    ```
    
    - **Descripción:** Esta columna contiene información general sobre el grupo de tutores/as. Utiliza acordeones para mostrar detalles individuales de cada tutor/a.
3. **Acordeones de Tutores/as:**
    
    ```html
    <div class="acordeon" style="display: flex; flex-wrap: wrap;">
        <!-- ... (Contenido de los acordeones) ... -->
    </div>
    
    ```
    
    - **Descripción:** Esta sección utiliza acordeones para organizar y mostrar información detallada sobre cada tutor/a de forma oculta hasta que se haga clic.
4. **Script para el Funcionamiento del Acordeón:**
    
    ```html
    <script>
        var acordeonLabels = document.querySelectorAll('.acordeon-label');
    
        acordeonLabels.forEach(function(label) {
            label.addEventListener('click', function() {
                var content = this.nextElementSibling;
                content.style.display = (content.style.display === 'block') ? 'none' : 'block';
            });
        });
    </script>
    
    ```
    
    - **Descripción:** Este script en JavaScript añade funcionalidad a los acordeones, permitiendo que se expandan o contraigan al hacer clic en las etiquetas.
5. **Secciones ¿Qué hacemos? y ¿Para qué sirve este aula virtual?:**
    
    ```html
    <!-- ... (Contenido de las secciones) ... -->
    
    ```
    
    - **Descripción:** Estas secciones contienen información sobre las actividades y el propósito del aula virtual de tutores/as.
6. **Sección de Foros Generales:**
    
    ```html
    <!-- ... (Contenido de la sección de foros generales) ... -->
    
    ```
    
    - **Descripción:** Esta sección describe el propósito de los foros generales, específicamente el Foro de Avisos y el Foro de Preguntas Generales.

## Acordeones

### Contenedor de Acordeones

```html
<div class="acordeon" style="display: flex; flex-wrap: wrap;">
    <!-- Contenido de los acordeones -->
</div>

```

- **Clase:** `acordeon`
- **Estilo:** Utiliza flexbox para alinear los acordeones en una fila y permite el ajuste de línea si es necesario.

### Acordeón Individual

```html
<div class="acordeon-item" style="flex: 0 1 calc(33.33% - 10px); margin-bottom: 10px;">
    <!-- Contenido de un acordeón individual -->
</div>

```

- **Clase:** `acordeon-item`
- **Estilo:**
    - `flex: 0 1 calc(33.33% - 10px)`: Establece que cada acordeón ocupa inicialmente el 33.33% del ancho del contenedor, con un espacio entre ellos.
    - `margin-bottom: 10px`: Agrega un margen inferior de 10px entre los acordeones.

### Etiqueta de Acordeón

```html
<label class="acordeon-label">Nico ▼</label>

```

- **Clase:** `acordeon-label`
- **Estilo:** No hay estilos específicos aquí, pero esta etiqueta se utiliza como el encabezado del acordeón que se puede hacer clic para expandir o contraer el contenido.

### Contenido del Acordeón

```html
<div class="acordeon-content" style="display: none;">
    <!-- Contenido del acordeón que está oculto inicialmente -->
</div>

```

- **Clase:** `acordeon-content`
- **Estilo:** `display: none` oculta inicialmente el contenido del acordeón.

### Script para Funcionamiento del Acordeón (JavaScript)

```html
<script>
    var acordeonLabels = document.querySelectorAll('.acordeon-label');

    acordeonLabels.forEach(function(label) {
        label.addEventListener('click', function() {
            var content = this.nextElementSibling;
            content.style.display = (content.style.display === 'block') ? 'none' : 'block';
        });
    });
</script>

```

- **Descripción:** Este script agrega funcionalidad al acordeón, permitiendo que se expanda o contraiga al hacer clic en la etiqueta.

## Dos columnas pegadas

### Contenedor de Columnas

```html
<div style="display: flex; justify-content: space-between; flex-wrap: wrap;">
    <!-- Contenido de las columnas -->
</div>

```

- **Estilo:**
    - `display: flex`: Convierte al contenedor en un contenedor flexible.
    - `justify-content: space-between`: Distribuye el espacio entre los elementos hijos para que estén pegados a los extremos del contenedor.
    - `flex-wrap: wrap`: Permite que los elementos hijos se envuelvan a la siguiente línea si no caben en una sola línea.

### Columna 1

```html
<div style="flex: 0 1 calc(100% - 20px); margin-bottom: 0;">
    <!-- Contenido de la primera columna -->
</div>

```

- **Estilo:**
    - `flex: 0 1 calc(100% - 20px)`: Establece que la primera columna ocupa inicialmente el 100% del ancho del contenedor y permite un espacio a la derecha de 20px.
    - `margin-bottom: 0`: Elimina el margen inferior de la primera columna.

### Columna 2

```html
<div style="flex: 0 1 calc(50% - 10px); margin-bottom: 0;">
    <!-- Contenido de la segunda columna -->
</div>

```

- **Estilo:**
    - `flex: 0 1 calc(50% - 10px)`: Establece que la segunda columna ocupa inicialmente el 50% del ancho del contenedor y permite un espacio a la derecha de 10px.
    - `margin-bottom: 0`: Elimina el margen inferior de la segunda columna.
    

# Documentación de las demás secciones

A continuación, proporcionaré descipciones detalladas sobre cómo hice las otras secciones del aula virtual. Básicamente, usé una estructura de título con color de fondo y de letra, así como una estructura de un cuadrado de texto con fondo de color y borde punteado.

## Título resaltado

```html
<h2 style="text-align: left; background-color: #660066; color: #fff; margin-bottom: 20px; padding: 10px; border-radius: 5px;">
    Encuentro virtual por Discord
</h2>

```

- **Elemento HTML:** `<h2>`
- **Estilo:**
    - `text-align: left`: Alinea el texto a la izquierda.
    - `background-color: #660066`: Establece el color de fondo del título.
    - `color: #fff`: Define el color del texto como blanco.
    - `margin-bottom: 20px`: Agrega un margen inferior de 20px para separar el título del contenido siguiente.
    - `padding: 10px`: Añade un espacio interno alrededor del texto del título.
    - `border-radius: 5px`: Suaviza las esquinas del fondo del título con un radio de 5px.

## Cuadradito con fondo de color y borde punteado

```html
<div style="text-align: left; background-color: #FFE9FF; color: black; margin-bottom: 20px; padding: 10px; border-radius: 5px; border: 2px dashed #000; border-color: #660066">
    <h3>📢Próximas actualizaciones</h3>
    <ul>
        <li>Estamos trabajando en los detalles de la organización de actividades y talleres virtuales.</li>
        <li>La fecha y horarios se compartirán próximamente.</li>
    </ul>
</div>

```

- **Elemento HTML:** `<div>`
- **Estilo:**
    - `text-align: left`: Alinea el contenido del cuadro a la izquierda.
    - `background-color: #FFE9FF`: Establece el color de fondo del cuadro.
    - `color: black`: Define el color del texto como negro.
    - `margin-bottom: 20px`: Agrega un margen inferior de 20px para separar el cuadro del contenido siguiente.
    - `padding: 10px`: Añade un espacio interno alrededor del contenido del cuadro.
    - `border-radius: 5px`: Suaviza las esquinas del fondo del cuadro con un radio de 5px.
    - `border: 2px dashed #000`: Crea un borde punteado de 2px con color negro.
    - `border-color: #660066`: Establece el color del borde del cuadro.

# Cronograma

## Tabla y códigos de color

1. **División y Título del Cronograma**
    
    ```html
    <div style="background-color: #c9e9fc; color: black; margin-bottom: 20px; padding: 10px; border-radius: 5px;">
        <h2>Cronograma de actividades y talleres</h2>
    </div>
    
    ```
    
2. **Tabla de Cronograma**
    
    ```html
    <table style="width: 100%; border-collapse: collapse;">
        <caption style="caption-side: top; font-weight: bold; font-size: 1.2em;">Cronograma de marzo y principios de abril</caption>
        <thead>
            <!-- Encabezado de la tabla con estilos específicos -->
        </thead>
        <tbody>
            <!-- Filas y celdas de contenido -->
        </tbody>
    </table>
    
    ```
    
3. **Filas y Celdas de Contenido**
    
    ```html
    <tr>
        <!-- Celdas para cada día de la semana con estilos específicos -->
    </tr>
    
    ```
    
4. **Códigos de Color**
    
    ```html
    <div style="background-color: #fff; color: black; margin-bottom: 20px; padding: 10px; border-radius: 5px;">
        <!-- Códigos de color con círculos coloreados -->
    </div>
    
    ```
    

## Días en circulito y eventos en un día

1. **Numeración en Circulitos**
    
    ```html
    <td style="padding: 15px; border: 1px solid #ddd; background-color: #ddd; color: #fff;">
        <span style="display: inline-block; width: 20px; height: 20px; border-radius: 50%; background-color: #ddd; color: black;margin-right: 10px; text-align: center; line-height: 20px;">11<br><br><br><br><br><br><br><br><br></span>
    </td>
    
    ```
    
    - Cada día de la semana está representado por una celda `<td>`.
    - Se utiliza un círculo (`<span>`) con estilos específicos para crear un contorno redondo.
    - El número del día se coloca dentro del círculo para proporcionar la numeración correspondiente.
2. **Evento en un Día**
    
    ```html
    <td style="padding: 15px; border: 1px solid #ddd; background-color: #fff; color: black;">
        <div style="display: inline-block; width: 20px; height: 20px; border-radius: 50%; background-color: #ddd; color: black; margin-right: 10px; text-align: center; line-height: 20px;">12<br><br></div>
        <div style=" margin-bottom: 10px; background-color: #990000; padding: 10px; border-radius: 5px;">
            <p style="margin-bottom: 10px; color: #fff;"><strong>Herramientas para dar tus primeros pasos en FAMAF. Aula 31. 18 hs.</strong></p>
        </div>
    </td>
    
    ```
    
    - Se agrega un círculo similar al anterior para la numeración del día.
    - Se añade un segundo `<div>` dentro de la celda para representar un evento específico.
    - Este evento tiene un fondo de color bordó (`#990000`), con detalles de texto y estilos adicionales.
