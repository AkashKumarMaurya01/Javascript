# Project 6

## Key checker code

```HTML
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>Event KeyCodes</title>

    <style>
        table,th,td {
            border: 1px solid #e7e7e7;
        }

        .project {
            background-color: #1c1c1c;
            color: #ffffff;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            height: 100vh;
        }

        .color {
            color: aliceblue;
            display: flex;
            flex-direction: row;
        }
    </style>
</head>

<body>

    <div class="project">
        <div id="insert">
            <div class="key">Press the key and watch magic</div>
        </div>
    </div>

    <script src="5_project.js"></script>
</body>

</html>
```

```JAVA SCRIPT

const insert = document.getElementById('insert')

window.addEventListener('keydown', (e) => {
    insert.innerHTML = `
     <div class="color">

    <table>
        <tr>
            <th>key</th>
            <th>keycode</th>
            <th>Code</th>
        </tr>
        <tr>
            <td>${e.key===' ' ? " Sapce ":e.key}</td>
            <td>${e.keyCode}</td>
            <td>${e.code}</td>
        </tr>
    
    </table>
     </div>
     `;
});

```