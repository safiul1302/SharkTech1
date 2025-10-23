<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SharkTech | Secure Your Digital Ocean</title>
    
    <!-- Load Tailwind CSS --><script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Configure Tailwind to use the Inter font and a custom color palette --><script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        'shark-dark': '#01050d', // Very dark for core effect
                        'shark-blue': '#00ffff', // Pure Cyan for strong glow and accent
                        'shark-light': '#f0f9ff', // Sky 50
                        'deep-nav-blue': '#161c28', 
                        'shark-primary-blue': '#1a2233', // Darker blue for background blocks
                    }
                }
            }
        }
    </script>
    <style>
        /* Ensures smooth scrolling to anchor links */
        html {
            scroll-behavior: smooth;
        }

        /* Keyframes for subtle background movement */
        @keyframes move-bg {
            0% { background-position: 0% 0%; }
            100% { background-position: 100% 100%; }
        }
        
        /* Moving Computer Core Pattern for the background */
        body {
            background-color: #01050d; /* Very dark background */
            /* Intricate grid pattern for computer core effect */
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120' viewBox='0 0 120 120'%3E%3Cdefs%3E%3Cfilter id='f1' x='-50%25' y='-50%25' width='200%25' height='200%25'%3E%3CfeGaussianBlur in='SourceGraphic' stdDeviation='1.5' /%3E%3C/filter%3E%3C/defs%3E%3Crect x='0' y='0' width='120' height='120' fill='%2301050d'/%3E%3Cg stroke='%2300ffff' stroke-width='0.7' opacity='0.08'%3E%3Cline x1='0' y1='0' x2='120' y2='120'/%3E%3Cline x1='0' y1='120' x2='120' y2='0'/%3Cpath d='M0 60h120M60 0v120'/%3E%3C/g%3E%3Cg stroke='%2300ffff' stroke-width='0.5' opacity='0.05'%3E%3Cpath d='M0 30h120M0 90h120M30 0v120M90 0v120'/%3E%3C/g%3E%3Cg fill='%2300ffff' opacity='0.1'%3E%3Ccircle cx='60' cy='60' r='2' filter='url(%23f1)'/%3E%3Ccircle cx='0' cy='0' r='1' filter='url(%23f1)'/%3E%3Ccircle cx='120' cy='0' r='1' filter='url(%23f1)'/%3E%3Ccircle cx='0' cy='120' r='1' filter='url(%23f1)'/%3E%3Ccircle cx='120' cy='120' r='1' filter='url(%23f1)'/%3E%3C/g%3E%3C/svg%3E");
            background-size: 120px 120px; 
            animation: move-bg 60s linear infinite alternate; 
        }

        /* Custom glow effect (reduced intensity for professional look) */
        .text-glow {
            text-shadow: 0 0 4px rgba(0, 255, 255, 0.4); 
        }
        .shadow-glow {
            box-shadow: 0 0 8px rgba(0, 255, 255, 0.4); 
            transition: all 0.3s ease;
        }
        .shadow-glow:hover {
            box-shadow: 0 0 15px rgba(0, 255, 255, 0.7); 
        }
        
        /* New card style based on user's image (image_099ebe.jpg) */
        .enhanced-service-card {
            background-color: var(--tw-colors-shark-primary-blue); /* Custom dark blue */
            padding: 2.5rem; /* p-10 */
            border-radius: 0.75rem; /* rounded-xl */
            border-left: 4px solid transparent;
            transition: all 0.3s ease;
        }
        .enhanced-service-card:hover {
            border-left-color: #00ffff; /* shark-blue highlight */
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.4);
        }
        
    </style>
