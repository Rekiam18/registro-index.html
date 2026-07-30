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
body,html{
background-image: url("images.jpg");
}
h2{
    color: white;
    text-align: center;
}
p{
    color: white;
    text-align: center;
}
.contenedor-registro{ 
    background-color:blueviolet;
    max-width: 500px; 
    margin: 50px auto;
    padding: 30px;
    border-radius: 15px;
box-shadow: 0px 6px 15px rgba(16, 182, 233, 0.1);
font-family: Arial, sans-serif;
}
.contenedor-registro h2{
    color:aquamarine;
    margin-bottom: 20px;
    text-align: center;
}

.contenedor-registro p{
    color: white;
    font-size: 16px;
    text-align: center;
    margin-bottom: 20px;
}

label{ 
    display: block;
    color:aquamarine;
    font-size: 20px;
    font-weight: bold;
    margin-bottom: 5px;

}

input{
    width: 50%;
    padding: 15px;
    margin-bottom: 10px;
    border:1px solid purple;
border-radius: 50px;
font-size: 14px;
box-sizing: border-box;
transition:border-color 0.3s ease;
}

input:focus{
    border-color: aquamarine;
    outline: none;
}

.btn-registro{
    width: 50%;
    background-color: aquamarine;
    color: purple;
    padding: 10px;
    border: none;   
    border-radius: 50px;
    cursor: pointer;
    font-size: 16px;
    font-weight: bold;
    transition: background-color 0.3s ease;
}

.btn-registro:hover{
    background-color: purple;
    color: aquamarine;
}
.registro{
    text-align: center;
    box-shadow: inset 0px 50px 50px white;
    width: 50%;
    margin: 0 auto;

}
