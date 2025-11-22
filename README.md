# Ghost-Melo
<!DOCTYPE html>
<html>
<head>
    <title>Web, UI/UX, React Native Quiz</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>HTML, CSS, JS Quiz</h1>
    <div id="quiz-container">
        <p>1. Which tag is used to make a paragraph in HTML?</p>
        <ul>
            <li>A. &lt;para&gt;</li>
            <li>B. &lt;p&gt;</li>
            <li>C. &lt;pg&gt;</li>
            <li>D. &lt;text&gt;</li>
        </ul>
        <p class="answer">Answer: B</p>

        <p>2. Which tag is used to add a hyperlink?</p>
        <ul>
            <li>A. &lt;a&gt;</li>
            <li>B. &lt;link&gt;</li>
            <li>C. &lt;url&gt;</li>
            <li>D. &lt;href&gt;</li>
        </ul>
        <p class="answer">Answer: A</p>
        
        <!-- Add more questions in similar format -->
    </div>

    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 20px;
}

h1 {
    color: #0a9396;
}

ul {
    list-style-type: none;
}

.answer {
    color: green;
    font-weight: bold;
    margin-bottom: 20px;
}
document.querySelectorAll('.answer').forEach(ans => {
    ans.style.display = 'none';
});

document.querySelectorAll('#quiz-container p').forEach(question => {
    question.addEventListener('click', () => {
        let next = question.nextElementSibling;
        if (next && next.classList.contains('answer')) {
            next.style.display = next.style.display === 'none' ? 'block' : 'none';
        }
    });
});
