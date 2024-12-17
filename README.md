# Date:16-11-2024
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
gallery.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MY GALLERY</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background-color: #e8eeef;
    }

    .gallery-container {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      padding: 20px;
      justify-content: center;
    }

    .gallery-item {
      width: 200px;
      height: 150px;
      overflow: hidden;
      cursor: pointer;
      border-radius: 8px;
      box-shadow: 0 4px 6px rgba(12, 215, 93, 0.1);
    }

    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.3s ease;
    }

    .gallery-item:hover img {
      transform: scale(1.1);
    }

    .lightbox {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      display: none;
      align-items: center;
      justify-content: center;
      z-index: 1000;
    }

    .lightbox-image {
      max-width: 90%;
      max-height: 90%;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(223, 123, 8, 0.252);
    }

    .close {
      position: absolute;
      top: 20px;
      right: 30px;
      font-size: 30px;
      color: #fff;
      cursor: pointer;
      z-index: 1001;
    }

    .close:hover {
      color: #ff6b6b;
    }
    .footer {
        text-align: center;
        margin-top:40%;
        background-color: bisque;
        color:black;
        font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
        font-size: 30px;
    }
  </style>
</head>
<body>
    <center>
  <div class="gallery-container">
    <div class="gallery-item">
      <img src="Screenshot (105).png" alt="Image 1">
    </div>
    <br>
    <div class="gallery-item">
      <img src="Screenshot (101).png" alt="Image 2">
    </div>
    <br>
    <div class="gallery-item">
      <img src="Screenshot (102).png" alt="Image 3">
    </div>
    <br>
    <div class="gallery-item">
        <img src="Screenshot (107).png" alt="Image 4">
    </div>
    <br>
    <div class="gallery-item">
        <img src="Screenshot (110).png" alt="Image 5">
    </div>
    <br>
    <div class="gallery-item">
        <img src="Screenshot (112).png" alt="Image 6">
    </div>
</center>
    <br>
    </div>
  <div class="lightbox">
    <span class="close">&times;</span>
    <img class="lightbox-image" src="" alt="Enlarged Image">
  </div>
  <div class="footer">
    <footer>
        designed by:Maha shree M
    </footer>
  </div>

  <script>
    document.addEventListener('DOMContentLoaded', () => {
      const galleryItems = document.querySelectorAll('.gallery-item img');
      const lightbox = document.querySelector('.lightbox');
      const lightboxImage = document.querySelector('.lightbox-image');
      const closeBtn = document.querySelector('.close');

      // Open lightbox on image click
      galleryItems.forEach(item => {
        item.addEventListener('click', () => {
          lightbox.style.display = 'flex';
          lightboxImage.src = item.src;
        });
      });

      // Close lightbox on close button click
      closeBtn.addEventListener('click', () => {
        lightbox.style.display = 'none';
        lightboxImage.src = '';
      });

      // Close lightbox on clicking outside the image
      lightbox.addEventListener('click', (e) => {
        if (e.target !== lightboxImage) {
          lightbox.style.display = 'none';
          lightboxImage.src = '';
        }
      });
    });
  </script>
</body>
</html>
```
# OUTPUT:
![Screenshot (122)](https://github.com/user-attachments/assets/c2316889-25b1-4fdc-ab1f-1b7467f28fc6)
![Screenshot (128)](https://github.com/user-attachments/assets/b80bc9a9-ab41-4cc2-8ec0-5260ca039166)
![Screenshot (127)](https://github.com/user-attachments/assets/9e96304b-7c9c-4536-9721-93d4c55a597f)
![Screenshot (126)](https://github.com/user-attachments/assets/b3b9a667-1494-46de-bffb-8488484a3d51)
![Screenshot (125)](https://github.com/user-attachments/assets/c388bb5e-76a6-447e-9bdd-6a2362ed2eda)
![Screenshot (123)](https://github.com/user-attachments/assets/37e4ff73-be05-4387-9b21-e954ca663add)
![Screenshot (124)](https://github.com/user-attachments/assets/159db2b1-caed-42f9-90b5-423e68b7c4ec)



# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