</head>
<body class="text-shark-light font-sans">

    <!-- Full-Screen Mobile/Flyout Menu -->
    <div id="mobile-menu" class="fixed inset-0 z-[100] bg-deep-nav-blue backdrop-blur-md transform -translate-x-full transition-transform duration-500 ease-in-out sm:hidden">
        
        <div class="flex justify-between items-center p-4 border-b border-gray-700">
            <span class="text-3xl font-extrabold tracking-tight text-shark-light">Shark<span class="text-shark-blue">Tech</span></span>
            <button id="menu-close" class="p-2 rounded-lg hover:bg-gray-800 transition duration-300">
                <svg class="w-7 h-7 text-shark-blue" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/></svg>
            </button>
        </div>

        <!-- Menu Links based on Sherazi IT structure -->
        <nav class="p-2 space-y-1">
            <a href="#home" class="block py-3 px-4 text-xl text-gray-200 hover:bg-gray-800 hover:text-shark-blue rounded-lg transition duration-300" onclick="closeMenu()">Home</a>
            <a href="#blog" class="block py-3 px-4 text-xl text-gray-200 hover:bg-gray-800 hover:text-shark-blue rounded-lg transition duration-300" onclick="closeMenu()">Blog</a>
            <a href="#services" class="block py-3 px-4 text-xl text-gray-200 hover:bg-gray-800 hover:text-shark-blue rounded-lg transition duration-300" onclick="closeMenu()">Service</a>
            <a href="#products" class="block py-3 px-4 text-xl text-gray-200 hover:bg-gray-800 hover:text-shark-blue rounded-lg transition duration-300" onclick="closeMenu()">Product</a>
            <a href="#works" class="block py-3 px-4 text-xl text-gray-200 hover:bg-gray-800 hover:text-shark-blue rounded-lg transition duration-300" onclick="closeMenu()">Works</a>
            <a href="#about" class="block py-3 px-4 text-xl text-gray-200 hover:bg-gray-800 hover:text-shark-blue rounded-lg transition duration-300" onclick="closeMenu()">About Us (Pages)</a>
            <a href="#support" class="block py-3 px-4 text-xl text-gray-200 hover:bg-gray-800 hover:text-shark-blue rounded-lg transition duration-300" onclick="closeMenu()">Support</a>
            <a href="#contact" class="block py-3 px-4 text-xl text-gray-200 hover:bg-gray-800 hover:text-shark-blue rounded-lg transition duration-300" onclick="closeMenu()">Contact</a>

            <div class="border-t border-gray-700 my-2 pt-4"></div>
            <!-- Dynamic Mobile Auth Button -->
            <button id="mobile-auth-button" class="w-full text-left py-3 px-4 text-xl text-shark-blue font-bold bg-gray-900 hover:bg-gray-800 rounded-xl transition duration-300" onclick="handleSignOut()">
                <svg class="w-5 h-5 inline mr-2 align-text-bottom" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"/></svg>
                <span id="mobile-auth-button-text">Account / CRM Login</span>
            </button>
        </nav>
    </div>

    <!-- Navigation Bar -->
    <header class="sticky top-0 z-50 bg-shark-dark/95 backdrop-blur-sm shadow-xl border-b border-shark-blue/20">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <!-- Logo/Brand -->
            <a href="#home" class="flex items-center space-x-2">
                <!-- Simple Geometric SharkTech Logo -->
                <svg class="w-10 h-10 text-shark-blue" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                    <path d="M4 12c0-1.66 1.34-3 3-3h10c1.66 0 3 1.34 3 3s-1.34 3-3 3H7c-1.66 0-3-1.34-3-3z"/>
                    <path d="M10 9L7 6l-3 3M14 9l3-3 3 3"/>
                    <path d="M12 17l3-3m-6 0l3 3"/>
                </svg>
                <span class="text-3xl font-extrabold tracking-tight text-shark-light">Shark<span class="text-shark-blue">Tech</span></span>
            </a>

            <!-- Desktop Navigation Links & Auth Status -->
            <div class="hidden sm:flex space-x-4 text-base font-medium items-center">
                <a href="#services" class="text-gray-300 hover:text-shark-blue transition duration-300">Service</a>
                <a href="#products" class="text-gray-300 hover:text-shark-blue transition duration-300">Product</a>
                <a href="#works" class="text-gray-300 hover:text-shark-blue transition duration-300">Works</a>
                <a href="#about" class="text-gray-300 hover:text-shark-blue transition duration-300">About</a>
                <a href="#blog" class="text-gray-300 hover:text-shark-blue transition duration-300">Blog</a>
                <a href="#support" class="text-gray-300 hover:text-shark-blue transition duration-300">Support</a>
                
                <!-- Authentication Status Display -->
                <div id="auth-status" class="text-right ml-4 pr-3 border-r border-gray-700">
                    <span class="text-sm text-gray-400">Not Logged In</span>
                </div>
                
                <!-- Dynamic Auth Button (CRM Login / Sign Out) -->
                <button id="auth-button" class="px-4 py-2 bg-gray-800 text-shark-blue rounded-lg transition duration-300 border border-shark-blue/50 text-sm hover:bg-gray-700 hover:shadow-glow">Account Login</button> 
                
                <!-- Primary CTA -->
                <a href="#contact" class="px-4 py-2 bg-shark-blue text-shark-dark rounded-lg font-bold hover:bg-cyan-400 transition duration-300 transform hover:scale-105">
                    Contact Us
                </a>
            </div>

            <!-- Mobile Menu Toggle (Hamburger Icon) -->
            <button id="menu-toggle" class="sm:hidden p-2 rounded-lg hover:bg-gray-800 transition duration-300">
                <svg class="w-7 h-7 text-shark-blue" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/></svg>
            </button>
        </nav>
    </header>

    <main>
        <!-- 1. Hero Section (Home) - Focused and Professional -->
        <section id="home" class="relative overflow-hidden pt-24 pb-28 sm:pt-40 sm:pb-40 text-center bg-shark-dark/90">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="relative z-10">
                    <p class="text-sm tracking-widest uppercase text-shark-blue mb-4 font-semibold">
                        Business. Technology. Security.
                    </p>
                    <h1 class="text-4xl sm:text-6xl lg:text-7xl font-extrabold leading-tight mb-6">
                        <span class="text-shark-light">Future-Proof </span> Your Operations
                        <br><span class="text-shark-blue text-glow">with AI-Driven Strategy.</span>
                    </h1>
                    <p class="text-lg sm:text-xl text-gray-400 max-w-3xl mx-auto mb-10">
                        SharkTech specializes in integrated business development and support, leveraging cutting-edge security and cloud architecture to ensure your enterprise scales efficiently and securely.
                    </p>
                    <div class="flex flex-col sm:flex-row justify-center space-y-4 sm:space-y-0 sm:space-x-4">
                        <a href="#contact" class="bg-shark-blue text-shark-dark font-bold px-8 py-3 rounded-xl shadow-md hover:bg-cyan-400 transition duration-300 transform hover:scale-105 inline-block">
                            Schedule a Consultation
                        </a>
                        <a href="#services" class="bg-gray-700 text-shark-light font-medium px-8 py-3 rounded-xl shadow-md hover:bg-gray-600 transition duration-300 transform hover:scale-105 inline-block border border-gray-600">
                            View Our Services
                        </a>
                    </div>
                </div>

                <!-- Abstract Data Flow Visualization (SVG) -->
                <div class="mt-20 max-w-4xl mx-auto opacity-70">
                    <svg class="w-full h-auto" viewBox="0 0 800 150" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <defs>
                            <filter id="glow">
                                <feGaussianBlur in="SourceGraphic" stdDeviation="2" result="blur" />
                                <feFlood flood-color="#00FFFF" flood-opacity="0.5" result="flood" />
                                <feComposite in="flood" in2="blur" operator="in" result="glow_effect" />
                                <feMerge>
                                    <feMergeNode in="glow_effect"/>
                                    <feMergeNode in="SourceGraphic"/>
                                </feMerge>
                            </filter>
                        </defs>
                        <!-- Main Data Line -->
                        <path d="M50 75C200 25, 600 25, 750 75" stroke="#00FFFF" stroke-width="4" stroke-linecap="round" filter="url(#glow)"/>
                        <!-- Side Data Line 1 -->
                        <path d="M50 100C250 150, 550 150, 750 100" stroke="#00FFFF" stroke-width="2" stroke-dasharray="8 8" opacity="0.5"/>
                        <!-- Side Data Line 2 -->
                        <path d="M50 50C250 0, 550 0, 750 50" stroke="#00FFFF" stroke-width="2" stroke-dasharray="8 8" opacity="0.5"/>

                        <!-- Data Nodes -->
                        <circle cx="50" cy="75" r="5" fill="#00FFFF" filter="url(#glow)"/>
                        <circle cx="200" cy="50" r="5" fill="#00FFFF" filter="url(#glow)"/>
                        <circle cx="400" cy="75" r="7" fill="#00FFFF" filter="url(#glow)"/>
                        <circle cx="600" cy="50" r="5" fill="#00FFFF" filter="url(#glow)"/>
                        <circle cx="750" cy="75" r="5" fill="#00FFFF" filter="url(#glow)"/>
                    </svg>
                </div>

            </div>
        </section>

        <!-- NEW: 1.5 Stats Section (Based on image_ffb11a.jpg) -->
        <section id="stats" class="py-16 bg-shark-primary-blue border-b border-shark-blue/20">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="grid grid-cols-2 md:grid-cols-4 gap-8 text-center">
                    
                    <!-- Stat 1: Projects Completed -->
                    <div class="flex flex-col items-center p-4">
                        <svg class="w-12 h-12 text-shark-blue mb-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"/></svg>
                        <p class="text-4xl font-extrabold text-shark-light text-glow">3700</p>
                        <p class="text-gray-400 mt-1 uppercase text-xs tracking-wider">Projects Completed</p>
                    </div>

                    <!-- Stat 2: Happy Customers -->
                    <div class="flex flex-col items-center p-4">
                        <svg class="w-12 h-12 text-shark-blue mb-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18 9v3m0 0v3m0-3h3m-3 0h-3m-1-4a3 3 0 11-6 0 3 3 0 016 0zM12 15h2m-2-2h.01M10 15h.01M5.757 17.07l.793.793.793-.793M18.243 17.07l-.793.793-.793-.793"/></svg>
                        <p class="text-4xl font-extrabold text-shark-light text-glow">4048</p>
                        <p class="text-gray-400 mt-1 uppercase text-xs tracking-wider">Happy Customers</p>
                    </div>

                    <!-- Stat 3: Running Projects -->
                    <div class="flex flex-col items-center p-4">
                        <svg class="w-12 h-12 text-shark-blue mb-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/></svg>
                        <p class="text-4xl font-extrabold text-shark-light text-glow">387</p>
                        <p class="text-gray-400 mt-1 uppercase text-xs tracking-wider">Running Projects</p>
                    </div>

                    <!-- Stat 4: Followers -->
                    <div class="flex flex-col items-center p-4">
                        <svg class="w-12 h-12 text-shark-blue mb-3" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4.354a4 4 0 110 5.292M12 19v-5.5M12 12.5v-1m-4 0h8M12 12.5a.5.5 0 100 1 .5.5 0 000-1z"/></svg>
                        <p class="text-4xl font-extrabold text-shark-light text-glow">370K+</p>
                        <p class="text-gray-400 mt-1 uppercase text-xs tracking-wider">Followers</p>
                    </div>

                </div>
            </div>
        </section>

        <!-- 2. Services Section - Enhanced to include 6 blocks -->
        <section id="services" class="py-24 bg-shark-dark">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <p class="text-center text-sm tracking-widest uppercase text-gray-400 mb-2">
                    Our Core Offering
                </p>
                <h2 class="text-3xl sm:text-4xl font-bold text-center mb-16">
                    Integrated <span class="text-shark-blue">Service </span> Solutions
                </h2>

                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

                    <!-- Service Card 1: Cybersecurity & Compliance (Original) -->
                    <div class="enhanced-service-card shadow-xl transition duration-500">
                        <div class="text-shark-blue mb-4">
                            <svg class="w-10 h-10" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6-6v4m12-4v4m-3-11v10c0 .6-.4 1-1 1H8c-.6 0-1-.4-1-1V5c0-.6.4-1 1-1h4c.6 0 1 .4 1 1zM20 12h2M2 12h2"/></svg>
                        </div>
                        <h3 class="text-xl font-extrabold mb-3 text-shark-light">Cybersecurity & Compliance</h3>
                        <p class="text-gray-400 mb-4 text-sm">
                            Establish a multi-layered defense. From zero-trust policies to real-time threat hunting, we lock down your data and ensure regulatory compliance.
                        </p>
                        <a href="#" class="text-shark-blue font-semibold text-sm hover:underline">Secure My Business &rarr;</a>
                    </div>

                    <!-- Service Card 2: Bespoke Software Development (Original) -->
                    <div class="enhanced-service-card shadow-xl transition duration-500">
                        <div class="text-shark-blue mb-4">
                            <svg class="w-10 h-10" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"/></svg>
                        </div>
                        <h3 class="text-xl font-extrabold mb-3 text-shark-light">Bespoke Software Development</h3>
                        <p class="text-gray-400 mb-4 text-sm">
                            Build scalable, user-centric applications tailored for complex business workflows. Accelerate your digital transformation with our full-stack expertise.
                        </p>
                        <a href="#" class="text-shark-blue font-semibold text-sm hover:underline">View Portfolio &rarr;</a>
                    </div>

                    <!-- Service Card 3: Cloud Architecture & Migration (Original) -->
                    <div class="enhanced-service-card shadow-xl transition duration-500">
                        <div class="text-shark-blue mb-4">
                            <svg class="w-10 h-10" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 15a4 4 0 004 4h9a5 5 0 10-.1-9.999 5.002 5.002 0 10-9.76 3.001z"/></svg>
                        </div>
                        <h3 class="text-xl font-extrabold mb-3 text-shark-light">Cloud Architecture & Migration</h3>
                        <p class="text-gray-400 mb-4 text-sm">
                            Optimize your performance and reduce costs with elastic cloud infrastructure. We handle seamless migration and management on all major platforms.
                        </p>
                        <a href="#" class="text-shark-blue font-semibold text-sm hover:underline">Explore Cloud Services &rarr;</a>
                    </div>
                    
                    <!-- Service Card 4: Website Development & Sales (NEW - Based on 'Increase Business Sales' & 'Professional Website') -->
                    <div class="enhanced-service-card shadow-xl transition duration-500">
                        <div class="text-shark-blue mb-4">
                            <!-- Stats/Sales Icon -->
                            <svg class="w-10 h-10" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M11 3.055A9.001 9.001 0 1020.945 13H11V3.055z"/><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 2v20M4 12h16"/></svg>
                        </div>
                        <h3 class="text-xl font-extrabold mb-3 text-shark-light">Professional Web & SEO Services</h3>
                        <p class="text-gray-400 mb-4 text-sm">
                            Design high-performance, user-friendly websites that attract, convert, and retain customers. Boost your online presence and organic traffic.
                        </p>
                        <a href="#" class="text-shark-blue font-semibold text-sm hover:underline">Elevate Your Sales &rarr;</a>
                    </div>

                    <!-- Service Card 5: E-commerce & POS (NEW - Based on 'Streamline Business' & 'Advanced POS') -->
                    <div class="enhanced-service-card shadow-xl transition duration-500">
                        <div class="text-shark-blue mb-4">
                            <!-- Globe/Manage Business Icon -->
                            <svg class="w-10 h-10" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 7v10a2 2 0 002 2h14a2 2 0 002-2V9a2 2 0 00-2-2h-3m-1 5h2m-6-4h.01M16 16h.01M12 4h.01M3 9h5M16 9h5"/></svg>
                        </div>
                        <h3 class="text-xl font-extrabold mb-3 text-shark-light">E-commerce & POS Solutions</h3>
                        <p class="text-gray-400 mb-4 text-sm">
                            Streamline retail and online operations with integrated Point-of-Sale, inventory management, and secure e-commerce platforms.
                        </p>
                        <a href="#" class="text-shark-blue font-semibold text-sm hover:underline">See Demo Works &rarr;</a>
                    </div>
                    
                    <!-- Service Card 6: Managed IT & Support (NEW - Based on 'Business Support') -->
                    <div class="enhanced-service-card shadow-xl transition duration-500">
                        <div class="text-shark-blue mb-4">
                            <!-- Handshake/Support Icon -->
                            <svg class="w-10 h-10" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"/></svg>
                        </div>
                        <h3 class="text-xl font-extrabold mb-3 text-shark-light">Managed IT & Business Support</h3>
                        <p class="text-gray-400 mb-4 text-sm">
                            We provide comprehensive, worldwide support and technical solutions to organize your IT infrastructure and keep your business running smoothly 24/7.
                        </p>
                        <a href="#" class="text-shark-blue font-semibold text-sm hover:underline">View Support Plans &rarr;</a>
                    </div>

                </div>
            </div>
        </section>
        
        <!-- 3. Call to Action Banner (NEW - Based on image_099b5c.png) -->
        <section class="bg-shark-primary-blue py-16">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row items-center justify-between space-y-6 md:space-y-0">
                <div class="text-center md:text-left">
                    <h2 class="text-3xl sm:text-4xl font-extrabold text-shark-light mb-2">
                        Are you looking to grow your business?
                    </h2>
                    <p class="text-lg text-gray-400">
                        We deploy advanced, tailored software solutions to help you grow and manage your business easily.
                    </p>
                </div>
                <div class="flex-shrink-0">
                    <a href="#contact" class="px-10 py-4 bg-shark-blue text-shark-dark font-extrabold text-lg rounded-xl shadow-2xl hover:bg-cyan-400 transition duration-300 transform hover:scale-105 inline-block">
                        Call +1 (555) 555-SHARK
                    </a>
                </div>
            </div>
        </section>


        <!-- 4. Products Section (Existing) -->
        <section id="products" class="py-24 bg-shark-dark/90 border-t border-b border-shark-blue/20 backdrop-blur-sm">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <p class="text-center text-sm tracking-widest uppercase text-gray-400 mb-2">
                    Our Software Ecosystem
                </p>
                <h2 class="text-3xl sm:text-4xl font-bold text-center mb-16">
                    SharkTech <span class="text-shark-blue">Products</span>
                </h2>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
                    <!-- Product 1 -->
                    <div class="flex items-start space-x-6 bg-gray-900 p-8 rounded-2xl border border-gray-700 shadow-xl transition duration-300 hover:border-shark-blue/50">
                        <div class="flex-shrink-0 text-shark-blue mt-1">
                            <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.75 17L12 19.25L14.25 17M12 4V19.25M7 11h10"/></svg>
                        </div>
                        <div>
                            <h3 class="text-2xl font-bold mb-2 text-shark-light">Sentinel Core (Threat Intelligence)</h3>
                            <p class="text-gray-400">
                                An integrated threat intelligence platform that provides proactive monitoring and automated defense response across all endpoints. Ideal for high-stakes compliance environments.
                            </p>
                            <a href="#" class="mt-3 inline-block text-shark-blue font-semibold text-sm hover:underline">Product Sheet &rarr;</a>
                        </div>
                    </div>
                    
                    <!-- Product 2 -->
                    <div class="flex items-start space-x-6 bg-gray-900 p-8 rounded-2xl border border-gray-700 shadow-xl transition duration-300 hover:border-shark-blue/50">
                        <div class="flex-shrink-0 text-shark-blue mt-1">
                            <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 12H8m4-4l4 4-4 4"/></svg>
                        </div>
                        <div>
                            <h3 class="text-2xl font-bold mb-2 text-shark-light">FlowMaster ERP (Business Logic)</h3>
                            <p class="text-gray-400">
                                A customizable Enterprise Resource Planning (ERP) system designed to streamline supply chain, finance, and human resources in a single, secure environment.
                            </p>
                            <a href="#" class="mt-3 inline-block text-shark-blue font-semibold text-sm hover:underline">Get Demo Access &rarr;</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- NEW: 4.5 Pricing Section (Based on image_ffb15c.png) -->
        <section id="pricing" class="py-24 bg-shark-primary-blue border-b border-shark-blue/20">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <p class="text-center text-sm tracking-widest uppercase text-gray-400 mb-2">
                    Transparent Investment
                </p>
                <h2 class="text-3xl sm:text-4xl font-bold text-center mb-16">
                    Software <span class="text-shark-blue">Pricing Plans</span>
                </h2>
                
                <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                    
                    <!-- Plan 1: Basic POS -->
                    <div class="bg-gray-900 rounded-xl shadow-2xl overflow-hidden transform hover:scale-[1.02] transition duration-300 border-2 border-transparent hover:border-shark-blue/50">
                        <div class="bg-shark-primary-blue/70 p-6 text-center border-b border-gray-700">
                            <svg class="w-8 h-8 text-shark-blue inline-block mb-2" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 9V7a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2m2 4h10a2 2 0 002-2v-6a2 2 0 00-2-2H9a2 2 0 00-2 2v6a2 2 0 002 2zm7-5a2 2 0 11-4 0 2 2 0 014 0z"/></svg>
                            <h3 class="text-2xl font-extrabold text-shark-light">BASIC POS</h3>
                        </div>
                        <div class="p-8 text-center">
                            <p class="text-5xl font-extrabold text-shark-blue">$5<span class="text-xl text-gray-400 font-medium">/Monthly</span></p>
                            
                            <ul class="mt-6 text-sm text-gray-300 space-y-4">
                                <li class="border-b border-gray-800 pb-2 flex justify-between"><span>Number of Branch</span><span class="font-bold text-shark-light">1</span></li>
                                <li class="border-b border-gray-800 pb-2 flex justify-between"><span>Number of Products</span><span class="font-bold text-shark-light">1000</span></li>
                                <li class="border-b border-gray-800 pb-2 flex justify-between"><span>Number of Invoices</span><span class="font-bold text-shark-light">Unlimited</span></li>
                                <li class="border-b border-gray-800 pb-2 flex justify-between"><span>Number of User Account</span><span class="font-bold text-shark-light">20</span></li>
                                <li class="flex justify-between"><span>24/7 Priority Support</span><span class="text-red-500 font-bold">&times;</span></li>
                            </ul>

                            <button class="mt-8 w-full py-3 bg-gray-700 text-shark-light rounded-lg font-bold hover:bg-gray-600 transition">Start Basic</button>
                        </div>
                    </div>

                    <!-- Plan 2: Standard POS (Recommended) -->
                    <div class="bg-gray-900 rounded-xl shadow-2xl overflow-hidden transform scale-[1.05] transition duration-300 border-2 border-shark-blue shadow-glow">
                        <div class="bg-shark-blue/20 p-6 text-center border-b border-shark-blue">
                            <svg class="w-8 h-8 text-shark-blue inline-block mb-2" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M3.636 5.636l.707.707M12 20.25V21m-4.636-1.364l-.707-.707M18.636 19.364l.707.707M6.343 12L5 11.5V12m.5-6.5h-1"/></svg>
                            <h3 class="text-2xl font-extrabold text-shark-blue">STANDARD POS</h3>
                            <p class="text-xs font-semibold text-gray-400 mt-1">Recommended</p>
                        </div>
                        <div class="p-8 text-center">
                            <p class="text-5xl font-extrabold text-shark-blue">$10<span class="text-xl text-gray-400 font-medium">/Monthly</span></p>
                            
                            <ul class="mt-6 text-sm text-gray-300 space-y-4">
                                <li class="border-b border-gray-800 pb-2 flex justify-between"><span>Number of Branch</span><span class="font-bold text-shark-light">3</span></li>
                                <li class="border-b border-gray-800 pb-2 flex justify-between"><span>Number of Products</span><span class="font-bold text-shark-light">1500</span></li>
                                <li class="border-b border-gray-800 pb-2 flex justify-between"><span>Number of Invoices</span><span class="font-bold text-shark-light">Unlimited</span></li>
                                <li class="border-b border-gray-800 pb-2 flex justify-between"><span>Number of User Account</span><span class="font-bold text-shark-light">30</span></li>
                                <li class="flex justify-between"><span>24/7 Priority Support</span><span class="text-green-400 font-bold">&check;</span></li>
                            </ul>

                            <button class="mt-8 w-full py-3 bg-shark-blue text-shark-dark rounded-lg font-extrabold hover:bg-cyan-400 transition transform hover:scale-[1.01]">Get Standard</button>
                        </div>
                    </div>

                    <!-- Plan 3: Premium POS -->
                    <div class="bg-gray-900 rounded-xl shadow-2xl overflow-hidden transform hover:scale-[1.02] transition duration-300 border-2 border-transparent hover:border-shark-blue/50">
                        <div class="bg-shark-primary-blue/70 p-6 text-center border-b border-gray-700">
                            <svg class="w-8 h-8 text-shark-blue inline-block mb-2" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 6.5l8 4.5v9l-8 4.5-8-4.5v-9l8-4.5zM12 6.5v9M20 11l-8 4.5M4 11l8 4.5"/></svg>
                            <h3 class="text-2xl font-extrabold text-shark-light">PREMIUM POS</h3>
                        </div>
                        <div class="p-8 text-center">
                            <p class="text-5xl font-extrabold text-shark-blue">$20<span class="text-xl text-gray-400 font-medium">/Monthly</span></p>
                            
                            <ul class="mt-6 text-sm text-gray-300 space-y-4">
                                <li class="border-b border-gray-800 pb-2 flex justify-between"><span>Number of Branch</span><span class="font-bold text-shark-light">6</span></li>
                                <li class="border-b border-gray-800 pb-2 flex justify-between"><span>Number of Products</span><span class="font-bold text-shark-light">2000</span></li>
                                <li class="border-b border-gray-800 pb-2 flex justify-between"><span>Number of Invoices</span><span class="font-bold text-shark-light">Unlimited</span></li>
                                <li class="border-b border-gray-800 pb-2 flex justify-between"><span>Number of User Account</span><span class="font-bold text-shark-light">30</span></li>
                                <li class="flex justify-between"><span>24/7 Priority Support</span><span class="text-green-400 font-bold">&check;</span></li>
                            </ul>

                            <button class="mt-8 w-full py-3 bg-gray-700 text-shark-light rounded-lg font-bold hover:bg-gray-600 transition">Go Premium</button>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 5. Works Section (Previously Projects) -->
        <section id="works" class="py-24">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <p class="text-center text-sm tracking-widest uppercase text-gray-400 mb-2">
                    Our Track Record
                </p>
                <h2 class="text-3xl sm:text-4xl font-bold mb-6">Featured <span class="text-shark-blue">Works</span></h2>
                <p class="text-lg text-gray-400 max-w-3xl mx-auto mb-10">
                    Explore our recent successful case studies in enterprise security and cloud modernization. We deliver results that speak for themselves.
                </p>
                
                <!-- Works Gallery Placeholder -->
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <div class="bg-gray-900 p-6 rounded-xl border border-gray-700">
                        <img src="https://placehold.co/400x250/0d121c/00ffff?text=Financial+Modernization" alt="Project Image" class="w-full rounded-lg mb-4" onerror="this.onerror=null; this.src='https://placehold.co/400x250/0d121c/00ffff?text=Image+Unavailable';">
                        <h3 class="text-xl font-bold text-shark-blue">Global Bank Data Shield</h3>
                        <p class="text-gray-400 text-sm mt-1">Sector: FinTech | Service: Cyber Audit & Policy</p>
                    </div>
                    <div class="bg-gray-900 p-6 rounded-xl border border-gray-700">
                        <img src="https://placehold.co/400x250/0d121c/00ffff?text=Logistics+Optimization" alt="Project Image" class="w-full rounded-lg mb-4" onerror="this.onerror=null; this.src='https://placehold.co/400x250/0d121c/00ffff?text=Image+Unavailable';">
                        <h3 class="text-xl font-bold text-shark-blue">Supply Chain Logic App</h3>
                        <p class="text-gray-400 text-sm mt-1">Sector: Logistics | Service: Custom Software</p>
                    </div>
                    <div class="bg-gray-900 p-6 rounded-xl border border-gray-700">
                        <img src="https://placehold.co/400x250/0d121c/00ffff?text=Healthcare+Cloud" alt="Project Image" class="w-full rounded-lg mb-4" onerror="this.onerror=null; this.src='https://placehold.co/400x250/0d121c/00ffff?text=Image+Unavailable';">
                        <h3 class="text-xl font-bold text-shark-blue">HIPAA-Compliant Cloud</h3>
                        <p class="text-gray-400 text-sm mt-1">Sector: Healthcare | Service: Cloud Migration</p>
                    </div>
                </div>
                
            </div>
        </section>

        <!-- 6. About Section -->
        <section id="about" class="py-24 bg-shark-dark/90 border-t border-b border-gray-800 backdrop-blur-sm">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="md:flex md:items-center md:space-x-12">
                    <div class="md:w-1/2 mb-8 md:mb-0">
                        <p class="text-sm tracking-widest uppercase text-gray-400 mb-2">
                            Our Philosophy
                        </p>
                        <h2 class="text-3xl sm:text-4xl font-bold mb-6">
                            Delivering <span class="text-shark-blue">Scalable Outcomes</span>, Not Just Code.
                        </h2>
                        <p class="text-lg text-gray-400 mb-6">
                            We are an extension of your business, committed to a partnership model that prioritizes measurable growth and security. Our team consists of domain experts in finance, logistics, and data science, ensuring technology aligns perfectly with your strategic goals.
                        </p>
                        <a href="#" class="bg-gray-700 text-shark-light font-medium px-6 py-3 rounded-lg shadow-md hover:bg-gray-600 transition duration-300 border border-gray-600 inline-block">
                            Meet the Leadership
                        </a>
                    </div>
                    <div class="md:w-1/2 relative">
                        <!-- Placeholder Image with Clean Border -->
                        <img src="https://placehold.co/600x400/0d121c/00ffff?text=Strategic+Development" alt="Abstract strategic development visualization" class="rounded-xl shadow-2xl border-2 border-shark-blue/50 w-full h-auto object-cover transition duration-500" onerror="this.onerror=null; this.src='https://placehold.co/600x400/0d121c/00ffff?text=Image+Unavailable';">
                    </div>
                </div>
            </div>
        </section>
        
        <!-- 7. Blog Section (ENHANCED) -->
        <section id="blog" class="py-24">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
                <p class="text-center text-sm tracking-widest uppercase text-gray-400 mb-2">
                    Latest Insights
                </p>
                <h2 class="text-3xl sm:text-4xl font-bold mb-6">SharkTech <span class="text-shark-blue">Blog</span></h2>
                <p class="text-lg text-gray-400 max-w-3xl mx-auto mb-10">
                    Read the latest articles on cybersecurity trends, AI innovations, and cloud strategy from our expert team.
                </p>
                
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    
                    <!-- Blog Post 1: The Zero-Trust Model -->
                    <div class="bg-gray-900 rounded-xl border border-gray-700 transition duration-300 hover:border-shark-blue/50 overflow-hidden text-left">
                        <div class="h-40 border-b border-gray-700"
                             style="background-image: url('https://placehold.co/600x400/1a2233/00ffff?text=Zero+Trust+Strategy'); background-size: cover; background-position: center;">
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold text-shark-blue mb-2">The Zero-Trust Model: A Practical Guide</h3>
                            <p class="text-gray-400 text-sm">How to implement network micro-segmentation in enterprise environments.</p>
                            <div class="mt-3 text-xs text-gray-500 space-x-2 border-t border-gray-800 pt-3">
                                <span class="text-shark-blue font-semibold">15 Oct 2025</span>
                                <span class="text-gray-600">|</span>
                                <span class="text-gray-400">Security</span>
                            </div>
                            <a href="#" class="mt-3 inline-block text-shark-blue font-semibold text-xs hover:underline">Read Article &rarr;</a>
                        </div>
                    </div>

                    <!-- Blog Post 2: Scaling SaaS with Serverless -->
                    <div class="bg-gray-900 rounded-xl border border-gray-700 transition duration-300 hover:border-shark-blue/50 overflow-hidden text-left">
                        <div class="h-40 border-b border-gray-700"
                             style="background-image: url('https://placehold.co/600x400/1a2233/00ffff?text=Serverless+Cloud'); background-size: cover; background-position: center;">
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold text-shark-blue mb-2">Scaling SaaS with Serverless Architecture</h3>
                            <p class="text-gray-400 text-sm">A look at cost optimization and performance gains using AWS Lambda and GCP Functions.</p>
                            <div class="mt-3 text-xs text-gray-500 space-x-2 border-t border-gray-800 pt-3">
                                <span class="text-shark-blue font-semibold">01 Sep 2025</span>
                                <span class="text-gray-600">|</span>
                                <span class="text-gray-400">Cloud Strategy</span>
                            </div>
                            <a href="#" class="mt-3 inline-block text-shark-blue font-semibold text-xs hover:underline">Read Article &rarr;</a>
                        </div>
                    </div>

                    <!-- Blog Post 3: The Future of AI -->
                    <div class="bg-gray-900 rounded-xl border border-gray-700 transition duration-300 hover:border-shark-blue/50 overflow-hidden text-left">
                        <div class="h-40 border-b border-gray-700"
                             style="background-image: url('https://placehold.co/600x400/1a2233/00ffff?text=AI+in+Business'); background-size: cover; background-position: center;">
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-bold text-shark-blue mb-2">The Future of AI in Business Development</h3>
                            <p class="text-gray-400 text-sm">Exploring generative AI for market analysis and personalized customer experiences.</p>
                            <div class="mt-3 text-xs text-gray-500 space-x-2 border-t border-gray-800 pt-3">
                                <span class="text-shark-blue font-semibold">20 Aug 2025</span>
                                <span class="text-gray-600">|</span>
                                <span class="text-gray-400">Innovation</span>
                            </div>
                            <a href="#" class="mt-3 inline-block text-shark-blue font-semibold text-xs hover:underline">Read Article &rarr;</a>
                        </div>
                    </div>

                </div>
            </div>
        </section>

        <!-- 8. Support Section (Existing) -->
        <section id="support" class="py-24 bg-shark-blue/10 border-t border-b border-shark-blue/20 text-center backdrop-blur-sm">
            <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
                <p class="text-sm tracking-widest uppercase text-shark-blue mb-2 font-semibold">
                    After Sales Service
                </p>
                <h2 class="text-3xl sm:text-4xl font-extrabold mb-4 text-shark-light">
                    Need Technical Support?
                </h2>
                <p class="text-xl text-gray-300 mb-8">
                    Our dedicated support team is ready to assist with any product inquiries, technical issues, or managed service needs. Log a ticket below.
                </p>
                
                <a href="#contact" class="bg-shark-blue text-shark-dark font-extrabold px-10 py-3 rounded-xl text-lg shadow-2xl hover:bg-cyan-400 transition duration-300 transform hover:scale-105 inline-block">
                    Open a Support Ticket
                </a>
                
                <div class="mt-8 text-sm text-gray-500">
                    For immediate concerns, please call our 24/7 line: (555) 555-SHARK
                </div>

                <!-- AI Support Assistant Feature -->
                <div class="mt-10 max-w-3xl mx-auto text-left">
                    <h3 class="text-xl font-bold text-shark-blue mb-4">✨ AI Support Assistant</h3>
                    <div class="flex space-x-2">
                        <input type="text" id="ai-support-input" placeholder="Ask a question about security, cloud, or our services..." class="flex-grow px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:border-shark-blue focus:ring-shark-blue text-white outline-none">
                        <button type="button" id="ai-support-button" 
                                class="bg-shark-blue text-shark-dark font-bold px-4 py-3 rounded-xl hover:bg-cyan-400 transition duration-300">
                            Ask
                        </button>
                    </div>
                    
                    <!-- AI Answer Display -->
                    <div id="ai-support-answer" class="mt-4 p-4 bg-gray-900 border border-gray-800 rounded-xl min-h-[50px] transition-all duration-300">
                        <p id="answer-text" class="text-gray-400 italic">Answers will appear here. Powered by Google Search Grounding.</p>
                        <div id="answer-sources" class="mt-3 text-xs text-gray-500 hidden border-t border-gray-800 pt-2">
                            <strong>Sources:</strong> <span id="source-list"></span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 9. Contact Section (Existing) -->
        <section id="contact" class="py-24">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <h2 class="text-3xl sm:text-4xl font-bold text-center mb-12">Get In <span class="text-shark-blue">Touch</span></h2>

                <!-- Contact form container with solid background -->
                <div class="max-w-3xl mx-auto bg-gray-900 p-8 sm:p-12 rounded-2xl border border-gray-700 shadow-2xl">
                    <form onsubmit="event.preventDefault(); showMessage();" class="space-y-6">
                        <div>
                            <label for="name" class="block text-sm font-medium text-gray-300 mb-2">Full Name</label>
                            <input type="text" id="name" name="name" required class="w-full px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:border-shark-blue focus:ring-shark-blue text-white outline-none">
                        </div>
                        <div>
                            <label for="email" class="block text-sm font-medium text-gray-300 mb-2">Work Email</label>
                            <input type="email" id="email" name="email" required class="w-full px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:border-shark-blue focus:ring-shark-blue text-white outline-none">
                        </div>
                        <div>
                            <label for="service" class="block text-sm font-medium text-gray-300 mb-2">Inquiry Type (Service, Product, or Support)</label>
                            <select id="service" name="service" required class="w-full px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:border-shark-blue focus:ring-shark-blue text-white outline-none appearance-none">
                                <option value="" disabled selected>Select an Inquiry Type</option>
                                <option value="Cybersecurity & Compliance">Service: Cybersecurity & Compliance</option>
                                <option value="Bespoke Software Development">Service: Bespoke Software Development</option>
                                <option value="Website Development & Marketing">Service: Website Development & Marketing</option>
                                <option value="E-commerce & POS Solutions">Service: E-commerce & POS Solutions</option>
                                <option value="Sentinel Core Product">Product: Sentinel Core</option>
                                <option value="FlowMaster ERP Product">Product: FlowMaster ERP</option>
                                <option value="Support Ticket">Support Ticket / After Sales</option>
                                <option value="General Inquiry">General Inquiry</option>
                            </select>
                        </div>
                        <div>
                            <label for="message" class="block text-sm font-medium text-gray-300 mb-2">Tell us about your project goals</label>
                            <textarea id="message" name="message" rows="4" required class="w-full px-4 py-3 bg-gray-800 border border-gray-700 rounded-lg focus:border-shark-blue focus:ring-shark-blue text-white outline-none resize-none"></textarea>
                            
                            <!-- AI Drafting Feature Button -->
                            <button type="button" id="draft-message-btn" 
                                class="mt-2 w-full flex items-center justify-center space-x-2 bg-gray-700 text-shark-blue font-bold px-4 py-2 rounded-lg hover:bg-gray-600 transition duration-300 transform hover:scale-[1.005]">
                                <span id="draft-message-text">✨ Draft Message with AI</span>
                                <svg id="draft-message-spinner" class="animate-spin h-5 w-5 text-shark-blue hidden" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"><circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle><path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path></svg>
                            </button>

                        </div>
                        <button type="submit" class="w-full bg-shark-blue text-shark-dark font-bold px-4 py-3 rounded-xl hover:bg-cyan-400 transition duration-300 transform hover:scale-[1.01]">
                            Send Inquiry
                        </button>
                    </form>
                    <!-- Success Message Box -->
                    <div id="success-message" class="mt-6 p-4 bg-green-900 border border-green-700 text-green-200 rounded-lg text-center hidden">
                        Thank you! Your strategic inquiry has been received. We'll be in touch within 24 hours.
                    </div>
                </div>
            </div>
        </section>

    </main>

    <!-- Footer (ENHANCED) -->
    <footer class="bg-shark-primary-blue border-t border-shark-blue/20 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-12 text-gray-400">
                
                <!-- Column 1: Logo & About -->
                <div>
                    <a href="#home" class="flex items-center space-x-2 mb-4">
                        <svg class="w-8 h-8 text-shark-blue" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                            <path d="M4 12c0-1.66 1.34-3 3-3h10c1.66 0 3 1.34 3 3s-1.34 3-3 3H7c-1.66 0-3-1.34-3-3z"/>
                            <path d="M10 9L7 6l-3 3M14 9l3-3 3 3"/>
                            <path d="M12 17l3-3m-6 0l3 3"/>
                        </svg>
                        <span class="text-2xl font-extrabold tracking-tight text-shark-light">Shark<span class="text-shark-blue">Tech</span></span>
                    </a>
                    <p class="text-sm">
                        SharkTech is a leading global provider of AI-driven strategy, cloud architecture, and bespoke software solutions, committed to securing your digital future.
                    </p>
                    <div class="flex space-x-4 mt-4 text-gray-500">
                        <!-- Social Icons Placeholder -->
                        <a href="#" class="hover:text-shark-blue transition"><svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M22.6 13.6c0 5.5-4.5 10-10 10s-10-4.5-10-10 4.5-10 10-10 10 4.5 10 10zm-6.5-1.5h-2v5h-3v-5h-2v-2h2v-1.5c0-1.2 1.2-2.5 2.5-2.5h2v2h-1.5c-.3 0-.5.2-.5.5v1.5h2.5l-.5 2z"/></svg></a>
                        <a href="#" class="hover:text-shark-blue transition"><svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.799-1.574 2.167-2.724-.951.564-2.005.974-3.127 1.195-.89-.982-2.152-1.594-3.558-1.594-2.736 0-4.966 2.23-4.966 4.965 0 .39.044.765.122 1.125-4.133-.207-7.788-2.182-10.245-5.188-.426.726-.666 1.558-.666 2.441 0 1.713.87 3.228 2.196 4.122-.807-.026-1.56-.248-2.215-.61.004.02.004.04.004.062 0 2.41 1.717 4.417 3.996 4.88-.42.115-.86.17-1.314.17-.322 0-.63-.03-.93-.08.636 1.98 2.483 3.42 4.672 3.461-1.696 1.334-3.84 2.127-6.172 2.127-.402 0-.799-.023-1.19-.074 2.18 1.397 4.768 2.21 7.54 2.21 9.043 0 13.99-7.498 13.99-13.988 0-.214-.005-.426-.014-.637.962-.695 1.795-1.562 2.457-2.54z"/></svg></a>
                        <a href="#" class="hover:text-shark-blue transition"><svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.6.111.822-.258.822-.577 0-.285-.01-1.04-.015-2.043-3.338.724-4.042-1.61-4.042-1.61-.546-1.387-1.334-1.756-1.334-1.756-1.09-.743.082-.728.082-.728 1.205.084 1.838 1.238 1.838 1.238 1.07 1.836 2.809 1.305 3.493.998.108-.775.419-1.305.762-1.605-2.665-.304-5.466-1.332-5.466-5.93 0-1.31.467-2.38 1.238-3.22-.124-.304-.535-1.523.117-3.176 0 0 1.008-.322 3.301 1.23A11.536 11.536 0 0112 5.823c1.04.002 2.083.14 3.085.405 2.292-1.552 3.3-1.23 3.3-1.23.653 1.653.242 2.872.118 3.176.772.84 1.237 1.91 1.237 3.22 0 4.612-2.802 5.626-5.474 5.922.43.37.822 1.102.822 2.217 0 1.597-.015 2.887-.015 3.28 0 .323.218.692.827.576C20.563 21.796 24 17.302 24 12 24 5.373 18.627 0 12 0z"/></svg></a>
                        <a href="#" class="hover:text-shark-blue transition"><svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M19.615 3.097c-.779-.214-2.585-.494-5.385-.494s-4.606.28-5.385.494c-1.728.473-2.657 1.542-3.13 3.27-1.12 3.847-1.12 7.71 0 11.557.473 1.728 1.402 2.797 3.13 3.27.779.214 2.585.494 5.385.494s4.606-.28 5.385-.494c1.728-.473 2.657-1.542 3.13-3.27.473-1.728.537-3.486.537-5.385s-.064-3.657-.537-5.385c-.473-1.728-1.402-2.797-3.13-3.27zM12 18.5c-3.59 0-6.5-2.91-6.5-6.5S8.41 5.5 12 5.5s6.5 2.91 6.5 6.5-2.91 6.5-6.5 6.5zM12 7.5c-2.485 0-4.5 2.015-4.5 4.5s2.015 4.5 4.5 4.5 4.5-2.015 4.5-4.5-2.015-4.5-4.5-4.5z"/></svg></a>
                    </div>
                </div>

                <!-- Column 2: Recent Posts (Blog Links) -->
                <div>
                    <h4 class="text-lg font-bold text-shark-light mb-4 border-b border-gray-800 pb-2">Recent Posts</h4>
                    <ul class="space-y-3">
                        <li><a href="#blog" class="hover:text-shark-blue transition text-sm">The Practical Guide to Zero-Trust Implementation</a><p class="text-xs text-gray-600 mt-0.5">Oct 15, 2025</p></li>
                        <li><a href="#blog" class="hover:text-shark-blue transition text-sm">Scaling with Serverless Architecture: Cost Analysis</a><p class="text-xs text-gray-600 mt-0.5">Sep 01, 2025</p></li>
                        <li><a href="#blog" class="hover:text-shark-blue transition text-sm">AI in Business: Market Analysis and Personalized UX</a><p class="text-xs text-gray-600 mt-0.5">Aug 20, 2025</p></li>
                    </ul>
                </div>

                <!-- Column 3: Contact Us -->
                <div>
                    <h4 class="text-lg font-bold text-shark-light mb-4 border-b border-gray-800 pb-2">Contact Us</h4>
                    <ul class="space-y-3 text-sm">
                        <li class="flex items-start space-x-2">
                            <svg class="w-5 h-5 text-shark-blue flex-shrink-0 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.828 0l-4.243-4.243m10.121-10.121L13.414 3.1a1.998 1.998 0 00-2.828 0L6.343 7.343a1.998 1.998 0 000 2.828l4.243 4.243"/></svg>
                            <span>123 Data Center Ave, San Jose, CA 95134</span>
                        </li>
                        <li class="flex items-center space-x-2">
                            <svg class="w-5 h-5 text-shark-blue" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.5l1 4h5l1-4H19a2 2 0 012 2v14a2 2 0 01-2 2h-4.5l-1-4h-5l-1 4H5a2 2 0 01-2-2V5z"/></svg>
                            <span>(555) 555-SHARK (24/7 Support)</span>
                        </li>
                        <li class="flex items-center space-x-2">
                            <svg class="w-5 h-5 text-shark-blue" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.8 4.7a1 1 0 001.4 0L21 8m-17 0l7.8 4.7a1 1 0 001.4 0L21 8M3 8v12a2 2 0 002 2h14a2 2 0 002-2V8"/></svg>
                            <a href="mailto:contact@sharktech.com" class="hover:text-shark-blue transition">contact@sharktech.com</a>
                        </li>
                    </ul>
                </div>

                <!-- Column 4: Newsletter -->
                <div>
                    <h4 class="text-lg font-bold text-shark-light mb-4 border-b border-gray-800 pb-2">Newsletter</h4>
                    <p class="text-sm mb-4">Subscribe for monthly insights on cybersecurity and AI advancements.</p>
                    <form onsubmit="event.preventDefault(); console.log('Newsletter subscription submitted.');">
                        <div class="flex">
                            <input type="email" placeholder="Your Email" required class="flex-grow px-4 py-3 bg-gray-800 border border-gray-700 rounded-l-lg focus:border-shark-blue focus:ring-shark-blue text-white outline-none text-sm">
                            <button type="submit" class="bg-shark-blue text-shark-dark font-bold px-4 py-3 rounded-r-lg hover:bg-cyan-400 transition">
                                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                            </button>
                        </div>
                    </form>
                </div>
            </div>
            
            <div class="mt-12 pt-8 border-t border-gray-800 text-center">
                <p class="text-sm text-gray-600">&copy; 2025 SharkTech. All rights reserved. | Built with strategic security in mind.</p>
            </div>
        </div>
    </footer>


    <!-- JavaScript for form submission handling, menu toggle, and Firebase Auth -->
    <script type="module">
        // Firebase Imports
        import { initializeApp } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-app.js";
        import { getAuth, signInAnonymously, signInWithCustomToken, onAuthStateChanged, signOut, setPersistence, browserSessionPersistence } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-auth.js";
        import { getFirestore, setLogLevel } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-firestore.js";

        // Gemini API Configuration
        const API_KEY = ""; // Leave as-is
        const MODEL_NAME = 'gemini-2.5-flash-preview-09-2025';

        // Exponential backoff helper function for robust API calls
        async function fetchWithExponentialBackoff(url, options, maxRetries = 5, delay = 1000) {
            for (let i = 0; i < maxRetries; i++) {
                try {
                    const response = await fetch(url, options);
                    if (response.status !== 429 && response.status < 500) {
                        return response;
                    }
                    if (i === maxRetries - 1) {
                        throw new Error(`Request failed after ${maxRetries} retries with status ${response.status}.`);
                    }
                    await new Promise(resolve => setTimeout(resolve, delay * (2 ** i)));
                } catch (error) {
                    if (i === maxRetries - 1) throw error;
                    await new Promise(resolve => setTimeout(resolve, delay * (2 ** i)));
                }
            }
        }

        // Main Gemini API call utility
        async function geminiCall(userQuery, systemPrompt, useGrounding) {
            const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/${MODEL_NAME}:generateContent?key=${API_KEY}`;
            
            const payload = {
                contents: [{ parts: [{ text: userQuery }] }],
                systemInstruction: { parts: [{ text: systemPrompt }] },
            };

            if (useGrounding) {
                payload.tools = [{ "google_search": {} }];
            }

            const response = await fetchWithExponentialBackoff(apiUrl, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify(payload)
            });

            const result = await response.json();
            const candidate = result.candidates?.[0];

            if (candidate && candidate.content?.parts?.[0]?.text) {
                const text = candidate.content.parts[0].text;

                let sources = [];
                const groundingMetadata = candidate.groundingMetadata;
                if (groundingMetadata && groundingMetadata.groundingAttributions) {
                    sources = groundingMetadata.groundingAttributions
                        .map(attribution => ({
                            uri: attribution.web?.uri,
                            title: attribution.web?.title,
                        }))
                        .filter(source => source.uri && source.title);
                }

                return { text, sources };
            } else {
                // If there's an error message in the response, use it
                throw new Error(result.error?.message || "LLM response structure invalid or empty.");
            }
        }

        // Global variables provided by the environment
        const appId = typeof __app_id !== 'undefined' ? __app_id : 'default-app-id';
        const firebaseConfig = JSON.parse(typeof __firebase_config !== 'undefined' ? __firebase_config : '{}');

        // 1. Initialize Firebase Services
        const app = initializeApp(firebaseConfig);
        const db = getFirestore(app);
        const auth = getAuth(app);
        setLogLevel('debug'); // Set log level for debugging

        // Function to handle form success message
        window.showMessage = function() {
            document.querySelector('#contact form').classList.add('hidden');
            document.getElementById('success-message').classList.remove('hidden');

            setTimeout(() => {
                document.getElementById('success-message').classList.add('hidden');
                document.querySelector('#contact form').classList.remove('hidden');
                document.querySelector('#contact form').reset();
            }, 5000);
        }

        // 2. Auth State Change Listener and UI Updater
        onAuthStateChanged(auth, (user) => {
            let userIdDisplayElement = document.getElementById('auth-status');
            let authButton = document.getElementById('auth-button');
            let mobileAuthButton = document.getElementById('mobile-auth-button');
            let mobileAuthButtonText = document.getElementById('mobile-auth-button-text');

            if (user) {
                // User is signed in.
                const userId = user.uid;

                // Desktop UI Update
                userIdDisplayElement.innerHTML = `
                    <span class="text-xs text-gray-400 block mb-1">Authenticated User ID:</span>
                    <span class="text-shark-blue font-mono text-xs break-all">${userId}</span>
                `;
                authButton.textContent = 'Sign Out';
                authButton.onclick = handleSignOut;
                authButton.classList.remove('bg-gray-800', 'text-shark-blue', 'border-shark-blue/50', 'hover:bg-gray-700', 'hover:shadow-glow');
                authButton.classList.add('bg-red-700', 'hover:bg-red-600', 'text-white', 'border-red-700/50');
                
                // Mobile UI Update
                mobileAuthButtonText.textContent = 'Sign Out';
                mobileAuthButton.onclick = handleSignOut;
                mobileAuthButton.classList.remove('text-shark-blue', 'bg-gray-900', 'hover:bg-gray-800');
                mobileAuthButton.classList.add('bg-red-700', 'text-white', 'hover:bg-red-600');


            } else {
                // User is signed out.

                // Desktop UI Update
                userIdDisplayElement.innerHTML = `<span class="text-sm text-gray-400">Not Logged In</span>`;
                authButton.textContent = 'Account Login';
                // FIX: Replace window.location.href='/crm-login' with a console log to avoid invalid URL error
                authButton.onclick = () => { closeMenu(); console.log("Simulating navigation to /crm-login page..."); };
                authButton.classList.add('bg-gray-800', 'text-shark-blue', 'border-shark-blue/50', 'hover:bg-gray-700', 'hover:shadow-glow');
                authButton.classList.remove('bg-red-700', 'hover:bg-red-600', 'text-white', 'border-red-700/50');

                // Mobile UI Update
                mobileAuthButtonText.textContent = 'Account / CRM Login';
                // FIX: Replace window.location.href='/crm-login' with a console log to avoid invalid URL error
                mobileAuthButton.onclick = () => { closeMenu(); console.log("Simulating navigation to /crm-login page..."); };
                mobileAuthButton.classList.add('text-shark-blue', 'bg-gray-900', 'hover:bg-gray-800');
                mobileAuthButton.classList.remove('bg-red-700', 'text-white', 'hover:bg-red-600');
            }
        });

        // 3. Initial Sign In with Custom Token (Mandatory if available)
        async function initialSignIn() {
            try {
                // Set persistence to session to maintain login state across tab closures
                await setPersistence(auth, browserSessionPersistence);
                
                if (typeof __initial_auth_token !== 'undefined' && __initial_auth_token) {
                    await signInWithCustomToken(auth, __initial_auth_token);
                    console.log("Signed in with custom token.");
                } else {
                    // Fallback to anonymous sign-in if no custom token is available
                    await signInAnonymously(auth);
                    console.log("Signed in anonymously.");
                }
            } catch (error) {
                console.error("Authentication failed:", error.message);
            }
        }

        // 4. Sign Out Function
        window.handleSignOut = async function() {
            try {
                await signOut(auth);
                console.log("User signed out.");
                // Close mobile menu on sign out
                closeMenu();
            } catch (error) {
                console.error("Sign out error:", error.message);
            }
        }

        // 5. Mobile Menu Functions (moved into module script for access)
        const mobileMenu = document.getElementById('mobile-menu');
        const menuToggle = document.getElementById('menu-toggle');
        const menuClose = document.getElementById('menu-close');

        window.openMenu = function() {
            mobileMenu.classList.remove('-translate-x-full');
            mobileMenu.classList.add('translate-x-0');
        }

        window.closeMenu = function() {
            mobileMenu.classList.add('-translate-x-full');
            mobileMenu.classList.remove('translate-x-0');
        }

        menuToggle.addEventListener('click', openMenu);
        menuClose.addEventListener('click', closeMenu);

        // --- GEMINI API Feature 1: AI Support Assistant (Grounding) ---
        window.askAISupport = async function() {
            const input = document.getElementById('ai-support-input');
            const button = document.getElementById('ai-support-button');
            const answerDiv = document.getElementById('ai-support-answer');
            const answerText = document.getElementById('answer-text');
            const sourceDiv = document.getElementById('answer-sources');
            const sourceListSpan = document.getElementById('source-list');
            
            const question = input.value.trim();

            if (!question) {
                answerText.textContent = "Please enter a question to get a response.";
                return;
            }

            // UI state: Loading
            button.disabled = true;
            button.textContent = 'Searching...';
            answerDiv.classList.add('animate-pulse');
            answerText.textContent = "Processing your query with real-time grounding...";
            sourceDiv.classList.add('hidden');

            const systemPrompt = `You are a helpful and knowledgeable AI Support Agent for SharkTech, a technology company. Answer the user's question concisely and professionally. If the question is about a general technical topic (like 'What is Zero Trust'), use Google Search Grounding to provide the most up-to-date factual information.`;

            try {
                // Call Gemini with Grounding enabled
                const response = await geminiCall(question, systemPrompt, true); 
                
                answerText.textContent = response.text || "I was unable to find a definitive answer for that right now. Please try rephrasing.";
                
                // Handle Sources
                if (response.sources && response.sources.length > 0) {
                    const sourceLinks = response.sources.map(s => 
                        `<a href="${s.uri}" target="_blank" rel="noopener noreferrer" class="text-shark-blue hover:underline break-words">${s.title || s.uri}</a>`
                    ).join(' | ');
                    sourceListSpan.innerHTML = sourceLinks;
                    sourceDiv.classList.remove('hidden');
                } else {
                    sourceListSpan.innerHTML = "No external sources found for this answer.";
                    sourceDiv.classList.add('hidden'); // Ensure hidden if no sources
                }

            } catch (error) {
                console.error("AI Support Error:", error);
                answerText.textContent = "A connection error occurred with the AI service. Please check your network or try again later.";
                sourceDiv.classList.add('hidden');
            } finally {
                // UI state: Complete
                button.disabled = false;
                button.textContent = 'Ask';
                answerDiv.classList.remove('animate-pulse');
            }
        }

        // --- GEMINI API Feature 2: AI Message Drafter ---
        window.draftMessage = async function() {
            const btn = document.getElementById('draft-message-btn');
            const textSpan = document.getElementById('draft-message-text');
            const spinner = document.getElementById('draft-message-spinner');
            const inquiryType = document.getElementById('service').value;
            const messageField = document.getElementById('message');

            if (!inquiryType || inquiryType === "") {
                messageField.value = "Please select an Inquiry Type (e.g., Cybersecurity & Compliance) before drafting a message.";
                return;
            }

            // UI state: Loading
            btn.disabled = true;
            textSpan.textContent = "Drafting...";
            spinner.classList.remove('hidden');

            const systemPrompt = `You are a professional business development assistant for a high-tech firm. Your task is to generate a concise, formal, and goal-oriented message draft for a prospective client. The message should propose an initial meeting or consultation based on the service/product mentioned. Do not use markdown (no bullet points or headings). Start directly with the body of the message.`;
            const userQuery = `Draft a professional message (one short paragraph) for a client inquiring about the following service or product: ${inquiryType}.`;

            try {
                // Call Gemini without grounding
                const response = await geminiCall(userQuery, systemPrompt, false); 
                messageField.value = response.text.trim();
            } catch (error) {
                console.error("AI Drafting Error:", error);
                messageField.value = "Sorry, the AI drafting service encountered an error. Please write your message manually.";
            } finally {
                // UI state: Complete
                btn.disabled = false;
                textSpan.textContent = '✨ Draft Message with AI';
                spinner.classList.add('hidden');
            }
        }

        // Attach event listeners
        document.getElementById('draft-message-btn').addEventListener('click', window.draftMessage);
        document.getElementById('ai-support-button').addEventListener('click', window.askAISupport);


        // Start the authentication process
        initialSignIn();
    </script>
</body>
</html>
