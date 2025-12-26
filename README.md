# Ex.07 Design of Interactive Image Gallery
## Date:26-12-2025

## AIM:
To design a web application for an inteactive image gallery for a minimum five images with next and previous buttons.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM:
```
gallery.html

<html>
<head>
<title>Anime Image Gallery</title>
<link rel="stylesheet" href="style.css">
</head>
<body>

<header>Anime Gallery</header>

<div class="container">
    <div class="gallery-box">
        <img id="galleryImage" src="img1.webp" alt="Anime Image">
        <p class="caption" id="caption">Shokudaikiri Mitsutada</p>

        <div class="buttons">
            <button onclick="prev()">Previous</button>
            <button onclick="next()">Next</button>
        </div>
    </div>
</div>

<footer>
Designed & Developed by Sanjay Babu M &copy; 2025
</footer>

<script>
let gallery = [
    "img1.webp",
    "img2.jpg",
    "img3.jpg",
    "img4.jpg",
    "img5.webp"
    
];

let captions = [
    "Shokudaikiri mitsutada",
    "Yato",
    "Aoba seragaki",
    "Madara uchiha",
    "Monkey D.luffy"
];

let index = 0;

function next(){
    index++;
    if(index >= gallery.length){
        index = 0;
    }
    document.getElementById("galleryImage").src = gallery[index];
    document.getElementById("caption").innerText = captions[index];
}

function prev(){
    index--;
    if(index < 0){
        index = gallery.length - 1;
    }
    document.getElementById("galleryImage").src = gallery[index];
    document.getElementById("caption").innerText = captions[index];
}
</script>

</body>
</html>

style.css

body{
    margin:0;
    background: linear-gradient(rgb(255, 0, 0),rgb(0, 0, 0),rgb(255, 0, 0));
    display:flex;
    flex-direction:column;
    min-height:100vh;
}

header{
    background-color: rgb(11, 228, 235);
    color:rgb(255, 0, 0);
    text-align:center;
    padding:15px;
    font-size:22px;
}

.container{
    flex:1;
    display:flex;
    justify-content:center;
    align-items:center;
}

.gallery-box{
    background-image: rgb(0, 0, 0);
    width:420px;
    padding:20px;
    border-radius:10px;
    box-shadow:0 5px 15px rgba(255, 0, 0, 0.15);
    text-align:center;
}

.gallery-box img{
    width:100%;
    height:260px;
    object-fit:contain;
    background-color:rgb(0, 0, 0);
    border-radius:8px;
}

.caption{
    margin-top:12px;
    font-size:16px;
    color:#10d8df;
}

.buttons{
    margin-top:15px;
    display:flex;
    justify-content:space-between;
}

.buttons button{
    padding:8px 18px;
    background-color:#0cbad8;
    color:rgb(0, 0, 0);
    border:none;
    border-radius:6px;
    font-size:14px;
    cursor:pointer;
}

.buttons button:hover{
    background: linear-gradient(rgb(255, 0, 0),rgb(0, 0, 0));
}

footer{
    text-align:center;
    padding:10px;
    font-size:13px;
    color:rgb(0, 0, 0);
}
```
## OUTPUT:
![alt text](<Screenshot (31)-1.png>)
![alt text](<Screenshot (32).png>)
![alt text](<Screenshot (33).png>)
![alt text](<Screenshot (34).png>)
![alt text](<Screenshot (35).png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
