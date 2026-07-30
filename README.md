<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container-registro">
    <h2>Hola</h2>
    <p>REGISTRATE PRIMERO</p>
  </div>

  <div class="registro">
    
    <form id="formRegistro">

        <label for="NOMBRE">Nombre (obligatorio):</label>
        <input type="text" id="NOMBRE" placeholder="Nombre completo" required>

        <label for="apellido">Apellido (obligatorio):</label>
        <input type="text" id="apellido" placeholder="Apellido completo" required>
   
        <label for="correo">correo (obligatorio):</label>
        <input type="email" id="correo" placeholder="ejemplo@correo.com" required>
   
        <label for="contraseña">Contraseña (obligatorio):</label>
        <input type="password" id="contraseña" placeholder="Contraseña" required>   

     <button type="submit" class="btn-registro">Registrarse</button>
    </form>
  </div>

<script>
    // Capturamos el evento de envío del formulario
    document.getElementById('formRegistro').addEventListener('submit', function(event) {
        // Evitamos que la página se recargue por defecto
        event.preventDefault();

        // HACER SOLO ESTA ACCIÓN SOLO SI: el navegador valida que los campos requeridos son válidos
        // El método checkValidity() verifica si todos los campos "required" están llenos y correctos
        if (this.checkValidity()) {
            // Acción: Redirigir a la página deseada
            window.location.href = 'https://rekiam18.github.io/index.html/';
        } else {
            // Si falta algún campo, el navegador mostrará sus avisos nativos automáticamente
            this.reportValidity();
        }
    });
</script>

</body>
</html>
