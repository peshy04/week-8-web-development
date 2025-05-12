# week-8-web-development

//HTML 5
//Each page uses html 5 for better accessibility and CEO

//HTML5
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home | My Website</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Welcome to My Website</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="about.html">About</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>
    <section>
        <div class="slider">
            <img src="image1.jpg" class="active">
            <img src="image2.jpg">
            <img src="image3.jpg">
        </div>
    </section>
    <script src="script.js"></script>
</body>
</html>


//CSS
//Ensures responsiveness and style

//CSSbody 
{
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    text-align: center;
}

header {
    background-color: #333;
    color: white;
    padding: 10px;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 15px;
}

nav ul li a {
    color: white;
    text-decoration: none;
}

.slider img {
    width: 100%;
    max-height: 300px;
    display: none;
}

.slider img.active {
    display: block;
}

//JS
//Ensures image slider and form validation


//js

document.addEventListener("DOMContentLoaded", function () {
    let images = document.querySelectorAll(".slider img");
    let index = 0;

    setInterval(() => {
        images.forEach(img => img.classList.remove("active"));
        index = (index + 1) % images.length;
        images[index].classList.add("active");
    }, 3000);
});
