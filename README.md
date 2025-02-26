<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Card</title>
    <style>
        .card {
            width: 300px;
            height: 150px;
            background-color: #3498db;
            color: white;
            text-align: center;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5em;
            border-radius: 10px;
            transition: background-color 0.3s ease;
            text-decoration: none;
        }

        .card:hover {
            background-color: #2ecc71; /* Change color on hover */
            cursor: pointer;
        }
    </style>
</head>
<body>
    <a href="https://your-link.com" class="card">Click Me</a>
</body>
</html>
