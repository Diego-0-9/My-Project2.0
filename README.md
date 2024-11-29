# My-Project2.0
edit in my project2.0
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Menu Principal</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>PROGRAMACIÓN</h1>
    </header>
    <main>
        <section id="inicio" class="contenedor visible">
            <button onclick="mostrarSeccion('HTML')">HTML</button>
            <button onclick="mostrarSeccion('CSS')">CSS</button>
            <button onclick="mostrarSeccion('JAVASCRIPT')">JAVASCRIPT</button>
            <button onclick="mostrarSeccion('JAVA')">JAVA</button>
        </section>
        <section id="HTML" class="contenedor"> 
            <h2>HTML:Etiquetas</h2>
            <ol>
                <li>Head</li>
                <li>Header</li>
                <li>Boddy</li>
            </ol>
            <button onclick="mostrarSeccion('inicio')">Volver</button>
        </section>
        <section id="CSS" class="contenedor">
            <h2>CSS:propioedades</h2>
            <ul>
                <li>Font-family</li>
                <li>Background-color</li>
                <li>Border</li>
            </ul>
            <button onclick="mostrarSeccion('inicio')">Volver</button>
        </section>
        <section id="JAVASCRIPT" class="contenedor">
            <h2>JAVASCRIPT: SCRIPT</h2>
            <table>
                <thead>
                    <tr>
                        <th>Pros</th>
                        <th>Contras</th>
                        <th>Caracteristicas</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Lenguaje de programación interpretado y dinámico.</td>
                        <td>Puede ser lento en tareas complejas.</td>
                        <td>Compatible con objetos, funciones y eventos.</td>
                    </tr>
                    <tr>
                        <td>Amplio soporte en todos los navegadores.</td>
                        <td>Es fácil cometer errores debido a su naturaleza flexible.</td>
                        <td>Se ejecuta en el navegador y en el servidor (Node.js)</td>
                    </tr>
                </tbody>
            </table>
            <button onclick="mostrarSeccion('inicio')">Volver</button>
        </section>
        <section id="JAVA" class="contenedor">
            <h2>JAVA: Formulario</h2>
            <form>
                <label for="nombre">Nombre:</label>
                <input id="nombre" name="nombre" type="text" required>
                <label for="email">Correo Electrónico:</label>
                <input id="email" name="email" type="email" required>
                <fieldset>
                    <legend>Género:</legend>
                    <label><input name="genero" type="radio" value="masculino"> Masculino</label>
                    <label><input name="genero" type="radio" value="femenino"> Femenino</label>
                </fieldset>
                <label for="pais">País:</label>
                <select id="pais" name="pais">
                    <option value="mx">México</option>
                    <option value="us">Estados Unidos</option>
                    <option value="es">España</option>
                </select>
                <button type="submit">Enviar</button>
            </form>
            <button onclick="mostrarSeccion('inicio')">Volver</button>
        </section>
    </main>
    <footer>
        <p>&copy; 2024 Derechos Reservados</p>
    </footer>
    <script>
        function mostrarSeccion(seccionId) {
            document.querySelectorAll('.contenedor').forEach((seccion) => {
                seccion.classList.remove('visible');
            });
            document.getElementById(seccionId).classList.add('visible');
        }
    </script>
</body>
</html>

/* Estilo General */
body {
    display: flex;
    flex-direction: column;
    font-family: 'Arial', sans-serif;
    margin: 0;
    min-height: 100vh;
    padding: 0;
    text-align: center;
    background-color: #f7f7f7; 
    color: #333; 
}

/* Estilo del header y footer */
header, footer {
    background-color: #000000; 
    color: white;
    font-family: 'Georgia', serif;
    padding: 20px 0;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15); 
}

/* Títulos */
h1, h2 {
    font-weight: 700;
    margin-bottom: 15px;
    color: rgb(134, 134, 134); 
    font-size: 32px;
}

/* Estilo de los botones */
button {
    background-color: #007BFF; 
    border: 2px solid #007BFF;
    border-radius: 50px; 
    font-family: 'Arial', sans-serif;
    font-size: 18px;
    color: white;
    padding: 12px 30px;
    cursor: pointer;
    margin: 10px;
    text-transform: uppercase;
    font-weight: bold;
    transition: all 0.5s ease-in-out; 
    box-shadow: 0 6px 15px rgba(0, 123, 255, 0.5); 
}

/* Efecto hover en los botones */
button:hover {
    background-color: #007bff;
    border-color: #0056b3;
    color: white;
    box-shadow: 0 8px 20px rgba(0, 38, 255, 0.329); 
}

/* Estilo de las secciones contenedor */
.contenedor {
    display: none;
    margin: 0 auto;
    max-width: 700px;
    text-align: center;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    padding: 30px 20px;
    background-color: #ffffff;
    border-radius: 12px; 
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1); 
    transform: scale(0.98);
    opacity: 0;
    transition: transform 0.3s ease, opacity 0.3s ease;
}

/* Al mostrar la sección, hacemos una transición de visibilidad y tamaño */
.contenedor.visible {
    display: block;
    opacity: 1;

}

/* Estilo de listas */
ul, ol {
    margin: 20px auto;
    max-width: 350px;
    text-align: left;
    font-size: 18px;
}

ul li, ol li {
    margin-bottom: 10px;
    color: #3b3b3b;
}

/* Estilo para tablas */
table {
    width: 90%;
    margin: 30px auto;
    border-collapse: collapse;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

th, td {
    border: 1px solid #757373;
    padding: 12px;
    text-align: left;
}

th {
    background-color: #f9f9f9;
    font-weight: bold;
    color: #2c2c2c;
}

tbody tr:hover {
    background-color: #f4f4f4;}

/* Estilo de formularios */
form {
    display: flex;
    flex-direction: column;
    gap: 15px;
    text-align: left;
    max-width: 400px;
    margin: 20px auto;
}

input, select {
    padding: 12px;
    border: 1px solid #ddd;
    border-radius: 8px;
    margin-top: 5px;
    font-size: 16px;
    transition: border-color 0.3s ease;
}

input:focus, select:focus {
    border-color: #007BFF; 
}

/* Estilo de links */
a {
    color: #0077f7;
    text-decoration: none; 
    font-weight: bold;
    transition: color 0.3s ease, transform 0.3s ease; 
    position: relative; 
}

/* Efecto hover en los enlaces */
a:hover {
    color: #0055af; 
    transform: translateY(-2px); 
}

/* Subrayado animado */
a::after {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 0;
    height: 2px;
    background-color: #007BFF;
    transition: width 0.3s ease; 
}

/* Cuando el usuario pasa el mouse, se extiende el subrayado */
a:hover::after {
    width: 100%;
}

/* Agregar sombra al texto */
a:hover {
    text-shadow: 0 0 5px rgba(0, 123, 255, 0.6); 
}

/* Footer con detalles más sutiles */
footer {
    background-color: #1e1e1e; 
    color: white;
    font-family: 'Georgia', serif;
    padding: 20px 0;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.15); 
    margin-top: auto; 
}

footer p {
    font-size: 14px;
    opacity: 0.7;
    color: #fff;
    margin: 0;
    padding: 10px 0;
    transition: opacity 0.3s ease; 
}

footer p:hover {
    opacity: 1; 
}

/* Para los botones de envío */
button[type="submit"] {
    background-color: #28a745;
    border-color: #28a745;
}

button[type="submit"]:hover {
    background-color: #218838;
    border-color: #218838;
    box-shadow: 0 6px 12px rgba(40, 167, 69, 0.5); 
}
















