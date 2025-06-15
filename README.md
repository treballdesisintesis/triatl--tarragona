<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Triatló Tarragona 2025</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; padding: 0; background-color: #f4f4f4; }
    header { background: #0077b6; color: white; padding: 20px 0; text-align: center; }
    main { padding: 30px; max-width: 800px; margin: auto; background: white; border-radius: 8px; }
    h1, h2 { color: #023e8a; }
    form { display: flex; flex-direction: column; gap: 15px; margin-top: 20px; }
    label { font-weight: bold; }
    input, select { padding: 10px; border: 1px solid #ccc; border-radius: 4px; }
    button { background: #0077b6; color: white; padding: 12px; border: none; border-radius: 4px; cursor: pointer; }
    button:hover { background: #023e8a; }
    .section { margin-top: 30px; }
    #countdown { font-size: 1.5em; color: #d00000; font-weight: bold; }
    iframe { width: 100%; height: 300px; border: 0; margin-top: 20px; border-radius: 8px; }
  </style>
</head>
<body>
  <header>
    <h1>Triatló Tarragona 2025</h1>
    <p>¡Inscríbete ahora al triatlón más emocionante de la Costa Daurada!</p>
    <div id="countdown"></div>
  </header>
  <main>
    <section class="section">
      <h2>📅 Fecha del Evento</h2>
      <p>Domingo, 12 de octubre de 2025</p>
    </section>

    <section class="section">
      <h2>🗺️ Recorrido</h2>
      <ul>
        <li><strong>Nado:</strong> 1.5 km en la Playa del Miracle</li>
        <li><strong>Bicicleta:</strong> 40 km por Via Augusta, Passeig Marítim y Camí del Llorito</li>
        <li><strong>Carrera a pie:</strong> 10 km por Rambla Nova y Parc Francolí</li>
      </ul>
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2993.010313283397!2d1.2477494157007975!3d41.11714461890209!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x12a151c8fc3c2157%3A0x24a2c4bcbd601041!2sPlatja%20del%20Miracle!5e0!3m2!1ses!2ses!4v1621524098735!5m2!1ses!2ses" allowfullscreen="" loading="lazy"></iframe>
    </section>

    <section class="section">
      <h2>💸 Precio de Inscripción</h2>
      <p>Inscripción general: 60€<br> Federados: 50€</p>
    </section>

    <section class="section">
      <h2>✉️ Formulario de Inscripción</h2>
      <form>
        <label for="nombre">Nombre completo:</label>
        <input type="text" id="nombre" name="nombre" required>

        <label for="email">Correo electrónico:</label>
        <input type="email" id="email" name="email" required>

        <label for="telefono">Teléfono de contacto:</label>
        <input type="tel" id="telefono" name="telefono" required>

        <label for="federado">¿Estás federado?</label>
        <select id="federado" name="federado">
          <option value="si">Sí</option>
          <option value="no">No</option>
        </select>

        <button type="submit">Enviar inscripción</button>
      </form>
    </section>

    <section class="section">
      <h2>💳 Pago Seguro</h2>
      <p>Próximamente podrás pagar con tarjeta de crédito o Bizum mediante nuestra pasarela de pago segura.</p>
    </section>
  </main>

  <script>
    const eventDate = new Date("2025-10-12T09:00:00").getTime();
    const countdown = document.getElementById("countdown");

    const interval = setInterval(() => {
      const now = new Date().getTime();
      const distance = eventDate - now;

      const days = Math.floor(distance / (1000 * 60 * 60 * 24));
      const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((distance % (1000 * 60)) / 1000);

      countdown.innerHTML = `Faltan ${days}d ${hours}h ${minutes}m ${seconds}s`;

      if (distance < 0) {
        clearInterval(interval);
        countdown.innerHTML = "¡El evento ha comenzado!";
      }
    }, 1000);
  </script>
</body>
</html>
