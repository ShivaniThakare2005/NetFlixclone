<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Netflix Clone</title>
<link rel="stylesheet" href="style.css">
</head>
<body>

<header>
    <nav>
        <h1 class="logo">NETFLIX</h1>
        <button class="sign-in">Sign In</button>
    </nav>

    <div class="hero">
        <h1>Unlimited movies, TV shows and more</h1>
        <h3>Watch anywhere. Cancel anytime.</h3>

        <p>
            Ready to watch? Enter your email to create
            or restart your membership.
        </p>

        <div class="email-box">
            <input type="email" placeholder="Email address">
            <button>Get Started</button>
        </div>
    </div>
</header>

<section class="features">

    <div class="feature">
        <div>
            <h2>Enjoy on your TV</h2>
            <p>
                Watch on Smart TVs, PlayStation,
                Xbox and more.
            </p>
        </div>
    </div>

    <div class="feature">
        <div>
            <h2>Download shows</h2>
            <p>
                Save your favourites easily.
            </p>
        </div>
    </div>

    <div class="feature">
        <div>
            <h2>Watch Everywhere</h2>
            <p>
                Stream on phone, tablet and laptop.
            </p>
        </div>
    </div>

</section>

<section class="faq">

    <h2>Frequently Asked Questions</h2>

    <div class="faq-item">
        <button class="question">
            What is Netflix?
        </button>

        <div class="answer">
            Netflix is a streaming service.
        </div>
    </div>

    <div class="faq-item">
        <button class="question">
            How much does Netflix cost?
        </button>

        <div class="answer">
            Plans vary depending on region.
        </div>
    </div>

</section>

<script src="script.js"></script>

</body>
</html>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,sans-serif;
}

body{
    background:black;
    color:white;
}

header{
    height:100vh;
    background:
    linear-gradient(
    rgba(0,0,0,.7),
    rgba(0,0,0,.7)),
    url("https://images.unsplash.com/photo-1489599849927-2ee91cede3ba");
    background-size:cover;
    background-position:center;
}

nav{
    display:flex;
    justify-content:space-between;
    padding:20px 50px;
}

.logo{
    color:red;
    font-size:40px;
}

.sign-in{
    background:red;
    color:white;
    border:none;
    padding:10px 20px;
    cursor:pointer;
}

.hero{
    text-align:center;
    margin-top:180px;
}

.hero h1{
    font-size:55px;
    margin-bottom:20px;
}

.hero h3{
    margin-bottom:20px;
}

.hero p{
    margin-bottom:20px;
}

.email-box{
    display:flex;
    justify-content:center;
    gap:10px;
}

.email-box input{
    width:300px;
    padding:15px;
}

.email-box button{
    background:red;
    color:white;
    border:none;
    padding:15px 20px;
}

.features{
    padding:60px;
}

.feature{
    border-top:8px solid #222;
    padding:50px 0;
}

.faq{
    padding:50px;
}

.faq h2{
    text-align:center;
    margin-bottom:30px;
}

.question{
    width:100%;
    text-align:left;
    background:#333;
    color:white;
    border:none;
    padding:20px;
    font-size:20px;
    cursor:pointer;
}

.answer{
    display:none;
    background:#444;
    padding:20px;
}const questions =
document.querySelectorAll(".question");

questions.forEach(question => {

    question.addEventListener("click", () => {

        const answer =
        question.nextElementSibling;

        if(answer.style.display === "block"){
            answer.style.display = "none";
        }
        else{
            answer.style.display = "block";
        }
    });

});
