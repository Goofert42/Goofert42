<html><head><base href="<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Goofert | Digital Presence</title>
    <style>
        :root {
            --navy: #001f3f;
            --navy-light: #183153;
            --accent: #4a9eff;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--navy);
            color: white;
            line-height: 1.6;
        }

        .nav-bar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            padding: 1rem 2rem;
            background: rgba(0, 31, 63, 0.9);
            backdrop-filter: blur(10px);
            display: flex;
            justify-content: space-between;
            align-items: center;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.2);
        }

        .nav-logo {
            font-size: 1.5rem;
            font-weight: 900;
            letter-spacing: -1px;
            background: linear-gradient(45deg, var(--accent), #ffffff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 600;
            position: relative;
            padding: 0.5rem 0;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--accent);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        header {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            padding-top: 80px;
        }

        .hero-content {
            text-align: center;
            z-index: 2;
        }

        .logo {
            font-size: 5rem;
            font-weight: 900;
            letter-spacing: -2px;
            margin-bottom: 1rem;
            background: linear-gradient(45deg, var(--accent), #ffffff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: pulse 3s infinite;
        }

        .tagline {
            font-size: 1.5rem;
            color: #ffffff90;
            margin-bottom: 2rem;
        }

        .cta-button {
            display: inline-block;
            padding: 1rem 2rem;
            background: var(--accent);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: transform 0.3s ease;
        }

        .cta-button:hover {
            transform: translateY(-3px);
        }

        .background-animation {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 1;
        }

        @keyframes pulse {
            0% { opacity: 1; }
            50% { opacity: 0.8; }
            100% { opacity: 1; }
        }

        .social-links {
            margin-top: 2rem;
        }

        .social-links a {
            margin: 0 1rem;
            color: white;
            text-decoration: none;
            font-size: 1.2rem;
            opacity: 0.7;
            transition: opacity 0.3s ease;
        }

        .social-links a:hover {
            opacity: 1;
        }

        .projects-section {
            min-height: 100vh;
            padding: 6rem 0;
            background-color: var(--navy-light);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            padding: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 15px;
            padding: 1.5rem;
            transition: transform 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-5px);
        }

        .project-card h3 {
            color: var(--accent);
            margin-bottom: 1rem;
        }

        .project-card p {
            opacity: 0.8;
            margin-bottom: 1rem;
        }

        .project-buttons {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }

        .project-button {
            padding: 0.5rem 1rem;
            border-radius: 5px;
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 600;
            transition: all 0.2s ease;
        }

        .website-button {
            background: var(--accent);
            color: white;
        }

        .website-button:hover {
            background: #3b8eff;
        }

        .github-button {
            background: rgba(255, 255, 255, 0.1);
            color: white;
        }

        .github-button:hover {
            background: rgba(255, 255, 255, 0.2);
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: var(--accent);
        }

        .social-section {
            min-height: 50vh;
            padding: 6rem 0;
            background-color: var(--navy);
        }

        .social-grid {
            display: flex;
            justify-content: center;
            gap: 2rem;
            padding: 2rem;
            max-width: 1200px;
            margin: 0 auto;
            flex-wrap: wrap;
        }

        .social-card {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 1rem;
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 15px;
            color: white;
            text-decoration: none;
            width: 200px;
            transition: all 0.3s ease;
        }

        .social-card:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.1);
        }

        .social-icon {
            width: 40px;
            height: 40px;
            color: var(--accent);
        }

        .social-card span {
            font-size: 1.2rem;
            font-weight: 600;
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;900&display=swap" rel="stylesheet">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
</head>
<body>
    <nav class="nav-bar">
        <a href="#" class="nav-logo">GOOFERT</a>
        <div class="nav-links">
            <a href="#">Home</a>
            <a href="#projects">Projects</a>
            <a href="#status">Status</a>
        </div>
    </nav>

    <header>
        <div class="background-animation" id="bg-animation"></div>
        <div class="hero-content">
            <h1 class="logo">GOOFERT</h1>
            <p class="tagline">Digital Creator & Explorer</p>
            <a href="#projects" class="cta-button">View Projects</a>
            <div class="social-links">
                <a href="https://twitter.com/goofert">Twitter</a>
                <a href="https://github.com/goofert">GitHub</a>
                <a href="https://linkedin.com/in/goofert">LinkedIn</a>
            </div>
        </div>
    </header>

    <section id="projects" class="projects-section">
        <h2 class="section-title">My Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <h3>Project 1</h3>
                <p>A brief description of your first project. Highlight the key features and technologies used.</p>
                <div class="project-buttons">
                    <a href="https://project1.com" class="project-button website-button">View Website</a>
                    <a href="https://github.com/goofert/project1" class="project-button github-button">GitHub</a>
                </div>
            </div>
            <div class="project-card">
                <h3>Project 2</h3>
                <p>A brief description of your second project. Highlight the key features and technologies used.</p>
                <div class="project-buttons">
                    <a href="https://project2.com" class="project-button website-button">View Website</a>
                    <a href="https://github.com/goofert/project2" class="project-button github-button">GitHub</a>
                </div>
            </div>
            <div class="project-card">
                <h3>Project 3</h3>
                <p>A brief description of your third project. Highlight the key features and technologies used.</p>
                <div class="project-buttons">
                    <a href="https://project3.com" class="project-button website-button">View Website</a>
                    <a href="https://github.com/goofert/project3" class="project-button github-button">GitHub</a>
                </div>
            </div>
        </div>
    </section>

    <section id="status" class="social-section">
        <h2 class="section-title">Connect With Me</h2>
        <div class="social-grid">
            <a href="https://twitter.com/goofert" class="social-card">
                <svg class="social-icon" viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/>
                </svg>
                <span>Twitter</span>
            </a>
            <a href="https://github.com/goofert" class="social-card">
                <svg class="social-icon" viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/>
                </svg>
                <span>GitHub</span>
            </a>
            <a href="https://linkedin.com/in/goofert" class="social-card">
                <svg class="social-icon" viewBox="0 0 24 24" width="24" height="24">
                    <path fill="currentColor" d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                </svg>
                <span>LinkedIn</span>
            </a>
        </div>
    </section>

    <script>
        // Three.js background animation
        const scene = new THREE.Scene();
        const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
        const renderer = new THREE.WebGLRenderer({ alpha: true });
        renderer.setSize(window.innerWidth, window.innerHeight);
        document.getElementById('bg-animation').appendChild(renderer.domElement);

        // Create particles
        const geometry = new THREE.BufferGeometry();
        const vertices = [];
        for (let i = 0; i < 5000; i++) {
            vertices.push(
                Math.random() * 2000 - 1000,
                Math.random() * 2000 - 1000,
                Math.random() * 2000 - 1000
            );
        }
        geometry.setAttribute('position', new THREE.Float32BufferAttribute(vertices, 3));
        const material = new THREE.PointsMaterial({ color: 0x4a9eff, size: 2 });
        const points = new THREE.Points(geometry, material);
        scene.add(points);

        camera.position.z = 1000;

        function animate() {
            requestAnimationFrame(animate);
            points.rotation.x += 0.0003;
            points.rotation.y += 0.0003;
            renderer.render(scene, camera);
        }

        animate();

        // Handle window resize
        window.addEventListener('resize', () => {
            camera.aspect = window.innerWidth / window.innerHeight;
            camera.updateProjectionMatrix();
            renderer.setSize(window.innerWidth, window.innerHeight);
        });
    </script>
</body>
</html>
