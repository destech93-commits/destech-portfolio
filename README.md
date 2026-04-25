<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DESTECH | Future-Proof Digital Solutions</title>
    <!-- Essential Tools: Tailwind for design, GSAP for animations -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
    <style>
        :root {
            --purple: #2E0249;
            --neon-pink: #A91079;
            --deep-black: #0D0D0D;
        }
        body {
            background-color: var(--deep-black);
            color: white;
            font-family: 'Inter', sans-serif;
            overflow-x: hidden;
        }
        .mesh-bg {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: radial-gradient(circle at 20% 30%, rgba(46, 2, 73, 0.6), transparent 40%),
                        radial-gradient(circle at 80% 70%, rgba(169, 16, 121, 0.3), transparent 40%);
            z-index: -1;
        }
        .glass {
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
        }
        .nav-link:hover { color: var(--neon-pink); transition: 0.3s; }
        .hero-title {
            background: linear-gradient(to right, #ffffff, #A91079);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
    </style>
</head>
<body>
    <div class="mesh-bg"></div>

    <!-- Navigation Bar -->
    <nav class="flex justify-between items-center p-6 fixed w-full top-0 z-50 glass">
        <div class="text-2xl font-bold tracking-tighter">DESTECH</div>
        <div class="space-x-8 hidden md:flex">
            <a href="#" class="nav-link">Home</a>
            <a href="#services" class="nav-link">Services</a>
            <a href="#portfolio" class="nav-link">Portfolio</a>
            <a href="https://instagram.com" class="px-6 py-2 border border-pink-500 rounded-full hover:bg-pink-600 transition">Instagram</a>
        </div>
    </nav>

    <!-- Animated Hero Section -->
    <section class="h-screen flex flex-col items-center justify-center text-center px-4">
        <h1 class="hero-title text-6xl md:text-9xl font-black mb-4 opacity-0 translate-y-10" id="title">DESTECH</h1>
        <p class="text-gray-400 tracking-[0.4em] uppercase mb-8 opacity-0" id="tagline">Future-Proof Digital Solutions</p>
        <div class="flex space-x-4 opacity-0" id="hero-btns">
            <button class="px-10 py-4 bg-white text-black font-bold rounded-full hover:scale-105 transition">Hire Me</button>
            <a href="#services" class="px-10 py-4 glass border border-white/20 rounded-full inline-block">Explore Gigs</a>
        </div>
    </section>

    <!-- Services Overview -->
    <section id="services" class="py-20 px-8 max-w-7xl mx-auto">
        <h2 class="text-4xl font-bold mb-12 text-center">Master Services</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="glass p-8 hover:-translate-y-2 transition border-l-4 border-pink-600">
                <h3 class="text-xl font-bold mb-2">Author & Publishing</h3>
                <p class="text-gray-400 text-sm mb-4">Starting at ₦150k • Pro Tier Design</p>
                <button class="text-pink-500 font-bold hover:underline">View Gigs &rarr;</button>
            </div>
            <div class="glass p-8 hover:-translate-y-2 transition border-l-4 border-purple-600">
                <h3 class="text-xl font-bold mb-2">Cybersecurity</h3>
                <p class="text-gray-400 text-sm mb-4">Enterprise Audits & Tech Support</p>
                <button class="text-purple-500 font-bold hover:underline">View Gigs &rarr;</button>
            </div>
            <div class="glass p-8 hover:-translate-y-2 transition border-l-4 border-blue-600">
                <h3 class="text-xl font-bold mb-2">App Development</h3>
                <p class="text-gray-400 text-sm mb-4">iOS/Android + UBA Integration</p>
                <button class="text-blue-500 font-bold hover:underline">View Gigs &rarr;</button>
            </div>
        </div>
    </section>

    <!-- Animation Trigger Script -->
    <script>
        window.onload = () => {
            const tl = gsap.timeline();
            tl.to("#title", { opacity: 1, y: 0, duration: 1.2, ease: "power4.out" })
              .to("#tagline", { opacity: 1, duration: 1 }, "-=0.5")
              .to("#hero-btns", { opacity: 1, y: 0, duration: 1 }, "-=0.5");
        };
    </script>
</body>
</html>
