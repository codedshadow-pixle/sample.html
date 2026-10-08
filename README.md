<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Jayesh Godara | BCA Student & Developer</title>

    <meta name="description"
        content="Jayesh Godara - BCA student, developer and learner from Jaipur, Rajasthan.">

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap"
        rel="stylesheet">

    <style>
        :root {
            --bg: #070a12;
            --bg-light: #0d1220;
            --card: rgba(17, 24, 39, 0.72);
            --card-solid: #111827;

            --text: #f5f7ff;
            --muted: #9ca7ba;

            --blue: #3b82f6;
            --blue-light: #60a5fa;
            --purple: #8b5cf6;

            --border: rgba(255, 255, 255, 0.08);

            --max-width: 1150px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: "Inter", sans-serif;
            background: var(--bg);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }

        body::before {
            content: "";
            position: fixed;
            width: 500px;
            height: 500px;
            top: -200px;
            left: -200px;
            background: radial-gradient(
                circle,
                rgba(59, 130, 246, 0.12),
                transparent 70%
            );
            pointer-events: none;
            z-index: -1;
        }

        body::after {
            content: "";
            position: fixed;
            width: 500px;
            height: 500px;
            bottom: -250px;
            right: -200px;
            background: radial-gradient(
                circle,
                rgba(139, 92, 246, 0.10),
                transparent 70%
            );
            pointer-events: none;
            z-index: -1;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        button,
        input,
        textarea {
            font-family: inherit;
        }

        .container {
            width: min(92%, var(--max-width));
            margin: auto;
        }

        /* ================= HEADER ================= */

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;

            background: rgba(7, 10, 18, 0.75);
            backdrop-filter: blur(18px);
            -webkit-backdrop-filter: blur(18px);

            border-bottom: 1px solid var(--border);
        }

        .nav {
            height: 75px;

            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            width: 42px;
            height: 42px;

            display: flex;
            align-items: center;
            justify-content: center;

            border-radius: 12px;

            background: linear-gradient(
                135deg,
                var(--blue),
                var(--purple)
            );

            font-size: 19px;
            font-weight: 800;

            box-shadow: 0 10px 30px rgba(59, 130, 246, 0.18);
        }

        .nav-links {
            display: flex;
            gap: 28px;
            list-style: none;
        }

        .nav-links a {
            color: var(--muted);
            font-size: 14px;
            font-weight: 500;

            transition: 0.25s ease;
        }

        .nav-links a:hover {
            color: white;
        }

        .menu-btn {
            display: none;

            background: none;
            border: none;

            color: white;
            font-size: 26px;
            cursor: pointer;
        }

        /* ================= HERO ================= */

        .hero {
            min-height: 100vh;

            display: flex;
            align-items: center;

            padding-top: 110px;
        }

        .hero-grid {
            display: grid;
            grid-template-columns: 1.2fr 0.8fr;
            gap: 70px;
            align-items: center;
        }

        .badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;

            padding: 8px 13px;

            border: 1px solid var(--border);
            border-radius: 50px;

            background: rgba(255, 255, 255, 0.03);

            color: var(--blue-light);

            font-size: 12px;
            font-weight: 600;

            margin-bottom: 22px;
        }

        .badge::before {
            content: "";
            width: 7px;
            height: 7px;

            border-radius: 50%;

            background: #22c55e;
            box-shadow: 0 0 10px rgba(34, 197, 94, 0.6);
        }

        .hero h1 {
            font-size: clamp(45px, 7vw, 78px);
            line-height: 1.03;
            letter-spacing: -3px;

            margin-bottom: 22px;
        }

        .hero h1 span {
            background: linear-gradient(
                90deg,
                var(--blue-light),
                #a78bfa
            );

            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }

        .hero p {
            max-width: 650px;

            color: var(--muted);

            font-size: 17px;
            line-height: 1.8;

            margin-bottom: 30px;
        }

        .buttons {
            display: flex;
            gap: 13px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;

            padding: 12px 20px;

            border-radius: 10px;

            font-size: 14px;
            font-weight: 600;

            border: 1px solid var(--border);

            transition: 0.25s ease;
        }

        .btn-primary {
            background: linear-gradient(
                135deg,
                var(--blue),
                #6366f1
            );

            border-color: transparent;

            box-shadow: 0 10px 30px rgba(59, 130, 246, 0.2);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 15px 35px rgba(59, 130, 246, 0.3);
        }

        .btn-secondary {
            background: rgba(255, 255, 255, 0.03);
        }

        .btn-secondary:hover {
            background: rgba(255, 255, 255, 0.07);
            transform: translateY(-2px);
        }

        /* ================= PROFILE CARD ================= */

        .profile-card {
            position: relative;

            padding: 35px;

            border-radius: 24px;

            background: var(--card);

            border: 1px solid var(--border);

            backdrop-filter: blur(20px);

            box-shadow: 0 25px 80px rgba(0, 0, 0, 0.3);
        }

        .profile-avatar {
            width: 120px;
            height: 120px;

            display: flex;
            align-items: center;
            justify-content: center;

            margin-bottom: 25px;

            border-radius: 30px;

            background: linear-gradient(
                135deg,
                var(--blue),
                var(--purple)
            );

            font-size: 46px;
            font-weight: 800;

            box-shadow: 0 20px 50px rgba(59, 130, 246, 0.25);
        }

        .profile-card h2 {
            font-size: 27px;
            margin-bottom: 5px;
        }

        .profile-card .role {
            color: var(--blue-light);
            font-size: 14px;
            font-weight: 600;
        }

        .profile-card p {
            color: var(--muted);
            margin-top: 18px;
            font-size: 14px;
        }

        .social-links {
            display: flex;
            gap: 10px;
            margin-top: 25px;
        }

        .social-links a {
            padding: 9px 13px;

            border: 1px solid var(--border);
            border-radius: 8px;

            color: var(--muted);

            font-size: 13px;

            transition: 0.25s ease;
        }

        .social-links a:hover {
            color: white;
            border-color: rgba(96, 165, 250, 0.4);
            background: rgba(59, 130, 246, 0.08);
        }

        /* ================= SECTIONS ================= */

        section {
            padding: 100px 0;
        }

        .section-heading {
            max-width: 650px;
            margin-bottom: 50px;
        }

        .section-heading span {
            color: var(--blue-light);

            font-size: 13px;
            font-weight: 700;

            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .section-heading h2 {
            font-size: clamp(30px, 5vw, 45px);

            letter-spacing: -1.5px;

            margin-top: 8px;
        }

        .section-heading p {
            color: var(--muted);
            margin-top: 12px;
        }

        /* ================= STATS ================= */

        .stats {
            display: grid;
            grid-template-columns: repeat(3, 1fr);

            border: 1px solid var(--border);
            border-radius: 18px;

            background: rgba(255, 255, 255, 0.02);

            overflow: hidden;
        }

        .stat {
            padding: 30px;
            text-align: center;

            border-right: 1px solid var(--border);
        }

        .stat:last-child {
            border-right: none;
        }

        .stat h3 {
            font-size: 28px;
            color: white;
        }

        .stat p {
            color: var(--muted);
            font-size: 13px;
        }

        /* ================= ABOUT ================= */

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 25px;
        }

        .card {
            padding: 30px;

            background: var(--card);
            border: 1px solid var(--border);

            border-radius: 18px;

            backdrop-filter: blur(15px);

            transition: 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: rgba(96, 165, 250, 0.2);
        }

        .card h3 {
            margin-bottom: 12px;
            font-size: 20px;
        }

        .card p {
            color: var(--muted);
            font-size: 14px;
            line-height: 1.8;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 9px;

            margin-top: 20px;
        }

        .skill {
            padding: 8px 12px;

            border-radius: 8px;

            background: rgba(59, 130, 246, 0.08);
            border: 1px solid rgba(96, 165, 250, 0.12);

            color: #bfdbfe;

            font-size: 12px;
            font-weight: 600;
        }

        /* ================= SERVICES ================= */

        .services-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 18px;
        }

        .service-icon {
            width: 44px;
            height: 44px;

            display: flex;
            align-items: center;
            justify-content: center;

            margin-bottom: 20px;

            border-radius: 12px;

            background: rgba(59, 130, 246, 0.1);

            color: var(--blue-light);

            font-size: 18px;
        }

        /* ================= PROJECTS ================= */

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        .project-card {
            position: relative;

            min-height: 240px;

            padding: 27px;

            display: flex;
            flex-direction: column;

            background: var(--card);

            border: 1px solid var(--border);
            border-radius: 18px;

            transition: 0.3s ease;

            overflow: hidden;
        }

        .project-card::before {
            content: "";

            position: absolute;

            width: 150px;
            height: 150px;

            top: -80px;
            right: -80px;

            background: radial-gradient(
                circle,
                rgba(59, 130, 246, 0.2),
                transparent 70%
            );
        }

        .project-card:hover {
            transform: translateY(-7px);
            border-color: rgba(96, 165, 250, 0.25);
        }

        .project-number {
            color: var(--blue-light);

            font-size: 12px;
            font-weight: 700;

            margin-bottom: 20px;
        }

        .project-card h3 {
            font-size: 20px;
            margin-bottom: 10px;
        }

        .project-card p {
            color: var(--muted);
            font-size: 13px;
        }

        .project-link {
            margin-top: auto;
            padding-top: 20px;

            color: var(--blue-light);

            font-size: 13px;
            font-weight: 600;
        }

        /* ================= FAQ ================= */

        .faq {
            max-width: 800px;
        }

        .faq-item {
            border-bottom: 1px solid var(--border);
        }

        .faq-question {
            width: 100%;

            padding: 20px 0;

            display: flex;
            justify-content: space-between;
            align-items: center;

            background: none;
            border: none;

            color: white;

            font-size: 15px;
            font-weight: 600;

            text-align: left;

            cursor: pointer;
        }

        .faq-answer {
            max-height: 0;
            overflow: hidden;

            color: var(--muted);

            font-size: 14px;

            transition: 0.3s ease;
        }

        .faq-item.active .faq-answer {
            max-height: 150px;
            padding-bottom: 20px;
        }

        .faq-question span {
            font-size: 22px;
            color: var(--blue-light);

            transition: 0.3s;
        }

        .faq-item.active .faq-question span {
            transform: rotate(45deg);
        }

        /* ================= CONTACT ================= */

        .contact-grid {
            display: grid;
            grid-template-columns: 0.8fr 1.2fr;
            gap: 25px;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 14px;
        }

        .contact-item {
            padding: 18px;

            background: rgba(255, 255, 255, 0.025);

            border: 1px solid var(--border);
            border-radius: 12px;
        }

        .contact-item small {
            display: block;

            color: var(--muted);

            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 1px;

            margin-bottom: 5px;
        }

        .contact-item a,
        .contact-item p {
            font-size: 14px;
            color: white;
        }

        form {
            display: flex;
            flex-direction: column;
            gap: 14px;
        }

        input,
        textarea {
            width: 100%;

            padding: 14px 15px;

            border-radius: 10px;

            background: rgba(255, 255, 255, 0.03);

            border: 1px solid var(--border);

            color: white;

            outline: none;

            transition: 0.25s;
        }

        input:focus,
        textarea:focus {
            border-color: rgba(96, 165, 250, 0.5);
            background: rgba(255, 255, 255, 0.05);
        }

        textarea {
            min-height: 150px;
            resize: vertical;
        }

        /* ================= FOOTER ================= */

        footer {
            padding: 30px 0;

            border-top: 1px solid var(--border);

            color: var(--muted);

            font-size: 13px;
        }

        .footer-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 20px;
        }

        .footer-links {
            display: flex;
            gap: 18px;
        }

        .footer-links a:hover {
            color: white;
        }

        /* ================= ANIMATION ================= */

        .reveal {
            opacity: 0;
            transform: translateY(20px);

            transition:
                opacity 0.7s ease,
                transform 0.7s ease;
        }

        .reveal.show {
            opacity: 1;
            transform: translateY(0);
        }

        /* ================= RESPONSIVE ================= */

        @media (max-width: 850px) {

            .menu-btn {
                display: block;
            }

            .nav-links {
                position: absolute;

                top: 75px;
                left: 0;

                width: 100%;

                display: none;
                flex-direction: column;

                padding: 20px;

                background: rgba(7, 10, 18, 0.97);

                border-bottom: 1px solid var(--border);
            }

            .nav-links.active {
                display: flex;
            }

            .hero-grid,
            .about-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }

            .services-grid,
            .projects-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .hero {
                padding-top: 130px;
            }

            .profile-card {
                max-width: 500px;
            }
        }

        @media (max-width: 600px) {

            section {
                padding: 75px 0;
            }

            .hero h1 {
                font-size: 47px;
                letter-spacing: -2px;
            }

            .hero p {
                font-size: 15px;
            }

            .services-grid,
            .projects-grid {
                grid-template-columns: 1fr;
            }

            .stats {
                grid-template-columns: 1fr;
            }

            .stat {
                border-right: none;
                border-bottom: 1px solid var(--border);
            }

            .stat:last-child {
                border-bottom: none;
            }

            .footer-content {
                flex-direction: column;
                text-align: center;
            }
        }
    </style>
