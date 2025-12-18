# Ex.07 Design of Interactive Image Gallery
## Date: 18.12.2025

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
<title>Car Image Gallery</title>
<link rel="stylesheet" href="style.css">
</head>
<body>

<header>Cars Gallery</header>

<div class="container">
    <div class="gallery-box">
        <img id="galleryImage" src="img1.jpg" alt="Car Image">
        <p class="caption" id="caption">Mercedes Mayback</p>

        <div class="buttons">
            <button onclick="prev()">Previous</button>
            <button onclick="next()">Next</button>
        </div>
    </div>
</div>

<footer>
Designed & Developed by Harikrishnan P &copy; 2025
</footer>

<script>
let gallery = [
    "img1.jpg",
    "img2.jpg",
    "img3.jpg",
    "img4.jpg",
    "img5.jpg"
];

let captions = [
    "Mercedes Mayback",
    "Bentley Continental GT",
    "Ferrari",
    "Rolls Royce Phantom",
    "BMW"
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
    font-family: Arial, sans-serif;
    background: linear-gradient(black,silver,black);
    display:flex;
    flex-direction:column;
    min-height:100vh;
}

header{
    background-color: gray;
    color:black;
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
    background-image: white;
    width:420px;
    padding:20px;
    border-radius:10px;
    box-shadow:0 5px 15px rgba(0,0,0,0.15);
    text-align:center;
}

.gallery-box img{
    width:100%;
    height:260px;
    object-fit:contain;
    background-color:silver;
    border-radius:8px;
}

.caption{
    margin-top:12px;
    font-size:16px;
    color:#1f2933;
}

.buttons{
    margin-top:15px;
    display:flex;
    justify-content:space-between;
}

.buttons button{
    padding:8px 18px;
    background-color:#6b7280;
    color:white;
    border:none;
    border-radius:6px;
    font-size:14px;
    cursor:pointer;
}

.buttons button:hover{
    background: linear-gradient(black,silver);
}

footer{
    text-align:center;
    padding:10px;
    font-size:13px;
    color:skyblue;
}

```
## OUTPUT:

![alt text](<Screenshot (45).png>)
![alt text](<Screenshot (46).png>)
![alt text](<Screenshot (47).png>)
![alt text](<Screenshot (48).png>)
![alt text](<Screenshot (49).png>)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
