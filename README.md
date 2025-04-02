<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Line Scroll Reading</title>
    <style>
        #scrollArea {
            width: 100%;
            height: 50px;
            overflow: hidden;
            border: 1px solid #ccc;
            position: relative;
            font-family: Arial, sans-serif;
            font-size: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .line {
            position: absolute;
            animation: scroll 3s linear infinite;
            white-space: nowrap;
        }

        @keyframes scroll {
            0% {
                transform: translateY(100%);
            }
            50% {
                transform: translateY(0%);
            }
            100% {
                transform: translateY(-100%);
            }
        }
    </style>
</head>
<body>
    <div id="scrollArea"></div>

    <script>
        const lines = [
           "Hi,I'm Priyanshu Kumar👋"
        ];

        const scrollArea = document.getElementById("scrollArea");

        let currentLineIndex = 0;

        function showLine() {
            scrollArea.innerHTML = ""; // Clear previous line
            const line = document.createElement("div");
            line.className = "line";
            line.textContent = lines[currentLineIndex];
            scrollArea.appendChild(line);

            currentLineIndex = (currentLineIndex + 1) % lines.length; // Loop lines
        }

        setInterval(showLine, 3000); // Change line every 3 seconds
        showLine(); // Display the first line
    </script>
</body>
</html>

- 👋 Hi, I’m @priyanshu
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
priyanshu102005/priyanshu102005 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
