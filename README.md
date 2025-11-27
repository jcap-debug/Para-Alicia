<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tarjeta Interactiva</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f0f0f0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .card {
            width: 320px;
            background: white;
            border-radius: 20px;
            padding: 20px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            text-align: center;
            animation: fadeIn 1.2s;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .image-box img {
            width: 100%;
            border-radius: 12px;
        }
        button {
            padding: 10px 15px;
            border: none;
            background: #4a6cf7;
            color: white;
            border-radius: 10px;
            cursor: pointer;
            margin-top: 15px;
        }
        #note {
            display: none;
            text-align: left;
            margin-top: 15px;
            background: #e8ecff;
            padding: 15px;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <div class="card">
        <h2>✨ Tu Tarjeta Interactiva ✨</h2>
        
        <div class="image-box">
            <!-- AQUI PON LA URL DE TU IMAGEN -->
            <img src="https://pixabay.com/es/photos/fondo-de-navidad-navidad-1869902/" alt="Imagen especial">
        </div>

        <button onclick="playAudio()">▶ Reproducir Audio</button>
        
        <!-- AQUI PON LA URL DE TU AUDIO -->
        <audio id="audio" src="https://youtu.be/EKkzbbLYPuI?si=_ds64SrsbmhPjVFJ"></audio>

        <button onclick="toggleNote()">📩 Abrir Nota</button>

        <div id="note">
            <!-- AQUI PON TU TEXTO PERSONALIZADO -->
            <p>Segundo detalle… ¿ya tienes sospechas? Tal vez soy alguien que te observa en silencio… o alguien que ni notas cuando pasa. 👀
Que hoy te vaya tan bien como este pequeño regalito espera alegrarte.".</p>
            
            <!-- AQUI PUEDES PONER TAMBIÉN UN VIDEO -->
            <!-- Ejemplo:
            <video width="100%" controls>
                <source src="AQUI_URL_DE_TU_VIDEO.mp4" type="video/mp4">
            </video>
            -->
        </div>
    </div>

    <script>
        function playAudio() {
            document.getElementById('audio').play();
        }

        function toggleNote() {
            const note = document.getElementById('note');
            note.style.display = note.style.display === 'none' ? 'block' : 'none';
        }
    </script>
</body>
</html>
