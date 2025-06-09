<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>EYECAB International University | Application Form</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Raleway:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
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
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
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
        
        /* Application Form Section */
        .application-section {
            padding: 10rem 0 5rem;
            background-color: #f8f9fa;
        }
        
        .application-container {
            max-width: 1000px;
            margin: 0 auto;
            background: white;
            padding: 3rem;
            box-shadow: 0 0 20px rgba(0,0,0,0.1);
            border-radius: 8px;
        }
        
        .application-header {
            text-align: center;
            margin-bottom: 3rem;
            border-bottom: 2px solid var(--secondary);
            padding-bottom: 2rem;
        }
        
        .application-header h1 {
            font-family: var(--font-heading);
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .application-header h2 {
            font-family: var(--font-heading);
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        
        .application-header p {
            color: #666;
            font-size: 1.1rem;
        }
        
        .form-group {
            margin-bottom: 2rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.8rem;
            font-weight: 600;
            color: var(--primary);
        }
        
        .form-group label.required:after {
            content: " *";
            color: red;
        }
        
        input[type="text"],
        input[type="email"],
        input[type="tel"],
        input[type="date"],
        input[type="number"],
        select,
        textarea {
            width: 100%;
            padding: 1rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-family: var(--font-body);
            font-size: 1rem;
            transition: all 0.3s ease;
        }
        
        input:focus,
        select:focus,
        textarea:focus {
            outline: none;
            border-color: var(--secondary);
            box-shadow: 0 0 0 3px rgba(62, 146, 204, 0.2);
        }
        
        .row {
            display: flex;
            flex-wrap: wrap;
            margin: 0 -1rem;
        }
        
        .col {
            flex: 1;
            padding: 0 1rem;
            min-width: 200px;
        }
        
        .btn-submit {
            background-color: var(--accent);
            color: var(--primary);
            padding: 1.2rem 2.5rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 600;
            display: block;
            margin: 3rem auto 0;
            transition: all 0.3s ease;
        }
        
        .btn-submit:hover {
            background-color: var(--primary);
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(10, 36, 99, 0.3);
        }
        
        .fee-info {
            background-color: #e9f7fe;
            padding: 1.5rem;
            border-radius: 4px;
            margin: 2rem 0;
            border-left: 4px solid var(--secondary);
        }
        
        .warning {
            background-color: #fff3cd;
            padding: 1.5rem;
            border-radius: 4px;
            margin: 2rem 0;
            border-left: 4px solid #ffc107;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 2rem 0;
        }
        
        th, td {
            border: 1px solid #ddd;
            padding: 1rem;
            text-align: left;
        }
        
        th {
            background-color: #f2f2f2;
        }
        
        .course-selection {
            max-height: 300px;
            overflow-y: auto;
            border: 1px solid #ddd;
            padding: 1rem;
            margin-bottom: 2rem;
            border-radius: 4px;
        }
        
        .course-option {
            margin-bottom: 1rem;
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
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            nav {
                display: none;
            }
            
            .col {
                flex: 100%;
                margin-bottom: 1.5rem;
            }
            
            .application-container {
                padding: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="container header-container">
            <a href="index.html" class="logo">
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
                    <li><a href="index.html">Home</a></li>
                    <li><a href="index.html#about">About</a></li>
                    <li><a href="index.html#programs">Programs</a></li>
                    <li><a href="application.html" class="active">Apply Now</a></li>
                    <li><a href="index.html#contact">Contact</a></li>
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
            <li><a href="index.html">Home</a></li>
            <li><a href="index.html#about">About</a></li>
            <li><a href="index.html#programs">Programs</a></li>
            <li><a href="application.html" class="active">Apply Now</a></li>
            <li><a href="index.html#contact">Contact</a></li>
            <li><a href="index.html#virtual-tour">Virtual Tour</a></li>
            <li><a href="index.html#calculator">Tuition Calculator</a></li>
        </ul>
    </div>

    <!-- Application Form Section -->
    <section class="application-section">
        <div class="application-container">
            <div class="application-header">
                <img src="https://via.placeholder.com/150x50?text=Eyecab+University" alt="Eyecab International University Logo" class="logo">
                <h1>Eyecab International University</h1>
                <h2>Undergraduate Application Form</h2>
                <p>2024/2025 Academic Year - Private Admissions</p>
            </div>

            <form id="applicationForm">
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
                            <label for="middleName">Middle Name</label>
                            <input type="text" id="middleName" name="middleName">
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
                    <div class="col">
                        <div class="form-group">
                            <label for="nationality" class="required">Nationality</label>
                            <input type="text" id="nationality" name="nationality" required>
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
                            <input type="text" id="uaceGrade3" name="uaceGrade3">
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
                        <option value="business-school">Business School</option>
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
                    </select>
                </div>

                <div class="form-group">
                    <label for="secondChoice">Second Choice Programme (Optional)</label>
                    <select id="secondChoice" name="secondChoice">
                        <option value="">Select Second Choice</option>
                        <!-- Same options as above -->
                    </select>
                </div>

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

                <button type="submit" class="btn-submit">Submit Application</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-container">
                <div class="footer-col">
                    <h3>About EYECAB</h3>
                    <p>EYECAB International University is a leading institution of higher education in Africa, committed to academic excellence, research innovation, and community engagement.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                
                <div class="footer-col">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="index.html">Home</a></li>
                        <li><a href="index.html#about">About Us</a></li>
                        <li><a href="index.html#programs">Programs</a></li>
                        <li><a href="application.html">Admissions</a></li>
                        <li><a href="index.html#contact">Contact</a></li>
                    </ul>
                </div>
                
                <div class="footer-col">
                    <h3>Academic</h3>
                    <ul class="footer-links">
                        <li><a href="#">Schools & Departments</a></li>
                        <li><a href="#">Academic Calendar</a></li>
                        <li><a href="#">Library</a></li>
                        <li><a href="#">Research Centers</a></li>
                        <li><a href="#">Online Learning</a></li>
                    </ul>
                </div>
                
                <div class="footer-col">
                    <h3>Resources</h3>
                    <ul class="footer-links">
                        <li><a href="#">Student Portal</a></li>
                        <li><a href="#">Faculty Portal</a></li>
                        <li><a href="#">Alumni Network</a></li>
                        <li><a href="#">Career Services</a></li>
                        <li><a href="#">News & Events</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2023 EYECAB International University. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        const mobileMenuBtn = document.getElementById('mobileMenuBtn');
        const closeMenuBtn = document.getElementById('closeMenuBtn');
        const mobileMenu = document.getElementById('mobileMenu');
        
        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.add('active');
        });
        
        closeMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.remove('active');
        });
        
        // Close mobile menu when clicking on a link
        document.querySelectorAll('.mobile-menu a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.remove('active');
            });
        });
        
        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
        
        // Dark Mode Toggle
        const themeToggle = document.getElementById('themeToggle');
        const prefersDarkScheme = window.matchMedia('(prefers-color-scheme: dark)');
        
        const currentTheme = localStorage.getItem('theme');
        if (currentTheme === 'dark' || (!currentTheme && prefersDarkScheme.matches)) {
            document.body.setAttribute('data-theme', 'dark');
            themeToggle.innerHTML = '<i class="fas fa-sun"></i>';
        }
        
        themeToggle.addEventListener('click', () => {
            if (document.body.getAttribute('data-theme') === 'dark') {
                document.body.removeAttribute('data-theme');
                themeToggle.innerHTML = '<i class="fas fa-moon"></i>';
                localStorage.setItem('theme', 'light');
            } else {
                document.body.setAttribute('data-theme', 'dark');
                themeToggle.innerHTML = '<i class="fas fa-sun"></i>';
                localStorage.setItem('theme', 'dark');
            }
        });
        
        // Application Form Functionality
        document.addEventListener('DOMContentLoaded', function() {
            // Update payment details based on payment method
            const paymentMethod = document.getElementById('paymentMethod');
            const paymentDetails = document.getElementById('paymentDetails');
            
            paymentMethod.addEventListener('change', function() {
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
                } else {
                    paymentDetails.innerHTML = '';
                }
            });
            
            // Filter programmes based on college selection
            const collegeSelect = document.getElementById('college');
            const programmeSelect = document.getElementById('programme');
            const secondChoiceSelect = document.getElementById('secondChoice');
            
            collegeSelect.addEventListener('change', function() {
                const selectedCollege = this.value;
                
                // Enable all options first
                for (let i = 0; i < programmeSelect.options.length; i++) {
                    programmeSelect.options[i].style.display = '';
                }
                
                // Hide options that don't match the selected college
                if (selectedCollege) {
                    for (let i = 0; i < programmeSelect.options.length; i++) {
                        const option = programmeSelect.options[i];
                        if (option.value && option.dataset.college !== selectedCollege) {
                            option.style.display = 'none';
                        }
                    }
                }
                
                // Reset the selection
                programmeSelect.value = '';
            });
            
            // Copy all programme options to second choice select
            for (let i = 0; i < programmeSelect.options.length; i++) {
                const option = programmeSelect.options[i];
                secondChoiceSelect.add(new Option(option.text, option.value));
            }
            
            // Form submission handler
            document.getElementById('applicationForm').addEventListener('submit', function(e) {
                e.preventDefault();
                alert('Application submitted successfully!');
                // In a real application, you would send the data to a server here
            });
        });
    </script>
</body>
</html>
