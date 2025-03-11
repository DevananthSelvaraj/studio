<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Thiru Studio</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }

        /* Navigation Bar */
        nav {
            background-color: #333;
            color: white;
            padding: 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 1rem;
        }

        nav a:hover {
            text-decoration: underline;
        }

        /* Hero Section */
        .hero {
            background: url('./4.jpg') no-repeat center center/cover;
            height: 400px;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        .hero h1 {
            font-size: 3rem;
            margin: 0;
        }

        /* Welcome Section */
        .welcome {
            padding: 2rem;
            text-align: center;
        }

        /* Services Section */
        .services {
            padding: 2rem;
            background-color: #f4f4f4;
        }

        .service-card {
            border: 1px solid #ddd;
            padding: 1rem;
            margin: 1rem 0;
            text-align: center;
        }

        /* Gallery Section */
        .gallery {
            padding: 2rem;
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
        }

        .gallery img {
            width: 200px;
            height: 150px;
            object-fit: cover;
            cursor: pointer;
        }

        #lightbox {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            display: none;
            justify-content: center;
            align-items: center;
        }

        #lightbox img {
            max-width: 90%;
            max-height: 90%;
        }

        /* Staff Section */
        .staff-section {
            padding: 2rem;
            background-color: #f9f9f9;
            text-align: center;
        }

        .staff-grid {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
        }

        .staff-card {
            border: 1px solid #ddd;
            padding: 1rem;
            border-radius: 8px;
            width: 200px;
            text-align: center;
        }

        .staff-card img {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            object-fit: cover;
        }

        /* Footer */
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1rem;
            margin-top: 2rem;
        }
    </style>
</head>
<body>
    <!-- Navigation Bar -->
    <nav>
        <h2>Thiru Studio</h2>
        <div>
            <a href="#">Home</a>
            <a href="#services">Services</a>
            <a href="#gallery">Gallery</a>
            <a href="#team">Team</a>
        </div>
    </nav>

    <!-- Hero Section -->
    <div class="hero">
        <h1>Welcome to Thiru Studio</h1>
    </div>

    <!-- Welcome Section -->
    <section class="welcome">
        <h2>About Us</h2>
        <p>Thiru Studio is dedicated to capturing your precious moments and turning them into timeless memories. With a skilled team and state-of-the-art equipment, we offer photography and videography services tailored to your needs.</p>
    </section>

    <!-- Services Section -->
    <section id="services" class="services">
        <h2>Our Services</h2>
        <div class="service-card">
            <h3>Wedding Photography</h3>
            <p>Capture the joy and emotions of your special day with our wedding photography packages.</p>
        </div>
        <div class="service-card">
            <h3>Portrait Photography</h3>
            <p>Create stunning portraits that tell your story.</p>
        </div>
        <div class="service-card">
            <h3>Event Coverage</h3>
            <p>From birthdays to corporate events, we cover it all with style.</p>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="gallery" class="gallery">
        <h2>Gallery</h2>
        <img src="4.webp" alt="Gallery Image">
        <img src="5.webp" alt="Gallery Image">
        <img src="6.webp" alt="Gallery Image">
        <img src="7.webp" alt="Gallery Image">
    </section>

    <div id="lightbox"></div>

    <!-- Staff Section -->
    <section id="team" class="staff-section">
        <h2>Meet Our Team</h2>
        <div class="staff-grid">
            <div class="staff-card">
                <img src="manager.jpg" alt="Manager">
                <h3>Karthikeyan</h3>
                <p>Manager</p>
            </div>
            <div class="staff-card">
                <img src="asst mang.jpg" alt="Assistant Manager">
                <h3>Subha</h3>
                <p>Assistant Manager</p>
            </div>
        </div>
    </section>

    <!-- Footer Section -->
    <footer>
        <p>&copy; 2025 Thiru Studio. All Rights Reserved. | Designed with ❤️ by Deva</p>
    </footer>

    <!-- Lightbox Script -->
    <script>
        const galleryImages = document.querySelectorAll('.gallery img');
        const lightbox = document.getElementById('lightbox');

        galleryImages.forEach(img => {
            img.addEventListener('click', () => {
                const lightboxImg = document.createElement('img');
                lightboxImg.src = img.src;

                while (lightbox.firstChild) {
                    lightbox.removeChild(lightbox.firstChild);
                }

                lightbox.appendChild(lightboxImg);
                lightbox.style.display = 'flex';
            });
        });

        lightbox.addEventListener('click', () => {
            lightbox.style.display = 'none';
        });
    </script>
</body>
</html>
