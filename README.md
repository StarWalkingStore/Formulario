<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulario de Compra</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f3f3f3;
            margin: 0;
            padding: 0;
        }

        #formularioCompra {
            max-width: 600px;
            margin: 20px auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        label {
            display: block;
            margin-bottom: 8px;
        }

        input, select {
            width: 100%;
            padding: 10px;
            margin-bottom: 16px;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }

        button {
            background-color: #ff9900;
            color: #fff;
            border: none;
            padding: 12px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }

        button:hover {
            background-color: #e68a00;
        }
    </style>
</head>
<body>

<form id="formularioCompra" action="procesar_compra.php" method="post">
    <!-- Campos del formulario -->
    <label for="nombre">Nombre y Apellido:</label>
    <input type="text" id="nombre" name="nombre" required>

    <label for="correo">Correo:</label>
    <input type="email" id="correo" name="correo" required>

    <label for="telefono">Teléfono:</label>
    <input type="tel" id="telefono" name="telefono" required>

    <label for="direccion">Dirección:</label>
    <input type="text" id="direccion" name="direccion" required>

    <label for="referencia">Referencia:</label>
    <input type="text" id="referencia" name="referencia">

    <label for="departamento">Departamento:</label>
    <input type="text" id="departamento" name="departamento">

    <label for="distrito">Distrito:</label>
    <input type="text" id="distrito" name="distrito">

    <label for="producto">Nombre del Producto:</label>
    <input type="text" id="producto" name="producto" required>

    <label for="cantidad">Cantidad de Unidades:</label>
    <select id="cantidad" name="cantidad" required>
        <option value="1">1</option>
        <option value="2">2</option>
        <option value="3">3</option>
        <option value="4">4</option>
        <option value="5">5</option>
        <option value="6">6</option>
        <option value="7">7</option>
        <option value="8">8</option>
        <option value="9">9</option>
        <option value="10">10</option>
    </select>

    <!-- Botón Confirmar Compra -->
    <button type="button" onclick="validarYConfirmarCompra()">Confirmar Compra</button>
</form>

<script>
    function validarYConfirmarCompra() {
        // Validar campos antes de mostrar el mensaje de agradecimiento
        var nombre = document.getElementById("nombre").value;
        var correo = document.getElementById("correo").value;
        var telefono = document.getElementById("telefono").value;
        var direccion = document.getElementById("direccion").value;

        if (nombre === "" || correo === "" || telefono === "" || direccion === "") {
            alert("Por favor, completa todos los campos obligatorios.");
            return;
        }

        // Resto del código para confirmar la compra y enviar correo
        // ...

        // Muestra el mensaje de agradecimiento
        alert("¡Gracias por tu compra en Star Walking Store!");

        // Resto del código para redirigir o procesar la compra si es necesario
        // ...
    }
</script>

</body>
</html>
