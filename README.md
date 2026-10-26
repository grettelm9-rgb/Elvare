# Elvare

<html lang="es" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ÉLVARÉ Perfumería | Encuentra tu Aroma Ideal</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts: Playfair Display, Cormorant Garamond & Plus Jakarta Sans -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,600;0,700;1,400&family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        obsidian: '#0b0b0e',
                        charcoal: '#141419',
                        gold: {
                            light: '#f3e5ab',
                            DEFAULT: '#d4af37',
                            dark: '#aa820a'
                        }
                    },
                    fontFamily: {
                        serif: ['"Playfair Display"', 'serif'],
                        garamond: ['"Cormorant Garamond"', 'serif'],
                        sans: ['"Plus Jakarta Sans"', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <style>
        /* Custom Glassmorphism & Gold Styling */
        .glass-card {
            background: rgba(20, 20, 25, 0.7);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(212, 175, 55, 0.15);
        }
        .glass-card-active {
            background: rgba(30, 30, 38, 0.85);
            border: 1px solid rgba(212, 175, 55, 0.5);
            box-shadow: 0 0 25px rgba(212, 175, 55, 0.15);
        }
        .gold-gradient-text {
            background: linear-gradient(135deg, #FFF6D6 0%, #D4AF37 50%, #AA820A 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .gold-border-glow {
            box-shadow: 0 0 15px rgba(212, 175, 55, 0.2);
        }
        .gold-btn {
            background: linear-gradient(135deg, #d4af37 0%, #aa820a 100%);
            transition: all 0.3s ease;
        }
        .gold-btn:hover {
            background: linear-gradient(135deg, #e5be48 0%, #c19614 100%);
            box-shadow: 0 0 20px rgba(212, 175, 55, 0.4);
        }
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0b0b0e;
        }
        ::-webkit-scrollbar-thumb {
            background: #2a2a35;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #d4af37;
        }
    </style>
</head>
<body class="bg-obsidian text-gray-200 font-sans antialiased selection:bg-gold selection:text-black min-h-screen flex flex-col justify-between">

    <!-- Header / Nav (Con nuevo Logo de ÉLVARÉ) -->
    <header class="fixed top-0 left-0 w-full z-50 bg-obsidian/90 backdrop-blur-md border-b border-gold/10">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-24 flex items-center justify-between">
            <!-- Brand Logo SVG Monogram ÉLVARÉ -->
            <a href="#inicio" onclick="showSection('inicio')" class="flex items-center gap-4 group py-2">
                <div class="flex flex-col items-center">
                    <!-- SVG Monogram É monogram -->
                    <svg class="w-10 h-10 text-gold group-hover:scale-105 transition-transform" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <!-- Upper Accent -->
                        <path d="M56 16 L68 8 L60 8 Z" fill="currentColor"/>
                        <!-- Main É Letter -->
                        <text x="50%" y="58%" text-anchor="middle" font-family="'Cormorant Garamond', 'Playfair Display', serif" font-size="52" font-weight="600" fill="currentColor" letter-spacing="0">É</text>
                        <!-- Intertwined C Loop -->
                        <path d="M 52 46 C 30 38, 25 65, 48 74 C 54 76, 60 72, 62 70" stroke="currentColor" stroke-width="2.5" fill="none" stroke-linecap="round"/>
                    </svg>
                    <div class="flex items-center gap-1.5 -mt-1">
                        <span class="font-garamond text-xl tracking-[0.25em] text-white font-semibold group-hover:text-gold transition-colors">ÉLVARÉ</span>
                    </div>
                    <span class="text-[8px] tracking-[0.3em] text-gold/80 uppercase font-light">PERFUMERÍA</span>
                </div>
            </a>

            <!-- Desktop Navigation -->
            <nav class="hidden md:flex items-center gap-8 text-xs uppercase tracking-widest text-gray-300 font-medium">
                <a href="#inicio" onclick="showSection('inicio')" class="hover:text-gold transition-colors py-1 relative group">
                    Inicio
                    <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-gold transition-all duration-300 group-hover:w-full"></span>
                </a>
                <a href="#familias" onclick="showSection('inicio', 'familias')" class="hover:text-gold transition-colors py-1 relative group">
                    Familias Olfativas
                    <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-gold transition-all duration-300 group-hover:w-full"></span>
                </a>
                <a href="#cuestionario" onclick="startQuiz()" class="hover:text-gold transition-colors py-1 relative group">
                    Descubrir mi Aroma
                    <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-gold transition-all duration-300 group-hover:w-full"></span>
                </a>
            </nav>

            <!-- CTA Button -->
            <div class="hidden md:block">
                <button onclick="startQuiz()" class="gold-btn text-black font-semibold text-xs uppercase tracking-widest px-5 py-2.5 rounded-full flex items-center gap-2 shadow-md">
                    <i class="fa-solid fa-sparkles"></i>
                    <span>Descubrir Mi Aroma</span>
                </button>
            </div>

            <!-- Mobile Hamburger Button -->
            <button id="mobile-menu-btn" onclick="toggleMobileMenu()" class="md:hidden text-gray-300 hover:text-gold text-2xl focus:outline-none">
                <i class="fa-solid fa-bars"></i>
            </button>
        </div>

        <!-- Mobile Navigation Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-charcoal border-b border-gold/20 px-6 py-6 flex flex-col gap-4 text-xs uppercase tracking-wider">
            <a href="#inicio" onclick="showSection('inicio'); toggleMobileMenu()" class="text-gray-200 hover:text-gold py-2 border-b border-gray-800">Inicio</a>
            <a href="#familias" onclick="showSection('inicio', 'familias'); toggleMobileMenu()" class="text-gray-200 hover:text-gold py-2 border-b border-gray-800">Familias Olfativas</a>
            <a href="#cuestionario" onclick="startQuiz(); toggleMobileMenu()" class="text-gold py-2 font-semibold flex items-center gap-2">
                <i class="fa-solid fa-sparkles"></i> Descubrir mi Aroma
            </a>
        </div>
    </header>

    <!-- Main Container -->
    <main class="flex-grow pt-24">

        <!-- SECTION 1: INICIO / HOME -->
        <section id="section-inicio" class="block transition-opacity duration-500">
            <!-- Hero Banner -->
            <div class="relative min-h-[85vh] flex items-center justify-center overflow-hidden py-20 px-4">
                <div class="absolute inset-0 bg-[radial-gradient(ellipse_at_center,_var(--tw-gradient-stops))] from-charcoal via-obsidian to-black -z-10"></div>
                <div class="absolute w-[500px] h-[500px] bg-gold/5 rounded-full blur-3xl -z-10 pointer-events-none"></div>

                <div class="max-w-4xl mx-auto text-center space-y-8">
                    <!-- Brand Monogram Header Large -->
                    <div class="flex flex-col items-center justify-center space-y-2">
                        <svg class="w-16 h-16 text-gold mb-1" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M56 16 L68 8 L60 8 Z" fill="currentColor"/>
                            <text x="50%" y="58%" text-anchor="middle" font-family="'Cormorant Garamond', 'Playfair Display', serif" font-size="52" font-weight="600" fill="currentColor">É</text>
                            <path d="M 52 46 C 30 38, 25 65, 48 74 C 54 76, 60 72, 62 70" stroke="currentColor" stroke-width="2.5" fill="none" stroke-linecap="round"/>
                        </svg>
                        <h2 class="font-garamond text-3xl tracking-[0.3em] text-white font-semibold uppercase">ÉLVARÉ</h2>
                        <div class="w-32 h-[1px] bg-gradient-to-r from-transparent via-gold to-transparent my-1"></div>
                        <p class="font-serif italic text-gold text-sm tracking-widest">"Tu esencia, tu presencia."</p>
                    </div>

                    <h1 class="font-serif text-3xl sm:text-5xl md:text-6xl text-white font-normal leading-tight pt-4">
                        Encuentra tu <span class="gold-gradient-text italic font-serif">Aroma Ideal</span>
                    </h1>

                    <p class="text-gray-400 text-sm sm:text-base max-w-2xl mx-auto font-light leading-relaxed">
                        Cada aroma transmite una sensación diferente. Descubre las colonias que mejor se adaptan a tus gustos, tu personalidad y tu estilo de vida. Responde unas preguntas y encuentra tu próxima fragancia favorita.
                    </p>

                    <div class="pt-4 flex flex-col sm:flex-row items-center justify-center gap-4">
                        <button onclick="startQuiz()" class="w-full sm:w-auto gold-btn text-black font-semibold text-xs uppercase tracking-widest px-8 py-4 rounded-full flex items-center justify-center gap-3 shadow-lg">
                            <i class="fa-solid fa-compass"></i>
                            <span>Descubrir mi aroma</span>
                        </button>
                        <a href="#familias" class="w-full sm:w-auto glass-card hover:border-gold/50 text-white font-medium text-xs uppercase tracking-widest px-8 py-4 rounded-full transition-colors flex items-center justify-center gap-2">
                            <span>Conocer Familias</span>
                            <i class="fa-solid fa-arrow-down text-xs text-gold"></i>
                        </a>
                    </div>
                </div>
            </div>

            <!-- SECTION: 8 FAMILIAS OLFATIVAS -->
            <div id="familias" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-20 border-t border-gold/10">
                <div class="text-center max-w-3xl mx-auto mb-16">
                    <span class="text-gold text-xs font-semibold uppercase tracking-[0.3em]">Asesoría de Fragancias</span>
                    <h2 class="font-serif text-3xl sm:text-4xl text-white mt-2 mb-4">Las 8 Familias Olfativas</h2>
                    <p class="text-gray-400 text-xs sm:text-sm">Explora las principales familias aromáticas y descubre cómo influyen en la elección de tu colonia ideal.</p>
                </div>

                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
                    <!-- 1. Cítricas -->
                    <div class="glass-card p-6 rounded-2xl border border-gold/10 hover:border-gold/40 transition-all duration-300 group">
                        <div class="w-12 h-12 rounded-xl bg-amber-500/10 border border-amber-500/20 flex items-center justify-center text-amber-400 mb-4 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-lemon text-xl"></i>
                        </div>
                        <h3 class="font-serif text-xl text-white mb-2">1. Cítricas</h3>
                        <p class="text-xs text-gray-400 leading-relaxed mb-3">Frescas, chispeantes y revitalizantes.</p>
                        <p class="text-[11px] text-gray-400 mb-4"><strong class="text-gold font-normal">Notas:</strong> limón, naranja, bergamota y mandarina.</p>
                    </div>

                    <!-- 2. Florales -->
                    <div class="glass-card p-6 rounded-2xl border border-gold/10 hover:border-gold/40 transition-all duration-300 group">
                        <div class="w-12 h-12 rounded-xl bg-pink-500/10 border border-pink-500/20 flex items-center justify-center text-pink-400 mb-4 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-fan text-xl"></i>
                        </div>
                        <h3 class="font-serif text-xl text-white mb-2">2. Florales</h3>
                        <p class="text-xs text-gray-400 leading-relaxed mb-3">Románticas, elegantes y luminosas.</p>
                        <p class="text-[11px] text-gray-400 mb-4"><strong class="text-gold font-normal">Notas:</strong> rosa, jazmín, lavanda y azahar.</p>
                    </div>

                    <!-- 3. Dulces o gourmand -->
                    <div class="glass-card p-6 rounded-2xl border border-gold/10 hover:border-gold/40 transition-all duration-300 group">
                        <div class="w-12 h-12 rounded-xl bg-yellow-600/10 border border-yellow-600/20 flex items-center justify-center text-yellow-500 mb-4 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-cookie-bite text-xl"></i>
                        </div>
                        <h3 class="font-serif text-xl text-white mb-2">3. Dulces / Gourmand</h3>
                        <p class="text-xs text-gray-400 leading-relaxed mb-3">Cálidas, apetitosas y reconfortantes.</p>
                        <p class="text-[11px] text-gray-400 mb-4"><strong class="text-gold font-normal">Notas:</strong> vainilla, caramelo, chocolate y praliné.</p>
                    </div>

                    <!-- 4. Amaderadas -->
                    <div class="glass-card p-6 rounded-2xl border border-gold/10 hover:border-gold/40 transition-all duration-300 group">
                        <div class="w-12 h-12 rounded-xl bg-amber-800/10 border border-amber-800/30 flex items-center justify-center text-amber-600 mb-4 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-tree text-xl"></i>
                        </div>
                        <h3 class="font-serif text-xl text-white mb-2">4. Amaderadas</h3>
                        <p class="text-xs text-gray-400 leading-relaxed mb-3">Sobrias, profundas y sofisticadas.</p>
                        <p class="text-[11px] text-gray-400 mb-4"><strong class="text-gold font-normal">Notas:</strong> cedro, sándalo, vetiver y pachulí.</p>
                    </div>

                    <!-- 5. Acuáticas o marinas -->
                    <div class="glass-card p-6 rounded-2xl border border-gold/10 hover:border-gold/40 transition-all duration-300 group">
                        <div class="w-12 h-12 rounded-xl bg-cyan-500/10 border border-cyan-500/20 flex items-center justify-center text-cyan-400 mb-4 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-water text-xl"></i>
                        </div>
                        <h3 class="font-serif text-xl text-white mb-2">5. Acuáticas / Marinas</h3>
                        <p class="text-xs text-gray-400 leading-relaxed mb-3">Puras, limpias y refrescantes.</p>
                        <p class="text-[11px] text-gray-400 mb-4"><strong class="text-gold font-normal">Notas:</strong> brisa marina, notas de agua y acordes frescos.</p>
                    </div>

                    <!-- 6. Verdes y herbales -->
                    <div class="glass-card p-6 rounded-2xl border border-gold/10 hover:border-gold/40 transition-all duration-300 group">
                        <div class="w-12 h-12 rounded-xl bg-emerald-500/10 border border-emerald-500/20 flex items-center justify-center text-emerald-400 mb-4 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-leaf text-xl"></i>
                        </div>
                        <h3 class="font-serif text-xl text-white mb-2">6. Verdes / Herbales</h3>
                        <p class="text-xs text-gray-400 leading-relaxed mb-3">Naturales, silvestres y relajantes.</p>
                        <p class="text-[11px] text-gray-400 mb-4"><strong class="text-gold font-normal">Notas:</strong> menta, hierba fresca, albahaca y té verde.</p>
                    </div>

                    <!-- 7. Especiadas -->
                    <div class="glass-card p-6 rounded-2xl border border-gold/10 hover:border-gold/40 transition-all duration-300 group">
                        <div class="w-12 h-12 rounded-xl bg-orange-500/10 border border-orange-500/20 flex items-center justify-center text-orange-400 mb-4 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-pepper-hot text-xl"></i>
                        </div>
                        <h3 class="font-serif text-xl text-white mb-2">7. Especiadas</h3>
                        <p class="text-xs text-gray-400 leading-relaxed mb-3">Vibrantes, intensas y estimulantes.</p>
                        <p class="text-[11px] text-gray-400 mb-4"><strong class="text-gold font-normal">Notas:</strong> canela, pimienta, cardamomo y nuez moscada.</p>
                    </div>

                    <!-- 8. Orientales o ambaradas -->
                    <div class="glass-card p-6 rounded-2xl border border-gold/10 hover:border-gold/40 transition-all duration-300 group">
                        <div class="w-12 h-12 rounded-xl bg-red-500/10 border border-red-500/20 flex items-center justify-center text-red-400 mb-4 group-hover:scale-110 transition-transform">
                            <i class="fa-solid fa-fire text-xl"></i>
                        </div>
                        <h3 class="font-serif text-xl text-white mb-2">8. Orientales / Ambaradas</h3>
                        <p class="text-xs text-gray-400 leading-relaxed mb-3">Sensuales, envolventes y opulentas.</p>
                        <p class="text-[11px] text-gray-400 mb-4"><strong class="text-gold font-normal">Notas:</strong> ámbar, incienso, resinas, almizcle y vainilla.</p>
                    </div>
                </div>
            </div>
        </section>


        <!-- SECTION 2: CUESTIONARIO INTERACTIVO (9 PREGUNTAS EXACTAS) -->
        <section id="section-cuestionario" class="hidden min-h-[80vh] py-12 px-4 sm:px-6 lg:px-8 max-w-4xl mx-auto">
            <div class="mb-8 text-center">
                <span class="text-gold text-xs font-semibold uppercase tracking-widest">ÉLVARÉ PERFUMERÍA</span>
                <h2 class="font-serif text-3xl sm:text-4xl text-white mt-1">Cuestionario de Recomendación</h2>
                <p class="text-gray-400 text-xs sm:text-sm mt-2">Responde estas 9 preguntas para encontrar tu fragancia compatible.</p>
            </div>

            <!-- Progress Bar -->
            <div class="mb-10 glass-card p-4 rounded-xl border border-gold/10">
                <div class="flex justify-between items-center text-xs text-gray-400 mb-2 font-medium">
                    <span id="quiz-progress-text">Pregunta 1 de 9</span>
                    <span id="quiz-progress-percent" class="text-gold font-bold">11%</span>
                </div>
                <div class="w-full bg-charcoal h-2 rounded-full overflow-hidden border border-gold/10">
                    <div id="quiz-progress-bar" class="bg-gradient-to-r from-gold-dark to-gold h-full w-[11%] transition-all duration-500"></div>
                </div>
            </div>

            <!-- Question Card -->
            <div id="quiz-card" class="glass-card p-6 sm:p-10 rounded-2xl border border-gold/20 shadow-2xl relative">
                <div id="question-header" class="mb-8">
                    <h3 id="question-title" class="font-serif text-xl sm:text-2xl text-white font-medium mb-2">
                        <!-- JS Title -->
                    </h3>
                    <p id="question-subtitle" class="text-xs sm:text-sm text-gray-400">
                        Selecciona la opción que mejor se adapte a tus gustos.
                    </p>
                </div>

                <!-- Options List -->
                <div id="options-container" class="grid grid-cols-1 sm:grid-cols-2 gap-4 mb-8">
                    <!-- JS Options -->
                </div>

                <!-- Navigation Controls -->
                <div class="flex justify-between items-center border-t border-gold/10 pt-6">
                    <button id="btn-prev-question" onclick="prevQuestion()" class="px-5 py-2.5 rounded-full border border-gray-700 text-gray-400 hover:text-white hover:border-gold/40 text-xs font-semibold uppercase tracking-wider transition-all disabled:opacity-30 disabled:pointer-events-none">
                        <i class="fa-solid fa-arrow-left mr-2"></i> Anterior
                    </button>
                    <button id="btn-next-question" onclick="nextQuestion()" class="gold-btn text-black font-semibold text-xs uppercase tracking-widest px-6 py-2.5 rounded-full flex items-center gap-2">
                        <span>Siguiente</span>
                        <i class="fa-solid fa-arrow-right"></i>
                    </button>
                </div>
            </div>
        </section>


        <!-- SECTION 3: RESULTADOS & RECOMENDACIONES -->
        <section id="section-resultados" class="hidden min-h-[80vh] py-12 px-4 sm:px-6 lg:px-8 max-w-7xl mx-auto">
            <div class="text-center max-w-3xl mx-auto mb-12">
                <div class="inline-flex items-center gap-2 px-4 py-1 rounded-full border border-gold/30 bg-gold/10 text-gold text-xs uppercase tracking-widest mb-3">
                    <i class="fa-solid fa-sparkles"></i>
                    <span>Diagnóstico Completado</span>
                </div>
                <h2 class="font-serif text-3xl sm:text-5xl text-white">Tus Fragancias Compatibles</h2>
                <p class="text-gray-400 text-xs sm:text-sm mt-3">Basado en tus elecciones de aroma, sensación, momento, intensidad y estilo, ÉLVARÉ te recomienda las siguientes colonias.</p>
            </div>

            <!-- Profile Summary Tags -->
            <div id="user-profile-summary" class="glass-card p-6 rounded-2xl border border-gold/30 mb-12 text-center max-w-4xl mx-auto bg-gradient-to-r from-gold/5 via-charcoal to-gold/5">
                <h4 class="text-xs uppercase tracking-widest text-gold font-semibold mb-1">Tu Selección de Preferencias</h4>
                <div id="profile-tags" class="flex flex-wrap justify-center gap-2 mt-3">
                    <!-- Tags -->
                </div>
            </div>

            <!-- Recommendation Cards Grid -->
            <div id="results-cards-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mb-16">
                <!-- Perfume Cards JS -->
            </div>

            <!-- Fragrance Comparison Section -->
            <div id="comparison-section" class="glass-card p-8 rounded-3xl border border-gold/30 my-16 hidden">
                <div class="flex items-center justify-between mb-8 pb-4 border-b border-gold/20">
                    <div>
                        <span class="text-gold text-xs font-semibold uppercase tracking-widest">ÉLVARÉ Selección</span>
                        <h3 class="font-serif text-2xl text-white mt-1">Comparador de Fragancias</h3>
                    </div>
                    <button onclick="clearComparison()" class="text-xs text-gray-400 hover:text-red-400 transition-colors">
                        <i class="fa-solid fa-xmark mr-1"></i> Limpiar Comparación
                    </button>
                </div>

                <div id="comparison-table-container" class="overflow-x-auto">
                    <!-- Table JS -->
                </div>
            </div>

            <!-- Action Buttons -->
            <div class="text-center pt-8 border-t border-gold/10 flex flex-col sm:flex-row justify-center gap-4">
                <button onclick="startQuiz()" class="glass-card hover:border-gold text-white px-8 py-3.5 rounded-full text-xs font-semibold uppercase tracking-widest transition-all">
                    <i class="fa-solid fa-rotate-left mr-2 text-gold"></i> Reiniciar Cuestionario
                </button>
                <a href="#inicio" onclick="showSection('inicio')" class="gold-btn text-black font-semibold text-xs uppercase tracking-widest px-8 py-3.5 rounded-full flex items-center justify-center gap-2">
                    <i class="fa-solid fa-house"></i>
                    <span>Volver al Inicio</span>
                </a>
            </div>
        </section>

    </main>

    <!-- DETAILED MODAL DE PERFUME -->
    <div id="perfume-modal" class="fixed inset-0 z-50 bg-black/80 backdrop-blur-md hidden flex items-center justify-center p-4 overflow-y-auto">
        <div class="glass-card bg-charcoal border border-gold/40 rounded-3xl max-w-3xl w-full max-h-[90vh] overflow-y-auto relative p-6 sm:p-8 my-8 text-left shadow-2xl">
            <button onclick="closeModal()" class="absolute top-6 right-6 text-gray-400 hover:text-gold text-2xl transition-colors">
                <i class="fa-solid fa-xmark"></i>
            </button>

            <div id="modal-content">
                <!-- JS Modal Content -->
            </div>
        </div>
    </div>

    <!-- Toast Notification -->
    <div id="toast" class="fixed bottom-6 right-6 z-50 glass-card border border-gold/40 px-5 py-3 rounded-xl text-xs text-gold flex items-center gap-3 transform translate-y-20 opacity-0 transition-all duration-300">
        <i class="fa-solid fa-circle-info text-base"></i>
        <span id="toast-message">Notificación</span>
    </div>

    <!-- Footer con el nuevo Logo de ÉLVARÉ -->
    <footer class="bg-black border-t border-gold/10 py-12 px-4 sm:px-6 lg:px-8 mt-20">
        <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-8 mb-8 text-center md:text-left">
            <div class="flex flex-col items-center md:items-start">
                <div class="flex flex-col items-center md:items-start mb-3">
                    <svg class="w-10 h-10 text-gold mb-1" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M56 16 L68 8 L60 8 Z" fill="currentColor"/>
                        <text x="50%" y="58%" text-anchor="middle" font-family="'Cormorant Garamond', 'Playfair Display', serif" font-size="52" font-weight="600" fill="currentColor">É</text>
                        <path d="M 52 46 C 30 38, 25 65, 48 74 C 54 76, 60 72, 62 70" stroke="currentColor" stroke-width="2.5" fill="none" stroke-linecap="round"/>
                    </svg>
                    <span class="font-garamond text-xl tracking-[0.25em] text-white font-semibold">ÉLVARÉ</span>
                    <span class="text-[8px] tracking-[0.3em] text-gold/80 uppercase">PERFUMERÍA</span>
                </div>
                <p class="font-serif italic text-gold text-xs tracking-wider mb-2">"Tu esencia, tu presencia."</p>
                <p class="text-xs text-gray-400 leading-relaxed max-w-sm">
                    Recomendación inteligente de fragancias y asesoría aromática personalizada.
                </p>
            </div>

            <div class="flex flex-col items-center md:items-start text-xs text-gray-400 gap-2">
                <span class="text-white font-semibold uppercase tracking-widest text-[11px] mb-2">Navegación</span>
                <a href="#inicio" onclick="showSection('inicio')" class="hover:text-gold transition-colors">Inicio</a>
                <a href="#familias" onclick="showSection('inicio', 'familias')" class="hover:text-gold transition-colors">Familias Olfativas</a>
                <a href="#cuestionario" onclick="startQuiz()" class="hover:text-gold transition-colors">Descubrir mi Aroma</a>
            </div>

            <div class="text-xs text-gray-400 space-y-2">
                <span class="text-white font-semibold uppercase tracking-widest text-[11px] block mb-2">Atención ÉLVARÉ</span>
                <p><i class="fa-solid fa-location-dot text-gold mr-2"></i> Boutique ÉLVARÉ</p>
                <p><i class="fa-solid fa-envelope text-gold mr-2"></i> contacto@elvareperfumeria.com</p>
                <div class="flex justify-center md:justify-start gap-4 pt-2 text-base text-gray-400">
                    <a href="#" class="hover:text-gold transition-colors"><i class="fa-brands fa-instagram"></i></a>
                    <a href="#" class="hover:text-gold transition-colors"><i class="fa-brands fa-pinterest"></i></a>
                    <a href="#" class="hover:text-gold transition-colors"><i class="fa-brands fa-facebook"></i></a>
                </div>
            </div>
        </div>

        <div class="max-w-7xl mx-auto border-t border-gray-900 pt-6 text-center text-[11px] text-gray-500">
            <p>&copy; 2026 ÉLVARÉ Perfumería. Todos los derechos reservados.</p>
        </div>
    </footer>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        /* ==========================================================================
           BASE DE DATOS DE COLONIAS (Incluye Curve Chill en lugar de Curve Black)
           ========================================================================== */
        const PERFUMES_DB = [
            {
                id: 'p1',
                nombre: 'Curve Chill',
                marca: 'Liz Claiborne',
                familia: 'Verdes y herbales / Cítricas',
                genero: 'Masculina',
                sensacion: 'Limpieza y frescura',
                intensidad: 'Moderada y equilibrada',
                duracion: 'Duración intermedia (4-6 hrs)',
                ocasion: 'En el día a día / Para salir con amigos',
                clima: 'Templado / Caluroso',
                precio: 'Económica',
                dulzura: 'Nada dulce',
                salida: ['Bergamota', 'Limón', 'Menta helada', 'Aldehídos'],
                corazon: ['Té verde', 'Cilantro', 'Violeta', 'Jengibre'],
                fondo: ['Almizcle blanco', 'Sándalo', 'Vetiver', 'Ámbar claro'],
                descripcion: 'Una fragancia vibrante, fresca y relajada con notas heladas de menta y citrus, ideal para un estilo dinámico y juvenil.',
                icon: 'fa-snowflake',
                matchKeys: ['fresco_citrico', 'fresco_herbal', 'limpieza', 'dia_a_dia', 'amigos', 'moderada', 'intermedia', 'caluroso', 'templado', 'masculina', 'nada_dulce', 'economica']
            },
            {
                id: 'p2',
                nombre: 'Acqua Di Giò',
                marca: 'Giorgio Armani',
                familia: 'Acuáticas o marinas',
                genero: 'Masculina',
                sensacion: 'Limpieza y frescura',
                intensidad: 'Moderada y equilibrada',
                duracion: 'Duración intermedia',
                ocasion: 'En el día a día / En el trabajo',
                clima: 'Caluroso y húmedo / Templado',
                precio: 'Relación equilibrada',
                dulzura: 'Nada dulce',
                salida: ['Lima', 'Limón', 'Bergamota', 'Jazmín', 'Naranja'],
                corazon: ['Notas marinas', 'Calone', 'Melocotón', 'Freesia', 'Romero'],
                fondo: ['Almizcle blanco', 'Cedro', 'Musgo de roble', 'Pachulí', 'Ámbar'],
                descripcion: 'Icono del frescor acuático que combina brisa marina con matices cítricos limpios y transparentes.',
                icon: 'fa-water',
                matchKeys: ['acuatico', 'fresco_citrico', 'limpieza', 'trabajo', 'dia_a_dia', 'moderada', 'intermedia', 'caluroso', 'masculina', 'nada_dulce', 'equilibrada']
            },
            {
                id: 'p3',
                nombre: 'Bleu de Chanel',
                marca: 'Chanel',
                familia: 'Amaderadas / Cítricas',
                genero: 'Masculina',
                sensacion: 'Elegancia y sofisticación',
                intensidad: 'Intensa y llamativa',
                duracion: 'Muchas horas',
                ocasion: 'Para citas / Fiestas / Cualquier ocasión',
                clima: 'Variado durante el año',
                precio: 'Opciones de mayor precio',
                dulzura: 'Ligeramente dulce',
                salida: ['Pomelo', 'Limón', 'Menta', 'Pimienta rosa'],
                corazon: ['Jengibre', 'Nuez moscada', 'Jazmín'],
                fondo: ['Incienso', 'Veterver', 'Cedro', 'Sándalo', 'Pachulí'],
                descripcion: 'Una declaración amaderada aromática de elegancia pura con estela magnética e intemporal.',
                icon: 'fa-tree',
                matchKeys: ['amaderado', 'fresco_citrico', 'elegancia', 'citas', 'fiestas', 'cualquiera', 'intensa', 'muchas_horas', 'variado', 'masculina', 'ligeramente_dulce', 'mayor_precio']
            },
            {
                id: 'p4',
                nombre: 'Black Opium',
                marca: 'Yves Saint Laurent',
                familia: 'Dulces o gourmand / Orientales',
                genero: 'Femenina',
                sensacion: 'Sensualidad y misterio',
                intensidad: 'Intensa y llamativa',
                duracion: 'Muchas horas',
                ocasion: 'Para citas / Fiestas y eventos nocturnos',
                clima: 'Frío o fresco',
                precio: 'Relación equilibrada',
                dulzura: 'Muy dulce',
                salida: ['Pera', 'Flor de azahar', 'Pimienta rosa'],
                corazon: ['Café', 'Jazmín', 'Almendra amarga', 'Regaliz'],
                fondo: ['Vainilla', 'Pachulí', 'Cedro', 'Madera de cachemira'],
                descripcion: 'Fragancia adictiva basada en notas de café negro, vainilla gourmand y flores blancas envueltas en misterio nocturno.',
                icon: 'fa-fire',
                matchKeys: ['dulce_cremoso', 'oriental', 'sensualidad', 'citas', 'fiestas', 'intensa', 'muchas_horas', 'frio', 'femenina', 'muy_dulce', 'equilibrada']
            },
            {
                id: 'p5',
                nombre: 'La Vie Est Belle',
                marca: 'Lancôme',
                familia: 'Dulces o gourmand / Florales',
                genero: 'Femenina',
                sensacion: 'Dulzura y cercanía',
                intensidad: 'Intensa y llamativa',
                duracion: 'Muchas horas',
                ocasion: 'Para cualquier ocasión / Citas',
                clima: 'Templado / Frío',
                precio: 'Relación equilibrada',
                dulzura: 'Moderadamente dulce',
                salida: ['Grosella negra', 'Pera'],
                corazon: ['Iris', 'Jazmín', 'Flor de azahar'],
                fondo: ['Praliné', 'Vainilla', 'Pachulí', 'Haba tonka'],
                descripcion: 'Una oda floral gourmand que proyecta alegría de vivir, calidez y un abrazo dulce inolvidable.',
                icon: 'fa-cookie-bite',
                matchKeys: ['dulce_cremoso', 'floral', 'dulzura', 'citas', 'cualquiera', 'intensa', 'muchas_horas', 'frio', 'templado', 'femenina', 'moderadamente_dulce', 'equilibrada']
            },
            {
                id: 'p6',
                nombre: 'CK One',
                marca: 'Calvin Klein',
                familia: 'Cítricas / Verdes y herbales',
                genero: 'Unisex',
                sensacion: 'Limpieza y frescura',
                intensidad: 'Ligera y discreta',
                duracion: 'Fragancia fresca para unas horas',
                ocasion: 'En el trabajo / En el día a día',
                clima: 'Caluroso y húmedo / Templado',
                precio: 'Económica',
                dulzura: 'Nada dulce',
                salida: ['Limón', 'Notas verdes', 'Bergamota', 'Piña', 'Mandarina'],
                corazon: ['Lirio de los valles', 'Jazmín', 'Violeta', 'Nuez moscada'],
                fondo: ['Almizcle', 'Cedro', 'Ámbar', 'Sándalo', 'Musgo de roble'],
                descripcion: 'El pionero unisex por excelencia: limpio, ligero, natural y sumamente fácil de llevar.',
                icon: 'fa-lemon',
                matchKeys: ['fresco_citrico', 'verde_herbal', 'limpieza', 'trabajo', 'dia_a_dia', 'ligera', 'pocas_horas', 'caluroso', 'unisex', 'nada_dulce', 'economica']
            },
            {
                id: 'p7',
                nombre: 'Terre d\'Hermès',
                marca: 'Hermès',
                familia: 'Amaderadas / Especiadas',
                genero: 'Masculina',
                sensacion: 'Seguridad y carácter',
                intensidad: 'Moderada y equilibrada',
                duracion: 'Muchas horas',
                ocasion: 'En el trabajo / Para cualquier ocasión',
                clima: 'Variado durante el año',
                precio: 'Opciones de mayor precio',
                dulzura: 'Nada dulce',
                salida: ['Naranja', 'Pomelo'],
                corazon: ['Pimienta', 'Pelargonio', 'Pedernal mineral'],
                fondo: ['Vetiver', 'Cedro', 'Pachulí', 'Benzuí'],
                descripcion: 'Conexión poética entre la tierra y el cielo a través de notas minerales, cítricos amargos y vetiver profundo.',
                icon: 'fa-earth-americas',
                matchKeys: ['amaderado', 'especiado', 'seguridad', 'trabajo', 'cualquiera', 'moderada', 'muchas_horas', 'variado', 'masculina', 'nada_dulce', 'mayor_precio']
            },
            {
                id: 'p8',
                nombre: 'Baccarat Rouge 540',
                marca: 'Maison Francis Kurkdjian',
                familia: 'Orientales o ambaradas / Especiadas',
                genero: 'Unisex',
                sensacion: 'Elegancia y sofisticación',
                intensidad: 'Intensa y llamativa',
                duracion: 'Muchas horas',
                ocasion: 'Para citas / Fiestas / Eventos especiales',
                clima: 'Variado durante el año',
                precio: 'Opciones de mayor precio',
                dulzura: 'Moderadamente dulce',
                salida: ['Azafrán', 'Jazmín de Egipto'],
                corazon: ['Amberwood (Madera de ámbar)', 'Ámbar gris'],
                fondo: ['Resina de abeto', 'Cedro de Virginia'],
                descripcion: 'Opulencia cristalina donde el azafrán y el ámbar gris crean una firma olfativa etérea y fascinante.',
                icon: 'fa-gem',
                matchKeys: ['oriental', 'especiado', 'elegancia', 'sensualidad', 'citas', 'fiestas', 'intensa', 'muchas_horas', 'variado', 'unisex', 'open', 'moderadamente_dulce', 'mayor_precio']
            }
        ];

        /* ==========================================================================
           LAS 9 PREGUNTAS DEL CUESTIONARIO EXPLICITAS
           ========================================================================== */
        const QUIZ_QUESTIONS = [
            {
                id: 1,
                title: 'Pregunta 1. ¿Qué tipo de aroma te gusta más?',
                key: 'aroma',
                options: [
                    { label: 'Fresco y cítrico', value: 'fresco_citrico', icon: 'fa-lemon' },
                    { label: 'Dulce y cremoso', value: 'dulce_cremoso', icon: 'fa-cookie-bite' },
                    { label: 'Amaderado y elegante', value: 'amaderado', icon: 'fa-tree' },
                    { label: 'Acuático y limpio', value: 'acuatico', icon: 'fa-water' },
                    { label: 'Especiado e intenso', value: 'especiado', icon: 'fa-pepper-hot' },
                    { label: 'Floral y suave', value: 'floral', icon: 'fa-fan' },
                    { label: 'Verde y herbal', value: 'verde_herbal', icon: 'fa-leaf' },
                    { label: 'Cálido y ambarado', value: 'oriental', icon: 'fa-fire' },
                    { label: 'Me gustan varios tipos de aromas', value: 'varios', icon: 'fa-sparkles' }
                ]
            },
            {
                id: 2,
                title: 'Pregunta 2. ¿Qué sensación quieres transmitir con tu colonia?',
                key: 'sensacion',
                options: [
                    { label: 'Limpieza y frescura', value: 'limpieza', icon: 'fa-shower' },
                    { label: 'Elegancia y sofisticación', value: 'elegancia', icon: 'fa-crown' },
                    { label: 'Dulzura y cercanía', value: 'dulzura', icon: 'fa-heart' },
                    { label: 'Seguridad y carácter', value: 'seguridad', icon: 'fa-shield-halved' },
                    { label: 'Sensualidad y misterio', value: 'sensualidad', icon: 'fa-eye' },
                    { label: 'Naturalidad y tranquilidad', value: 'naturalidad', icon: 'fa-sun' }
                ]
            },
            {
                id: 3,
                title: 'Pregunta 3. ¿En qué momento utilizarás la colonia principalmente?',
                key: 'momento',
                options: [
                    { label: 'En el trabajo o centro educativo', value: 'trabajo', icon: 'fa-briefcase' },
                    { label: 'En el día a día', value: 'dia_a_dia', icon: 'fa-calendar-day' },
                    { label: 'Para salir con amigos', value: 'amigos', icon: 'fa-users' },
                    { label: 'Para citas o encuentros especiales', value: 'citas', icon: 'fa-heart-pulse' },
                    { label: 'Para fiestas y eventos nocturnos', value: 'fiestas', icon: 'fa-glass-cheers' },
                    { label: 'Para cualquier ocasión', value: 'cualquiera', icon: 'fa-globe' }
                ]
            },
            {
                id: 4,
                title: 'Pregunta 4. ¿Qué intensidad prefieres?',
                key: 'intensidad',
                options: [
                    { label: 'Ligera y discreta', value: 'ligera', icon: 'fa-feather' },
                    { label: 'Moderada y equilibrada', value: 'moderada', icon: 'fa-scale-balanced' },
                    { label: 'Intensa y llamativa', value: 'intensa', icon: 'fa-bolt' }
                ]
            },
            {
                id: 5,
                title: 'Pregunta 5. ¿Qué duración esperas?',
                key: 'duracion',
                options: [
                    { label: 'Una fragancia fresca para unas horas', value: 'pocas_horas', icon: 'fa-clock' },
                    { label: 'Una duración intermedia', value: 'intermedia', icon: 'fa-hourglass-half' },
                    { label: 'Una fragancia que permanezca durante muchas horas', value: 'muchas_horas', icon: 'fa-hourglass-end' }
                ]
            },
            {
                id: 6,
                title: 'Pregunta 6. ¿Qué clima predomina donde utilizarás la colonia?',
                key: 'clima',
                options: [
                    { label: 'Caluroso y húmedo', value: 'caluroso', icon: 'fa-temperature-high' },
                    { label: 'Templado', value: 'templado', icon: 'fa-cloud-sun' },
                    { label: 'Frío o fresco', value: 'frio', icon: 'fa-snowflake' },
                    { label: 'Variado durante el año', value: 'variado', icon: 'fa-calendar' }
                ]
            },
            {
                id: 7,
                title: 'Pregunta 7. ¿Qué tipo de colonia prefieres?',
                key: 'tipo',
                options: [
                    { label: 'Masculina', value: 'masculina', icon: 'fa-mars' },
                    { label: 'Femenina', value: 'femenina', icon: 'fa-venus' },
                    { label: 'Unisex', value: 'unisex', icon: 'fa-venus-mars' },
                    { label: 'Estoy abierto a diferentes opciones', value: 'open', icon: 'fa-compass' }
                ]
            },
            {
                id: 8,
                title: 'Pregunta 8. ¿Qué nivel de dulzura prefieres?',
                key: 'dulzura',
                options: [
                    { label: 'Nada dulce', value: 'nada_dulce', icon: 'fa-ban' },
                    { label: 'Ligeramente dulce', value: 'ligeramente_dulce', icon: 'fa-seedling' },
                    { label: 'Moderadamente dulce', value: 'moderadamente_dulce', icon: 'fa-cookie' },
                    { label: 'Muy dulce', value: 'muy_dulce', icon: 'fa-candy-cane' }
                ]
            },
            {
                id: 9,
                title: 'Pregunta 9. ¿Qué importancia tiene el precio?',
                key: 'precio',
                options: [
                    { label: 'Busco opciones económicas', value: 'economica', icon: 'fa-tag' },
                    { label: 'Prefiero una relación equilibrada entre precio y calidad', value: 'equilibrada', icon: 'fa-scale-balanced' },
                    { label: 'Estoy dispuesto a considerar opciones de mayor precio', value: 'mayor_precio', icon: 'fa-gem' }
                ]
            }
        ];

        /* STATE MANAGEMENT */
        let currentQuestionIndex = 0;
        let quizAnswers = {};
        let comparedPerfumeIds = [];

        /* NAVIGATION LOGIC */
        function showSection(sectionId, scrollToId = null) {
            document.getElementById('section-inicio').classList.add('hidden');
            document.getElementById('section-cuestionario').classList.add('hidden');
            document.getElementById('section-resultados').classList.add('hidden');

            const target = document.getElementById('section-' + sectionId);
            if (target) {
                target.classList.remove('hidden');
                window.scrollTo({ top: 0, behavior: 'smooth' });
            }

            if (scrollToId) {
                setTimeout(() => {
                    const el = document.getElementById(scrollToId);
                    if (el) el.scrollIntoView({ behavior: 'smooth' });
                }, 100);
            }
        }

        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        }

        /* QUIZ LOGIC */
        function startQuiz() {
            currentQuestionIndex = 0;
            quizAnswers = {};
            showSection('cuestionario');
            renderQuestion();
        }

        function renderQuestion() {
            const q = QUIZ_QUESTIONS[currentQuestionIndex];
            const total = QUIZ_QUESTIONS.length;
            const progressPercent = Math.round(((currentQuestionIndex + 1) / total) * 100);

            document.getElementById('quiz-progress-text').innerText = `Pregunta ${currentQuestionIndex + 1} de ${total}`;
            document.getElementById('quiz-progress-percent').innerText = `${progressPercent}%`;
            document.getElementById('quiz-progress-bar').style.width = `${progressPercent}%`;

            document.getElementById('question-title').innerText = q.title;

            const container = document.getElementById('options-container');
            container.innerHTML = '';

            const selectedValue = quizAnswers[q.id];

            q.options.forEach(opt => {
                const isSelected = selectedValue === opt.value;
                const card = document.createElement('div');
                card.className = `p-4 sm:p-5 rounded-2xl cursor-pointer transition-all flex items-center gap-4 ${
                    isSelected ? 'glass-card-active border-gold' : 'glass-card hover:border-gold/50'
                }`;
                card.onclick = () => selectOption(q.id, opt.value, opt.label);

                card.innerHTML = `
                    <div class="w-10 h-10 rounded-xl ${isSelected ? 'bg-gold text-black' : 'bg-charcoal border border-gold/20 text-gold'} flex items-center justify-center flex-shrink-0 transition-colors">
                        <i class="fa-solid ${opt.icon} text-base"></i>
                    </div>
                    <span class="text-xs sm:text-sm font-medium ${isSelected ? 'text-white font-semibold' : 'text-gray-300'}">${opt.label}</span>
                `;
                container.appendChild(card);
            });

            document.getElementById('btn-prev-question').disabled = (currentQuestionIndex === 0);
            const nextBtn = document.getElementById('btn-next-question');
            if (currentQuestionIndex === total - 1) {
                nextBtn.innerHTML = `<span>Ver Resultados</span> <i class="fa-solid fa-wand-magic-sparkles"></i>`;
            } else {
                nextBtn.innerHTML = `<span>Siguiente</span> <i class="fa-solid fa-arrow-right"></i>`;
            }
        }

        function selectOption(questionId, value, label) {
            quizAnswers[questionId] = value;
            quizAnswers[questionId + '_label'] = label;
            renderQuestion();
        }

        function prevQuestion() {
            if (currentQuestionIndex > 0) {
                currentQuestionIndex--;
                renderQuestion();
            }
        }

        function nextQuestion() {
            const currentQ = QUIZ_QUESTIONS[currentQuestionIndex];
            if (!quizAnswers[currentQ.id]) {
                showToast('Por favor selecciona una opción para continuar.');
                return;
            }

            if (currentQuestionIndex < QUIZ_QUESTIONS.length - 1) {
                currentQuestionIndex++;
                renderQuestion();
            } else {
                calculateAndShowResults();
            }
        }

        /* ALGORITMO DE COINCIDENCIA (% MATCH) Y RESULTADOS */
        function calculateAndShowResults() {
            const userValues = Object.keys(quizAnswers)
                .filter(k => !k.endsWith('_label'))
                .map(k => quizAnswers[k]);

            const scoredPerfumes = PERFUMES_DB.map(perfume => {
                let matches = 0;
                userValues.forEach(val => {
                    if (val !== 'varios' && val !== 'open' && perfume.matchKeys.includes(val)) {
                        matches += 1;
                    }
                });

                // Calculate affinity match percentage
                let percentage = Math.round((matches / 8) * 100) + 55;
                if (percentage > 99) percentage = 99;

                return { ...perfume, matchPercentage: percentage };
            });

            // Sort descending
            scoredPerfumes.sort((a, b) => b.matchPercentage - a.matchPercentage);
            const topRecommendations = scoredPerfumes.slice(0, 3);

            renderResults(topRecommendations);
            showSection('resultados');
        }

        function renderResults(perfumes) {
            // Render Profile Summary Tags
            const profileContainer = document.getElementById('profile-tags');
            profileContainer.innerHTML = '';
            
            QUIZ_QUESTIONS.forEach(q => {
                const label = quizAnswers[q.id + '_label'];
                if (label) {
                    const tag = document.createElement('span');
                    tag.className = 'px-3 py-1 rounded-full bg-gold/10 border border-gold/30 text-gold text-[11px] uppercase tracking-wider font-semibold';
                    tag.innerText = label;
                    profileContainer.appendChild(tag);
                }
            });

            // Render Recommended Perfume Cards
            const grid = document.getElementById('results-cards-grid');
            grid.innerHTML = '';

            perfumes.forEach((perfume) => {
                const card = document.createElement('div');
                card.className = 'glass-card rounded-3xl border border-gold/20 p-6 flex flex-col justify-between hover:border-gold/50 transition-all duration-300 group relative';

                card.innerHTML = `
                    <div>
                        <!-- Match Ribbon -->
                        <div class="flex items-center justify-between mb-4">
                            <span class="px-3 py-1 rounded-full bg-gold/20 text-gold font-bold text-xs tracking-wider">
                                <i class="fa-solid fa-star mr-1"></i> ${perfume.matchPercentage}% COINCIDENCIA
                            </span>
                            <span class="text-[10px] uppercase text-gray-400 font-semibold tracking-widest">${perfume.genero}</span>
                        </div>

                        <!-- Bottle Icon -->
                        <div class="w-20 h-20 mx-auto my-4 rounded-full bg-gold/10 border border-gold/30 flex items-center justify-center text-gold text-3xl group-hover:scale-110 transition-transform">
                            <i class="fa-solid ${perfume.icon}"></i>
                        </div>

                        <!-- Title -->
                        <div class="text-center mb-4">
                            <h3 class="font-serif text-2xl text-white font-semibold">${perfume.nombre}</h3>
                            <p class="text-xs text-gold/80 font-medium">${perfume.marca}</p>
                        </div>

                        <p class="text-xs text-gray-300 leading-relaxed text-center mb-6">
                            "${perfume.descripcion}"
                        </p>

                        <!-- Specifications -->
                        <div class="bg-charcoal/80 p-4 rounded-xl border border-gold/10 text-xs space-y-2 mb-6">
                            <div class="flex justify-between">
                                <span class="text-gray-400">Familia:</span>
                                <span class="text-white font-medium">${perfume.familia}</span>
                            </div>
                            <div class="flex justify-between">
                                <span class="text-gray-400">Sensación:</span>
                                <span class="text-white font-medium">${perfume.sensacion}</span>
                            </div>
                            <div class="flex justify-between">
                                <span class="text-gray-400">Intensidad:</span>
                                <span class="text-white font-medium">${perfume.intensidad}</span>
                            </div>
                            <div class="flex justify-between">
                                <span class="text-gray-400">Duración:</span>
                                <span class="text-white font-medium">${perfume.duracion}</span>
                            </div>
                        </div>
                    </div>

                    <!-- Actions -->
                    <div class="space-y-2 pt-2">
                        <button onclick="openPerfumeModal('${perfume.id}')" class="w-full gold-btn text-black font-semibold text-xs uppercase tracking-widest py-3 rounded-xl transition-all flex items-center justify-center gap-2">
                            <i class="fa-solid fa-eye"></i> Pirámide Olfativa & Notas
                        </button>
                        <button onclick="toggleComparePerfume('${perfume.id}')" class="w-full glass-card hover:border-gold text-white text-xs uppercase tracking-widest py-2.5 rounded-xl transition-all flex items-center justify-center gap-2">
                            <i class="fa-solid fa-code-compare text-gold"></i>
                            <span id="btn-compare-text-${perfume.id}">
                                ${comparedPerfumeIds.includes(perfume.id) ? 'Quitar de Comparación' : 'Comparar Colonia'}
                            </span>
                        </button>
                    </div>
                `;
                grid.appendChild(card);
            });
        }

        /* MODAL DE PERFUME */
        function openPerfumeModal(perfumeId) {
            const perfume = PERFUMES_DB.find(p => p.id === perfumeId);
            if (!perfume) return;

            const modalContent = document.getElementById('modal-content');
            modalContent.innerHTML = `
                <div class="flex flex-col md:flex-row gap-6 items-start">
                    <div class="w-24 h-24 rounded-2xl bg-gold/10 border border-gold/30 flex items-center justify-center text-gold text-4xl flex-shrink-0 mx-auto md:mx-0">
                        <i class="fa-solid ${perfume.icon}"></i>
                    </div>
                    <div class="flex-grow text-center md:text-left">
                        <span class="text-gold text-xs font-semibold uppercase tracking-widest">${perfume.familia} &bull; ${perfume.genero}</span>
                        <h2 class="font-serif text-3xl text-white font-semibold mt-1">${perfume.nombre}</h2>
                        <p class="text-xs text-gray-400">${perfume.marca}</p>
                    </div>
                </div>

                <p class="text-sm text-gray-300 leading-relaxed my-6 bg-black/40 p-4 rounded-xl border border-gold/10 italic">
                    "${perfume.descripcion}"
                </p>

                <!-- PIRÁMIDE OLFATIVA -->
                <div class="mb-8">
                    <h4 class="font-serif text-lg text-white mb-4 flex items-center gap-2">
                        <i class="fa-solid fa-layer-group text-gold text-sm"></i>
                        <span>Pirámide Olfativa Completa</span>
                    </h4>

                    <div class="space-y-3">
                        <div class="glass-card p-4 rounded-xl border border-gold/10">
                            <span class="text-xs font-semibold uppercase text-gold tracking-wider block mb-1">Notas de Salida (Primeros minutos)</span>
                            <div class="flex flex-wrap gap-2 mt-2">
                                ${perfume.salida.map(n => `<span class="px-2.5 py-1 rounded-md bg-gold/10 text-xs text-gray-200 border border-gold/20">${n}</span>`).join('')}
                            </div>
                        </div>

                        <div class="glass-card p-4 rounded-xl border border-gold/10">
                            <span class="text-xs font-semibold uppercase text-gold tracking-wider block mb-1">Notas de Corazón (Núcleo aromático)</span>
                            <div class="flex flex-wrap gap-2 mt-2">
                                ${perfume.corazon.map(n => `<span class="px-2.5 py-1 rounded-md bg-gold/10 text-xs text-gray-200 border border-gold/20">${n}</span>`).join('')}
                            </div>
                        </div>

                        <div class="glass-card p-4 rounded-xl border border-gold/10">
                            <span class="text-xs font-semibold uppercase text-gold tracking-wider block mb-1">Notas de Fondo (Fijación y estela)</span>
                            <div class="flex flex-wrap gap-2 mt-2">
                                ${perfume.fondo.map(n => `<span class="px-2.5 py-1 rounded-md bg-gold/10 text-xs text-gray-200 border border-gold/20">${n}</span>`).join('')}
                            </div>
                        </div>
                    </div>
                </div>

                <!-- FICHA TÉCNICA RECOMENDADA -->
                <div class="grid grid-cols-2 sm:grid-cols-3 gap-3 text-xs mb-8">
                    <div class="bg-charcoal p-3 rounded-xl border border-gold/10">
                        <span class="text-gray-400 block mb-1">Ocasión</span>
                        <span class="text-white font-medium">${perfume.ocasion}</span>
                    </div>
                    <div class="bg-charcoal p-3 rounded-xl border border-gold/10">
                        <span class="text-gray-400 block mb-1">Clima Recomendado</span>
                        <span class="text-white font-medium">${perfume.clima}</span>
                    </div>
                    <div class="bg-charcoal p-3 rounded-xl border border-gold/10">
                        <span class="text-gray-400 block mb-1">Nivel de Dulzura</span>
                        <span class="text-white font-medium">${perfume.dulzura}</span>
                    </div>
                </div>

                <div class="pt-4 border-t border-gold/10 flex flex-col sm:flex-row gap-3">
                    <button onclick="showToast('Fragancia guardada en tu selección de ÉLVARÉ'); closeModal();" class="gold-btn flex-grow text-black font-semibold text-xs uppercase tracking-widest py-3.5 rounded-xl transition-all text-center">
                        <i class="fa-solid fa-bookmark mr-2"></i> Guardar Fragancia
                    </button>
                    <button onclick="closeModal()" class="glass-card hover:border-gold text-gray-300 text-xs uppercase tracking-widest py-3.5 px-6 rounded-xl transition-all">
                        Cerrar
                    </button>
                </div>
            `;

            document.getElementById('perfume-modal').classList.remove('hidden');
        }

        function closeModal() {
            document.getElementById('perfume-modal').classList.add('hidden');
        }

        /* COMPARADOR DE COLONIAS */
        function toggleComparePerfume(perfumeId) {
            const index = comparedPerfumeIds.indexOf(perfumeId);
            if (index > -1) {
                comparedPerfumeIds.splice(index, 1);
                showToast('Colonia removida de la comparación');
            } else {
                if (comparedPerfumeIds.length >= 3) {
                    showToast('Puedes comparar hasta 3 fragancias simultáneamente.');
                    return;
                }
                comparedPerfumeIds.push(perfumeId);
                showToast('Colonia agregada a la comparación');
            }

            const btnText = document.getElementById(`btn-compare-text-${perfumeId}`);
            if (btnText) {
                btnText.innerText = comparedPerfumeIds.includes(perfumeId) ? 'Quitar de Comparación' : 'Comparar Colonia';
            }

            renderComparisonTable();
        }

        function renderComparisonTable() {
            const container = document.getElementById('comparison-section');
            const tableContainer = document.getElementById('comparison-table-container');

            if (comparedPerfumeIds.length === 0) {
                container.classList.add('hidden');
                return;
            }

            container.classList.remove('hidden');

            const perfumes = comparedPerfumeIds.map(id => PERFUMES_DB.find(p => p.id === id));

            let html = `
                <table class="w-full text-left border-collapse text-xs">
                    <thead>
                        <tr class="border-b border-gold/20">
                            <th class="p-3 text-gold uppercase tracking-wider">Atributo</th>
                            ${perfumes.map(p => `<th class="p-3 font-serif text-lg text-white">${p.nombre}</th>`).join('')}
                        </tr>
                    </thead>
                    <tbody class="divide-y divide-gray-800 text-gray-300">
                        <tr>
                            <td class="p-3 font-semibold text-gray-400">Marca</td>
                            ${perfumes.map(p => `<td class="p-3 text-gold">${p.marca}</td>`).join('')}
                        </tr>
                        <tr>
                            <td class="p-3 font-semibold text-gray-400">Familia Olfativa</td>
                            ${perfumes.map(p => `<td class="p-3">${p.familia}</td>`).join('')}
                        </tr>
                        <tr>
                            <td class="p-3 font-semibold text-gray-400">Sensación</td>
                            ${perfumes.map(p => `<td class="p-3">${p.sensacion}</td>`).join('')}
                        </tr>
                        <tr>
                            <td class="p-3 font-semibold text-gray-400">Intensidad</td>
                            ${perfumes.map(p => `<td class="p-3">${p.intensidad}</td>`).join('')}
                        </tr>
                        <tr>
                            <td class="p-3 font-semibold text-gray-400">Duración Estimada</td>
                            ${perfumes.map(p => `<td class="p-3">${p.duracion}</td>`).join('')}
                        </tr>
                        <tr>
                            <td class="p-3 font-semibold text-gray-400">Notas de Salida</td>
                            ${perfumes.map(p => `<td class="p-3">${p.salida.join(', ')}</td>`).join('')}
                        </tr>
                        <tr>
                            <td class="p-3 font-semibold text-gray-400">Notas de Corazón</td>
                            ${perfumes.map(p => `<td class="p-3">${p.corazon.join(', ')}</td>`).join('')}
                        </tr>
                    </tbody>
                </table>
            `;

            tableContainer.innerHTML = html;
        }

        function clearComparison() {
            comparedPerfumeIds = [];
            renderComparisonTable();
            PERFUMES_DB.forEach(p => {
                const btnText = document.getElementById(`btn-compare-text-${p.id}`);
                if (btnText) btnText.innerText = 'Comparar Colonia';
            });
            showToast('Comparación vaciada.');
        }

        /* TOAST NOTIFICATIONS */
        function showToast(message) {
            const toast = document.getElementById('toast');
            const toastMsg = document.getElementById('toast-message');
            toastMsg.innerText = message;

            toast.classList.remove('translate-y-20', 'opacity-0');
            toast.classList.add('translate-y-0', 'opacity-100');

            setTimeout(() => {
                toast.classList.remove('translate-y-0', 'opacity-100');
                toast.classList.add('translate-y-20', 'opacity-0');
            }, 3000);
        }

        window.onclick = function(event) {
            const modal = document.getElementById('perfume-modal');
            if (event.target === modal) {
                closeModal();
            }
        };
    </script>
</body>
</html>
