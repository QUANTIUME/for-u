# for-u
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Would You Be Mine?</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            height: 100vh;
            background-color: pink;
            font-family: Arial, sans-serif;
        }
        #container {
            text-align: center;
        }
        .button {
            padding: 10px 20px;
            font-size: 18px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: 0.3s;
            font-weight: bold;
        }
        #yes-button {
            background-color: green;
            color: white;
        }
        #no-button {
            background-color: red;
            color: white;
            position: absolute;
        }
        #creature {
            font-size: 24px;
            display: none;
            margin-top: 20px;
        }
        #sloth {
            display: none;
            text-align: center;
        }
        #sloth img {
            width: 200px;
        }
    </style>
</head>
<body>
    <div id="container">
        <h1>Would you be mine and only mine?</h1>
        <button id="yes-button" class="button">YES</button>
        <button id="no-button" class="button">NO</button>
        <div id="creature">
            <span>💖</span> I love you... <span>💖</span>
        </div>
        <div id="sloth">
            <img src="https://media.tenor.com/images/0e3ea05f392364df74869cf9ed6c49e5/tenor.gif" alt="Sloth">
            <p>Thank you, love. I love you sooooo much! 💌</p>
        </div>
    </div>

    <script>
        const yesButton = document.getElementById('yes-button');
        const noButton = document.getElementById('no-button');
        const creature = document.getElementById('creature');
        const sloth = document.getElementById('sloth');

        noButton.addEventListener('mouseover', () => {
            const maxX = window.innerWidth - noButton.offsetWidth;
            const maxY = window.innerHeight - noButton.offsetHeight;
            const randomX = Math.random() * maxX;
            const randomY = Math.random() * maxY;
            noButton.style.transform = `translate(${randomX}px, ${randomY}px)`;
        });

        yesButton.addEventListener('click', () => {
            noButton.style.display = 'none';
            yesButton.style.width = '50%';
            yesButton.style.height = '10%';
            creature.style.display = 'block';
            setTimeout(() => {
                creature.style.display = 'none';
                sloth.style.display = 'block';
            }, 2000);
        });
    </script>
</body>
</html>
