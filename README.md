<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Te Amo</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      overflow: hidden;
      background: linear-gradient(to right, #ffe6e6, #fff);
      font-family: 'Arial', sans-serif;
      position: relative;
      height: 100vh;
      width: 100vw;
    }

    header {
      position: fixed;
      top: 0;
      width: 100%;
      background-color: #ff4d4d;
      color: white;
      text-align: center;
      padding: 20px;
      font-size: 24px;
      z-index: 1000;
    }

    .message {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 24px;
      color: #ff4d4d;
      opacity: 0;
      animation: fadeIn 1s forwards;
      text-align: center;
      padding: 20px;
      background-color: rgba(255, 255, 255, 0.8);
      border-radius: 10px;
      z-index: 999;
    }

    @keyframes fadeIn {
      to {
        opacity: 1;
      }
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: #ff4d4d;
      transform: rotate(45deg);
      animation: float 5s linear infinite;
      z-index: 0;
    }

    .heart::before,
    .heart::after {
      content: "";
      position: absolute;
      width: 20px;
      height: 20px;
      background-color: #ff4d4d;
      border-radius: 50%;
    }

    .heart::before {
      top: -10px;
      left: 0;
    }

    .heart::after {
      top: 0;
      left: -10px;
    }

    @keyframes float {
      0% {
        transform: translateY(0) rotate(45deg);
        opacity: 1;
      }
      100% {
        transform: translateY(-100vh) rotate(45deg);
        opacity: 0;
      }
    }

    .crif {
      position: fixed;
      bottom: 10px;
      left: 50%;
      transform: translateX(-50%);
      font-size: 32px;
      color: #ff4d4d;
      font-weight: bold;
      z-index: 1000;
    }
  </style>
</head>
<body>
  <header> 50 razones del por que Te Amo</header>
  <div class="crif">C R I S MY LOVE MON AMOUR</div>
  <script>
    const messages = [
      "Porque me aceptas tal y como soy.",
      "Porque me haces sentir especial.",
      "Por hacerme feliz cada día.",
      "Porque tienes la sonrisa más bonita.",
      "Porque me comprendes.",
      "Porque siempre me haces reír.",
      "Porque me proteges.",
      "Porque te unes a mis locuras.",
      "Porque recuerdas hasta las cosas pequeñas que te digo.",
      "Porque un abrazo tuyo mejora mi día.",
      "Porque me quieres tal y como soy.",
      "Porque todos los días aprendo algo nuevo contigo.",
      "Porque me haces sonreír.",
      "Porque soy una mejor persona cuando estoy contigo.",
      "Porque te encontré cuando no buscaba nada.",
      "Porque me escuchas.",
      "Porque siempre estás ahí para mí aunque estés peor que yo.",
      "Porque eres increíble.",
      "Porque me enamoré hasta de tus defectos.",
      "Porque eres lo mejor del mundo.",
      "Porque estás conmigo.",
      "Porque me dices cosas tan lindas.",
      "Porque te preocupas por mí.",
      "Porque me haces sentir amado.",
      "Porque me inspiras a ser mejor.",
      "Porque compartes tus sueños conmigo.",
      "Porque confías en mí.",
      "Porque me haces sentir seguro.",
      "Porque me das paz.",
      "Porque me haces sentir vivo.",
      "Porque me haces ver la vida de otra manera.",
      "Porque me haces sentir que todo es posible.",
      "Porque me haces sentir único.",
      "Porque me haces sentir que soy suficiente.",
      "Porque me haces sentir que pertenezco.",
      "Porque me haces sentir que tengo un hogar en ti.",
      "Porque me haces sentir que soy importante.",
      "Porque me haces sentir que soy amado.",
      "Porque me haces sentir que soy deseado.",
      "Porque me haces sentir que soy necesario.",
      "Porque me haces sentir que soy especial.",
      "Porque me haces sentir que soy tu todo.",
      "Porque me haces sentir que soy tu mundo.",
      "Porque me haces sentir que soy tu amor.",
      "Porque me haces sentir que soy tu vida.",
      "Porque me haces sentir que soy tu felicidad.",
      "Porque me haces sentir que soy tu razón de ser.",
      "Porque me haces sentir que soy tu destino.",
      "Porque me haces sentir que soy tu futuro.",
      "Porque me haces sentir que soy tu eternidad."
    ];

    let index = 0;

    document.body.addEventListener('click', () => {
      if (index < messages.length) {
        const msg = document.createElement('div');
        msg.classList.add('message');
        msg.textContent = messages[index];
        document.body.appendChild(msg);
        setTimeout(() => {
          msg.remove();
        }, 3000);
        index++;
      }

      // Crear corazón que cae
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.style.left = Math.random() * window.innerWidth + 'px';
      heart.style.top = window.innerHeight + 'px';
      document.body.appendChild(heart);
      setTimeout(() => {
        heart.remove();
      }, 5000);
    });
  </script>
</body>
</html>


