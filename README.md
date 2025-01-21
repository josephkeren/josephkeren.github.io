# josephkeren.github.io
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mariage de Keren & Joseph</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background: url('https://source.unsplash.com/1600x900/?wedding') no-repeat center center fixed;
            background-size: cover;
            color: white;
            margin: 0;
            padding: 0;
        }
        .container {
            padding: 50px;
            background: rgba(0, 0, 0, 0.6);
            border-radius: 10px;
            display: inline-block;
            margin-top: 50px;
        }
        h1, h2 {
            margin: 10px 0;
        }
        .countdown {
            font-size: 24px;
            margin-top: 20px;
        }
        .timer {
            display: flex;
            justify-content: center;
            gap: 20px;
            font-size: 24px;
            margin-top: 20px;
        }
        .timer div {
            background: rgba(255, 255, 255, 0.8);
            color: black;
            padding: 20px;
            border-radius: 10px;
            font-weight: bold;
        }
        .rsvp-form {
            margin-top: 20px;
        }
        input, button {
            padding: 10px;
            margin: 5px;
            border: none;
            border-radius: 5px;
        }
        button {
            background: #ff4081;
            color: white;
            cursor: pointer;
        }
        .map-container {
            margin-top: 30px;
        }
        .agenda-links {
            margin-top: 20px;
        }
        .agenda-links a {
            text-decoration: none;
            padding: 10px 20px;
            background: #d4c4aa;
            color: black;
            border-radius: 5px;
            margin: 10px;
            display: inline-block;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Bienvenue au Mariage de Keren & Joseph</h1>
        <h2>Le 18 Mai 2025</h2>
        <p>Rejoignez-nous pour célébrer notre union dans un cadre magnifique.</p>
        <div class="timer">
            <div><span id="days">00</span> Jour(s)</div>
            <div><span id="hours">00</span> Heure(s)</div>
            <div><span id="minutes">00</span> Minute(s)</div>
            <div><span id="seconds">00</span> Seconde(s)</div>
        </div>
        <div class="agenda-links">
            <a href="https://www.google.com/calendar/render?action=TEMPLATE&text=Mariage+de+Keren+%26+Joseph&dates=20250518T120000Z/20250518T180000Z&details=Rejoignez-nous+pour+notre+mariage+au+Hilton+Strasbourg&location=Hilton+Strasbourg" target="_blank">📅 Ajouter à Google Agenda</a>
            <a href="data:text/calendar;charset=utf8,BEGIN:VCALENDAR%0AVERSION:2.0%0ABEGIN:VEVENT%0ASUMMARY:Mariage%20de%20Keren%20%26%20Joseph%0ADESCRIPTION:Rejoignez-nous%20pour%20notre%20mariage%20au%20Hilton%20Strasbourg%0ADTSTART:20250518T120000Z%0ADTEND:20250518T180000Z%0ALOCATION:Hilton%20Strasbourg%0AEND:VEVENT%0AEND:VCALENDAR" download="mariage-keren-joseph.ics">📅 Ajouter à Apple Agenda</a>
        </div>
        <div class="map-container">
            <h3>Lieu de l'événement</h3>
            <p>Hilton Strasbourg</p>
            <iframe
                width="600"
                height="450"
                style="border:0"
                loading="lazy"
                allowfullscreen
                referrerpolicy="no-referrer-when-downgrade"
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2625.2614442477685!2d7.758353315674178!3d48.59750207926813!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4796c97e7bfb6e17%3A0x8f34c93e2d39dfb9!2sHilton%20Strasbourg!5e0!3m2!1sen!2sfr!4v1705854534685!5m2!1sen!2sfr">
            </iframe>
        </div>
    </div>
    
    <script>
        function updateCountdown() {
            const eventDate = new Date('2025-05-18T00:00:00').getTime();
            const now = new Date().getTime();
            const timeLeft = eventDate - now;
            
            const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
            const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);
            
            document.getElementById('days').innerText = days;
            document.getElementById('hours').innerText = hours;
            document.getElementById('minutes').innerText = minutes;
            document.getElementById('seconds').innerText = seconds;
        }
        setInterval(updateCountdown, 1000);
        updateCountdown();
    </script>
</body>
</html>
