# Ex.08 Design of Interactive Image Gallery
# Date: 13/12/2025
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
                              
  <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cosmic Wonders Gallery</title>
  <style>
    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      background-color: #0b0d17; /* Deep space dark */
      color: #e0e0e0;
    }

    header {
      padding: 40px 20px;
      text-align: center;
      background: linear-gradient(to bottom, #1a1c2c, #0b0d17);
    }

    h1 {
      margin: 0;
      font-family: 'Orbitron', sans-serif; /* A space-like font feel */
      text-transform: uppercase;
      letter-spacing: 4px;
      color: #4cc9f0;
      background-color: rgba(255, 255, 255, 0.05);
      display: inline-block;
      padding: 10px 20px;
      border-radius: 4px;
    }

    h2 {
      font-size: 1rem;
      font-weight: 300;
      color: #7209b7;
      margin-top: 10px;
    }

    .gallery-container {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      padding: 40px;
      justify-content: center;
      max-width: 1200px;
      margin: 0 auto;
    }

    .gallery-item {
      width: 280px;
      height: 200px;
      overflow: hidden;
      cursor: pointer;
      border-radius: 12px;
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.5);
      border: 1px solid rgba(255, 255, 255, 0.1);
      transition: all 0.3s ease;
    }

    .gallery-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.5s ease;
    }

    .gallery-item:hover {
      border-color: #4cc9f0;
      box-shadow: 0 0 20px rgba(76, 201, 240, 0.4);
    }

    .gallery-item:hover img {
      transform: scale(1.1);
    }

    /* Lightbox Styles */
    .lightbox {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.95);
      display: none;
      align-items: center;
      justify-content: center;
      z-index: 1000;
    }

    .lightbox-image {
      max-width: 85%;
      max-height: 85%;
      border-radius: 4px;
      box-shadow: 0 0 30px rgba(255, 255, 255, 0.1);
    }

    .close {
      position: absolute;
      top: 30px;
      right: 40px;
      font-size: 50px;
      color: #fff;
      cursor: pointer;
      line-height: 1;
    }

    .close:hover {
      color: #4cc9f0;
    }

    footer {
      text-align: center;
      padding: 40px;
      font-size: 0.9rem;
      opacity: 0.6;
    }
  </style>
</head>
<body>

  <header>
    <h1>Cosmic Wonders</h1>
    <h2></h2>
  </header>

  <div class="gallery-container">
    <div class="gallery-item">
    </div>
    <div class="gallery-item">
      <img src="https://images.unsplash.com/photo-1446776811953-b23d57bd21aa?auto=format&fit=crop&w=500" alt="Satellite View">
    </div>
    <div class="gallery-item">
      <img src="https://images.unsplash.com/photo-1614730321146-b6fa6a46bcb4?auto=format&fit=crop&w=500" alt="Earth">
    </div>
    <div class="gallery-item">
      <img src="https://images.unsplash.com/photo-1462331940025-496dfbfc7564?auto=format&fit=crop&w=500" alt="Nebula">
    </div>
    <div class="gallery-item">
    
    </div>
    <div class="gallery-item">
      <img src="https://images.unsplash.com/photo-1451187580459-43490279c0fa?auto=format&fit=crop&w=500" alt="Deep Space">
    </div>
  </div>

  <div class="lightbox">
    <span class="close">&times;</span>
    <img class="lightbox-image" src="" alt="Enlarged Image">
  </div>

  <footer>
    &copy; Sairam K
  </footer>

  <script>
    document.addEventListener('DOMContentLoaded', () => {
      const galleryItems = document.querySelectorAll('.gallery-item img');
      const lightbox = document.querySelector('.lightbox');
      const lightboxImage = document.querySelector('.lightbox-image');
      const closeBtn = document.querySelector('.close');

      galleryItems.forEach(item => {
        item.addEventListener('click', () => {
          lightbox.style.display = 'flex';
          lightboxImage.src = item.src;
          document.body.style.overflow = 'hidden'; 
        });
      });

      const closeLightbox = () => {
        lightbox.style.display = 'none';
        lightboxImage.src = '';
        document.body.style.overflow = 'auto'; // Re-enable scrolling
      };

      closeBtn.addEventListener('click', closeLightbox);

      lightbox.addEventListener('click', (e) => {
        if (e.target !== lightboxImage) {
          closeLightbox();
        }
      });
    });
  </script>
</body>
</html>```


# OUTPUT:
<img width="1280" height="707" alt="image" src="https://github.com/user-attachments/assets/2663c15e-70c3-4b07-866e-1aab34281f6f" />


<img width="1280" height="699" alt="image" src="https://github.com/user-attachments/assets/e40ee093-eae3-4ceb-9412-bf2c91d6bed3" />











# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
