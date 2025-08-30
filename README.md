<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Povești și Poezii</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 800px;
            margin: auto;
            padding: 20px;
            background: #f0f0f0;
        }
        h1 { text-align: center; }
        .story {
            background: #fff;
            padding: 15px;
            margin: 15px 0;
            border-radius: 10px;
            box-shadow: 0 0 5px rgba(0,0,0,0.1);
        }
        textarea {
            width: 100%;
            height: 80px;
            margin-bottom: 10px;
        }
        button {
            padding: 10px 20px;
            background: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover { background: #45a049; }
    </style>
</head>
<body>
    <h1>Povești și Poezii</h1>

    <textarea id="title" placeholder="Titlul..."></textarea>
    <textarea id="content" placeholder="Scrie aici povestea sau poezia..."></textarea>
    <button onclick="addStory()">Adaugă</button>

    <div id="stories"></div>

    <script>
        function addStory() {
            const title = document.getElementById('title').value;
            const content = document.getElementById('content').value;
            if(title && content) {
                const storyDiv = document.createElement('div');
                storyDiv.classList.add('story');
                storyDiv.innerHTML = `<h2>${title}</h2><p>${content}</p>`;
                document.getElementById('stories').appendChild(storyDiv);
                document.getElementById('title').value = '';
                document.getElementById('content').value = '';
            } else {
                alert("Completează titlul și conținutul!");
            }
        }
    </script>
</body>
</html>
