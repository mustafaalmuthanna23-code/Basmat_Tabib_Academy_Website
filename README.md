# Basmat_Tabib_Academy_Website
Official website for Basmat Tabib Academy 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Basmat Tabib Academy - Excellence in Education</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        :root {
            --primary: #6a11cb;
            --secondary: #2575fc;
            --accent1: #ff5e7d;
            --accent2: #ff9a3d;
            --accent3: #00c9a7;
            --light: #f8f9fa;
            --dark: #212529;
        }

        body {
            background-color: #f5f7ff;
            color: var(--dark);
            line-height: 1.6;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Header Styles */
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo i {
            font-size: 2rem;
            color: var(--accent2);
        }

        .logo h1 {
            font-size: 1.8rem;
            font-weight: 700;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 1.5rem;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            padding: 0.5rem 0.8rem;
            border-radius: 4px;
        }

        nav ul li a:hover {
            background-color: rgba(255, 255, 255, 0.2);
        }

        .cta-button {
            background-color: var(--accent1);
            color: white;
            padding: 0.7rem 1.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 10px rgba(255, 94, 125, 0.4);
        }

        .cta-button:hover {
            background-color: #ff3d64;
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(255, 94, 125, 0.5);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 5rem 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="%23ffffff" fill-opacity="0.1" d="M0,224L48,213.3C96,203,192,181,288,181.3C384,181,480,203,576,192C672,181,768,139,864,138.7C960,139,1056,181,1152,181.3C1248,181,1344,139,1392,117.3L1440,96L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"></path></svg>');
            background-size: cover;
            background-position: center;
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h2 {
            font-size: 3rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        /* Features Section */
        .features {
            padding: 5rem 0;
            background-color: white;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .section-title p {
            color: #666;
            max-width: 700px;
            margin: 0 auto;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .feature-card {
            background: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
            text-align: center;
            border-top: 4px solid var(--accent3);
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }

        .feature-icon {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, var(--accent1), var(--accent2));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1.5rem;
            color: white;
            font-size: 1.8rem;
        }

        .feature-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--dark);
        }

        .feature-card p {
            color: #666;
        }

        /* Programs Section */
        .programs {
            padding: 5rem 0;
            background: linear-gradient(135deg, #f5f7ff, #e3eeff);
        }

        .programs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .program-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
        }

        .program-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }

        .program-image {
            height: 200px;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 2.5rem;
        }

        .program-content {
            padding: 1.5rem;
        }

        .program-content h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }

        .program-content p {
            color: #666;
            margin-bottom: 1.5rem;
        }

        .program-link {
            color: var(--accent1);
            text-decoration: none;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 5px;
            transition: all 0.3s ease;
        }

        .program-link:hover {
            gap: 10px;
            color: var(--accent2);
        }

        /* Testimonials */
        .testimonials {
            padding: 5rem 0;
            background-color: white;
        }

        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .testimonial-card {
            background: linear-gradient(135deg, #f8f9fa, #e9ecef);
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            position: relative;
        }

        /* Corrected the content property here */
        .testimonial-card::before {
            content: "“";
            position: absolute;
            top: 10px;
            left: 20px;
            font-size: 4rem;
            color: var(--accent3);
            opacity: 0.2;
            font-family: Georgia, serif;
        }

        .testimonial-content {
            margin-bottom: 1.5rem;
            font-style: italic;
            color: #555;
        }

        .testimonial-author {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .author-avatar {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: linear-gradient(135deg, var(--accent1), var(--accent2));
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
        }

        .author-info h4 {
            color: var(--primary);
            margin-bottom: 5px;
        }

        .author-info p {
            color: #777;
            font-size: 0.9rem;
        }

        /* CTA Section */
        .cta-section {
            padding: 5rem 0;
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            text-align: center;
        }

        .cta-section h2 {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
        }

        .cta-section p {
            max-width: 700px;
            margin: 0 auto 2rem;
            font-size: 1.1rem;
            opacity: 0.9;
        }

        .cta-buttons {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
        }

        .cta-button.secondary {
            background-color: transparent;
            border: 2px solid white;
        }

        .cta-button.secondary:hover {
            background-color: white;
            color: var(--primary);
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 4rem 0 2rem;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 1.5rem;
            color: var(--accent2);
            position: relative;
            padding-bottom: 10px;
        }

        .footer-column h3::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--accent1);
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 0.8rem;
        }

        .footer-column ul li a {
            color: #bbb;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .footer-column ul li a:hover {
            color: white;
            padding-left: 5px;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: #333;
            border-radius: 50%;
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background-color: var(--accent1);
            transform: translateY(-5px);
        }

        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid #444;
            color: #999;
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 1rem;
            }

            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }

            nav ul li {
                margin: 0.5rem;
            }

            .hero h2 {
                font-size: 2.2rem;
            }

            .cta-buttons {
                flex-direction: column;
                align-items: center;
            }

            .cta-button {
                width: 100%;
                max-width: 300px;
                text-align: center;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <i class="fas fa-graduation-cap"></i>
                    <h1>Basmat Tabib Academy</h1>
                </div>
                <nav>
                    <ul>
                        <li><a href="#">Home</a></li>
                        <li><a href="#">About</a></li>
                        <li><a href="#">Programs</a></li>
                        <li><a href="#">Faculty</a></li>
                        <li><a href="#">Admissions</a></li>
                        <li><a href="#">Contact</a></li>
                    </ul>
                </nav>
                <a href="#" class="cta-button">Apply Now</a>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <div class="hero-content">
                <h2>Shaping Future Leaders Through Excellence in Education</h2>
                <p>At Basmat Tabib Academy, we provide a transformative learning experience that empowers students to achieve their fullest potential and make a positive impact in the world.</p>
                <a href="#" class="cta-button">Explore Our Programs</a>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features">
        <div class="container">
            <div class="section-title">
                <h2>Why Choose Basmat Tabib Academy?</h2>
                <p>We are committed to providing an exceptional educational experience that fosters intellectual growth, character development, and lifelong success.</p>
            </div>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-user-graduate"></i>
                    </div>
                    <h3>Expert Faculty</h3>
                    <p>Our distinguished professors and instructors are leaders in their fields, dedicated to mentoring and inspiring students.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-flask"></i>
                    </div>
                    <h3>Modern Facilities</h3>
                    <p>State-of-the-art laboratories, libraries, and learning spaces designed to enhance the educational experience.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-globe-americas"></i>
                    </div>
                    <h3>Global Perspective</h3>
                    <p>We offer international exchange programs and a curriculum that prepares students for global challenges.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Programs Section -->
    <section class="programs">
        <div class="container">
            <div class="section-title">
                <h2>Our Academic Programs</h2>
                <p>Discover our diverse range of programs designed to meet the needs of today's learners and tomorrow's leaders.</p>
            </div>
            <div class="programs-grid">
                <div class="program-card">
                    <div class="program-image">
                        <i class="fas fa-laptop-code"></i>
                    </div>
                    <div class="program-content">
                        <h3>Computer Science</h3>
                        <p>Master cutting-edge technologies and develop innovative solutions to complex problems in our comprehensive CS program.</p>
                        <a href="#" class="program-link">Learn More <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                <div class="program-card">
                    <div class="program-image">
                        <i class="fas fa-heartbeat"></i>
                    </div>
                    <div class="program-content">
                        <h3>Medical Sciences</h3>
                        <p>Prepare for a rewarding career in healthcare with our rigorous medical sciences program and clinical training opportunities.</p>
                        <a href="#" class="program-link">Learn More <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                <div class="program-card">
                    <div class="program-image">
                        <i class="fas fa-balance-scale"></i>
                    </div>
                    <div class="program-content">
                        <h3>Business & Law</h3>
                        <p>Develop critical thinking and leadership skills essential for success in the dynamic worlds of business and law.</p>
                        <a href="#" class="program-link">Learn More <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>What Our Students Say</h2>
                <p>Hear from our students about their experiences at Basmat Tabib Academy.</p>
            </div>
            <div class="testimonials-grid">
                <div class="testimonial-card">
                    <div class="testimonial-content">
                        <p>The faculty at Basmat Tabib Academy goes above and beyond to ensure students succeed. The supportive learning environment helped me grow both academically and personally.</p>
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">SA</div>
                        <div class="author-info">
                            <h4>Sarah Ahmed</h4>
                            <p>Computer Science, Class of 2022</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-content">
                        <p>The international exchange program was a life-changing experience. I studied abroad for a semester and gained perspectives that have enriched my academic journey.</p>
                    </div>
                    <div class="testimonial-author">
                        <div class="author-avatar">MJ</div>
                        <div class="author-info">
                            <h4>Mohammed Jamil</h4>
                            <p>Business Administration, Class of 2023</p>
                        </div>
                    </div>
                </div>
                <div class="testimonial-card">
                    <div class="testimonial-content">
                        <p>The research opportunities here are incredible. I've been able to work on cutting-edge projects alongside professors who are leaders in their fields.</p>
                    </div>
                    <div class="testimonial-author">
         