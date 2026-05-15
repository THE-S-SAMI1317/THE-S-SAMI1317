<!DOCTYPE html>
<html lang="en">
    <html lang="en" class="scroll-smooth"></html>

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shahriar - Future-Ready Developer</title>
    <meta name="description"
        content="Portfolio of Shahriar , a Computer Science Engineering Student specializing in Programming and Web Development.">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link
        href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700;800&family=Space+Grotesk:wght@300;400;500;600;700&family=Fira+Code:wght@400;500&display=swap"
        rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        primary: '#8B5CF6',
                        secondary: '#EC4899',
                        accent: '#06B6D4',
                        dark: '#0B0F19',
                        darker: '#020617',
                        light: '#F3F4F6',
                        cardDark: 'rgba(17, 24, 39, 0.7)',
                    },
                    fontFamily: {
                        sans: 'Outfit, sans-serif',
                        heading: 'Space Grotesk, sans-serif',
                        mono: 'Fira Code, monospace',
                    },
                    animation: {
                        blob: 'blob 10s infinite',
                        float: 'float 6s ease-in-out infinite',
                        'spin-slow': 'spin 15s linear infinite',
                        'pulse-glow': 'pulse-glow 3s ease-in-out infinite',
                    },
                    keyframes: {
                        blob: {
                            '0%': { transform: 'translate(0px, 0px) scale(1)' },
                            '33%': { transform: 'translate(30px, -50px) scale(1.1)' },
                            '66%': { transform: 'translate(-20px, 20px) scale(0.9)' },
                            '100%': { transform: 'translate(0px, 0px) scale(1)' },
                        },
                        float: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-20px)' },
                        },
                        'pulse-glow': {
                            '0%, 100%': { boxShadow: '0 0 15px rgba(139, 92, 246, 0.3)' },
                            '50%': { boxShadow: '0 0 30px rgba(139, 92, 246, 0.6)' },
                        },
                    },
                }
            }
        }
    </script>
    <style>
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }

        ::-webkit-scrollbar-track {
            background: #0B0F19;
        }

        ::-webkit-scrollbar-thumb {
            background: linear-gradient(to bottom, #8B5CF6, #EC4899);
            border-radius: 10px;
        }

        /* Glassmorphism Ultra */
        .glass {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
        }

        .dark .glass {
            background: rgba(11, 15, 25, 0.6);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }

        /* Spotlight Effect */
        .spotlight-card {
            position: relative;
            overflow: hidden;
        }

        .spotlight-card::before {
            content: '';
            position: absolute;
            background: radial-gradient(800px circle at var(--mouse-x), rgba(255, 255, 255, 0.06), transparent 40%);
            z-index: 3;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0;
            transition: opacity 0.5s;
            pointer-events: none;
        }

        .spotlight-card:hover::before {
            opacity: 1;
        }

        /* Text Gradient */
        .text-gradient {
            background: linear-gradient(to right, #8B5CF6, #EC4899, #06B6D4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .text-outline {
            -webkit-text-stroke: 1px rgba(139, 92, 246, 0.2);
            color: transparent;
        }

        .dark .text-outline {
            -webkit-text-stroke: 1px rgba(255, 255, 255, 0.1);
        }

        /* Loader */
        #preloader {
            position: fixed;
            inset: 0;
            z-index: 9999;
            background: #020617;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: opacity 0.6s ease, visibility 0.6s ease;
        }

        /* Scroll Progress */
        #scroll-progress {
            position: fixed;
            top: 0;
            left: 0;
            height: 3px;
            background: linear-gradient(90deg, #8B5CF6, #EC4899, #06B6D4);
            z-index: 100000;
            width: 0;
            box-shadow: 0 0 15px rgba(139, 92, 246, 0.7);
        }

        /* Bento Grid */
        .bento-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        /* Card Tilt */
        .tilt-card {
            transform-style: preserve-3d;
            transform: perspective(1000px);
        }
    </style>
</head>

<body
    class="font-sans text-gray-700 dark:text-gray-300 bg-white dark:bg-darker transition-colors duration-300 selection:bg-primary selection:text-white overflow-x-hidden">
    <div id="mouse-glow"
        class="fixed pointer-events-none inset-0 z-0 transition-opacity duration-300 opacity-50 dark:opacity-30">
        <div class="absolute w-500px h-500px bg-primary/20 rounded-full blur-100px -translate-x-12 -translate-y-12 transition-transform duration-75"
            id="glow-circle"></div>
    </div>

    <!-- Preloader -->
    <div id="preloader">
        <div class="relative w-24 h-24">
            <div class="absolute inset-0 border-t-4 border-primary rounded-full animate-spin"></div>
            <div class="absolute inset-2 border-r-4 border-secondary rounded-full animate-spin-slow"></div>
            <div class="absolute inset-4 border-l-4 border-accent rounded-full animate-spin"></div>
        </div>
    </div>

    <!-- Scroll Progress -->
    <div id="scroll-progress"></div>

    <!-- Navigation -->
    <nav class="fixed w-full z-50 glass transition-all duration-300 top-0 border-b border-white/10" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex-shrink-0 cursor-pointer group" onclick="window.scrollTo(0, 0)">
                    <span
                        class="font-heading font-bold text-2xl tracking-tighter text-dark dark:text-white group-hover:text-primary transition-colors">SAMI<span
                            class="text-primary">.DEV</span></span>
                </div>
                <div class="hidden md:flex space-x-8 items-center">
                    <a href="#home"
                        class="text-sm font-semibold tracking-wide hover:text-primary transition-colors relative group">Home
                        <span
                            class="absolute -bottom-1 left-12 w-0 h-0.5 bg-primary transition-all group-hover:w-full group-hover:left-0"></span></a>
                    <a href="#about"
                        class="text-sm font-semibold tracking-wide hover:text-primary transition-colors relative group">About
                        <span
                            class="absolute -bottom-1 left-12 w-0 h-0.5 bg-primary transition-all group-hover:w-full group-hover:left-0"></span></a>
                    <a href="#works"
                        class="text-sm font-semibold tracking-wide hover:text-primary transition-colors relative group">Works
                        <span
                            class="absolute -bottom-1 left-12 w-0 h-0.5 bg-primary transition-all group-hover:w-full group-hover:left-0"></span></a>
                    <div class="h-6 w-1px bg-gray-300 dark:bg-gray-700 mx-4"></div>
                    <button id="theme-toggle"
                        class="relative w-12 h-6 rounded-full bg-gray-200 dark:bg-gray-700 transition-colors focus:outline-none">
                        <div
                            class="absolute left-1 top-1 w-4 h-4 rounded-full bg-white shadow-sm transform transition-transform duration-300 dark:translate-x-6 flex items-center justify-center text-10px">
                            <i class="fas fa-sun text-yellow-500 dark:hidden"></i>
                            <i class="fas fa-moon text-primary hidden dark:block"></i>
                        </div>
                    </button>
                    <a href="#contact"
                        class="px-5 py-2.5 rounded-lg bg-white dark:bg-white/5 border border-gray-200 dark:border-white/10 hover:border-primary/50 text-sm font-bold hover:shadow-[0_0_20px_rgba(139,92,246,0.3)] transition-all">Let's
                        Talk</a>
                </div>
                <button id="mobile-menu-btn" class="md:hidden text-2xl dark:text-white">
                    <i class="fas fa-bars"></i>
                </button>
            </div>
        </div>
        <div id="mobile-menu"
            class="hidden md:hidden glass border-t border-gray-100 dark:border-gray-800 absolute w-full transition-all">
            <div class="px-4 pt-2 pb-6 space-y-2 text-center">
                <a href="#home"
                    class="block py-3 text-base font-medium border-b border-gray-100 dark:border-gray-800 hover:text-primary">Home</a>
                <a href="#about"
                    class="block py-3 text-base font-medium border-b border-gray-100 dark:border-gray-800 hover:text-primary">About</a>
                <a href="#works"
                    class="block py-3 text-base font-medium border-b border-gray-100 dark:border-gray-800 hover:text-primary">Works</a>
                <a href="#contact" class="block py-3 text-base font-bold text-primary">Contact Me</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="min-h-screen flex items-center justify-center pt-20 relative overflow-hidden">
        <div class="absolute inset-0 z-0">
            <canvas id="hero-canvas"></canvas>
        </div>
        <div
            class="absolute top-20 right-0 w-500px h-500px bg-primary/20 rounded-full mix-blend-screen filter blur-100px animate-blob">
        </div>
        <div
            class="absolute bottom-0 left-0 w-500px h-500px bg-secondary/20 rounded-full mix-blend-screen filter blur-100px animate-blob animation-delay-2000">
        </div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 w-full relative z-10">
            <div class="flex flex-col lg:flex-row items-center justify-between gap-12">
                <div class="flex-1 text-center lg:text-left" data-aos="fade-right">
                    <div
                        class="inline-flex items-center gap-2 px-4 py-2 mb-6 rounded-full glass border border-primary/30 text-xs font-bold tracking-widest uppercase text-primary">
                        <span class="relative flex h-2 w-2">
                            <span
                                class="animate-ping absolute inline-flex h-full w-full rounded-full bg-primary opacity-75"></span>
                            <span class="relative inline-flex rounded-full h-2 w-2 bg-primary"></span>
                        </span>
                        System Online
                    </div>
                    <h1
                        class="text-6xl sm:text-7xl lg:text-8xl font-heading font-bold text-dark dark:text-white leading-[0.9] mb-6 tracking-tight">
                        Shahriar<br>
                        <span
                            class="text-transparent bg-clip-text bg-gradient-to-r from-primary via-secondary to-accent">Sami</span>
                    </h1>
                    <div class="h-12 mb-6 flex items-center justify-center lg:justify-start">
                        <span class="text-xl sm:text-2xl font-mono text-gray-500 dark:text-gray-400"></span>
                        <span id="typewriter"
                            class="text-xl sm:text-2xl font-mono text-gray-600 dark:text-gray-300 ml-2"></span>
                        <span class="animate-pulse text-primary text-2xl">|</span>
                    </div>
                    <p
                        class="text-base sm:text-lg text-gray-500 dark:text-gray-400 mb-8 max-w-lg mx-auto lg:mx-0 leading-relaxed">
                        CSE Student @ AIUB. Architecting efficient software solutions with a focus on clean code and
                        scalable design.</p>
                    <div class="flex flex-col sm:flex-row justify-center lg:justify-start gap-4">
                        <a href="#works"
                            class="px-8 py-4 rounded-xl bg-gradient-to-r from-primary to-secondary text-white font-bold hover:shadow-[0_0_30px_rgba(236,72,153,0.5)] transition-all flex items-center justify-center gap-2 group">
                            Explore Works
                            <i class="fas fa-arrow-right group-hover:translate-x-1 transition-transform"></i>
                        </a>
                    </div>
                    <div class="flex gap-4 items-center px-6 mt-8">
                        <a href="https://github.com/THE-S-SAMI1317" target="_blank"
                            class="text-gray-400 hover:text-white hover:scale-125 transition-all duration-300"><i
                                class="fab fa-github text-2xl"></i></a>
                        <a href="" target="_blank"
                            class="text-gray-400 hover:text-[#0A66C2] hover:scale-125 transition-all duration-300"><i
                                class="fab fa-linkedin text-2xl"></i></a>
                        <a href="" target="_blank"
                            class="text-gray-400 hover:text-[#1877F2] hover:scale-125 transition-all duration-300"><i
                                class="fab fa-facebook text-2xl"></i></a>
                    </div>
                </div>

                <!-- Hero Image -->
                <div class="flex-1 relative perspective-1000" data-aos="fade-left">
                    <div class="relative w-80 h-96 sm:w-96 sm:h-500px mx-auto animate-float tilt-card group">
                        <div
                            class="absolute -inset-4 bg-gradient-to-r from-primary via-secondary to-accent rounded-3xl blur-2xl opacity-50 group-hover:opacity-100 transition duration-500">
                        </div>
                        <div
                            class="relative w-full h-full glass rounded-3xl border border-white/10 p-8 flex flex-col items-center justify-center overflow-hidden bg-gradient-to-br from-white/5 to-transparent">
                            <!-- Dashed Circle Background -->
                            <div class="absolute inset-0 rounded-3xl border-2 border-dashed border-primary/30 m-8">
                            </div>

                            <!-- Initials Circle -->
                            <div
                                class="relative w-40 h-40 sm:w-48 sm:h-48 rounded-full flex items-center justify-center mb-8 z-10">
                                <div
                                    class="absolute inset-0 rounded-full bg-gradient-to-br from-primary/20 via-secondary/20 to-accent/20 blur-xl">
                                </div>
                                <div
                                    class="relative rounded-full border-2 border-primary/40 w-full h-full overflow-hidden">
                                    <img src="https://avatars.githubusercontent.com/u/153972636?s=400&u=f3213e855e19a82ac8cd4d1310d4123f21382879&v=4"
                                        alt="Profile photo" class="w-full h-full object-cover">
                                </div>
                            </div>


                            <!-- Online Badge -->
                            <div
                                class="absolute top-24 right-4 bg-gradient-to-r from-green-400 to-emerald-500 text-black text-xs font-bold px-4 py-2 rounded-full border-2 border-green-300 shadow-lg shadow-green-500/50 animate-pulse">
                                ONLINE
                            </div>

                            <!-- Name and Role -->
                            <h3
                                class="text-3xl sm:text-4xl font-heading font-bold text-white mb-2 text-center relative z-10">
                                Shahriar Sami</h3>
                            <p class="text-base sm:text-lg text-primary font-mono mb-8 relative z-10">&lt;Developer
                                /&gt;</p>

                            <!-- Divider -->
                            <div
                                class="w-full h-px bg-gradient-to-r from-transparent via-white/20 to-transparent mb-6 relative z-10">
                            </div>

                            <!-- Info Grid -->
                            <div class="font-mono text-xs text-gray-300 w-full px-4 relative z-10">
                                <div class="grid grid-cols-3 gap-4 text-center">
                                    <div>
                                        <p class="text-gray-500 mb-1">ID:</p>
                                        <p class="text-white font-semibold">25-63748-3</p>
                                    </div>
                                    <div>
                                        <p class="text-gray-500 mb-1">LOC:</p>
                                        <p class="text-white font-semibold">Dhaka, BD</p>
                                    </div>
                                    <div>
                                        <p class="text-gray-500 mb-1">EXP:</p>
                                        <p class="text-white font-semibold">Level 1</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="absolute bottom-10 left-12 transform -translate-x-12 flex flex-col items-center gap-2">
                <div class="w-1px h-16 bg-gradient-to-b from-transparent via-primary to-transparent"></div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-24 relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <h2 class="text-4xl md:text-5xl font-heading font-bold text-center mb-16 dark:text-white"
                data-aos="fade-up">
                Decoding <span class="text-primary">The Dev</span>
            </h2>
            <div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4 gap-6 auto-rows-minmax-180px-auto">
                <div class="md:col-span-2 lg:col-span-2 glass rounded-3xl p-8 spotlight-card" data-aos="fade-up">
                    <div class="h-full flex flex-col justify-center">
                        <span class="text-accent font-mono text-sm mb-2">1. INTRODUCTION</span>
                        <h3 class="text-2xl font-bold dark:text-white mb-4">Driven by Innovation, Powered by Code.</h3>
                        <p class="text-gray-500 dark:text-gray-400 leading-relaxed mb-6">I am a first-year Computer
                            Science Engineering student at AIUB. My journey is defined by a
                            relentless curiosity for how things work under the hood. From low-level Java logic to
                            high-level web architecture, I aim to build systems that matter.</p>
                        <div class="flex gap-3 flex-wrap">
                            <span
                                class="px-3 py-1 bg-primary/10 text-primary rounded-full text-xs font-bold border border-primary/20">Java
                                Specialist</span>
                            <span
                                class="px-3 py-1 bg-secondary/10 text-secondary rounded-full text-xs font-bold border border-secondary/20">Problem
                                Solver</span>
                            <span
                                class="px-3 py-1 bg-accent/10 text-accent rounded-full text-xs font-bold border border-accent/20">Gamer</span>
                        </div>
                    </div>
                </div>

                

                <div class="glass rounded-3xl p-6 relative overflow-hidden spotlight-card" data-aos="fade-up"
                    data-aos-delay="200">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRVvqzn5ASPrIyuxcGJYva-IhP1EHrsas_5Yx6ZecgwpMrsHBth1mjopFiZn4vvFmt407m-&s"
                        alt="Dhaka" class="absolute inset-0 w-full h-full object-cover opacity-20 dark:opacity-30">
                    <div class="relative z-10 h-full flex flex-col justify-end">
                        <i class="fas fa-map-marker-alt text-red-500 text-3xl mb-2"></i>
                        <h4 class="text-xl font-bold dark:text-white">Dhaka, BD</h4>
                        <p class="text-xs text-gray-400">Base of Operations</p>
                    </div>
                </div>

                <div class="md:col-span-2 row-span-2 glass rounded-3xl p-8 spotlight-card" data-aos="fade-up"
                    data-aos-delay="300">
                    <span class="text-secondary font-mono text-sm mb-6 block">2. ACADEMIC DATABASE</span>
                    <div class="relative border-l-2 border-gray-700 ml-3 space-y-10">
                        <div class="relative pl-8 group">
                            <div
                                class="absolute -left-[9px] top-0 w-4 h-4 rounded-full bg-primary border-4 border-darker group-hover:scale-125 transition-transform">
                            </div>
                            <span
                                class="inline-block px-2 py-1 bg-primary/10 text-primary text-xs font-bold rounded mb-1">2024
                                - Present</span>
                            <h4 class="text-xl font-bold dark:text-white">B.Sc. in Computer Science Engineering</h4>
                            <p class="text-sm text-gray-400 mt-1">American International University - Bangladesh (AIUB)
                            <a href="https://www.aiub.edu/" target="_blank" class="text-sm text-gray-500 hover:text-primary transition-colors block">AIUB</a>
                            <img src="https://drive.google.com/thumbnail?id=13pGUL9xn3CG-Bi-xY06GB8cE4BLcdnpo&sz=w1000" class="w-full h-full object-cover">
                            <a href="https://www.youtube.com/watch?v=utfwfN7c9IY" target="_blank" class="w-8 h-8 rounded-full bg-red-100 text-red-600 flex items-center justify-center hover:bg-red-600 hover:text-white transition-all"><i class="fas fa-play text-xs"></i></a>    
                            </p>
                            
                        </div>
                        <div class="relative pl-8 group">
                            <div
                                class="absolute -left-[9px] top-0 w-4 h-4 rounded-full bg-secondary border-4 border-darker group-hover:scale-125 transition-transform">
                            </div>
                            <span
                                class="inline-block px-2 py-1 bg-secondary/10 text-secondary text-xs font-bold rounded mb-1">2022
                                - 2024</span>
                            <h4 class="text-xl font-bold dark:text-white">Higher Secondary Certificate (Science)</h4>
                            <p class="text-sm text-gray-400 mt-1">Jhenaidah KC College</p>
                            <div class="mt-2 text-sm font-bold text-green-400 flex items-center gap-2">
                                <i class="fas fa-star"></i>GPA 5.00 / 5.00
                            </div>
                        </div>
                        <div class="relative pl-8 group">
                            <div
                                class="absolute -left-[9px] top-0 w-4 h-4 rounded-full bg-accent border-4 border-darker group-hover:scale-125 transition-transform">
                            </div>
                            <span
                                class="inline-block px-2 py-1 bg-accent/10 text-accent text-xs font-bold rounded mb-1">2021
                                - 2022</span>
                            <h4 class="text-xl font-bold dark:text-white">Secondary School Certificate (Science)</h4>
                            <img src="data:image/jpeg;base64,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" class="w-full h-full object-cover">
                            <p class="text-sm text-gray-400 mt-1">Jhenaidha Govt. High School</p>
                            <a href="http://www.jhenidahghs.edu.bd/" target="_blank" class="text-sm text-gray-500 hover:text-primary transition-colors block">JGHS</a>
                            <div class="mt-2 text-sm font-bold text-green-400 flex items-center gap-2">
                                <i class="fas fa-medal"></i>GPA 5.00 / 5.00 (Golden)
                            </div>
                        </div>
                    </div>
                </div>

                <div class="md:col-span-2 lg:col-span-2 glass rounded-3xl p-8 spotlight-card" data-aos="fade-up"
                    data-aos-delay="400">
                    <span class="text-accent font-mono text-sm mb-6 block">3. TECH ARSENAL</span>
                    <div class="grid grid-cols-3 sm:grid-cols-4 gap-4">
                        <div class="flex flex-col items-center gap-2 group">
                            <i
                                class="fab fa-java text-4xl text-gray-400 group-hover:text-red-500 transition-colors"></i>
                            <span class="text-10px uppercase font-bold text-gray-500">Java</span>
                        </div>
                        <div class="flex flex-col items-center gap-2 group">
                            <i
                                class="fab fa-python text-4xl text-gray-400 group-hover:text-yellow-400 transition-colors"></i>
                            <span class="text-10px uppercase font-bold text-gray-500">Python</span>
                        </div>
                        <div class="flex flex-col items-center gap-2 group">
                            <i
                                class="fab fa-js text-4xl text-gray-400 group-hover:text-yellow-300 transition-colors"></i>
                            <span class="text-10px uppercase font-bold text-gray-500">JS</span>
                        </div>
                        <div class="flex flex-col items-center gap-2 group">
                            <i
                                class="fab fa-html5 text-4xl text-gray-400 group-hover:text-orange-500 transition-colors"></i>
                            <span class="text-10px uppercase font-bold text-gray-500">HTML</span>
                        </div>
                        <div class="flex flex-col items-center gap-2 group">
                            <i
                                class="fab fa-css3-alt text-4xl text-gray-400 group-hover:text-blue-500 transition-colors"></i>
                            <span class="text-10px uppercase font-bold text-gray-500">CSS</span>
                        </div>
                        <div class="flex flex-col items-center gap-2 group">
                            <i
                                class="fas fa-code text-4xl text-gray-400 group-hover:text-blue-400 transition-colors"></i>
                            <span class="text-10px uppercase font-bold text-gray-500">C</span>
                        </div>
                        <div class="flex flex-col items-center gap-2 group">
                            <i
                                class="fas fa-database text-4xl text-gray-400 group-hover:text-green-500 transition-colors"></i>
                            <span class="text-10px uppercase font-bold text-gray-500">SQL</span>
                        </div>
                        <div class="flex flex-col items-center gap-2 group">
                            <i
                                class="fab fa-git-alt text-4xl text-gray-400 group-hover:text-red-600 transition-colors"></i>
                            <span class="text-10px uppercase font-bold text-gray-500">Git</span>
                        </div>
                    </div>
                </div>

                <!-- Hobbies Section -->
                <div class="lg:col-span-2 glass rounded-3xl p-8 spotlight-card" data-aos="fade-up" data-aos-delay="500">
                    <span class="text-secondary font-mono text-sm mb-6 block">4. HOBBIES & INTERESTS</span>
                    <div class="flex flex-wrap gap-4 items-center justify-start">
                        <div class="group flex flex-col items-center gap-2">
                            <div
                                class="w-14 h-14 rounded-lg bg-primary/20 flex items-center justify-center group-hover:bg-primary/40 transition-colors">
                                <i class="fas fa-map-location-dot text-primary text-2xl"></i>
                            </div>
                            <span class="text-xs font-semibold text-gray-600 dark:text-gray-400">Travelling</span>
                        </div>
                        <div class="group flex flex-col items-center gap-2">
                            <div
                                class="w-14 h-14 rounded-lg bg-secondary/20 flex items-center justify-center group-hover:bg-secondary/40 transition-colors">
                                <i class="fas fa-gamepad text-secondary text-2xl"></i>
                            </div>
                            <span class="text-xs font-semibold text-gray-600 dark:text-gray-400">Gaming</span>
                        </div>
                        <div class="group flex flex-col items-center gap-2">
                            <div
                                class="w-14 h-14 rounded-lg bg-accent/20 flex items-center justify-center group-hover:bg-accent/40 transition-colors">
                                <i class="fas fa-palette text-accent text-2xl"></i>
                            </div>
                            <span class="text-xs font-semibold text-gray-600 dark:text-gray-400">Drawing</span>
                        </div>
                        <div class="group flex flex-col items-center gap-2">
                            <div
                                class="w-14 h-14 rounded-lg bg-primary/20 flex items-center justify-center group-hover:bg-primary/40 transition-colors">
                                <i class="fas fa-camera text-primary text-2xl"></i>
                            </div>
                            <span class="text-xs font-semibold text-gray-600 dark:text-gray-400">Photography</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Works Section -->
    <section id="works" class="py-24 bg-light/50 dark:bg-dark/50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-end mb-16">
                <div data-aos="fade-right">
                    <span class="text-primary font-mono text-sm tracking-wider">PROJECTS</span>
                    <h2 class="text-4xl md:text-5xl font-heading font-bold dark:text-white mt-2">Selected Works</h2>
                </div>
                <a href="https://github.com/THE-S-SAMI1317" target="_blank"
                    class="hidden md:flex items-center gap-2 text-sm font-bold border-b border-primary pb-1 hover:text-primary transition-colors">
                    View GitHub
                    <i class="fas fa-external-link-alt text-xs"></i>
                </a>
            </div>

            <div class="grid grid-cols-1 gap-8">
                

                <div class="group relative bg-light dark:bg-white/5 border-2 border-dashed border-gray-300 dark:border-gray-700 rounded-2xl flex flex-col items-center justify-center p-8 text-center min-h-[400px]"
                    data-aos="fade-up" data-aos-delay="100">
                    <div
                        class="w-20 h-20 bg-gradient-to-br from-gray-200 to-gray-300 dark:from-gray-800 dark:to-gray-700 rounded-full flex items-center justify-center mb-6 animate-pulse-glow">
                        <i class="fas fa-code-branch text-3xl text-gray-500 dark:text-gray-400"></i>
                    </div>
                    <h3 class="text-2xl font-bold dark:text-white mb-2 group-hover:text-primary transition-colors">Work
                        in Progress</h3>
                    <p class="text-gray-500 text-sm max-w-xs mx-auto">Something exciting is brewing in the lab. Check
                        back soon for new deployments.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section - From Shahriar-Sami-Portfolio.html -->
    <section id="contact" class="py-24 bg-darker text-white relative overflow-hidden cyber-grid">
        <div
            class="absolute inset-0 bg-gradient-to-b from-transparent via-primary/5 to-transparent h-full w-full pointer-events-none animate-scan">
        </div>

        <div class="max-w-7xl mx-auto px-4 relative z-10">
            <div class="text-center mb-16" data-aos="fade-up">
                <div
                    class="inline-flex items-center gap-2 px-4 py-1 rounded-full bg-primary/10 border border-primary/30 text-primary text-xs font-mono mb-4">
                    <span class="w-2 h-2 rounded-full bg-primary animate-pulse"></span>
                    SYSTEM ONLINE
                </div>
                <h2 class="text-5xl font-heading font-bold mb-4">Initiate <span class="text-gradient">Connection</span>
                </h2>
                <p class="text-gray-400 font-mono">Ready to start a new project? Send a transmission below.</p>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
                <!-- Contact Info -->
                <div class="lg:col-span-4 space-y-6" data-aos="fade-right">
                    <div class="glass p-6 rounded-2xl border border-white/10 relative overflow-hidden group">
                        <div class="flex justify-between items-center mb-6">
                            <span class="font-mono text-xs text-secondary">SIGNAL STRENGTH</span>
                            <div class="flex gap-1">
                                <div class="w-1 h-3 bg-secondary rounded-full"></div>
                                <div class="w-1 h-4 bg-secondary rounded-full"></div>
                                <div class="w-1 h-5 bg-secondary rounded-full"></div>
                                <div class="w-1 h-6 bg-secondary rounded-full"></div>
                            </div>
                        </div>
                        <h4 class="text-xl font-bold mb-1">Direct Neural Link</h4>
                        <p class="text-sm text-gray-400 mb-6">Fastest response within 2 hours.</p>
                        <div class="space-y-4">
                            <div class="flex items-center gap-4 group-hover:translate-x-2 transition-transform">
                                <div
                                    class="w-10 h-10 rounded-lg bg-white/5 flex items-center justify-center text-primary border border-white/10">
                                    <i class="fas fa-envelope"></i>
                                </div>
                                <div>
                                    <p class="text-10px text-gray-500 font-bold uppercase">Primary Mail</p>
                                    <p class="text-sm font-mono">shahriar.sami@mail.com</p>
                                </div>
                            </div>
                            <div class="flex items-center gap-4 group-hover:translate-x-2 transition-transform">
                                <div
                                    class="w-10 h-10 rounded-lg bg-white/5 flex items-center justify-center text-secondary border border-white/10">
                                    <i class="fas fa-location-dot"></i>
                                </div>
                                <div>
                                    <p class="text-10px text-gray-500 font-bold uppercase">Base Location</p>
                                    <p class="text-sm font-mono">Dhaka, Bangladesh</p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="glass p-6 rounded-2xl border border-white/10">
                        <p class="font-mono text-10px text-gray-500 mb-4 tracking-widest uppercase">Global Nodes</p>
                        <div class="grid grid-cols-4 gap-3">
                            <a href=""
                                class="h-12 rounded-xl bg-white/5 border border-white/10 flex items-center justify-center hover:bg-primary/20 hover:border-primary transition-all">
                                <i class="fab fa-github"></i>
                            </a>
                            <a href=""
                                class="h-12 rounded-xl bg-white/5 border border-white/10 flex items-center justify-center hover:bg-blue-500/20 hover:border-blue-500 transition-all">
                                <i class="fab fa-linkedin-in"></i>
                            </a>
                            <a href=""
                                class="h-12 rounded-xl bg-white/5 border border-white/10 flex items-center justify-center hover:bg-pink-500/20 hover:border-pink-500 transition-all">
                                <i class="fab fa-instagram"></i>
                            </a>
                            <a href=""
                                class="h-12 rounded-xl bg-white/5 border border-white/10 flex items-center justify-center hover:bg-blue-400/20 hover:border-blue-400 transition-all">
                                <i class="fab fa-facebook"></i>
                            </a>
                        </div>
                    </div>

                    <div class="glass p-4 rounded-2xl border border-white/10 text-center font-mono text-xs">
                        <p class="text-gray-500">SERVER TIME (DHAKA)</p>
                        <p id="dhaka-time" class="text-secondary font-bold text-lg mt-1">00:00:00</p>
                    </div>
                </div>

                <!-- Contact Form -->
                <div class="lg:col-span-8" data-aos="fade-left">
                    <div class="bg-slate-900/50 rounded-3xl p-8 border border-white/5 backdrop-blur-xl relative">
                        <div
                            class="absolute top-0 right-0 w-16 h-16 border-t-2 border-r-2 border-primary/30 rounded-tr-3xl">
                        </div>
                        <div
                            class="absolute bottom-0 left-0 w-16 h-16 border-b-2 border-l-2 border-secondary/30 rounded-bl-3xl">
                        </div>

                        <form class="space-y-6">
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                                <div class="space-y-2">
                                    <label class="text-xs font-mono text-gray-400 ml-1">USER IDENTIFICATION</label>
                                    <input type="text" placeholder="Full Name"
                                        class="contact-input w-full p-4 rounded-xl text-sm" required>
                                </div>
                                <div class="space-y-2">
                                    <label class="text-xs font-mono text-gray-400 ml-1">COMM CHANNEL</label>
                                    <input type="email" placeholder="Email Address"
                                        class="contact-input w-full p-4 rounded-xl text-sm" required>
                                </div>
                            </div>

                            <div class="space-y-2">
                                <label class="text-xs font-mono text-gray-400 ml-1">SUBJECT PARAMETER</label>
                                <select class="contact-input w-full p-4 rounded-xl text-sm appearance-none">
                                    <option>New Project Proposal</option>
                                    <option>Hiring Collaboration</option>
                                    <option>Technical Consultation</option>
                                    <option>Just Saying Hi</option>
                                </select>
                            </div>

                            <div class="space-y-2">
                                <label class="text-xs font-mono text-gray-400 ml-1">DATA STREAM</label>
                                <textarea rows="5" placeholder="Describe your vision..."
                                    class="contact-input w-full p-4 rounded-xl text-sm"></textarea>
                            </div>

                            <button type="submit"
                                class="w-full py-4 rounded-xl bg-gradient-to-r from-primary to-secondary text-white font-bold tracking-widest shadow-xl shadow-primary/20 hover:scale-1.02 active:scale-95 transition-all flex items-center justify-center gap-3 group">
                                <span class="group-hover:translate-x-2 transition-transform">TRANSMIT MESSAGE</span>
                                <i class="fas fa-paper-plane text-xs animate-bounce"></i>
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-10 bg-darker border-t border-white/5 text-center">
        <p class="text-gray-600 text-sm font-mono">copy 2025 SHAHRIAR SAMI. ALL RIGHTS RESERVED</p>
    </footer>

    <!-- Back to Top Button -->
    <button id="backToTop"
        class="fixed bottom-8 right-8 bg-white/10 backdrop-blur-md border border-white/20 text-white p-3 rounded-xl shadow-lg translate-y-20 opacity-0 transition-all duration-300 hover:bg-primary hover:border-primary z-40">
        <i class="fas fa-arrow-up"></i>
    </button>

    

    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        // Initialize AOS
        AOS.init({ duration: 800, once: true, offset: 50, easing: 'ease-out-cubic' });

        // Preloader Logic
        window.addEventListener('load', () => {
            const preloader = document.getElementById('preloader');
            preloader.style.opacity = '0';
            setTimeout(() => { preloader.style.visibility = 'hidden'; }, 600);
        });

        // Mouse Spotlight Effect
        const glowCircle = document.getElementById('glow-circle');
        document.addEventListener('mousemove', e => {
            const x = e.clientX;
            const y = e.clientY;
            glowCircle.style.transform = `translate(${x}px, ${y}px) translate(-50%, -50%)`;
            document.querySelectorAll('.spotlight-card').forEach(card => {
                const rect = card.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                card.style.setProperty('--mouse-x', `${x}px`);
                card.style.setProperty('--mouse-y', `${y}px`);
            });
        });

        // Tilt Effect for Cards
        document.querySelectorAll('.tilt-card').forEach(card => {
            card.addEventListener('mousemove', e => {
                const rect = card.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                const centerX = rect.width / 2;
                const centerY = rect.height / 2;
                const rotateX = ((y - centerY) / centerY) * -5;
                const rotateY = ((x - centerX) / centerX) * 5;
                card.style.transform = `perspective(1000px) rotateX(${rotateX}deg) rotateY(${rotateY}deg) scale(1.02)`;
            });
            card.addEventListener('mouseleave', () => {
                card.style.transform = 'perspective(1000px) rotateX(0) rotateY(0) scale(1)';
            });
        });

        // Theme Toggle
        const toggleBtn = document.getElementById('theme-toggle');
        const html = document.documentElement;
        if (!('theme' in localStorage)) localStorage.theme = 'dark';
        if (localStorage.theme === 'dark' || (!('theme' in localStorage) && window.matchMedia('prefers-color-scheme: dark').matches)) {
            html.classList.add('dark');
        } else {
            html.classList.remove('dark');
        }
        toggleBtn.addEventListener('click', () => {
            html.classList.toggle('dark');
            localStorage.theme = html.classList.contains('dark') ? 'dark' : 'light';
        });

        // Scroll Logic
        window.addEventListener('scroll', () => {
            let winScroll = document.body.scrollTop || document.documentElement.scrollTop;
            let height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            let scrolled = (winScroll / height) * 100;
            document.getElementById('scroll-progress').style.width = scrolled + '%';

            const backToTop = document.getElementById('backToTop');
            const nav = document.getElementById('navbar');
            if (winScroll > 50) {
                nav.classList.add('shadow-lg', 'bg-opacity-90');
            } else {
                nav.classList.remove('shadow-lg', 'bg-opacity-90');
            }
            if (winScroll > 300) {
                backToTop.classList.remove('translate-y-20', 'opacity-0');
            } else {
                backToTop.classList.add('translate-y-20', 'opacity-0');
            }
        });

        document.getElementById('backToTop').addEventListener('click', () => {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });

        // Mobile Menu
        const menuBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        menuBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Typewriter Effect
        const typewriter = document.getElementById('typewriter');
        const phrases = ['Building Systems.', 'Solving Problems.', 'Designing Future.', 'Learning Everyday.'];
        let phraseIndex = 0, charIndex = 0, isDeleting = false;

        function type() {
            const currentPhrase = phrases[phraseIndex];
            if (isDeleting) {
                typewriter.textContent = currentPhrase.substring(0, charIndex-- - 1);
            } else {
                typewriter.textContent = currentPhrase.substring(0, charIndex++ + 1);
            }
            if (!isDeleting && charIndex === currentPhrase.length) {
                isDeleting = true;
                setTimeout(type, 2000);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                phraseIndex = (phraseIndex + 1) % phrases.length;
                setTimeout(type, 500);
            } else {
                setTimeout(type, isDeleting ? 50 : 100);
            }
        }
        type();

        // Particles
        const canvas = document.getElementById('hero-canvas');
        const ctx = canvas.getContext('2d');
        let particles = [];

        function resizeCanvas() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        }
        window.addEventListener('resize', resizeCanvas);
        resizeCanvas();

        class Particle {
            constructor() {
                this.x = Math.random() * canvas.width;
                this.y = Math.random() * canvas.height;
                this.size = Math.random() * 2 + 0.5;
                this.speedX = Math.random() * 1 - 0.5;
                this.speedY = Math.random() * 1 - 0.5;
            }
            update() {
                this.x += this.speedX;
                this.y += this.speedY;
                if (this.x > canvas.width) this.x = 0;
                if (this.x < 0) this.x = canvas.width;
                if (this.y > canvas.height) this.y = 0;
                if (this.y < 0) this.y = canvas.height;
            }
            draw() {
                ctx.fillStyle = html.classList.contains('dark') ? 'rgba(139, 92, 246, 0.5)' : 'rgba(139, 92, 246, 0.3)';
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fill();
            }
        }

        function initParticles() {
            particles = [];
            for (let i = 0; i < 60; i++) {
                particles.push(new Particle());
            }
        }
        initParticles();

        function animateParticles() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            for (let i = 0; i < particles.length; i++) {
                particles[i].update();
                particles[i].draw();
                for (let j = i; j < particles.length; j++) {
                    const dx = particles[i].x - particles[j].x;
                    const dy = particles[i].y - particles[j].y;
                    const distance = Math.sqrt(dx * dx + dy * dy);
                    if (distance < 120) {
                        ctx.strokeStyle = html.classList.contains('dark') ? `rgba(139, 92, 246, ${0.1 - distance / 1200})` : `rgba(139, 92, 246, ${0.1 - distance / 1200})`;
                        ctx.lineWidth = 0.5;
                        ctx.beginPath();
                        ctx.moveTo(particles[i].x, particles[i].y);
                        ctx.lineTo(particles[j].x, particles[j].y);
                        ctx.stroke();
                    }
                }
            }
            requestAnimationFrame(animateParticles);
        }
        animateParticles();

        

        // Live Dhaka Time
        function updateTime() {
            const options = { timeZone: 'Asia/Dhaka', hour: '2-digit', minute: '2-digit', second: '2-digit', hour12: false };
            const timeString = new Intl.DateTimeFormat('en-US', options).format(new Date());
            document.getElementById('dhaka-time').innerText = timeString;
        }
        setInterval(updateTime, 1000);
        updateTime();

        // CSS Variables for Contact Styles
        const style = document.createElement('style');
        style.innerHTML = `
            .cyber-grid {
                background-image: radial-gradient(rgba(255, 107, 107, 0.1) 1px, transparent 1px);
                background-size: 30px 30px;
            }
            .contact-input {
                background: rgba(15, 23, 42, 0.4);
                border: 1px solid rgba(255, 255, 255, 0.1);
                transition: all 0.3s;
                color: white;
            }
            .contact-input:focus {
                border-color: #FF6B6B;
                box-shadow: 0 0 15px rgba(255, 107, 107, 0.2);
                outline: none;
            }
            @keyframes scan {
                0% { top: 0; }
                100% { top: 100%; }
            }
            .animate-scan {
                animation: scan 3s linear infinite;
            }
        `;
        document.head.appendChild(style);
    </script>
</body>

</html>
