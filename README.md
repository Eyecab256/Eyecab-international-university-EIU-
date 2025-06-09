```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>EYECAB International University | The Future of Higher Education</title>

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Raleway:wght@300;400;600&display=swap" rel="stylesheet">

    <!-- Font Awesome CDN for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">

    <!-- Slick Carousel CSS -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/slick-carousel/1.8.1/slick.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/slick-carousel/1.8.1/slick-theme.min.css">

    <style>
        :root {
            --primary: #0A2463;
            --secondary: #3E92CC;
            --accent: #FFD700;
            --light: #FFF9F0;
            --dark: #1A1A1A;
            --success: #28a745;
            --info: #17a2b8;
            --font-heading: 'Playfair Display', serif;
            --font-body: 'Raleway', sans-serif;
        }

        [data-theme="dark"] {
            --primary: #FFD700;
            --secondary: #1A1A1A;
            --light: #1A1A1A;
            --dark: #FFF9F0;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: var(--font-body);
            line-height: 1.8;
            color: var(--dark);
            background-color: var(--light);
            overflow-x: hidden;
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        .container {
            width: 90%;
            max-width: 1400px;
            margin: 0 auto;
        }

        header {
            background-color: var(--primary);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
        }

        .logo {
            display: flex;
            align-items: center;
            color: white;
            text-decoration: none;
        }

        .logo-icon {
            margin-right: 1rem;
        }

        .logo h1 {
            font-size: 1.2rem;
            margin-bottom: 0.2rem;
        }

        .logo p {
            font-size: 0.7rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            opacity: 0.8;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 2rem;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            font-size: 1rem;
            letter-spacing: 1px;
            position: relative;
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent);
            transition: width 0.3s ease;
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        .hero {
            background: linear-gradient(rgba(10, 36, 99, 0.7), rgba(10, 36, 99, 0.7)),
                        url('https://source.unsplash.com/1600x600/?university,africa') center/cover no-repeat;
            color: white;
            padding: 8rem 2rem;
            text-align: center;
        }

        .hero h1 {
            font-family: var(--font-heading);
            font-size: 4rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }

        .hero-btns .btn {
            margin: 0 0.5rem;
            padding: 0.8rem 1.5rem;
            font-weight: bold;
            text-decoration: none;
            border-radius: 5px;
            transition: all 0.3s ease;
        }

        .btn-primary {
            background-color: var(--secondary);
            color: white;
        }

        .btn-outline {
            background-color: transparent;
            border: 2px solid white;
            color: white;
        }

        .section {
            padding: 5rem 2rem;
            background-color: white;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }

        .section-title h2 {
            font-family: var(--font-heading);
            font-size: 3rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }

        label.required::after {
            content: " *";
            color: red;
        }

        input[type="text"],
        input[type="email"],
        input[type="tel"],
        input[type="date"],
        select,
        textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            margin-top: 5px;
            box-sizing: border-box;
            font-family: var(--font-body);
            font-size: 1rem;
            transition: all 0.3s ease;
        }

        input[type="text"]:focus,
        input[type="email"]:focus,
        input[type="tel"]:focus,
        input[type="date"]:focus,
        select:focus,
        textarea:focus {
            outline: none;
            border-color: var(--secondary);
        }

        .row {
            display: flex;
            flex-wrap: wrap;
            margin: 0 -10px;
        }

        .col {
            flex: 1;
            padding: 0 10px;
            min-width: 200px;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--primary);
        }

        .btn-submit {
            background-color: var(--secondary);
            color: white;
            padding: 12px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            display: block;
            margin: 20px auto 0;
            transition: all 0.3s ease;
        }

        .btn-submit:hover {
            background-color: #2980b9;
        }

        .fee-info,
        .warning {
            background-color: #f8f9fa;
            padding: 15px;
            border-radius: 4px;
            margin: 20px 0;
            border-left: 4px solid var(--secondary);
        }

        footer {
            background-color: var(--dark);
            color: white;
            padding: 5rem 2rem 2rem;
        }

        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            margin-bottom: 3rem;
        }

        .footer-col h3 {
            font-weight: 700;
            line-height: 1.2;
            color: white;
            margin-bottom: 1rem;
        }

        .footer-col p,
        .footer-col a {
            color: #ccc;
            font-size: 0.9rem;
            line-height: 1.8;
            text-decoration: none;
            display: inline-block;
            margin-bottom: 0.5rem;
        }

        .social-links {
            display: flex;
            gap: 1rem;
        }

        .social-links a {
            color: white;
            font-size: 1.2rem;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            transform: scale(1.1);
        }

        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }

            nav {
                position: fixed;
                top: 0;
                left: -100%;
                height: 100vh;
                width: 100%;
                background-color: var(--primary);
                flex-direction: column;
                align-items: center;
                justify-content: center;
                transition: left 0.3s ease;
                z-index: 1001;
            }

            nav.active {
                left: 0;
            }

            nav ul {
                flex-direction: column;
                gap: 2rem;
                font-size: 1.5rem;
            }
        }

        /* Additional Styles */
        .cta {
            background-color: var(--primary);
            color: white;
            padding: 4rem 2rem;
            text-align: center;
        }

        .testimonial-slider {
            max-width: 800px;
            margin: 0 auto;
        }

        .testimonial-card {
            background-color: #fff;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            text-align: center;
            transition: all 0.3s ease;
        }

        .ai-assistant {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            width: 350px;
            height: 500px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            display: flex;
            flex-direction: column;
            z-index: 999;
        }

        .ai-header {
            background-color: var(--primary);
            color: white;
            padding: 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .ai-messages {
            flex: 1;
            padding: 1rem;
            overflow-y: auto;
        }

        .ai-message {
            background-color: #f1f1f1;
            padding: 1rem;
            border-radius: 5px;
            margin-bottom: 1rem;
        }

        .chat-input {
            display: flex;
            gap: 0.5rem;
            padding: 1rem;
            border-top: 1px solid #eee;
        }

        .chat-input input {
            flex: 1;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        .chat-input button {
            background-color: var(--accent);
            color: var(--primary);
            border: none;
            padding: 0.8rem;
            border-radius: 5px;
            cursor: pointer;
        }

        .live-chat-btn {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            background-color: var(--accent);
            color: var(--primary);
            border: none;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .live-chat-btn:hover {
            transform: scale(1.1);
        }

        .theme-toggle {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            width: 40px;
            height: 40px;
            background-color: var(--accent);
            color: var(--primary);
            border: none;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .theme-toggle:hover {
            transform: rotate(30deg);
        }

        /* Stats Section */
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin: 4rem 0;
        }

        .stat-item {
            background-color: var(--secondary);
            color: white;
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: 1rem;
        }

        /* Program Filter */
        .filter-controls {
            display: flex;
            justify-content: center;
            margin-bottom: 3rem;
            flex-wrap: wrap;
            gap: 1rem;
        }

        .filter-btn {
            padding: 0.7rem 1.5rem;
            background-color: white;
            border: 1px solid #ddd;
            border-radius: 50px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .filter-btn:hover,
        .filter-btn.active {
            background-color: var(--primary);
            color: white;
            border-color: var(--primary);
        }

        .program-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
            display: none;
        }

        .program-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
        }

        .program-card-img img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .program-card-content {
            padding: 2rem;
        }

        .program-card-content h3 {
            font-family: var(--font-heading);
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .program-card-content p {
            margin-bottom: 1.5rem;
            color: #666;
        }

        .program-card-link {
            display: inline-flex;
            align-items: center;
            color: var(--secondary);
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .program-card-link i {
            margin-left: 0.5rem;
            transition: transform 0.3s ease;
        }

        .program-card-link:hover {
            color: var(--primary);
        }

        .program-card-link:hover i {
            transform: translateX(5px);
        }

        /* Footer */
        .footer {
            background-color: var(--dark);
            color: white;
            padding: 5rem 2rem 2rem;
        }

        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            margin-bottom: 3rem;
        }

        .footer-col h3 {
            font-weight: 700;
            margin-bottom: 1rem;
        }

        .footer-links li {
            margin-bottom: 0.8rem;
        }

        .footer-links a {
            color: white;
            text-decoration: none;
            opacity: 0.8;
            transition: all 0.3s ease;
        }

        .footer-links a:hover {
            opacity: 1;
            color: var(--accent);
            padding-left: 5px;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            opacity: 0.7;
        }

        /* About Section */
        .about-image {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 30px 60px rgba(10, 36, 99, 0.2);
            transform: rotate(-2deg);
        }

        .about-image img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s ease;
        }

        .about-image:hover img {
            transform: scale(1.05);
        }

        .about-image::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(10, 36, 99, 0.2), rgba(62, 146, 204, 0.2));
            z-index: 1;
        }

        /* Contact Section */
        .contact-form {
            background-color: white;
            padding: 3rem;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
        }

        .contact-form h3 {
            font-family: var(--font-heading);
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }

        .contact-form p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            line-height: 1.8;
        }

        /* Admissions Form */
        .admissions-form {
            background-color: white;
            padding: 3rem;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
        }

        .admissions-form h3 {
            font-family: var(--font-heading);
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }

        .admissions-form p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            line-height: 1.8;
        }

        /* File Upload */
        .file-upload {
            background-color: #f8f9fa;
            border: 2px dashed #ddd;
            padding: 2rem;
            border-radius: 10px;
            text-align: center;
            position: relative;
            transition: background-color 0.3s ease;
        }

        .file-upload:hover {
            background-color: #e9f7fe;
        }

        .file-upload input[type="file"] {
            opacity: 0;
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            cursor: pointer;
        }

        .file-label {
            display: block;
            padding: 1rem;
            background-color: #e9f7fe;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .file-label:hover {
            background-color: #d4edda;
        }

        /* Course Selection */
        .course-selection {
            max-height: 300px;
            overflow-y: auto;
            border: 1px solid #ddd;
            padding: 10px;
            margin-bottom: 20px;
            border-radius: 4px;
        }

        .course-option {
            margin-bottom: 10px;
        }

        /* Testimonials */
        .testimonials {
            padding: 5rem 2rem;
            background-color: #f8f9fa;
        }

        .testimonial-quote {
            font-size: 1.2rem;
            font-style: italic;
            color: #555;
            margin-bottom: 2rem;
            position: relative;
        }

        .testimonial-quote::before,
        .testimonial-quote::after {
            content: '"';
            font-size: 3rem;
            color: var(--accent);
            opacity: 0.3;
            position: absolute;
        }

        .testimonial-quote::before {
            top: -20px;
            left: -15px;
        }

        .testimonial-quote::after {
            bottom: -40px;
            right: -15px;
        }

        /* Mobile responsiveness */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1.2rem;
            }

            .admissions-form,
            .contact-form {
                padding: 2rem;
            }
        }

        @media (max-width: 576px) {
            .stats-container {
                grid-template-columns: 1fr;
            }

            .footer-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

<!-- Header -->
<header id="header">
    <div class="container header-container">
        <a href="#" class="logo">
            <div class="logo-icon"><i class="fas fa-university"></i></div>
            <div class="logo-text">
                <h1>EYECAB INTERNATIONAL UNIVERSITY</h1>
                <p>Redefining Global Higher Education</p>
            </div>
        </a>
        <button class="mobile-menu-btn" id="mobileMenuBtn"><i class="fas fa-bars"></i></button>
    </div>
    <nav id="mobileMenu">
        <button class="mobile-menu-btn" id="closeMenuBtn"><i class="fas fa-times"></i></button>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#programs">Programs</a></li>
            <li><a href="#application">Apply Now</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
</header>

<!-- Hero Section -->
<section class="hero" id="home">
    <div class="container hero-content">
        <h1>Welcome to Eyecab International University</h1>
        <p>Empowering Future Leaders Through Innovation and Excellence</p>
        <div class="hero-btns">
            <a href="#application" class="btn btn-primary">Apply Now</a>
            <a href="#programs" class="btn btn-outline">Explore Programs</a>
        </div>
    </div>
</section>

<!-- About Section -->
<section class="section" id="about">
    <div class="container">
        <div class="section-title">
            <h2>About EYECAB</h2>
            <p>Shaping the Future of African Education</p>
        </div>
        
        <div class="row">
            <div class="col">
                <p>Eyecab International University is a premier institution dedicated to providing world-class education rooted in African values and global standards. Our mission is to empower future leaders through innovation, research, and excellence in higher learning.</p>
                <p>Founded in the heart of Africa, we offer a unique educational experience that combines traditional wisdom with cutting-edge technology to prepare students for success in a rapidly changing world.</p>
                
                <div class="about-features">
                    <div class="feature-item">
                        <div class="feature-icon"><i class="fas fa-calendar-alt"></i></div>
                        <div class="feature-text">
                            <h4>Application Deadlines</h4>
                            <p>Fall Semester: June 30<br>Spring Semester: November 15</p>
                        </div>
                    </div>
                    <div class="feature-item">
                        <div class="feature-icon"><i class="fas fa-graduation-cap"></i></div>
                        <div class="feature-text">
                            <h4>Admission Requirements</h4>
                            <p>Vary by program. Most require transcripts, test scores, letters of recommendation, and a personal statement.</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="col about-image">
                <img src="https://source.unsplash.com/800x600/?university,africa" alt="Eyecab Campus" loading="lazy">
            </div>
        </div>
    </div>
</section>

<!-- Stats Section -->
<section class="section stats" style="background-color: #f8f9fa;">
    <div class="container">
        <div class="stats-container">
            <div class="stat-item">
                <div class="stat-number">25+</div>
                <div class="stat-label">Years of Excellence</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">15,000+</div>
                <div class="stat-label">Students Enrolled</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">95%</div>
                <div class="stat-label">Graduate Employment</div>
            </div>
            <div class="stat-item">
                <div class="stat-number">50+</div>
                <div class="stat-label">Countries Represented</div>
            </div>
        </div>
    </div>
</section>

<!-- Programs Section -->
<section class="section programs" id="programs">
    <div class="container">
        <div class="section-title">
            <h2>Our Academic Programs</h2>
            <p>Explore our wide range of undergraduate and postgraduate programs across various disciplines.</p>
        </div>
        
        <div class="filter-controls">
            <button class="filter-btn active" data-filter="all">All Programs</button>
            <button class="filter-btn" data-filter="business">Business & Management</button>
            <button class="filter-btn" data-filter="engineering">Engineering & Technology</button>
            <button class="filter-btn" data-filter="health">Health Sciences</button>
            <button class="filter-btn" data-filter="humanities">Humanities & Social Sciences</button>
        </div>
        
        <div class="programs-grid">
            <div class="program-card" data-category="business engineering">
                <div class="program-card-img">
                    <img src="https://source.unsplash.com/600x400/?business,technology" alt="Business Administration" loading="lazy">
                </div>
                <div class="program-card-content">
                    <h3>Bachelor of Business Administration</h3>
                    <p>A comprehensive program covering all aspects of business management, preparing students for leadership roles in diverse industries.</p>
                    <a href="#" class="program-card-link">Learn More <i class="fas fa-arrow-right"></i></a>
                </div>
            </div>
            
            <div class="program-card" data-category="health">
                <div class="program-card-img">
                    <img src="https://source.unsplash.com/600x400/?nursing,medicine" alt="Nursing" loading="lazy">
                </div>
                <div class="program-card-content">
                    <h3>Bachelor of Nursing Science</h3>
                    <p>A rigorous program combining theoretical knowledge with practical skills to prepare professional nurses ready to excel in modern healthcare environments.</p>
                    <a href="#" class="program-card-link">Learn More <i class="fas fa-arrow-right"></i></a>
                </div>
            </div>
            
            <div class="program-card" data-category="engineering">
                <div class="program-card-img">
                    <img src="https://source.unsplash.com/600x400/?computer,engineering" alt="Computer Engineering" loading="lazy">
                </div>
                <div class="program-card-content">
                    <h3>Bachelor of Computer Engineering</h3>
                    <p>An innovative program blending computer science and electrical engineering to produce graduates capable of designing and developing next-generation computing systems.</p>
                    <a href="#" class="program-card-link">Learn More <i class="fas fa-arrow-right"></i></a>
                </div>
            </div>
            
            <div class="program-card" data-category="humanities">
                <div class="program-card-img">
                    <img src="https://source.unsplash.com/600x400/?literature,education" alt="Arts and Humanities" loading="lazy">
                </div>
                <div class="program-card-content">
                    <h3>Bachelor of Arts in Social Sciences</h3>
                    <p>A versatile program exploring human society and social relationships, preparing students for careers in government, NGOs, media, and more.</p>
                    <a href="#" class="program-card-link">Learn More <i class="fas fa-arrow-right"></i></a>
                </div>
            </div>
        </div>
    </div>
</section>

<!-- Application Form Section -->
<section class="section" id="application">
    <div class="container">
        <div class="section-title">
            <h2>Undergraduate Application Form</h2>
            <p>2024/2025 Academic Year - Private Admissions</p>
        </div>
        
        <form id="applicationForm" enctype="multipart/form-data">
            <!-- Personal Information -->
            <h3>Personal Information</h3>
            <div class="row">
                <div class="col">
                    <div class="form-group">
                        <label for="firstName" class="required">First Name</label>
                        <input type="text" id="firstName" name="firstName" required>
                    </div>
                </div>
                <div class="col">
                    <div class="form-group">
                        <label for="lastName" class="required">Last Name</label>
                        <input type="text" id="lastName" name="lastName" required>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col">
                    <div class="form-group">
                        <label for="gender" class="required">Gender</label>
                        <select id="gender" name="gender" required>
                            <option value="">Select Gender</option>
                            <option value="male">Male</option>
                            <option value="female">Female</option>
                            <option value="other">Other</option>
                        </select>
                    </div>
                </div>
                <div class="col">
                    <div class="form-group">
                        <label for="dob" class="required">Date of Birth</label>
                        <input type="date" id="dob" name="dob" required>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col">
                    <div class="form-group">
                        <label for="email" class="required">Email Address</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                </div>
                <div class="col">
                    <div class="form-group">
                        <label for="phone" class="required">Phone Number</label>
                        <input type="tel" id="phone" name="phone" required>
                    </div>
                </div>
            </div>
            <div class="form-group">
                <label for="address" class="required">Permanent Address</label>
                <textarea id="address" name="address" rows="3" required></textarea>
            </div>
            
            <!-- Academic Information -->
            <h3>Academic Information</h3>
            <div class="row">
                <div class="col">
                    <div class="form-group">
                        <label for="uceYear" class="required">UCE Year of Sitting</label>
                        <input type="number" id="uceYear" name="uceYear" min="1900" max="2025" required>
                    </div>
                </div>
                <div class="col">
                    <div class="form-group">
                        <label for="uceIndex" class="required">UCE Index Number</label>
                        <input type="text" id="uceIndex" name="uceIndex" required>
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col">
                    <div class="form-group">
                        <label for="uaceYear" class="required">UACE Year of Sitting</label>
                        <input type="number" id="uaceYear" name="uaceYear" min="1900" max="2025" required>
                    </div>
                </div>
                <div class="col">
                    <div class="form-group">
                        <label for="uaceIndex" class="required">UACE Index Number</label>
                        <input type="text" id="uaceIndex" name="uaceIndex" required>
                    </div>
                </div>
            </div>
            
            <!-- UCE Results -->
            <div class="form-group">
                <label class="required">UCE Results (At least 5 passes)</label>
                <div class="row">
                    <div class="col">
                        <label for="uceSubject1">Subject 1</label>
                        <input type="text" id="uceSubject1" name="uceSubject1">
                    </div>
                    <div class="col">
                        <label for="uceGrade1">Grade</label>
                        <input type="text" id="uceGrade1" name="uceGrade1">
                    </div>
                </div>
                <div class="row">
                    <div class="col">
                        <label for="uceSubject2">Subject 2</label>
                        <input type="text" id="uceSubject2" name="uceSubject2">
                    </div>
                    <div class="col">
                        <label for="uceGrade2">Grade</label>
                        <input type="text" id="uceGrade2" name="uceGrade2">
                    </div>
                </div>
                <div class="row">
                    <div class="col">
                        <label for="uceSubject3">Subject 3</label>
                        <input type="text" id="uceSubject3" name="uceSubject3">
                    </div>
                    <div class="col">
                        <label for="uceGrade3">Grade</label>
                        <input type="text" id="uceGrade3" name="uceGrade3">
                    </div>
                </div>
                <div class="row">
                    <div class="col">
                        <label for="uceSubject4">Subject 4</label>
                        <input type="text" id="uceSubject4" name="uceSubject4">
                    </div>
                    <div class="col">
                        <label for="uceGrade4">Grade</label>
                        <input type="text" id="uceGrade4" name="uceGrade4">
                    </div>
                </div>
                <div class="row">
                    <div class="col">
                        <label for="uceSubject5">Subject 5</label>
                        <input type="text" id="uceSubject5" name="uceSubject5">
                    </div>
                    <div class="col">
                        <label for="uceGrade5">Grade</label>
                        <input type="text" id="uceGrade5" name="uceGrade5">
                    </div>
                </div>
            </div>
            
            <!-- UACE Results -->
            <div class="form-group">
                <label class="required">UACE Results (At least 2 Principal Passes)</label>
                <div class="row">
                    <div class="col">
                        <label for="uaceSubject1">Principal Subject 1</label>
                        <input type="text" id="uaceSubject1" name="uaceSubject1">
                    </div>
                    <div class="col">
                        <label for="uaceGrade1">Grade</label>
                        <input type="text" id="uaceGrade1" name="uaceGrade1">
                    </div>
                </div>
                <div class="row">
                    <div class="col">
                        <label for="uaceSubject2">Principal Subject 2</label>
                        <input type="text" id="uaceSubject2" name="uaceSubject2">
                    </div>
                    <div class="col">
                        <label for="uaceGrade2">Grade</label>
                        <input type="text" id="uaceGrade2" name="uaceGrade2">
                    </div>
                </div>
                <div class="row">
                    <div class="col">
                        <label for="uaceSubject3">Subsidiary Subject 1</label>
                        <input type="text" id="uaceSubject3" name="uaceSubject3">
                    </div>
                    <div class="col">
                        <label for="uaceGrade3">Grade</label>
                        <input type="text" id="uceGrade3" name="uceGrade3">
                    </div>
                </div>
                <div class="row">
                    <div class="col">
                        <label for="uaceSubject4">Subsidiary Subject 2</label>
                        <input type="text" id="uaceSubject4" name="uaceSubject4">
                    </div>
                    <div class="col">
                        <label for="uaceGrade4">Grade</label>
                        <input type="text" id="uaceGrade4" name="uaceGrade4">
                    </div>
                </div>
            </div>
            
            <!-- Programme Selection -->
            <h3>Programme Selection</h3>
            <div class="form-group">
                <label for="studyMode" class="required">Mode of Study</label>
                <select id="studyMode" name="studyMode" required>
                    <option value="">Select Mode</option>
                    <option value="day">Day Programme</option>
                    <option value="evening">Evening Programme</option>
                    <option value="afternoon">Afternoon Programme</option>
                    <option value="external">External Programme</option>
                </select>
            </div>
            <div class="form-group">
                <label for="college" class="required">College</label>
                <select id="college" name="college" required>
                    <option value="">Select College</option>
                    <option value="health">College of Health Sciences</option>
                    <option value="agriculture">College of Agricultural and Environmental Sciences</option>
                    <option value="engineering">College of Engineering, Design, Art and Technology</option>
                    <option value="business">College of Business and Management Sciences</option>
                    <option value="humanities">College of Humanities and Social Sciences</option>
                    <option value="education">College of Education and External Studies</option>
                    <option value="natural">College of Natural Sciences</option>
                    <option value="computing">College of Computing and Information Sciences</option>
                    <option value="law">School of Law</option>
                    <option value="veterinary">College of Veterinary Medicine, Animal Resources and Biosecurity</option>
                </select>
            </div>
            <div class="form-group">
                <label for="programme" class="required">Preferred Programme</label>
                <select id="programme" name="programme" required>
                    <option value="">Select Programme</option>
                    
                    <!-- Health Sciences -->
                    <option value="nursing" data-college="health">Bachelor of Nursing Science (5 Years)</option>
                    <option value="speech" data-college="health">Bachelor of Science in Speech and Language Therapy (4 Years)</option>
                    <option value="biomedical" data-college="health">Bachelor of Science in Biomedical Engineering (4 Years)</option>
                    <option value="cytotechnology" data-college="health">Bachelor of Cytotechnology (3 Years)</option>
                    <option value="optometry" data-college="health">Bachelor of Optometry (3 Years)</option>
                    <option value="dental" data-college="health">Bachelor of Science in Dental Laboratory Technology (3 Years)</option>
                    <option value="radiography" data-college="health">Bachelor of Science in Medical Radiography (3 Years)</option>
                    
                    <!-- Agricultural and Environmental Sciences -->
                    <option value="agriculture" data-college="agriculture">Bachelor of Science in Agriculture (4 Years)</option>
                    <option value="food" data-college="agriculture">Bachelor of Science in Food Science and Technology (4 Years)</option>
                    <option value="agri-engineering" data-college="agriculture">Bachelor of Science in Agricultural Engineering (4 Years)</option>
                    <option value="agribusiness" data-college="agriculture">Bachelor of Agribusiness Management (3 Years)</option>
                    <option value="rural" data-college="agriculture">Bachelor of Agricultural and Rural Innovation (3 Years)</option>
                    <option value="nutrition" data-college="agriculture">Bachelor of Science in Human Nutrition & Dietetics (4 Years)</option>
                    <option value="forestry" data-college="agriculture">Bachelor of Science in Forestry (4 Years)</option>
                    <option value="geographical" data-college="agriculture">Bachelor of Geographical Sciences (3 Years)</option>
                    <option value="tourism" data-college="agriculture">Bachelor of Tourism and Hospitality Management (3 Years)</option>
                    <option value="bioprocessing" data-college="agriculture">Bachelor of Science in Bioprocessing Engineering (4 Years)</option>
                    <option value="water" data-college="agriculture">Bachelor of Science in Water and Irrigation Engineering (4 Years)</option>
                    <option value="environmental" data-college="agriculture">Bachelor of Environmental Science (3 Years)</option>
                    
                    <!-- Engineering, Design, Art and Technology -->
                    <option value="civil" data-college="engineering">Bachelor of Science in Civil Engineering (4 Years)</option>
                    <option value="electrical" data-college="engineering">Bachelor of Science in Electrical Engineering (4 Years)</option>
                    <option value="mechanical" data-college="engineering">Bachelor of Science in Mechanical Engineering (4 Years)</option>
                    <option value="surveying" data-college="engineering">Bachelor of Science in Land Surveying and Geomatics (4 Years)</option>
                    <option value="architecture" data-college="engineering">Bachelor of Architecture (5 Years)</option>
                    <option value="quantity" data-college="engineering">Bachelor of Science in Quantity Surveying (4 Years)</option>
                    <option value="fine-art" data-college="engineering">Bachelor of Fine Art (3 Years)</option>
                    <option value="industrial" data-college="engineering">Bachelor of Industrial Art and Applied Design (3 Years)</option>
                    <option value="visual" data-college="engineering">Bachelor of Visual Communication, Design & Multi-Media (3 Years)</option>
                    <option value="urban" data-college="engineering">Bachelor of Urban and Regional Planning (4 Years)</option>
                    <option value="valuation" data-college="engineering">Bachelor of Science in Valuation (4 Years)</option>
                    
                    <!-- Business and Management Sciences -->
                    <option value="statistics" data-college="business">Bachelor of Statistics (3 Years)</option>
                    <option value="actuarial" data-college="business">Bachelor of Science in Actuarial Science (3 Years)</option>
                    <option value="economics" data-college="business">Bachelor of Arts in Economics (3 Years)</option>
                    <option value="quantitative" data-college="business">Bachelor of Science in Quantitative Economics (3 Years)</option>
                    <option value="commerce" data-college="business">Bachelor of Commerce (3 Years)</option>
                    <option value="business-admin" data-college="business">Bachelor of Business Administration (3 Years)</option>
                    <option value="population" data-college="business">Bachelor of Science in Population Studies (3 Years)</option>
                    
                    <!-- Humanities and Social Sciences -->
                    <option value="social-work" data-college="humanities">Bachelor of Social Work (4 Years)</option>
                    <option value="social-sciences" data-college="humanities">Bachelor of Arts in Social Sciences (3 Years)</option>
                    <option value="journalism" data-college="humanities">Bachelor of Journalism and Communication (4 Years)</option>
                    <option value="arts" data-college="humanities">Bachelor of Arts (3 Years)</option>
                    <option value="music" data-college="humanities">Bachelor of Arts in Music (3 Years)</option>
                    <option value="psychology" data-college="humanities">Bachelor of Applied Psychology (3 Years)</option>
                    <option value="asian" data-college="humanities">Bachelor of Chinese and Asian Studies (3 Years)</option>
                    <option value="performing" data-college="humanities">Diploma in Performing Arts (2 Years)</option>
                    
                    <!-- Education and External Studies -->
                    <option value="arts-edu" data-college="education">Bachelor of Arts with Education (3 Years)</option>
                    <option value="science-edu" data-college="education">Bachelor of Science with Education (3 Years)</option>
                    <option value="adult-edu" data-college="education">Bachelor of Adult and Community Education (3 Years)</option>
                    <option value="early-childhood" data-college="education">Bachelor of Early Childhood Care and Education (3 Years)</option>
                    <option value="youth" data-college="education">Bachelor of Youth in Development Work (External) (4 Years)</option>
                    <option value="education" data-college="education">Bachelor of Education (for Practising Diploma Holder Teachers only) (3 Years)</option>
                    
                    <!-- Natural Sciences -->
                    <option value="fisheries" data-college="natural">Bachelor of Science in Fisheries and Aquaculture (3 Years)</option>
                    <option value="sports" data-college="natural">Bachelor of Sports Science (3 Years)</option>
                    <option value="biological" data-college="natural">Bachelor of Science - Biological (3 Years)</option>
                    <option value="physical" data-college="natural">Bachelor of Science - Physical (3 Years)</option>
                    <option value="economics-science" data-college="natural">Bachelor of Science - Economics (3 Years)</option>
                    <option value="petroleum" data-college="natural">Bachelor of Science in Petroleum Geoscience & Production (4 Years)</option>
                    <option value="conservation" data-college="natural">Bachelor of Science in Conservation Biology (3 Years)</option>
                    <option value="biotechnology" data-college="natural">Bachelor of Science in Biotechnology (3 Years)</option>
                    
                    <!-- Computing and Information Sciences -->
                    <option value="computer-science" data-college="computing">Bachelor of Science in Computer Science (3 Years)</option>
                    <option value="information-systems" data-college="computing">Bachelor of Information Systems and Technology (3 Years)</option>
                    <option value="software" data-college="computing">Bachelor of Science in Software Engineering (4 Years)</option>
                    <option value="library" data-college="computing">Bachelor of Library and Information Science (3 Years)</option>
                    
                    <!-- Law -->
                    <option value="laws" data-college="law">Bachelor of Laws (4 Years)</option>
                    
                    <!-- Veterinary Medicine -->
                    <option value="veterinary-med" data-college="veterinary">Bachelor of Veterinary Medicine (5 Years)</option>
                    <option value="biomedical-lab" data-college="veterinary">Bachelor of Biomedical Laboratory Technology (3 Years)</option>
                    <option value="animal-production" data-college="veterinary">Bachelor of Animal Production Technology and Management (3 Years)</option>
                    <option value="livestock" data-college="veterinary">Bachelor of Industrial Livestock and Business (3 Years)</option>
                </select>
            </div>
            <div class="form-group">
                <label for="secondChoice">Second Choice Programme (Optional)</label>
                <select id="secondChoice" name="secondChoice">
                    <option value="">Select Second Choice</option>
                </select>
            </div>
            
            <!-- Payment Information -->
            <h3>Payment Information</h3>
            <div class="fee-info">
                <h4>Application Fees</h4>
                <p><strong>Ugandan and East African Applicants:</strong> UGX 50,000</p>
                <p><strong>International Applicants:</strong> USD 75 or equivalent</p>
                <p>Plus bank charges to be paid in any of the banks used by Uganda Revenue Authority (URA)</p>
            </div>
            <div class="form-group">
                <label for="paymentMethod" class="required">Payment Method</label>
                <select id="paymentMethod" name="paymentMethod" required>
                    <option value="">Select Payment Method</option>
                    <option value="bank">Bank Payment</option>
                    <option value="mobile">Mobile Money</option>
                </select>
            </div>
            <div class="form-group" id="paymentDetails">
                <!-- Will be populated based on payment method selection -->
            </div>
            
            <!-- File Upload -->
            <h3>Supporting Documents</h3>
            <div class="form-group">
                <label>Upload Academic Transcripts</label>
                <div class="file-upload">
                    <input type="file" id="transcriptUpload" name="transcript">
                    <label for="transcriptUpload" class="file-label">Choose Files</label>
                </div>
            </div>
            <div class="form-group">
                <label>Upload Identification</label>
                <div class="file-upload">
                    <input type="file" id="idUpload" name="idUpload">
                    <label for="idUpload" class="file-label">Choose Files</label>
                </div>
            </div>
            <div class="form-group">
                <label>Upload Passport Photo</label>
                <div class="file-upload">
                    <input type="file" id="photoUpload" name="photoUpload">
                    <label for="photoUpload" class="file-label">Choose Files</label>
                </div>
            </div>
            
            <!-- Declaration -->
            <h3>Declaration</h3>
            <div class="warning">
                <p><strong>WARNING:</strong></p>
                <ol>
                    <li>Applicants are strongly warned against presenting forged or other people's academic documents to support their applications for admission. Forging of documents shall lead to automatic cancellation of admission, revocation of the award where applicable and prosecution in the courts of law.</li>
                    <li>Do not buy any other documents not originating from the Academic Registrar's Office. Those who buy them do so at their own risk.</li>
                    <li>The Academic Registrar has not appointed any agent to act on his behalf to solicit for additional funds other than the application fee stated above.</li>
                    <li>Applicants are advised to use the right programme names and codes. The University will not be responsible for any wrong information entered in the system by applicants.</li>
                </ol>
            </div>
            <div class="form-group">
                <input type="checkbox" id="declaration" name="declaration" required>
                <label for="declaration" class="required">I declare that the information given in this application is complete and correct. I understand that giving false information may lead to disqualification of my application or subsequent cancellation of my registration if admitted.</label>
            </div>
            <div class="form-group">
                <label for="signature" class="required">Full Name (as signature)</label>
                <input type="text" id="signature" name="signature" required>
            </div>
            <div class="form-group">
                <label for="date" class="required">Date</label>
                <input type="date" id="date" name="date" required>
            </div>
            <button type="submit" class="btn btn-submit">Submit Application</button>
        </form>
    </div>
</section>

<!-- Testimonials Section -->
<section class="section testimonials" id="testimonials" style="background-color: #f8f9fa;">
    <div class="container">
        <div class="section-title">
            <h2>Student Voices</h2>
            <p>Hear from our amazing student community</p>
        </div>
        
        <div class="testimonial-slider">
            <div class="testimonial-card">
                <p>"Eyecab transformed my life. The professors were mentors, the courses challenged me, and the opportunities changed my career path completely. It was the best decision I ever made!"</p>
                <p>- Amina Okoye, Class of 2022</p>
            </div>
            <div class="testimonial-card">
                <p>"The combination of African cultural roots with international standards makes Eyecab unique. I gained both technical expertise and a deep understanding of how to apply it in the African context."</p>
                <p>- Kwame Mensah, Class of 2021</p>
            </div>
            <div class="testimonial-card">
                <p>"From day one, I felt welcomed into a community that truly cares about its students. The support services, internship opportunities, and career guidance set Eyecab apart from other institutions."</p>
                <p>- Sarah Wambua, Class of 2023</p>
            </div>
        </div>
    </div>
</section>

<!-- Contact Section -->
<section class="section contact" id="contact">
    <div class="container">
        <div class="section-title">
            <h2>Contact Us</h2>
            <p>We're here to help. Reach out to us today.</p>
        </div>
        
        <div class="row">
            <div class="col">
                <h3>Get in Touch</h3>
                <p><i class="fas fa-map-marker-alt contact-icon"></i>P.O. Box 784, Kampala, Uganda</p>
                <p><i class="fas fa-phone contact-icon"></i>+256 772 123 456</p>
                <p><i class="fas fa-envelope contact-icon"></i>admissions@eyecab.edu</p>
                <h3>Office Hours</h3>
                <p>Monday - Friday: 8:00 AM - 5:00 PM<br>Saturday: 9:00 AM - 1:00 PM<br>Sunday: Closed</p>
            </div>
            <div class="col">
                <form id="contactForm">
                    <div class="form-group">
                        <label for="contact-name" class="required">Your Name</label>
                        <input type="text" id="contact-name" name="name" required>
                    </div>
                    <div class="form-group">
                        <label for="contact-email" class="required">Your Email</label>
                        <input type="email" id="contact-email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="contact-subject" class="required">Subject</label>
                        <input type="text" id="contact-subject" name="subject" required>
                    </div>
                    <div class="form-group">
                        <label for="contact-message" class="required">Your Message</label>
                        <textarea id="contact-message" name="message" rows="5" required></textarea>
                    </div>
                    <button type="submit" class="btn btn-primary">Send Message</button>
                </form>
            </div>
        </div>
    </div>
</section>

<!-- CTA Section -->
<section class="cta">
    <div class="container">
        <h2>Ready to Transform Your Future?</h2>
        <p>Join EYECAB International University and become part of a new generation of African leaders and innovators.</p>
        <div class="hero-btns">
            <a href="#application" class="btn btn-primary">Apply Now</a>
            <a href="#contact" class="btn btn-outline">Contact Admissions</a>
        </div>
    </div>
</section>

<!-- Footer -->
<footer class="footer" id="footer">
    <div class="container">
        <div class="footer-container">
            <div class="footer-col">
                <h3>About EYECAB</h3>
                <p>EYECAB International University is a leading institution dedicated to providing quality education rooted in African values while meeting global standards. We prepare our students to be leaders in their chosen fields.</p>
                <div class="social-links">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    <a href="#"><i class="fab fa-instagram"></i></a>
                </div>
            </div>
            <div class="footer-col">
                <h3>Quick Links</h3>
                <ul class="footer-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#programs">Programs</a></li>
                    <li><a href="#application">Apply Now</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3>Contact Info</h3>
                <p><i class="fas fa-map-marker-alt contact-icon"></i>P.O. Box 784, Kampala, Uganda</p>
                <p><i class="fas fa-phone contact-icon"></i>+256 772 123 456</p>
                <p><i class="fas fa-envelope contact-icon"></i>admissions@eyecab.edu</p>
            </div>
        </div>
        <p class="footer-bottom">&copy; 2025 Eyecab International University. All rights reserved.</p>
    </div>
</footer>

<!-- Chat Buttons -->
<button class="live-chat-btn" id="liveChatBtn"><i class="fas fa-comments"></i></button>

<div class="ai-assistant" id="aiAssistant">
    <div class="ai-header">
        <span>AI Assistant</span>
        <button id="minimizeBtn" style="background: none; border: none; color: white; font-size: 1.2rem;">−</button>
    </div>
    <div class="ai-messages" id="aiChat">
        <div class="ai-message ai-response">Hello! How can I assist you today?</div>
    </div>
    <div class="ai-input">
        <input type="text" id="aiQuestion" placeholder="Ask a question...">
        <button id="aiSubmit"><i class="fas fa-paper-plane"></i></button>
    </div>
</div>

<!-- Scripts -->
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick.min.js"></script>
<script>
    // Mobile Menu Toggle
    document.getElementById('mobileMenuBtn').addEventListener('click', () => {
        document.getElementById('mobileMenu').classList.add('active');
    });

    document.getElementById('closeMenuBtn').addEventListener('click', () => {
        document.getElementById('mobileMenu').classList.remove('active');
    });

    // Close mobile menu when clicking links
    document.querySelectorAll('.mobile-menu a').forEach(link => {
        link.addEventListener('click', () => {
            document.getElementById('mobileMenu').classList.remove('active');
        });
    });

    // Header Scroll Effect
    window.addEventListener('scroll', () => {
        const header = document.getElementById('header');
        if (window.scrollY > 50) {
            header.classList.add('scrolled');
        } else {
            header.classList.remove('scrolled');
        }
    });

    // Testimonial Slider
    $(document).ready(function(){
        $('.testimonial-slider').slick({
            dots: true,
            infinite: true,
            speed: 300,
            slidesToShow: 1,
            adaptiveHeight: true,
            autoplay: true,
            arrows: true,
            prevArrow: '<button type="button" class="slick-prev"><i class="fas fa-chevron-left"></i></button>',
            nextArrow: '<button type="button" class="slick-next"><i class="fas fa-chevron-right"></i></button>'
        });
    });

    // Program Filter
    document.querySelectorAll('.filter-btn').forEach(button => {
        button.addEventListener('click', () => {
            document.querySelectorAll('.filter-btn').forEach(btn => btn.classList.remove('active'));
            button.classList.add('active');

            const filterValue = button.getAttribute('data-filter');
            document.querySelectorAll('.program-card').forEach(card => {
                card.style.display = filterValue === 'all' || card.getAttribute('data-category') === filterValue ? 'block' : 'none';
            });
        });
    });

    // Clone programme options to second choice
    const programmeSelect = document.getElementById('programme');
    const secondChoiceSelect = document.getElementById('secondChoice');

    for (let i = 0; i < programmeSelect.options.length; i++) {
        const option = programmeSelect.options[i];
        if (option.value) {
            secondChoiceSelect.add(new Option(option.text, option.value));
        }
    }

    // Filter programmes by college
    const collegeSelect = document.getElementById('college');
    const secondChoice = document.getElementById('secondChoice');

    collegeSelect.addEventListener('change', function () {
        const selectedCollege = this.value;
        for (let i = 0; i < programmeSelect.options.length; i++) {
            const option = programmeSelect.options[i];
            if (option.value && option.dataset.college !== selectedCollege) {
                option.style.display = 'none';
            } else {
                option.style.display = '';
            }
        }
        programmeSelect.value = '';
    });

    // Payment method toggle
    const paymentMethod = document.getElementById('paymentMethod');
    const paymentDetails = document.getElementById('paymentDetails');

    paymentMethod.addEventListener('change', function () {
        paymentDetails.innerHTML = '';
        
        if (this.value === 'bank') {
            paymentDetails.innerHTML = `
                <label for="bankName" class="required">Bank Name</label>
                <input type="text" id="bankName" name="bankName" required>
                <label for="receiptNumber" class="required">Receipt Number</label>
                <input type="text" id="receiptNumber" name="receiptNumber" required>
                <label for="paymentDate" class="required">Payment Date</label>
                <input type="date" id="paymentDate" name="paymentDate" required>
            `;
        } else if (this.value === 'mobile') {
            paymentDetails.innerHTML = `
                <p><strong>Mobile Money Payment Steps:</strong></p>
                <ol>
                    <li>Dial *272*8# on either MTN or Airtel</li>
                    <li>Select option 3-Admission</li>
                    <li>Select option 3-Pay Fees</li>
                    <li>Enter reference number obtained from Application portal</li>
                    <li>Details of Application form will be confirmed</li>
                    <li>Enter PIN to confirm payment</li>
                </ol>
                <label for="mobileNumber" class="required">Mobile Number Used</label>
                <input type="tel" id="mobileNumber" name="mobileNumber" required>
                <label for="transactionId" class="required">Transaction ID</label>
                <input type="text" id="transactionId" name="transactionId" required>
            `;
        }
    });

    // Form Submission
    document.getElementById('applicationForm').addEventListener('submit', function(e) {
        e.preventDefault();
        alert("Thank you for applying! Your application has been submitted.");
        this.reset();
    });

    // Contact Form Submission
    document.getElementById('contactForm').addEventListener('submit', function(e) {
        e.preventDefault();
        alert("Thank you for contacting us! We'll get back to you soon.");
        this.reset();
    });

    // Theme Toggle
    const themeToggle = document.getElementById('themeToggle');
    const currentTheme = localStorage.getItem('theme');

    if (currentTheme === 'dark') {
        document.body.setAttribute('data-theme', 'dark');
        themeToggle.innerHTML = '<i class="fas fa-sun"></i>';
    }

    themeToggle.addEventListener('click', () => {
        if (document.body.getAttribute('data-theme') === 'dark') {
            document.body.removeAttribute('data-theme');
            localStorage.setItem('theme', 'light');
            themeToggle.innerHTML = '<i class="fas fa-moon"></i>';
        } else {
            document.body.setAttribute('data-theme', 'dark');
            localStorage.setItem('theme', 'dark');
            themeToggle.innerHTML = '<i class="fas fa-sun"></i>';
        }
    });

    // AI Assistant
    const aiQuestion = document.getElementById('aiQuestion');
    const aiSubmit = document.getElementById('aiSubmit');
    const aiChat = document.getElementById('aiChat');

    aiSubmit.addEventListener('click', sendAIQuestion);
    aiQuestion.addEventListener('keypress', (e) => {
        if (e.key === 'Enter') sendAIQuestion();
    });

    function sendAIQuestion() {
        const question = aiQuestion.value.trim();
        if (!question) return;

        const userMessage = document.createElement('div');
        userMessage.className = 'ai-message';
        userMessage.textContent = question;
        aiChat.appendChild(userMessage);
        aiQuestion.value = '';
        aiChat.scrollTop = aiChat.scrollHeight;

        setTimeout(() => {
            const responses = [
                "Thank you for your question! Our team will review it and provide a detailed response.",
                "That's an excellent question! You can find more information in our FAQ section, or I can connect you with an advisor.",
                "We're currently reviewing your question. One of our advisors will respond shortly.",
                "Great question! Here's some general guidance... Would you like me to connect you with someone for more specific details?"
            ];
            const randomIndex = Math.floor(Math.random() * responses.length);

            const aiResponse = document.createElement('div');
            aiResponse.className = 'ai-message ai-response';
            aiResponse.textContent = responses[randomIndex];
            aiChat.appendChild(aiResponse);
            aiChat.scrollTop = aiChat.scrollHeight;
        }, 1500);
    }

    // Minimize AI Assistant
    document.getElementById('minimizeBtn').addEventListener('click', () => {
        document.getElementById('aiAssistant').style.display = 'none';
    });

    // Show AI Assistant again
    document.getElementById('aiSubmit').addEventListener('click', () => {
        document.getElementById('aiAssistant').style.display = 'flex';
    });

    // Live Chat Button
    const liveChatBtn = document.getElementById('liveChatBtn');
    const liveChatWidget = document.getElementById('liveChatWidget');
    const closeChatBtn = document.getElementById('closeChatBtn');
    const sendChatBtn = document.getElementById('sendChatBtn');
    const chatMessage = document.getElementById('chatMessage');
    const chatBody = document.getElementById('chatBody');

    liveChatBtn.addEventListener('click', () => {
        liveChatWidget.classList.toggle('active');
    });

    closeChatBtn.addEventListener('click', () => {
        liveChatWidget.classList.remove('active');
    });

    sendChatBtn.addEventListener('click', sendChatMessage);
    chatMessage.addEventListener('keypress', (e) => {
        if (e.key === 'Enter') {
            sendChatMessage();
        }
    });

    function sendChatMessage() {
        const message = chatMessage.value.trim();
        if (message) {
            const userMessageEl = document.createElement('div');
            userMessageEl.className = 'chat-message user';
            userMessageEl.innerHTML = `<strong>You:</strong> ${message}`;
            chatBody.appendChild(userMessageEl);
            chatMessage.value = '';
            chatBody.scrollTop = chatBody.scrollHeight;

            setTimeout(() => {
                const responses = [
                    "Thank you for your message. An admissions officer will reply shortly.",
                    "For information about application deadlines, please visit our admissions page.",
                    "Our typical response time is 1-2 business days.",
                    "Would you like us to email you more information about our programs?"
                ];
                const randomIndex = Math.floor(Math.random() * responses.length);

                const aiResponse = document.createElement('div');
                aiResponse.className = 'chat-message agent';
                aiResponse.innerHTML = `<strong>Admissions Officer:</strong> ${responses[randomIndex]}`;
                chatBody.appendChild(aiResponse);
                chatBody.scrollTop = chatBody.scrollHeight;
            }, 1500);
        }
    }
</script>

</body>
</html>
```
