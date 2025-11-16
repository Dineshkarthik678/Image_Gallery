# Ex.08 Design of Interactive Image Gallery

## AIM
  To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS

## Step 1:

Clone the github repository and create Django admin interface

## Step 2:

Change settings.py file to allow request from all hosts.

## Step 3:

Use CSS for positioning and styling.

## Step 4:

Write JavaScript program for implementing interactivit

## Step 5:

Validate the HTML and CSS code

## Step 6:

Publish the website in the given URL.

## PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Interactive Car Gallery</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: #1f1f1f;
            font-family: Arial, sans-serif;
            color: white;
        }

        h1 {
            text-align: center;
            padding: 20px;
            color: #ffc107;
        }

        .gallery {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            padding: 20px;
        }

        .gallery img {
            width: 250px;
            height: 160px;
            object-fit: cover;
            border-radius: 10px;
            transition: transform 0.3s ease;
            cursor: pointer;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
        }

        .gallery img:hover {
            transform: scale(1.05);
        }

        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            z-index: 10;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0, 0, 0, 0.8);
        }

        .modal-content {
            display: block;
            margin: 80px auto;
            max-width: 80%;
            max-height: 80%;
            border-radius: 10px;
        }

        .close {
            position: absolute;
            top: 30px;
            right: 50px;
            font-size: 40px;
            font-weight: bold;
            color: white;
            cursor: pointer;
        }
    </style>
</head>
<body>

<h1>Car Collection Gallery</h1>

<div class="gallery">
    <img src="https://i.pinimg.com/736x/de/f7/e0/def7e0d39707b3887edbf52d85caafc2.jpg" alt="Car 1" onclick="openModal(this.src)">
    <img src="https://i.pinimg.com/736x/4a/fc/f0/4afcf04cbfb77a89d47fea5021f825f7.jpg" alt="Car 2" onclick="openModal(this.src)">
    <img src="https://i.pinimg.com/736x/88/33/90/88339085f62e09c5761be5bf5ac68ce5.jpg" alt="Car 3" onclick="openModal(this.src)">
    <img src="https://i.pinimg.com/736x/f6/4a/f8/f64af80a8d0595e47a1aadfb31c2be51.jpg" alt="Car 4" onclick="openModal(this.src)">
    <img src="https://i.pinimg.com/736x/b8/e5/ea/b8e5ea97fa015c4b7eff63c79de31314.jpg" alt="Car 5" onclick="openModal(this.src)">
</div>

<!-- Modal for enlarged image -->
<div id="imageModal" class="modal" onclick="closeModal()">
    <span class="close">&times;</span>
    <img class="modal-content" id="modalImg">
</div>

<script>
    function openModal(src) {
        const modal = document.getElementById("imageModal");
        const modalImg = document.getElementById("modalImg");
        modal.style.display = "block";
        modalImg.src = src;
    }

    function closeModal() {
        document.getElementById("imageModal").style.display = "none";
    }

    // Optional: ESC key to close modal
    document.addEventListener("keydown", function(e) {
        if (e.key === "Escape") {
            closeModal();
        }
    });
</script>

</body>
</html>
```


## OUTPUT
<img width="1472" height="873" alt="image" src="https://github.com/user-attachments/assets/96b7280c-220f-49e7-93a1-ba72404b5b1d" />


## RESULT
  The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
