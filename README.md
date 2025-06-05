I'll implement all the requested features in your HTML code, incorporating African images where appropriate. Here's the complete implementation:

```html
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EYECAB International University | The Future of Higher Education</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Raleway:wght@300;400;600&display=swap" rel="stylesheet">
    <!-- Add required libraries -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
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
        
        /* Dark mode variables */
        [data-theme="dark"] {
            --primary: #3E92CC;
            --secondary: #0A2463;
            --light: #1A1A1A;
            --dark: #FFF9F0;
            --accent: #FFD700;
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
        
        /* Header Styles */
        header {
            background-color: rgba(10, 36, 99, 0.95);
            color: white;
            padding: 1.5rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            transition: all 0.3s ease;
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
            backdrop-filter: blur(8px);
        }
        
        header.scrolled {
            padding: 1rem 0;
            background-color: rgba(10, 36, 99, 0.98);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
        }
        
        .logo-icon {
            font-size: 2.5rem;
            color: var(--accent);
            margin-right: 15px;
        }
        
        .logo-text {
            font-family: var(--font-heading);
        }
        
        .logo-text h1 {
            font-size: 1.8rem;
            font-weight: 700;
            line-height: 1.2;
            color: white;
        }
        
        .logo-text p {
            font-size: 0.7rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            opacity: 0.8;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 2rem;
            position: relative;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            font-size: 1rem;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            padding: 0.5rem 0;
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
        
        nav ul li a.active {
            color: var(--accent);
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
            position: relative;
            z-index: 1001;
        }
        
        /* Mobile menu styles */
        .mobile-menu {
            position: fixed;
            top: 0;
            right: -100%;
            width: 80%;
            max-width: 400px;
            height: 100vh;
            background-color: var(--primary);
            z-index: 1000;
            transition: right 0.3s ease;
            padding: 5rem 2rem;
            overflow-y: auto;
        }
        
        .mobile-menu.active {
            right: 0;
        }
        
        .mobile-menu ul {
            list-style: none;
        }
        
        .mobile-menu li {
            margin-bottom: 1.5rem;
        }
        
        .mobile-menu a {
            color: white;
            text-decoration: none;
            font-size: 1.2rem;
            display: block;
            padding: 0.5rem 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .mobile-menu a:hover {
            color: var(--accent);
        }
        
        .close-menu-btn {
            position: absolute;
            top: 1.5rem;
            right: 1.5rem;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Dark mode toggle */
        .theme-toggle {
            background: none;
            border: none;
            color: white;
            font-size: 1.2rem;
            cursor: pointer;
            margin-left: 1rem;
            transition: transform 0.3s ease;
        }
        
        .theme-toggle:hover {
            transform: rotate(30deg);
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            min-height: 800px;
            background: linear-gradient(rgba(10, 36, 99, 0.7), rgba(10, 36, 99, 0.7)), 
                        url('https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            display: flex;
            align-items: center;
            text-align: center;
            padding-top: 80px;
        }
        
        .hero-content {
            max-width: 900px;
            margin: 0 auto;
            padding: 0 2rem;
        }
        
        .hero h1 {
            font-family: var(--font-heading);
            font-size: 4rem;
            margin-bottom: 1.5rem;
            line-height: 1.2;
            text-shadow: 2px 2px 8px rgba(0,0,0,0.3);
            animation: fadeInUp 1s ease;
        }
        
        .hero p {
            font-size: 1.5rem;
            margin-bottom: 2.5rem;
            opacity: 0.9;
            animation: fadeInUp 1s ease 0.2s forwards;
            opacity: 0;
        }
        
        .hero-btns {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            animation: fadeInUp 1s ease 0.4s forwards;
            opacity: 0;
        }
        
        .btn {
            display: inline-block;
            padding: 1rem 2.5rem;
            border-radius: 50px;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            letter-spacing: 1px;
        }
        
        .btn-primary {
            background-color: var(--accent);
            color: var(--primary);
            box-shadow: 0 4px 15px rgba(255, 215, 0, 0.3);
        }
        
        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(255, 215, 0, 0.4);
        }
        
        .btn-outline {
            border: 2px solid white;
            color: white;
        }
        
        .btn-outline:hover {
            background-color: white;
            color: var(--primary);
            transform: translateY(-3px);
        }
        
        /* About Section */
        .section {
            padding: 8rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 5rem;
        }
        
        .section-title h2 {
            font-family: var(--font-heading);
            font-size: 3rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
            margin-bottom: 1.5rem;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background-color: var(--accent);
        }
        
        .section-title p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto;
            color: #555;
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }
        
        .about-text h3 {
            font-family: var(--font-heading);
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }
        
        .about-text p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            line-height: 1.8;
        }
        
        .about-features {
            margin-top: 2rem;
        }
        
        .feature-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 1.5rem;
        }
        
        .feature-icon {
            font-size: 1.5rem;
            color: var(--accent);
            margin-right: 1rem;
            margin-top: 0.3rem;
        }
        
        .feature-text h4 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: var(--primary);
        }
        
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
        
        /* Schools Section */
        .schools {
            background-color: #f8f9fa;
        }
        
        .schools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .school-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
        }
        
        .school-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
        }
        
        .school-card-img {
            height: 200px;
            overflow: hidden;
        }
        
        .school-card-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .school-card:hover .school-card-img img {
            transform: scale(1.1);
        }
        
        .school-card-content {
            padding: 2rem;
        }
        
        .school-card-content h3 {
            font-family: var(--font-heading);
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .school-card-content p {
            margin-bottom: 1.5rem;
            color: #666;
        }
        
        .school-card-link {
            display: inline-flex;
            align-items: center;
            color: var(--secondary);
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .school-card-link i {
            margin-left: 0.5rem;
            transition: transform 0.3s ease;
        }
        
        .school-card-link:hover {
            color: var(--primary);
        }
        
        .school-card-link:hover i {
            transform: translateX(5px);
        }
        
        /* Stats Section */
        .stats {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 6rem 0;
            text-align: center;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 2rem;
        }
        
        .stat-item {
            padding: 2rem;
        }
        
        .stat-number {
            font-family: var(--font-heading);
            font-size: 3.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            color: var(--accent);
        }
        
        .stat-label {
            font-size: 1.2rem;
            letter-spacing: 1px;
            opacity: 0.9;
        }
        
        /* Testimonials */
        .testimonials {
            position: relative;
            padding: 8rem 0;
            background-color: var(--light);
        }
        
        .testimonial-slider {
            max-width: 1000px;
            margin: 0 auto;
            position: relative;
        }
        
        .testimonial-card {
            background-color: white;
            border-radius: 10px;
            padding: 3rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            text-align: center;
            margin: 0 1rem;
            transition: all 0.3s ease;
        }
        
        .testimonial-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
        }
        
        .testimonial-quote {
            font-size: 1.2rem;
            font-style: italic;
            color: #555;
            margin-bottom: 2rem;
            line-height: 1.8;
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
        
        .testimonial-author {
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .testimonial-author-img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            overflow: hidden;
            margin-right: 1rem;
        }
        
        .testimonial-author-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .testimonial-author-info h4 {
            font-family: var(--font-heading);
            color: var(--primary);
            margin-bottom: 0.3rem;
        }
        
        .testimonial-author-info p {
            color: #777;
            font-size: 0.9rem;
        }
        
        /* Slick slider customization */
        .slick-dots {
            bottom: -50px;
        }
        
        .slick-dots li button:before {
            font-size: 12px;
            color: var(--primary);
        }
        
        .slick-dots li.slick-active button:before {
            color: var(--accent);
        }
        
        .slick-prev, .slick-next {
            width: 40px;
            height: 40px;
            z-index: 1;
        }
        
        .slick-prev:before, .slick-next:before {
            font-size: 40px;
            color: var(--primary);
        }
        
        .slick-prev {
            left: -50px;
        }
        
        .slick-next {
            right: -50px;
        }
        
        /* CTA Section */
        .cta {
            background: linear-gradient(rgba(10, 36, 99, 0.9), rgba(10, 36, 99, 0.9)), 
                        url('https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
            text-align: center;
            padding: 8rem 0;
        }
        
        .cta h2 {
            font-family: var(--font-heading);
            font-size: 3rem;
            margin-bottom: 2rem;
        }
        
        .cta p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 3rem;
            opacity: 0.9;
        }
        
        /* Contact Form Section */
        .contact {
            padding: 8rem 0;
            background-color: #f8f9fa;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }
        
        .contact-info {
            margin-bottom: 2rem;
        }
        
        .contact-info h3 {
            font-family: var(--font-heading);
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }
        
        .contact-info p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            line-height: 1.8;
        }
        
        .contact-details {
            margin-top: 2rem;
        }
        
        .contact-item {
            display: flex;
            align-items: flex-start;
            margin-bottom: 1.5rem;
        }
        
        .contact-icon {
            font-size: 1.5rem;
            color: var(--accent);
            margin-right: 1rem;
            margin-top: 0.3rem;
        }
        
        .contact-form {
            background-color: white;
            padding: 3rem;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--primary);
        }
        
        .form-control {
            width: 100%;
            padding: 1rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: var(--font-body);
            font-size: 1rem;
            transition: all 0.3s ease;
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--secondary);
            box-shadow: 0 0 0 3px rgba(62, 146, 204, 0.2);
        }
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        .form-submit {
            background-color: var(--accent);
            color: var(--primary);
            border: none;
            padding: 1rem 2.5rem;
            font-size: 1rem;
            font-weight: 600;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .form-submit:hover {
            background-color: var(--primary);
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(10, 36, 99, 0.3);
        }
        
        /* Tuition Calculator Section */
        .calculator {
            padding: 8rem 0;
            background-color: var(--light);
        }
        
        .calculator-container {
            max-width: 800px;
            margin: 0 auto;
            background-color: white;
            padding: 3rem;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
        }
        
        .calculator h3 {
            font-family: var(--font-heading);
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
            text-align: center;
        }
        
        .calculator-form .form-group {
            margin-bottom: 2rem;
        }
        
        .calculator-result {
            margin-top: 2rem;
            padding: 1.5rem;
            background-color: #f8f9fa;
            border-radius: 5px;
            text-align: center;
            display: none;
        }
        
        .calculator-result h4 {
            font-family: var(--font-heading);
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .calculator-result p {
            font-size: 1.5rem;
            font-weight: 600;
            color: var(--secondary);
        }
        
        /* Program Filter Section */
        .programs {
            padding: 8rem 0;
            background-color: #f8f9fa;
        }
        
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
        
        .filter-btn:hover, .filter-btn.active {
            background-color: var(--primary);
            color: white;
            border-color: var(--primary);
        }
        
        .programs-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .program-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
            display: none; /* Hidden by default, shown by filter */
        }
        
        .program-card.active {
            display: block;
        }
        
        .program-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
        }
        
        .program-card-img {
            height: 200px;
            overflow: hidden;
        }
        
        .program-card-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .program-card:hover .program-card-img img {
            transform: scale(1.1);
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
        
        .program-meta {
            display: flex;
            justify-content: space-between;
            margin-bottom: 1.5rem;
            font-size: 0.9rem;
            color: #777;
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
        
        /* Virtual Tour Section */
        .virtual-tour {
            padding: 8rem 0;
            text-align: center;
        }
        
        .tour-container {
            max-width: 1000px;
            margin: 0 auto;
            position: relative;
        }
        
        .tour-iframe {
            width: 100%;
            height: 500px;
            border: none;
            border-radius: 10px;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.1);
        }
        
        .tour-controls {
            margin-top: 2rem;
            display: flex;
            justify-content: center;
            gap: 1rem;
        }
        
        /* Admissions Section */
        .admissions {
            padding: 8rem 0;
            background-color: #f8f9fa;
        }
        
        .admissions-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }
        
        .admissions-form {
            background-color: white;
            padding: 3rem;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
        }
        
        .admissions-info h3 {
            font-family: var(--font-heading);
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }
        
        .admissions-info p {
            margin-bottom: 1.5rem;
            font-size: 1.1rem;
            line-height: 1.8;
        }
        
        /* AI Assistant Section */
        .ai-assistant {
            padding: 8rem 0;
            background-color: var(--light);
            text-align: center;
        }
        
        .ai-container {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .ai-chat {
            background-color: white;
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            margin-bottom: 2rem;
            min-height: 300px;
            text-align: left;
        }
        
        .ai-message {
            margin-bottom: 1rem;
            padding: 1rem;
            border-radius: 5px;
            background-color: #f8f9fa;
        }
        
        .ai-message.ai-response {
            background-color: #e9f7fe;
        }
        
        .ai-input {
            display: flex;
            gap: 1rem;
        }
        
        .ai-input input {
            flex: 1;
            padding: 1rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: var(--font-body);
        }
        
        .ai-input button {
            background-color: var(--accent);
            color: var(--primary);
            border: none;
            padding: 1rem 1.5rem;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .ai-input button:hover {
            background-color: var(--primary);
            color: white;
        }
   /* Live Chat Widget */
        .live-chat-btn {
            position: fixed;
            bottom: 2rem;
            right: 2rem;
            width: 60px;
            height: 60px;
            background-color: var(--accent);
            color: var(--primary);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.2);
            cursor: pointer;
            z-index: 999;
            transition: all 0.3s ease;
        }
        
        .live-chat-btn:hover {
            transform: scale(1.1);
        }
        
        .live-chat-widget {
            position: fixed;
            bottom: 8rem;
            right: 2rem;
            width: 350px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            z-index: 1000;
            overflow: hidden;
            transform: translateY(20px);
            opacity: 0;
            visibility: hidden;
            transition: all 0.3s ease;
        }
        
        .live-chat-widget.active {
            transform: translateY(0);
            opacity: 1;
            visibility: visible;
        }
        
        .chat-header {
            background-color: var(--primary);
            color: white;
            padding: 1rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .chat-header h4 {
            margin: 0;
            font-size: 1.2rem;
        }
        
        .close-chat {
            background: none;
            border: none;
            color: white;
            font-size: 1.2rem;
            cursor: pointer;
        }
        
        .chat-body {
            padding: 1rem;
            height: 300px;
            overflow-y: auto;
        }
        
        .chat-message {
            margin-bottom: 1rem;
            padding: 0.8rem;
            border-radius: 5px;
            max-width: 80%;
        }
        
        .chat-message.user {
            background-color: #e9f7fe;
            margin-left: auto;
        }
        
        .chat-message.agent {
            background-color: #f1f1f1;
            margin-right: auto;
        }
        
        .chat-input {
            display: flex;
            padding: 1rem;
            border-top: 1px solid #eee;
        }
        
        .chat-input input {
            flex: 1;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            margin-right: 0.5rem;
        }
        
        .chat-input button {
            background-color: var(--accent);
            color: var(--primary);
            border: none;
            padding: 0 1rem;
            border-radius: 5px;
            cursor: pointer;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 5rem 0 2rem;
        }
        
        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            margin-bottom: 3rem;
        }
        
        .footer-col h3 {
            font-family: var(--font-heading);
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
            color: var(--accent);
        }
        
        .footer-col p {
            margin-bottom: 1rem;
            opacity: 0.8;
        }
        
        .footer-links {
            list-style: none;
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
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            color: white;
            font-size: 1.2rem;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: var(--accent);
            color: var(--primary);
            transform: translateY(-3px);
        }
        
        .footer-bottom {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            opacity: 0.7;
            font-size: 0.9rem;
        }
        
        /* Loading Optimizations */
        .lazy-load {
            opacity: 0;
            transition: opacity 0.5s ease;
        }
        
        .lazy-load.loaded {
            opacity: 1;
        }
        
        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        /* Responsive Styles */
        @media (max-width: 1200px) {
            .hero h1 {
                font-size: 3.5rem;
            }
            
            .stats-container {
                grid-template-columns: repeat(2, 1fr);
            }
        }
        
        @media (max-width: 992px) {
            .about-content, 
            .contact-container,
            .admissions-container {
                grid-template-columns: 1fr;
            }
            
            .about-image,
            .contact-form,
            .admissions-form {
                max-width: 600px;
                margin: 0 auto;
            }
            
            .hero h1 {
                font-size: 3rem;
            }
            
            .hero p {
                font-size: 1.3rem;
            }
            
            .section-title h2 {
                font-size: 2.5rem;
            }
        }
        
        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            nav {
                display: none;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .hero-btns {
                flex-direction: column;
                gap: 1rem;
            }
            
            .btn {
                width: 100%;
            }
            
            .section {
                padding: 5rem 0;
            }
            
            .section-title h2 {
                font-size: 2.2rem;
            }
            
            .cta h2 {
                font-size: 2.2rem;
            }
            
            .live-chat-widget {
                width: 90%;
                right: 5%;
                bottom: 7rem;
            }
        }
        
        @media (max-width: 576px) {
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .stats-container {
                grid-template-columns: 1fr;
            }
            
            .stat-item {
                padding: 1.5rem;
            }
            
            .footer-container {
                grid-template-columns: 1fr;
            }
            
            .tour-iframe {
                height: 300px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="container header-container">
            <a href="#" class="logo">
                <div class="logo-icon">
                    <i class="fas fa-university"></i>
                </div>
                <div class="logo-text">
                    <h1>EYECAB INTERNATIONAL UNIVERSITY</h1>
                    <p>Redefining Global Higher Education</p>
                </div>
            </a>

            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <i class="fas fa-bars"></i>
            </button>

            <nav id="mainNav">
                <ul>
                    <li><a href="#home" class="active">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#programs">Programs</a></li>
                    <li><a href="#admissions">Admissions</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>

            <button class="theme-toggle" id="themeToggle">
                <i class="fas fa-moon"></i>
            </button>
        </div>
    </header>

    <!-- Mobile Menu -->
    <div class="mobile-menu" id="mobileMenu">
        <button class="close-menu-btn" id="closeMenuBtn">
            <i class="fas fa-times"></i>
        </button>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#programs">Programs</a></li>
            <li><a href="#admissions">Admissions</a></li>
            <li><a href="#contact">Contact</a></li>
            <li><a href="#virtual-tour">Virtual Tour</a></li>
            <li><a href="#calculator">Tuition Calculator</a></li>
        </ul>
    </div>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Shaping Africa's Future Through Excellence in Education</h1>
            <p>Join a vibrant community of scholars and innovators at one of Africa's leading universities</p>
            <div class="hero-btns">
                <a href="#programs" class="btn btn-primary">Explore Programs</a>
                <a href="#admissions" class="btn btn-outline">Apply Now</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="section" id="about">
        <div class="container">
            <div class="section-title">
                <h2>About EYECAB University</h2>
                <p>Founded in 1995, EYECAB International University has grown to become a beacon of academic excellence in Africa, fostering innovation and leadership.</p>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Our Vision for African Higher Education</h3>
                    <p>EYECAB International University is committed to transforming Africa through education that combines academic rigor with practical skills development. Our interdisciplinary approach prepares students to tackle real-world challenges.</p>
                    <p>With campuses in five African countries and partnerships with leading global institutions, we offer a truly international educational experience rooted in African values and perspectives.</p>
                    <div class="about-features">
                        <div class="feature-item">
                            <div class="feature-icon">
                                <i class="fas fa-graduation-cap"></i>
                            </div>
                            <div class="feature-text">
                                <h4>World-Class Faculty</h4>
                                <p>Learn from distinguished professors and industry leaders from across Africa and the world.</p>
                            </div>
                        </div>
                        <div class="feature-item">
                            <div class="feature-icon">
                                <i class="fas fa-flask"></i>
                            </div>
                            <div class="feature-text">
                                <h4>Cutting-Edge Research</h4>
                                <p>Participate in groundbreaking research projects addressing Africa's most pressing challenges.</p>
                            </div>
                        </div>
                        <div class="feature-item">
                            <div class="feature-icon">
                                <i class="fas fa-globe-africa"></i>
                            </div>
                            <div class="feature-text">
                                <h4>Global Network</h4>
                                <p>Join a diverse community of students and alumni from over 50 countries worldwide.</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="about-image lazy-load">
                    <img src="https://images.unsplash.com/photo-1523050854058-8df90110c9f1?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="EYECAB University Campus" loading="lazy">
                </div>
            </div>
        </div>
    </section>

    <!-- Schools Section -->
    <section class="section schools">
        <div class="container">
            <div class="section-title">
                <h2>Our Academic Schools</h2>
                <p>Explore our diverse range of academic schools, each offering innovative programs designed to meet the needs of today's global economy.</p>
            </div>
            <div class="schools-grid">
                <div class="school-card">
                    <div class="school-card-img">
                        <img src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="School of Business" loading="lazy">
                    </div>
                    <div class="school-card-content">
                        <h3>School of Business & Economics</h3>
                        <p>Develop the skills to lead in Africa's growing economies with our internationally accredited business programs.</p>
                        <a href="#" class="school-card-link">Explore Programs <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                <div class="school-card">
                    <div class="school-card-img">
                        <img src="https://images.unsplash.com/photo-1532094349884-543bc11b234d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="School of Engineering" loading="lazy">
                    </div>
                    <div class="school-card-content">
                        <h3>School of Engineering & Technology</h3>
                        <p>Innovate solutions for Africa's infrastructure challenges with our hands-on engineering programs.</p>
                        <a href="#" class="school-card-link">Explore Programs <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                <div class="school-card">
                    <div class="school-card-img">
                        <img src="https://images.unsplash.com/photo-1576091160550-2173dba999ef?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="School of Health Sciences" loading="lazy">
                    </div>
                    <div class="school-card-content">
                        <h3>School of Health Sciences</h3>
                        <p>Train to meet Africa's healthcare needs with our world-class medical and health sciences programs.</p>
                        <a href="#" class="school-card-link">Explore Programs <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <div class="container stats-container">
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
    </section>

    <!-- Program Filter Section -->
    <section class="section programs" id="programs">
        <div class="container">
            <div class="section-title">
                <h2>Our Academic Programs</h2>
                <p>Discover our comprehensive range of undergraduate and graduate programs designed to prepare you for success in today's dynamic world.</p>
            </div>
            
            <div class="filter-controls">
                <button class="filter-btn active" data-filter="all">All Programs</button>
                <button class="filter-btn" data-filter="undergraduate">Undergraduate</button>
                <button class="filter-btn" data-filter="graduate">Graduate</button>
                <button class="filter-btn" data-filter="business">Business</button>
                <button class="filter-btn" data-filter="engineering">Engineering</button>
                <button class="filter-btn" data-filter="health">Health Sciences</button>
            </div>
            
            <div class="programs-grid">
                <!-- Undergraduate Programs -->
                <div class="program-card active" data-category="undergraduate business">
                    <div class="program-card-img">
                        <img src="https://images.unsplash.com/photo-1554224155-6726b3ff858f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Business Administration" loading="lazy">
                    </div>
                    <div class="program-card-content">
                        <h3>BSc Business Administration</h3>
                        <div class="program-meta">
                            <span><i class="fas fa-clock"></i> 4 Years</span>
                            <span><i class="fas fa-money-bill-wave"></i> $3,500/year</span>
                        </div>
                        <p>Develop leadership and management skills for Africa's growing business landscape with our comprehensive business program.</p>
                        <a href="#" class="program-card-link">Learn More <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                
                <div class="program-card active" data-category="undergraduate engineering">
                    <div class="program-card-img">
                        <img src="https://images.unsplash.com/photo-1517430816045-df4b7de11d1d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Computer Engineering" loading="lazy">
                    </div>
                    <div class="program-card-content">
                        <h3>BEng Computer Engineering</h3>
                        <div class="program-meta">
                            <span><i class="fas fa-clock"></i> 4 Years</span>
                            <span><i class="fas fa-money-bill-wave"></i> $4,200/year</span>
                        </div>
                        <p>Master the design and implementation of computing systems with our hands-on engineering program.</p>
                        <a href="#" class="program-card-link">Learn More <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                
                <div class="program-card active" data-category="undergraduate health">
                    <div class="program-card-img">
                        <img src="https://images.unsplash.com/photo-1579684385127-1ef15d508118?ixlib=rb-1.2.1&auto=format&
