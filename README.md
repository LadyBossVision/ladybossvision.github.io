<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Lady Boss Vision - Empowering creatives and entrepreneurs">
  <title>Lady Boss Vision</title>
  <link rel="stylesheet" href="style.css">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>

  <!-- Header with Logo and Navigation -->
  <header>
    <div class="logo">
      <img src="path/to/your-logo.png" alt="Lady Boss Vision Logo">
    </div>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Shop</a></li>
        <li><a href="#">Contact</a></li>
        <li><a href="#">Upload</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero Section with Video -->
  <section class="hero">
    <div class="hero-content">
      <h1>Welcome to Lady Boss Vision</h1>
      <p>Empowering creatives and entrepreneurs.</p>
      <video width="100%" controls>
        <source src="path/to/video.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </div>
  </section>

  <!-- Social Media Links -->
  <section class="social-media">
    <h2>Connect with Us</h2>
    <div class="social-links">
      <a href="https://www.instagram.com/kjparis" target="_blank"><i class="fab fa-instagram"></i></a>
      <a href="https://twitter.com/kjparis" target="_blank"><i class="fab fa-twitter"></i></a>
      <a href="https://facebook.com/kjparis" target="_blank"><i class="fab fa-facebook"></i></a>
      <a href="https://www.exclusiveenergyclothing.com" target="_blank"><i class="fas fa-store"></i></a>
    </div>
  </section>

  <!-- File Upload Section -->
  <section class="file-upload">
    <h2>Submit Your Work</h2>
    <form id="uploadForm" enctype="multipart/form-data">
      <label for="fileInput">Upload your creative project:</label>
      <input type="file" id="fileInput" name="fileInput" accept="image/*,video/*">
      <button type="submit">Upload</button>
    </form>
    <p id="uploadStatus"></p>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2024 Lady Boss Vision. All Rights Reserved.</p>
    <div class="social-links">
      <a href="https://www.instagram.com/kjparis" target="_blank"><i class="fab fa-instagram"></i></a>
      <a href="https://twitter.com/kjparis" target="_blank"><i class="fab fa-twitter"></i></a>
      <a href="https://facebook.com/kjparis" target="_blank"><i class="fab fa-facebook"></i></a>
      <a href="https://www.exclusiveenergyclothing.com" target="_blank"><i class="fas fa-store"></i></a>
    </div>
  </footer>

  <script src="script.js"></script>
</body>
</html>

/* General Styles */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #fff;
  color: #333;
}

/* Header */
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: #f4f4f4;
}

.logo img {
  width: 150px;
}

nav ul {
  list-style: none;
  display: flex;
  gap: 20px;
}

nav ul li a {
  text-decoration: none;
  color: #333;
  font-size: 18px;
}

nav ul li a:hover {
  color: #ff0000;
}

/* Hero Section */
.hero {
  text-align: center;
  padding: 60px 20px;
  background-color: #f8f8f8;
  color: #333;
}

.hero-content h1 {
  font-size: 48px;
  margin-bottom: 10px;
  color: #000;
}

.hero-content p {
  font-size: 24px;
  margin-bottom: 20px;
}

.hero-content video {
  border: 2px solid #ff0000;
  border-radius: 10px;
}

/* Social Media Section */
.social-media {
  text-align: center;
  padding: 40px;
  background-color: #eaeaea;
}

.social-media h2 {
  font-size: 32px;
  margin-bottom: 20px;
  color: #000;
}

.social-links a {
  font-size: 32px;
  margin: 0 10px;
  color: #333;
  text-decoration: none;
}

.social-links a:hover {
  color: #ff0000;
}

/* File Upload Section */
.file-upload {
  text-align: center;
  padding: 40px;
  background-color: #f4f4f4;
}

.file-upload form {
  display: inline-block;
  margin: 20px auto;
}

#fileInput {
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

button {
  padding: 10px 20px;
  background-color: #ff0000;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #cc0000;
}

#uploadStatus {
  margin-top: 20px;
  color: #333;
}

/* Footer */
footer {
  text-align: center;
  padding: 20px;
  background-color: #333;
  color: #fff;
}

footer .social-links a {
  color: #fff;
}

footer .social-links a:hover {
  color: #ff0000;
}

document.getElementById('uploadForm').addEventListener('submit', function(e) {
  e.preventDefault();
  
  var fileInput = document.getElementById('fileInput');
  var status = document.getElementById('uploadStatus');

  if (fileInput.files.length > 0) {
    status.innerHTML = 'File uploaded successfully!';
    status.style.color = 'green';
  } else {
    status.innerHTML = 'Please select a file to upload.';
    status.style.color = 'red';
  }
});
