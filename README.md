# Arelyy
Detalle pequeño para alguien importante 
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Mensaje</title>
  <style>
    body {
      background-color: black;
      color: white;
      font-family: 'Courier New', monospace;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-size: 2em;
    }
    #mensaje::after {
      content: '|';
      animation: blink 0.7s infinite;
    }
    @keyframes blink {
      0%, 100% { opacity: 1; }
      50% { opacity: 0; }
    }
  </style>
</head>
<body>

  <div id="mensaje"></div>

  <script>
    const texto = "Te quiero Arely ❤️";
    let i = 0;
    const velocidad = 100;

    function escribir() {
      if (i < texto.length) {
        document.getElementById("mensaje").innerHTML += texto.charAt(i);
        i++;
        setTimeout(escribir, velocidad);
      }
    }

    escribir();
  </script>

</body>
</html>