</head>

<body>

    <!-- ================= HEADER ================= -->

    <header>
        <div class="container nav">

            <a href="#home" class="logo">J.</a>

            <button class="menu-btn" id="menuBtn">
                ☰
            </button>

            <ul class="nav-links" id="navLinks">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Skills</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#faq">FAQ</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>

        </div>
    </header>


    <!-- ================= HERO ================= -->

    <main id="home">

        <section class="hero">

            <div class="container hero-grid">

                <div class="reveal">

                    <div class="badge">
                        BCA Student • Open to Opportunities
                    </div>

                    <h1>
                        Hi, I'm <span>Jayesh</span>.
                        <br>
                        I build & learn.
                    </h1>

                    <p>
                        I'm a BCA student from Jaipur, Rajasthan,
                        interested in web development, Python,
                        databases and technology. This website
                        is a collection of my work, skills and
                        learning journey.
                    </p>

                    <div class="buttons">

                        <a href="#projects" class="btn btn-primary">
                            View Projects
                        </a>

                        <a href="#contact" class="btn btn-secondary">
                            Get In Touch
                        </a>

                    </div>

                </div>


                <div class="profile-card reveal">

                    <div class="profile-avatar">
                        JG
                    </div>

                    <h2>Jayesh Godara</h2>

                    <div class="role">
                        BCA Student • Developer • Learner
                    </div>

                    <p>
                        Currently learning and building projects
                        around web development, Python, SQL and
                        database management.
                    </p>

                    <div class="social-links">

                        <a
                            href="https://github.com/codedshadow-pixle"
                            target="_blank"
                            rel="noopener noreferrer">
                            GitHub
                        </a>

                        <a
                            href="https://www.instagram.com/shadowvibes383/"
                            target="_blank"
                            rel="noopener noreferrer">
                            Instagram
                        </a>

                    </div>

                </div>

            </div>

        </section>


        <!-- ================= STATS ================= -->

        <section>

            <div class="container">

                <div class="stats reveal">

                    <div class="stat">
                        <h3>BCA</h3>
                        <p>Student</p>
                    </div>

                    <div class="stat">
                        <h3>8+</h3>
                        <p>Technical Skills</p>
                    </div>

                    <div class="stat">
                        <h3>∞</h3>
                        <p>Ideas to Build</p>
                    </div>

                </div>

            </div>

        </section>


        <!-- ================= ABOUT ================= -->

        <section id="about">

            <div class="container">

                <div class="section-heading reveal">
                    <span>About Me</span>

                    <h2>
                        Learning today.
                        Building tomorrow.
                    </h2>

                    <p>
                        A little about who I am and what I'm
                        currently working on.
                    </p>
                </div>


                <div class="about-grid">

                    <div class="card reveal">

                        <h3>Who I Am</h3>

                        <p>
                            I'm Jayesh Godara, a BCA student from
                            Jaipur, Rajasthan. I'm interested in
                            programming, web development and
                            databases.
                        </p>

                        <br>

                        <p>
                            I enjoy experimenting with different
                            technologies and turning ideas into
                            practical projects while continuously
                            improving my skills.
                        </p>

                    </div>


                    <div class="card reveal">

                        <h3>Skills & Interests</h3>

                        <p>
                            Technologies and areas I'm learning
                            and working with:
                        </p>

                        <div class="skills">

                            <span class="skill">HTML</span>
                            <span class="skill">CSS</span>
                            <span class="skill">JavaScript</span>
                            <span class="skill">Python</span>
                            <span class="skill">SQL</span>
                            <span class="skill">DBMS</span>
                            <span class="skill">Git</span>
                            <span class="skill">GitHub</span>
                            <span class="skill">Web Design</span>

                        </div>

                    </div>

                </div>

            </div>

        </section>


        <!-- ================= SKILLS ================= -->

        <section id="services">

            <div class="container">

                <div class="section-heading reveal">

                    <span>What I Work With</span>

                    <h2>
                        Skills I'm developing
                    </h2>

                    <p>
                        My current technical interests and
                        learning areas.
                    </p>

                </div>


                <div class="services-grid">

                    <div class="card reveal">

                        <div class="service-icon">
                            &lt;/&gt;
                        </div>

                        <h3>Web Development</h3>

                        <p>
                            Building responsive websites using
                            HTML, CSS and JavaScript.
                        </p>

                    </div>


                    <div class="card reveal">

                        <div class="service-icon">
                            PY
                        </div>

                        <h3>Python</h3>

                        <p>
                            Learning Python programming and
                            building small practical projects.
                        </p>

                    </div>


                    <div class="card reveal">

                        <div class="service-icon">
                            DB
                        </div>

                        <h3>SQL & DBMS</h3>

                        <p>
                            Working with databases, SQL queries,
                            tables and database concepts.
                        </p>

                    </div>


                    <div class="card reveal">

                        <div class="service-icon">
                            GH
                        </div>

                        <h3>GitHub</h3>

                        <p>
                            Using GitHub to store, manage and
                            showcase development projects.
                        </p>

                    </div>


                    <div class="card reveal">

                        <div class="service-icon">
                            UI
                        </div>

                        <h3>UI Design</h3>

                        <p>
                            Creating clean, modern and
                            user-friendly website interfaces.
                        </p>

                    </div>


                    <div class="card reveal">

                        <div class="service-icon">
                            +
                        </div>

                        <h3>Always Learning</h3>

                        <p>
                            Exploring new technologies and
                            continuously improving my skills.
                        </p>

                    </div>

                </div>

            </div>

        </section>


        <!-- ================= PROJECTS ================= -->

        <section id="projects">

            <div class="container">

                <div class="section-heading reveal">

                    <span>My Work</span>

                    <h2>
                        Projects & Experiments
                    </h2>

                    <p>
                        A few areas where I'm building and
                        experimenting.
                    </p>

                </div>


                <div class="projects-grid">

                    <div class="project-card reveal">

                        <div class="project-number">
                            PROJECT 01
                        </div>

                        <h3>Personal Portfolio</h3>

                        <p>
                            A professional personal website
                            created using HTML, CSS and JavaScript
                            to showcase my profile and projects.
                        </p>

                        <a
                            href="https://github.com/codedshadow-pixle"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="project-link">
                            View on GitHub →
                        </a>

                    </div>


                    <div class="project-card reveal">

                        <div class="project-number">
                            PROJECT 02
                        </div>

                        <h3>Python Projects</h3>

                        <p>
                            Small Python experiments and
                            programming projects created while
                            learning Python.
                        </p>

                        <a
                            href="https://github.com/codedshadow-pixle"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="project-link">
                            View GitHub →
                        </a>

                    </div>


                    <div class="project-card reveal">

                        <div class="project-number">
                            PROJECT 03
                        </div>

                        <h3>SQL & DBMS Projects</h3>

                        <p>
                            Database assignments and SQL projects
                            covering tables, queries and database
                            management concepts.
                        </p>

                        <a
                            href="https://github.com/codedshadow-pixle"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="project-link">
                            View GitHub →
                        </a>

                    </div>


                    <div class="project-card reveal">

                        <div class="project-number">
                            PROJECT 04
                        </div>

                        <h3>More Coming Soon</h3>

                        <p>
                            More projects will be added as I
                            continue learning and building.
                        </p>

                        <a
                            href="https://github.com/codedshadow-pixle"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="project-link">
                            Follow My Journey →
                        </a>

                    </div>

                </div>

            </div>

        </section>


        <!-- ================= FAQ ================= -->

        <section id="faq">

            <div class="container">

                <div class="section-heading reveal">

                    <span>FAQ</span>

                    <h2>
                        Frequently Asked Questions
                    </h2>

                </div>


                <div class="faq reveal">

                    <div class="faq-item">

                        <button class="faq-question">
                            What is this website?
                            <span>+</span>
                        </button>

                        <div class="faq-answer">
                            This is Jayesh Godara's personal
                            portfolio website for showcasing
                            skills, projects and learning.
                        </div>

                    </div>


                    <div class="faq-item">

                        <button class="faq-question">
                            What are you studying?
                            <span>+</span>
                        </button>

                        <div class="faq-answer">
                            I'm currently pursuing BCA and
                            developing my programming and
                            technical skills.
                        </div>

                    </div>


                    <div class="faq-item">

                        <button class="faq-question">
                            What technologies do you use?
                            <span>+</span>
                        </button>

                        <div class="faq-answer">
                            My current learning areas include
                            HTML, CSS, JavaScript, Python,
                            SQL, DBMS and GitHub.
                        </div>

                    </div>


                    <div class="faq-item">

                        <button class="faq-question">
                            Where can I see your projects?
                            <span>+</span>
                        </button>

                        <div class="faq-answer">
                            You can find my projects and future
                            work on my GitHub profile.
                        </div>

                    </div>

                </div>

            </div>

        </section>


        <!-- ================= CONTACT ================= -->

        <section id="contact">

            <div class="container">

                <div class="section-heading reveal">

                    <span>Contact</span>

                    <h2>
                        Let's connect.
                    </h2>

                    <p>
                        You can find me through my social
                        profiles or send a message below.
                    </p>

                </div>


                <div class="contact-grid">

                    <div class="card contact-info reveal">

                        <div class="contact-item">

                            <small>GitHub</small>

                            <a
                                href="https://github.com/codedshadow-pixle"
                                target="_blank"
                                rel="noopener noreferrer">
                                github.com/codedshadow-pixle
                            </a>

                        </div>


                        <div class="contact-item">

                            <small>Instagram</small>

                            <a
                                href="https://www.instagram.com/shadowvibes383/"
                                target="_blank"
                                rel="noopener noreferrer">
                                @shadowvibes383
                            </a>

                        </div>


                        <div class="contact-item">

                            <small>Location</small>

                            <p>
                                Jaipur, Rajasthan, India
                            </p>

                        </div>


                        <div class="contact-item">

                            <small>Status</small>

                            <p>
                                Open to learning & opportunities
                            </p>

                        </div>

                    </div>


                    <div class="card reveal">

                        <form id="contactForm">

                            <input
                                type="text"
                                placeholder="Your Name"
                                required>

                            <input
                                type="email"
                                placeholder="Your Email"
                                required>

                            <textarea
                                placeholder="Your Message"
                                required></textarea>

                            <button
                                type="submit"
                                class="btn btn-primary">
                                Send Message
                            </button>

                        </form>

                    </div>

                </div>

            </div>

        </section>


        <!-- ================= PRIVACY ================= -->

        <section>

            <div class="container">

                <div class="card reveal">

                    <h3>Privacy Policy</h3>

                    <p>
                        This personal portfolio does not
                        intentionally collect or sell personal
                        information. Any information submitted
                        through the contact form is intended only
                        for communication purposes.
                    </p>

                </div>

            </div>

        </section>

    </main>


    <!-- ================= FOOTER ================= -->

    <footer>

        <div class="container footer-content">

            <p>
                © 2026 Jayesh Godara. All Rights Reserved.
            </p>

            <div class="footer-links">

                <a href="#home">Home</a>

                <a href="#about">About</a>

                <a href="#projects">Projects</a>

                <a href="#contact">Contact</a>

            </div>

        </div>

    </footer>


    <!-- ================= JAVASCRIPT ================= -->

    <script>

        /* Mobile Menu */

        const menuBtn = document.getElementById("menuBtn");
        const navLinks = document.getElementById("navLinks");

        menuBtn.addEventListener("click", () => {
            navLinks.classList.toggle("active");
        });


        /* Close mobile menu */

        document.querySelectorAll(".nav-links a").forEach(link => {

            link.addEventListener("click", () => {
                navLinks.classList.remove("active");
            });

        });


        /* FAQ */

        document.querySelectorAll(".faq-question").forEach(button => {

            button.addEventListener("click", () => {

                const item = button.parentElement;

                document.querySelectorAll(".faq-item")
                    .forEach(other => {

                        if (other !== item) {
                            other.classList.remove("active");
                        }

                    });

                item.classList.toggle("active");

            });

        });


        /* Scroll Reveal */

        const observer = new IntersectionObserver(
            entries => {

                entries.forEach(entry => {

                    if (entry.isIntersecting) {

                        entry.target.classList.add("show");

                        observer.unobserve(entry.target);

                    }

                });

            },
            {
                threshold: 0.12
            }
        );


        document.querySelectorAll(".reveal").forEach(element => {
            observer.observe(element);
        });


        /* Contact Form */

        document.getElementById("contactForm")
            .addEventListener("submit", function(event) {

                event.preventDefault();

                alert(
                    "Thanks for reaching out, Jayesh will get back to you!"
                );

                this.reset();

            });

    </script>

</body>
</html>
