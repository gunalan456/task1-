# task1-
loading page 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modern Landing Page</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>
    <header>
        <div class="container">
            <div class="logo">Brand</div>
            <nav class="desktop-nav">
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Features</a></li>
                    <li><a href="#">Pricing</a></li>
                    <li><a href="#">About</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </nav>
            <button class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </button>
        </div>
    </header>

    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Welcome to Our Platform</h1>
                <p>Discover amazing features that will revolutionize your workflow. Join thousands of satisfied customers who trust our solution.</p>
                <div class="cta-buttons">
                    <a href="#" class="btn primary">Get Started</a>
                    <a href="#" class="btn secondary">Learn More</a>
                </div>
            </div>
            <div class="hero-image">
                <img src="https://via.placeholder.com/600x400" alt="Hero Image">
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-logo">Brand</div>
                <p>&copy; 2023 All Rights Reserved</p>
                <div class="social-links">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                    <a href="#"><i class="fab fa-linkedin-in"></i></a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Simple mobile menu toggle
        document.querySelector('.mobile-menu-btn').addEventListener('click', function() {
            const nav = document.querySelector('.desktop-nav');
            nav.style.display = nav.style.display === 'none' ? 'block' : 'none';
        });

        // Handle window resize to show/hide desktop nav appropriately
        window.addEventListener('resize', function() {
            const nav = document.querySelector('.desktop-nav');
            if (window.innerWidth > 768) {
                nav.style.display = 'block';
            } else {
                nav.style.display = 'none';
            }
        });
    </script>
</body>
</html>  




/* Reset and Base Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: #333;
}

.container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

a {
    text-decoration: none;
    color: inherit;
}

.btn {
    display: inline-block;
    padding: 12px 24px;
    border-radius: 4px;
    font-weight: 600;
    transition: all 0.3s ease;
}

.btn.primary {
    background-color: #4a6bff;
    color: white;
}

.btn.primary:hover {
    background-color: #3a5bef;
    transform: translateY(-2px);
}

.btn.secondary {
    background-color: transparent;
    color: #4a6bff;
    border: 2px solid #4a6bff;
    margin-left: 15px;
}

.btn.secondary:hover {
    background-color: #f0f3ff;
}

/* Header Styles */
header {
    background-color: white;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    position: sticky;
    top: 0;
    z-index: 100;
}

header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 0;
}

.logo {
    font-size: 24px;
    font-weight: 700;
    color: #4a6bff;
}

.desktop-nav ul {
    display: flex;
    list-style: none;
}

.desktop-nav ul li {
    margin-left: 30px;
}

.desktop-nav ul li a {
    font-weight: 500;
    transition: color 0.3s ease;
}

.desktop-nav ul li a:hover {
    color: #4a6bff;
}

.mobile-menu-btn {
    display: none;
    background: none;
    border: none;
    font-size: 24px;
    cursor: pointer;
    color: #333;
}

/* Hero Section Styles */
.hero {
    padding: 80px 0;
    background-color: #f9faff;
}

.hero .container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 50px;
}

.hero-content {
    flex: 1;
}

.hero-image {
    flex: 1;
}

.hero h1 {
    font-size: 48px;
    margin-bottom: 20px;
    color: #222;
}

.hero p {
    font-size: 18px;
    margin-bottom: 30px;
    color: #555;
}

.cta-buttons {
    display: flex;
}

.hero-image img {
    width: 100%;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

/* Footer Styles */
footer {
    background-color: #2a2e35;
    color: white;
    padding: 40px 0;
}

.footer-content {
    text-align: center;
}

.footer-logo {
    font-size: 24px;
    font-weight: 700;
    margin-bottom: 20px;
    color: #4a6bff;
}

.social-links {
    margin-top: 20px;
}

.social-links a {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    background-color: rgba(255, 255, 255, 0.1);
    border-radius: 50%;
    margin: 0 10px;
    transition: all 0.3s ease;
}

.social-links a:hover {
    background-color: #4a6bff;
    transform: translateY(-3px);
}

/* Responsive Styles */
@media (max-width: 992px) {
    .hero .container {
        flex-direction: column;
        text-align: center;
    }
    
    .cta-buttons {
        justify-content: center;
    }
    
    .hero-image {
        margin-top: 40px;
    }
}

@media (max-width: 768px) {
    .desktop-nav {
        display: none;
    }
    
    .mobile-menu-btn {
        display: block;
    }
    
    .desktop-nav.active {
        display: block;
        position: absolute;
        top: 80px;
        left: 0;
        width: 100%;
        background-color: white;
        box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
    }
    
    .desktop-nav.active ul {
        flex-direction: column;
        padding: 20px;
    }
    
    .desktop-nav.active ul li {
        margin: 10px 0;
    }
    
    .hero h1 {
        font-size: 36px;
    }
    
    .hero p {
        font-size: 16px;
    }
    
    .btn {
        padding: 10px 20px;
    }
}

@media (max-width: 576px) {
    .cta-buttons {
        flex-direction: column;
        gap: 15px;
    }
    
    .btn.secondary {
        margin-left: 0;
    }
    
    .hero h1 {
        font-size: 30px;
    }
}
