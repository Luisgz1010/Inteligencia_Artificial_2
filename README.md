<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Evento dblclick</title>
    <style>
        body { font-family: sans-serif; text-align: center; padding: 20px; transition: 0.5s; }
        .ejemplo { border: 2px solid #ccc; margin: 20px; padding: 15px; border-radius: 10px; cursor: pointer; user-select: none; }
        .caja { width: 100px; height: 100px; background: tomato; margin: 10px auto; }
        .item-lista { background: #eee; padding: 10px; list-style: none; width: 200px; margin: 5px auto; }
        img { width: 150px; border-radius: 10px; }
    </style>
</head>
<body>
 
    <h1>Ejemplos de Evento dblclick</h1>
    <p>(Haz doble clic en cada recuadro para ver el efecto)</p>
 
    <div class="ejemplo">
        <h3>1. Like de Foto</h3>
        <img id="miFoto" src="logo3.jpeg" alt="Foto">
        <p id="mensajeLike"></p>
    </div>
 
    <div class="ejemplo">
        <h3>2. Modo Oscuro</h3>
        <p>Haz doble clic en cualquier parte blanca de la página.</p>
    </div>
 
    <div class="ejemplo">
        <h3>3. Zoom Mágico</h3>
        <div id="miCaja" class="caja"></div>
    </div>
 
    <div class="ejemplo">
        <h3>4. Borrar Tarea</h3>
        <li id="miTarea" class="item-lista">Comprar pan (Doble clic para borrar)</li>
    </div>
 
    <div class="ejemplo">
        <h3>5. Mensaje Oculto</h3>
        <div id="sobreCerrado" style="font-size: 24px;">✉️ Doble clic para abrir</div>
    </div>
 
    <script>
        const foto = document.getElementById('miFoto');
        foto.addEventListener('dblclick', () => {
            document.getElementById('mensajeLike').textContent = '❤️ ¡Te gusta esta foto!';
        });
 
        // EJEMPLO 2: La "antena" escucha en todo el cuerpo de la página para cambiar los colores
        document.body.addEventListener('dblclick', () => {
            document.body.style.backgroundColor = '#333'; // Cambia el fondo a oscuro
            document.body.style.color = 'white';          // Cambia el texto a blanco
        });
 
        // EJEMPLO 3: Al reconocer el doble clic, la caja aumenta su tamaño con una transición suave
        const caja = document.getElementById('miCaja');
        caja.addEventListener('dblclick', () => {
            caja.style.transform = "scale(1.5)";
            caja.style.transition = "0.3s";
        });
 
        // EJEMPLO 4: Buscamos el elemento de la lista y lo ocultamos al recibir el evento
        const tarea = document.getElementById('miTarea');
        tarea.addEventListener('dblclick', () => {
            tarea.style.display = 'none'; // Oculta el elemento de la pantalla
        });
 
        // EJEMPLO 5: Cambiamos el contenido del texto y su color cuando se activa el doble clic
        const sobre = document.getElementById('sobreCerrado');
        sobre.addEventListener('dblclick', () => {
            sobre.textContent = "¡Ganaste un premio! 🎉";
            sobre.style.color = "gold";
 
        });
    </script>
</body>
</html>
