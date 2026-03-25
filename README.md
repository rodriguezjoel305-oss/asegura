<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="AseguraFL: Compara seguros de auto, hogar y más en Florida. Refiere amigos hispanohablantes y gana hasta $1,000 en tarjetas Amazon. ¡Cotizaciones gratis en segundos!">
    <title>AseguraFL | Seguros Baratos en Florida para Hispanos</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&amp;family=Poppins:wght@600&amp;display=swap');
        
        :root {
            --primary: #1e40af;
        }
        
        .tailwind-ready * {
            font-family: 'Inter', system_ui, sans-serif;
        }
        
        .logo-font {
            font-family: 'Poppins', sans-serif;
        }
        
        .hero-bg {
            background: linear-gradient(90deg, rgba(30, 64, 175, 0.85) 0%, rgba(30, 64, 175, 0.75) 100%),
                        url('https://picsum.photos/id/1015/2000/1200') center/cover no-repeat;
        }
        
        .quote-card {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        .quote-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 20px 25px -5px rgb(30 64 175 / 0.1), 0 8px 10px -6px rgb(30 64 175 / 0.1);
        }
        
        .nav-link {
            position: relative;
        }
        
        .nav-link:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -2px;
            left: 0;
            background-color: #1e40af;
            transition: all 0.3s;
        }
        
        .nav-link:hover:after {
            width: 100%;
        }
    </style>
</head>
<body class="tailwind-ready">
    <!-- NAVBAR -->
    <nav class="bg-white border-b sticky top-0 z-50 shadow-sm">
        <div class="max-w-7xl mx-auto px-6 py-4 flex items-center justify-between">
            <!-- Logo -->
            <div class="flex items-center gap-x-2">
                <div class="w-10 h-10 bg-[#1e40af] rounded-2xl flex items-center justify-center text-white text-2xl">
                    <i class="fas fa-shield-alt"></i>
                </div>
                <h1 class="logo-font text-3xl font-semibold tracking-tighter text-[#1e40af]">Asegura<span class="text-amber-500">FL</span></h1>
                <span class="text-xs bg-amber-100 text-amber-700 px-2 py-0.5 rounded-full font-medium">Miami • Orlando • Tampa</span>
            </div>

            <!-- Desktop Menu -->
            <div class="hidden md:flex items-center gap-x-8 text-sm font-medium">
                <a href="#comparar" class="nav-link text-gray-700 hover:text-[#1e40af]">Comparar Cotizaciones</a>
                <a href="#referidos" class="nav-link text-gray-700 hover:text-[#1e40af]">Programa de Referidos</a>
                <a href="#como-funciona" class="nav-link text-gray-700 hover:text-[#1e40af]">Cómo Funciona</a>
                <a href="#seguros" class="nav-link text-gray-700 hover:text-[#1e40af]">Tipos de Seguros</a>
                <a href="#blog" class="nav-link text-gray-700 hover:text-[#1e40af]">Blog en Español</a>
            </div>

            <div class="flex items-center gap-x-4">
                <!-- Florida flag indicator -->
                <div class="hidden sm:flex items-center text-xs font-medium bg-blue-50 text-blue-700 px-3 py-1 rounded-full">
                    <i class="fas fa-map-marker-alt mr-1"></i>
                    Florida • Hispanos
                </div>
                
                <!-- Login / Register -->
                <button onclick="showLoginModal()" 
                        class="px-5 py-2 text-sm font-medium text-gray-700 hover:text-[#1e40af] flex items-center gap-x-2">
                    <i class="fas fa-user"></i>
                    Iniciar Sesión
                </button>
                
                <button onclick="showReferralModal()" 
                        class="bg-[#1e40af] hover:bg-[#1e40af]/90 text-white px-6 py-2 rounded-2xl text-sm font-semibold flex items-center gap-x-2 transition">
                    <i class="fas fa-gift"></i>
                    Referir Amigos
                </button>
                
                <!-- Mobile menu button -->
                <button onclick="toggleMobileMenu()" class="md:hidden text-2xl text-gray-700">
                    <i class="fas fa-bars" id="menu-icon"></i>
                </button>
            </div>
        </div>
        
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white border-t px-6 py-4">
            <div class="flex flex-col gap-y-4 text-sm font-medium">
                <a href="#comparar" onclick="toggleMobileMenu()" class="py-2">Comparar Cotizaciones</a>
                <a href="#referidos" onclick="toggleMobileMenu()" class="py-2">Programa de Referidos</a>
                <a href="#como-funciona" onclick="toggleMobileMenu()" class="py-2">Cómo Funciona</a>
                <a href="#seguros" onclick="toggleMobileMenu()" class="py-2">Tipos de Seguros</a>
                <a href="#blog" onclick="toggleMobileMenu()" class="py-2">Blog en Español</a>
                <div class="pt-4 border-t flex gap-x-4">
                    <button onclick="showLoginModal();toggleMobileMenu()" class="flex-1 py-3 border border-gray-300 rounded-2xl">Iniciar Sesión</button>
                    <button onclick="showReferralModal();toggleMobileMenu()" class="flex-1 py-3 bg-[#1e40af] text-white rounded-2xl">Referir y Ganar</button>
                </div>
            </div>
        </div>
    </nav>

    <!-- HERO -->
    <header id="hero" class="hero-bg text-white">
        <div class="max-w-7xl mx-auto px-6 pt-16 pb-20 grid md:grid-cols-2 gap-12 items-center">
            <div class="space-y-8">
                <div class="inline-flex items-center gap-x-2 bg-white/20 backdrop-blur-md px-4 py-2 rounded-3xl text-sm font-medium">
                    <i class="fas fa-flag-usa"></i>
                    <span>Para hispanohablantes en Florida • 100% en Español</span>
                </div>
                
                <h1 class="text-5xl md:text-6xl font-semibold leading-none tracking-tighter">
                    Compara seguros de auto y hogar<br>en Florida y <span class="text-amber-400">ahorra hasta 40%</span>
                </h1>
                
                <p class="text-xl text-white/90 max-w-lg">
                    Cotizaciones instantáneas de 120+ aseguradoras. 
                    Refiere a tu familia y amigos y gana tarjetas de regalo Amazon de hasta $1,000.
                </p>
                
                <div class="flex flex-wrap gap-4">
                    <button onclick="document.getElementById('quote-form').scrollIntoView({behavior: 'smooth'})" 
                            class="bg-amber-400 hover:bg-amber-300 text-[#1e40af] font-semibold text-lg px-10 py-5 rounded-3xl flex items-center gap-x-3 shadow-lg shadow-amber-500/30">
                        <i class="fas fa-search"></i>
                        Obtener Cotización Gratis
                    </button>
                    
                    <button onclick="showReferralModal()" 
                            class="border-2 border-white hover:bg-white/10 font-semibold text-lg px-8 py-5 rounded-3xl flex items-center gap-x-3">
                        <i class="fas fa-share-alt"></i>
                        Referir &amp; Ganar $50+
                    </button>
                </div>
                
                <div class="flex items-center gap-x-8 text-sm">
                    <div class="flex -space-x-4">
                        <div class="w-8 h-8 bg-white rounded-2xl flex items-center justify-center text-[#1e40af] text-xs font-bold">GE</div>
                        <div class="w-8 h-8 bg-white rounded-2xl flex items-center justify-center text-[#1e40af] text-xs font-bold">PR</div>
                        <div class="w-8 h-8 bg-white rounded-2xl flex items-center justify-center text-[#1e40af] text-xs font-bold">SF</div>
                    </div>
                    <p class="text-white/80">+120 aseguradoras confiables<br><span class="font-medium text-amber-400">incluyendo soporte bilingüe</span></p>
                    
                    <div class="flex items-center gap-x-1 text-amber-400">
                        <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
                        <span class="ml-2 text-white font-medium">4.9/5 (8,742 reseñas)</span>
                    </div>
                </div>
                
                <!-- Trust signals -->
                <div class="flex flex-wrap items-center gap-x-6 text-xs opacity-75">
                    <div><i class="fas fa-lock mr-1"></i> Seguro SSL</div>
                    <div><i class="fas fa-shield-alt mr-1"></i> No compartimos tus datos</div>
                    <div><i class="fas fa-car mr-1"></i> Cubertura contra huracanes</div>
                    <div class="text-amber-400 font-medium">¡Funciona en Miami Beach, Orlando, Tampa y todo Florida!</div>
                </div>
            </div>
            
            <!-- Hero visual form preview -->
            <div class="bg-white rounded-3xl shadow-2xl p-8 text-gray-900">
                <h3 class="text-2xl font-semibold mb-6 text-center">Prueba en 30 segundos</h3>
                <div class="space-y-6">
                    <div>
                        <label class="block text-sm font-medium mb-2">Código postal en Florida</label>
                        <input id="hero-zip" type="text" value="33139" 
                               class="w-full px-4 py-4 border border-gray-200 rounded-2xl focus:outline-none focus:border-[#1e40af]">
                    </div>
                    <div class="grid grid-cols-2 gap-4">
                        <div>
                            <label class="block text-sm font-medium mb-2">Tipo de seguro</label>
                            <select id="hero-type" class="w-full px-4 py-4 border border-gray-200 rounded-2xl focus:outline-none focus:border-[#1e40af]">
                                <option value="auto">Seguro de Auto</option>
                                <option value="hogar">Seguro de Hogar</option>
                                <option value="renters">Seguro de Inquilinos</option>
                            </select>
                        </div>
                        <div>
                            <label class="block text-sm font-medium mb-2">Edad</label>
                            <input type="text" value="35" class="w-full px-4 py-4 border border-gray-200 rounded-2xl focus:outline-none focus:border-[#1e40af]">
                        </div>
                    </div>
                    <button onclick="simulateQuickQuote()" 
                            class="w-full bg-[#1e40af] text-white py-5 rounded-3xl font-semibold text-lg flex items-center justify-center gap-x-3">
                        <i class="fas fa-magic"></i>
                        Ver Cotizaciones Instantáneas
                    </button>
                    <p class="text-center text-xs text-gray-500">Miles de hispanos en Florida ya ahorraron con AseguraFL</p>
                </div>
            </div>
        </div>
    </header>

    <!-- REFERRAL HIGHLIGHT BANNER -->
    <div id="referidos" class="bg-gradient-to-r from-amber-400 to-yellow-500 py-6">
        <div class="max-w-7xl mx-auto px-6 flex flex-col md:flex-row items-center justify-between gap-6 text-[#1e40af]">
            <div class="flex items-center gap-x-4">
                <i class="fas fa-gift text-5xl"></i>
                <div>
                    <h2 class="text-3xl font-semibold">¡Programa de Referidos AseguraFL!</h2>
                    <p class="text-lg">Refiere a un amigo o familiar hispano en Florida → Ambos ganan</p>
                </div>
            </div>
            <div class="text-center md:text-right">
                <div class="flex items-baseline justify-center md:justify-end gap-x-2">
                    <span class="text-6xl font-bold">$50</span>
                    <span class="text-2xl">por cada referencia exitosa</span>
                </div>
                <p class="text-sm font-medium">Máximo $1,000 por persona • Tarjeta Amazon en 2-3 semanas</p>
            </div>
            <button onclick="showReferralModal()" 
                    class="bg-white text-[#1e40af] px-10 py-4 rounded-3xl font-semibold flex items-center gap-x-3 hover:scale-105 transition">
                <i class="fas fa-share-from-square"></i>
                Obtener mi enlace de referido
            </button>
        </div>
    </div>

    <!-- COMPARAR COTIZACIONES FORM -->
    <section id="comparar" class="max-w-7xl mx-auto px-6 py-20">
        <div class="text-center mb-12">
            <span class="px-6 py-2 bg-[#1e40af]/10 text-[#1e40af] rounded-3xl text-sm font-medium">Paso 1 • Gratis y sin compromiso</span>
            <h2 class="text-4xl font-semibold mt-4">Compara cotizaciones reales de seguros en Florida</h2>
            <p class="mt-4 max-w-md mx-auto text-gray-600">Solo dime tu código postal y tipo de seguro. En segundos verás precios de GEICO, Progressive, State Farm y más.</p>
        </div>
        
        <form id="quote-form" onsubmit="handleQuoteSubmit(event)" class="max-w-2xl mx-auto bg-white shadow-xl rounded-3xl p-10">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <!-- ZIP -->
                <div class="md:col-span-1">
                    <label class="block text-sm font-medium mb-3 text-gray-700">Código Postal <span class="text-[#1e40af]">(Florida)</span></label>
                    <div class="relative">
                        <i class="fas fa-map-marker-alt absolute left-5 top-1/2 -translate-y-1/2 text-gray-400"></i>
                        <input id="zip" type="text" value="33139" maxlength="5"
                               class="w-full pl-12 pr-6 py-6 border-2 border-gray-200 rounded-3xl text-2xl focus:border-[#1e40af] focus:outline-none">
                    </div>
                </div>
                
                <!-- Type -->
                <div class="md:col-span-1">
                    <label class="block text-sm font-medium mb-3 text-gray-700">¿Qué quieres asegurar?</label>
                    <select id="insurance-type" class="w-full py-6 px-6 border-2 border-gray-200 rounded-3xl text-lg focus:border-[#1e40af] focus:outline-none">
                        <option value="auto">🚗 Seguro de Auto</option>
                        <option value="hogar">🏠 Seguro de Hogar (huracanes)</option>
                        <option value="renters">🏡 Seguro de Inquilinos</option>
                        <option value="vida">🛡️ Seguro de Vida</option>
                    </select>
                </div>
                
                <!-- Submit -->
                <div class="md:col-span-1 flex items-end">
                    <button type="submit"
                            class="w-full bg-[#1e40af] hover:bg-[#1e40af]/90 text-white py-7 rounded-3xl text-xl font-semibold flex items-center justify-center gap-x-3">
                        <i class="fas fa-bolt"></i>
                        VER COTIZACIONES
                    </button>
                </div>
            </div>
            
            <p class="text-center text-xs text-gray-400 mt-8">🔒 Tus datos están protegidos • No vendemos tu información</p>
        </form>
        
        <!-- RESULTS AREA (hidden initially) -->
        <div id="quote-results" class="hidden mt-16">
            <h3 class="text-2xl font-semibold mb-8 text-center">¡Aquí están tus cotizaciones personalizadas para el ZIP 33139!</h3>
            
            <div class="grid md:grid-cols-3 gap-6" id="quotes-grid">
                <!-- Populated by JS -->
            </div>
            
            <div class="text-center mt-10">
                <button onclick="buyPolicy()" 
                        class="px-8 py-4 bg-emerald-500 text-white rounded-3xl font-medium flex items-center gap-x-3 mx-auto">
                    <i class="fas fa-check-circle"></i>
                    Comprar la mejor oferta ahora
                </button>
                <p class="text-sm text-gray-500 mt-3">O llama a un agente bilingüe: <span class="font-semibold">(305) 555-0123</span></p>
            </div>
        </div>
    </section>

    <!-- CÓMO FUNCIONA -->
    <section id="como-funciona" class="bg-gray-50 py-20">
        <div class="max-w-7xl mx-auto px-6">
            <div class="text-center mb-12">
                <h2 class="text-4xl font-semibold">Cómo funciona AseguraFL (en menos de 2 minutos)</h2>
            </div>
            
            <div class="grid md:grid-cols-4 gap-8">
                <div class="text-center">
                    <div class="w-14 h-14 mx-auto bg-[#1e40af] text-white rounded-2xl flex items-center justify-center text-3xl mb-6">1</div>
                    <h4 class="font-semibold text-xl mb-2">Ingresa tu ZIP</h4>
                    <p class="text-gray-600">Dinos dónde vives en Florida y qué seguro necesitas.</p>
                </div>
                <div class="text-center">
                    <div class="w-14 h-14 mx-auto bg-[#1e40af] text-white rounded-2xl flex items-center justify-center text-3xl mb-6">2</div>
                    <h4 class="font-semibold text-xl mb-2">Comparamos por ti</h4>
                    <p class="text-gray-600">Recibe cotizaciones de +120 aseguradoras con soporte en español.</p>
                </div>
                <div class="text-center">
                    <div class="w-14 h-14 mx-auto bg-[#1e40af] text-white rounded-2xl flex items-center justify-center text-3xl mb-6">3</div>
                    <h4 class="font-semibold text-xl mb-2">Elige y ahorra</h4>
                    <p class="text-gray-600">Compra en línea o habla con un agente bilingüe de Florida.</p>
                </div>
                <div class="text-center relative">
                    <div class="w-14 h-14 mx-auto bg-amber-400 text-white rounded-2xl flex items-center justify-center text-3xl mb-6">4</div>
                    <h4 class="font-semibold text-xl mb-2">Refiere y gana</h4>
                    <p class="text-gray-600">Comparte tu enlace único y recibe Amazon gift cards cuando tus amigos compren.</p>
                    <span class="absolute -top-3 -right-3 bg-amber-400 text-white text-[10px] font-bold px-3 py-1 rounded-3xl rotate-12">¡NUEVO!</span>
                </div>
            </div>
        </div>
    </section>

    <!-- TIPOS DE SEGUROS -->
    <section id="seguros" class="max-w-7xl mx-auto px-6 py-20">
        <h2 class="text-4xl font-semibold text-center mb-12">Seguros diseñados para familias hispanas en Florida</h2>
        
        <div class="grid md:grid-cols-4 gap-6">
            <div class="bg-white border border-gray-100 rounded-3xl p-8 hover:border-[#1e40af] transition">
                <i class="fas fa-car text-5xl text-[#1e40af] mb-6"></i>
                <h4 class="font-semibold text-2xl">Seguro de Auto</h4>
                <p class="text-gray-600 mt-2">Cobertura PIP, contra huracanes y robo. Precios desde $29/mes.</p>
                <div class="mt-8 flex justify-between items-end">
                    <span class="text-xs text-emerald-600 font-medium">Popular en Miami Beach</span>
                    <button onclick="quickAutoQuote()" class="text-[#1e40af] text-sm font-medium">Cotizar ahora →</button>
                </div>
            </div>
            
            <div class="bg-white border border-gray-100 rounded-3xl p-8 hover:border-[#1e40af] transition">
                <i class="fas fa-home text-5xl text-[#1e40af] mb-6"></i>
                <h4 class="font-semibold text-2xl">Seguro de Hogar</h4>
                <p class="text-gray-600 mt-2">Protección total contra tormentas y huracanes. Incluye inundación opcional.</p>
                <div class="mt-8 flex justify-between items-end">
                    <span class="text-xs text-emerald-600 font-medium">#1 en Florida</span>
                    <button onclick="quickHomeQuote()" class="text-[#1e40af] text-sm font-medium">Cotizar ahora →</button>
                </div>
            </div>
            
            <div class="bg-white border border-gray-100 rounded-3xl p-8 hover:border-[#1e40af] transition">
                <i class="fas fa-key text-5xl text-[#1e40af] mb-6"></i>
                <h4 class="font-semibold text-2xl">Seguro de Inquilinos</h4>
                <p class="text-gray-600 mt-2">Protege tus cosas en apartamentos de Miami, Orlando o Tampa.</p>
                <div class="mt-8 flex justify-between items-end">
                    <span class="text-xs text-emerald-600 font-medium">Desde $11/mes</span>
                    <button onclick="quickRentersQuote()" class="text-[#1e40af] text-sm font-medium">Cotizar ahora →</button>
                </div>
            </div>
            
            <div class="bg-white border border-gray-100 rounded-3xl p-8 hover:border-[#1e40af] transition">
                <i class="fas fa-heart text-5xl text-[#1e40af] mb-6"></i>
                <h4 class="font-semibold text-2xl">Seguro de Vida</h4>
                <p class="text-gray-600 mt-2">Protege a tu familia. Planes simples con pago mensual.</p>
                <div class="mt-8 flex justify-between items-end">
                    <span class="text-xs text-emerald-600 font-medium">Bilingüe 24/7</span>
                    <button onclick="quickLifeQuote()" class="text-[#1e40af] text-sm font-medium">Cotizar ahora →</button>
                </div>
            </div>
        </div>
    </section>

    <!-- TESTIMONIALS -->
    <section class="bg-[#1e40af] text-white py-20">
        <div class="max-w-7xl mx-auto px-6">
            <h2 class="text-4xl font-semibold text-center mb-12">Lo que dicen nuestros vecinos hispanos en Florida</h2>
            
            <div class="grid md:grid-cols-3 gap-8">
                <div class="bg-white/10 backdrop-blur-lg rounded-3xl p-8">
                    <div class="flex gap-x-1 mb-6 text-amber-400">★★★★★</div>
                    <p class="italic">"Ahorramos $780 al año en el seguro del auto de mi esposo. El agente habló en español perfecto y nos ayudó con el huracán Irma. ¡Recomendado 100%!"</p>
                    <div class="mt-8 flex items-center gap-x-3">
                        <div class="w-9 h-9 bg-white rounded-2xl flex items-center justify-center text-[#1e40af]">🇨🇺</div>
                        <div>
                            <p class="font-medium">María López</p>
                            <p class="text-xs">Miami Beach • ZIP 33139</p>
                        </div>
                    </div>
                </div>
                
                <div class="bg-white/10 backdrop-blur-lg rounded-3xl p-8">
                    <div class="flex gap-x-1 mb-6 text-amber-400">★★★★☆</div>
                    <p class="italic">"Refiero a toda mi familia. Ya gané tres tarjetas Amazon. El proceso es súper fácil y todo en español."</p>
                    <div class="mt-8 flex items-center gap-x-3">
                        <div class="w-9 h-9 bg-white rounded-2xl flex items-center justify-center text-[#1e40af]">🇻🇪</div>
                        <div>
                            <p class="font-medium">Carlos Ramírez</p>
                            <p class="text-xs">Orlando • ZIP 32801</p>
                        </div>
                    </div>
                </div>
                
                <div class="bg-white/10 backdrop-blur-lg rounded-3xl p-8">
                    <div class="flex gap-x-1 mb-6 text-amber-400">★★★★★</div>
                    <p class="italic">"Mi seguro de hogar cubre huracanes y fue más barato que directo con la aseguradora. Gracias AseguraFL por pensar en nosotros los latinos."</p>
                    <div class="mt-8 flex items-center gap-x-3">
                        <div class="w-9 h-9 bg-white rounded-2xl flex items-center justify-center text-[#1e40af]">🇵🇷</div>
                        <div>
                            <p class="font-medium">Ana González</p>
                            <p class="text-xs">Tampa • ZIP 33607</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- BLOG TEASER -->
    <section id="blog" class="max-w-7xl mx-auto px-6 py-20 bg-white">
        <div class="flex justify-between items-end mb-8">
            <h2 class="text-4xl font-semibold">Blog en Español para Hispanos en Florida</h2>
            <a href="#" class="text-[#1e40af] font-medium flex items-center gap-x-2">Ver todos los artículos <i class="fas fa-arrow-right"></i></a>
        </div>
        
        <div class="grid md:grid-cols-3 gap-6">
            <div class="border rounded-3xl overflow-hidden">
                <div class="h-48 bg-gradient-to-br from-blue-500 to-amber-400 flex items-center justify-center text-white text-4xl">🌀</div>
                <div class="p-6">
                    <h4 class="font-semibold">¿Cómo proteger tu auto contra huracanes en Florida?</h4>
                    <p class="text-sm text-gray-500 mt-3">Consejos reales de residentes hispanos + descuentos exclusivos.</p>
                </div>
            </div>
            <div class="border rounded-3xl overflow-hidden">
                <div class="h-48 bg-gradient-to-br from-emerald-500 to-blue-500 flex items-center justify-center text-white text-4xl">📱</div>
                <div class="p-6">
                    <h4 class="font-semibold">App bilingüe: Reclama tu seguro desde el celular</h4>
                    <p class="text-sm text-gray-500 mt-3">Guía paso a paso para después de una tormenta.</p>
                </div>
            </div>
            <div class="border rounded-3xl overflow-hidden">
                <div class="h-48 bg-gradient-to-br from-amber-500 to-red-400 flex items-center justify-center text-white text-4xl">👪</div>
                <div class="p-6">
                    <h4 class="font-semibold">Seguro de vida para familias latinas: Lo que debes saber</h4>
                    <p class="text-sm text-gray-500 mt-3">Evita errores comunes y protege a tus seres queridos.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer class="bg-gray-900 text-white py-16">
        <div class="max-w-7xl mx-auto px-6 grid md:grid-cols-12 gap-y-12">
            <div class="md:col-span-4">
                <div class="flex items-center gap-x-2 mb-6">
                    <div class="w-9 h-9 bg-white rounded-2xl flex items-center justify-center text-[#1e40af] text-3xl"><i class="fas fa-shield-alt"></i></div>
                    <h1 class="logo-font text-4xl font-semibold tracking-tighter">AseguraFL</h1>
                </div>
                <p class="text-gray-400 max-w-xs">La plataforma de comparación de seguros #1 para la comunidad hispanohablante de Florida.</p>
                <p class="text-xs text-gray-500 mt-8">© 2026 AseguraFL • Todos los derechos reservados</p>
            </div>
            
            <div class="md:col-span-2">
                <h6 class="font-semibold mb-4">Plataforma</h6>
                <ul class="space-y-3 text-sm text-gray-400">
                    <li><a href="#" class="hover:text-white">Comparar cotizaciones</a></li>
                    <li><a href="#" class="hover:text-white">Programa de referidos</a></li>
                    <li><a href="#" class="hover:text-white">App móvil</a></li>
                </ul>
            </div>
            
            <div class="md:col-span-2">
                <h6 class="font-semibold mb-4">Compañías</h6>
                <ul class="space-y-3 text-sm text-gray-400">
                    <li>GEICO • Progressive</li>
                    <li>State Farm • Allstate</li>
                    <li>Kemper (bilingüe)</li>
                    <li>Security First (hogar)</li>
                </ul>
            </div>
            
            <div class="md:col-span-2">
                <h6 class="font-semibold mb-4">Recursos</h6>
                <ul class="space-y-3 text-sm text-gray-400">
                    <li><a href="#" class="hover:text-white">Blog en español</a></li>
                    <li><a href="#" class="hover:text-white">Guía de huracanes</a></li>
                    <li><a href="#" class="hover:text-white">Agentes bilingües cerca de ti</a></li>
                    <li><a href="#" class="hover:text-white">Preguntas frecuentes</a></li>
                </ul>
            </div>
            
            <div class="md:col-span-2">
                <h6 class="font-semibold mb-4">Contáctanos</h6>
                <p class="text-sm text-gray-400">(305) 555-0199<br>WhatsApp: +1 (786) 555-0123</p>
                <p class="text-xs mt-8 text-gray-400">Miami Beach, FL • Hecho con ❤️ para la comunidad hispana</p>
            </div>
        </div>
    </footer>

    <!-- REFERRAL MODAL -->
    <div onclick="if(event.target.id === 'referral-modal')hideReferralModal()" 
         id="referral-modal"
         class="hidden fixed inset-0 bg-black/70 z-[9999] flex items-center justify-center">
        <div onclick="event.stopImmediatePropagation()" 
             class="bg-white rounded-3xl max-w-lg w-full mx-4 p-8">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-3xl font-semibold text-[#1e40af]">¡Tu enlace de referido!</h3>
                <button onclick="hideReferralModal()" class="text-4xl text-gray-300 hover:text-gray-500">×</button>
            </div>
            
            <p class="text-gray-600 mb-8">Comparte este enlace con amigos y familiares en Florida. Cuando ellos obtengan una cotización y compren, tú ganas $50 (Amazon) y ellos también reciben un bono.</p>
            
            <div class="bg-gray-100 rounded-2xl p-4 flex items-center justify-between mb-8">
                <code id="referral-link" class="text-[#1e40af] font-medium break-all">https://asegurafl.com/ref/joel-miami-2026</code>
                <button onclick="copyReferralLink()" 
                        class="bg-[#1e40af] text-white px-5 py-3 rounded-2xl text-sm font-medium flex items-center gap-x-2">
                    <i class="fas fa-copy"></i> Copiar
                </button>
            </div>
            
            <div class="flex gap-x-4">
                <button onclick="shareToWhatsApp()" 
                        class="flex-1 py-4 border border-gray-300 rounded-2xl flex items-center justify-center gap-x-2">
                    <i class="fab fa-whatsapp text-2xl text-green-500"></i>
                    WhatsApp
                </button>
                <button onclick="shareToEmail()" 
                        class="flex-1 py-4 border border-gray-300 rounded-2xl flex items-center justify-center gap-x-2">
                    <i class="fas fa-envelope text-2xl"></i>
                    Email
                </button>
            </div>
            
            <p class="text-center text-xs text-gray-400 mt-8">Ya has referido 3 amigos este mes • $150 ganados 🎉</p>
        </div>
    </div>

    <!-- LOGIN MODAL (simple mock) -->
    <div onclick="if(event.target.id === 'login-modal')hideLoginModal()" 
         id="login-modal"
         class="hidden fixed inset-0 bg-black/70 z-[9999] flex items-center justify-center">
        <div onclick="event.stopImmediatePropagation()" class="bg-white rounded-3xl max-w-sm w-full mx-4 p-8">
            <h3 class="text-2xl font-semibold mb-6">Bienvenido de nuevo a AseguraFL</h3>
            <input type="email" placeholder="Correo electrónico" value="joel@example.com" 
                   class="w-full px-6 py-5 border rounded-3xl mb-4">
            <input type="password" placeholder="Contraseña" value="demo123" 
                   class="w-full px-6 py-5 border rounded-3xl mb-6">
            <button onclick="fakeLogin()" 
                    class="w-full py-5 bg-[#1e40af] text-white rounded-3xl font-semibold">Iniciar sesión</button>
            <p class="text-center text-xs mt-8 text-gray-400">¿Nuevo? <span onclick="hideLoginModal()" class="text-[#1e40af] cursor-pointer">Crea cuenta gratis en 10 segundos</span></p>
        </div>
    </div>

    <script>
        // Tailwind initialization
        function initializeTailwind() {
            return {
                config(userConfig = {}) {
                    return {
                        content: [],
                        theme: {
                            extend: {
                                colors: {
                                    primary: '#1e40af'
                                }
                            }
                        },
                        plugins: [],
                        ...userConfig,
                    }
                },
                theme: {
                    extend: {},
                },
            }
        }
        
        // Mobile menu
        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu')
            const icon = document.getElementById('menu-icon')
            if (menu.classList.contains('hidden')) {
                menu.classList.remove('hidden')
                icon.classList.replace('fa-bars', 'fa-xmark')
            } else {
                menu.classList.add('hidden')
                icon.classList.replace('fa-xmark', 'fa-bars')
            }
        }
        
        // Referral modal
        function showReferralModal() {
            document.getElementById('referral-modal').classList.remove('hidden')
            document.getElementById('referral-modal').classList.add('flex')
        }
        
        function hideReferralModal() {
            const modal = document.getElementById('referral-modal')
            modal.classList.add('hidden')
            modal.classList.remove('flex')
        }
        
        function copyReferralLink() {
            const link = document.getElementById('referral-link').textContent
            navigator.clipboard.writeText(link).then(() => {
                const btn = event.currentTarget
                const original = btn.innerHTML
                btn.innerHTML = `<i class="fas fa-check"></i> ¡Copiado!`
                setTimeout(() => { btn.innerHTML = original }, 2000)
            })
        }
        
        function shareToWhatsApp() {
            const link = document.getElementById('referral-link').textContent
            window.open(`https://wa.me/?text=¡Únete a AseguraFL y ahorra en seguros en Florida! Mi enlace: ${link}`, '_blank')
        }
        
        function shareToEmail() {
            const link = document.getElementById('referral-link').textContent
            window.location.href = `mailto:?subject=Te invito a AseguraFL&body=Hola familia! Comparte este enlace y ahorremos juntos en seguros: ${link}`
        }
        
        // Login modal
        function showLoginModal() {
            document.getElementById('login-modal').classList.remove('hidden')
            document.getElementById('login-modal').classList.add('flex')
        }
        
        function hideLoginModal() {
            const modal = document.getElementById('login-modal')
            modal.classList.add('hidden')
            modal.classList.remove('flex')
        }
        
        function fakeLogin() {
            hideLoginModal()
            const toast = document.createElement('div')
            toast.style.cssText = 'position:fixed; bottom:20px; right:20px; background:#1e40af; color:white; padding:16px 24px; border-radius:9999px; box-shadow:0 10px 15px -3px rgb(0 0 0 / 0.3);'
            toast.innerHTML = '✅ Sesión iniciada como Joel (Miami Beach)'
            document.body.appendChild(toast)
            setTimeout(() => toast.remove(), 3000)
        }
        
        // Quote simulation
        function handleQuoteSubmit(e) {
            e.preventDefault()
            
            const zip = document.getElementById('zip').value
            const type = document.getElementById('insurance-type').value
            
            // Show results
            const results = document.getElementById('quote-results')
            results.classList.remove('hidden')
            results.scrollIntoView({ behavior: 'smooth' })
            
            const grid = document.getElementById('quotes-grid')
            grid.innerHTML = ''
            
            // Mock quotes depending on type
            let companies = []
            
            if (type === 'auto') {
                companies = [
                    { name: 'GEICO', price: '42', logo: 'GE', savings: '38%' },
                    { name: 'Progressive', price: '51', logo: 'PR', savings: '29%' },
                    { name: 'State Farm', price: '67', logo: 'SF', savings: '12%' },
                    { name: 'Allstate', price: '59', logo: 'AL', savings: '21%' },
                    { name: 'Kemper', price: '37', logo: 'KM', savings: '45%' }
                ]
            } else if (type === 'hogar') {
                companies = [
                    { name: 'Security First', price: '89', logo: 'SF', savings: '41%' },
                    { name: 'State Farm', price: '112', logo: 'SF', savings: '18%' },
                    { name: 'Allstate', price: '98', logo: 'AL', savings: '27%' }
                ]
            } else {
                companies = [
                    { name: 'GEICO', price: '19', logo: 'GE', savings: '33%' },
                    { name: 'Progressive', price: '24', logo: 'PR', savings: '25%' }
                ]
            }
            
            companies.forEach(company => {
                const cardHTML = `
                <div class="quote-card bg-white border border-gray-100 rounded-3xl p-6 flex flex-col">
                    <div class="flex justify-between items-start">
                        <div class="text-3xl font-bold text-[#1e40af]">${company.logo}</div>
                        <div>
                            <div class="text-5xl font-semibold">$${company.price}</div>
                            <div class="text-xs text-gray-400">/mes</div>
                        </div>
                    </div>
                    <h4 class="font-semibold mt-6">${company.name}</h4>
                    <p class="text-emerald-600 text-sm mt-1">${company.savings} de ahorro vs tu póliza actual</p>
                    <div class="mt-auto pt-8 flex justify-between text-xs">
                        <span class="flex items-center"><i class="fas fa-check mr-1"></i> Soporte español</span>
                        <button onclick="selectQuote('${company.name}', '${company.price}')" 
                                class="bg-emerald-500 hover:bg-emerald-600 text-white px-6 py-2 rounded-2xl text-sm">Seleccionar</button>
                    </div>
                </div>`
                grid.innerHTML += cardHTML
            })
        }
        
        function selectQuote(name, price) {
            alert(`¡Excelente elección! Has seleccionado ${name} por $${price}/mes.\n\nUn agente bilingüe de AseguraFL te contactará en minutos.`)
        }
        
        function buyPolicy() {
            alert('🎉 ¡Felicidades! Tu nueva póliza está activa. Recibirás la confirmación por email y WhatsApp en español.')
        }
        
        // Quick hero quote simulation
        function simulateQuickQuote() {
            const results = document.getElementById('quote-results')
            results.classList.remove('hidden')
            document.getElementById('quotes-grid').innerHTML = `
                <div class="col-span-3 text-center py-8">
                    <div class="animate-pulse flex justify-center gap-x-8">
                        <div class="quote-card bg-white p-8 rounded-3xl w-72">GEICO — $41/mes <span class="text-emerald-500">¡45% ahorro!</span></div>
                        <div class="quote-card bg-white p-8 rounded-3xl w-72">Kemper — $36/mes <span class="text-emerald-500">Bilingüe 24/7</span></div>
                        <div class="quote-card bg-white p-8 rounded-3xl w-72">Progressive — $49/mes</div>
                    </div>
                    <button onclick="handleQuoteSubmit(new Event('submit'))" class="mt-12 text-[#1e40af] underline">Ver todas las cotizaciones completas</button>
                </div>`
            results.scrollIntoView({ behavior: 'smooth' })
        }
        
        // Quick type buttons
        function quickAutoQuote() { 
            document.getElementById('insurance-type').value = 'auto'
            document.getElementById('quote-form').scrollIntoView({ behavior: 'smooth' })
        }
        function quickHomeQuote() { 
            document.getElementById('insurance-type').value = 'hogar'
            document.getElementById('quote-form').scrollIntoView({ behavior: 'smooth' })
        }
        function quickRentersQuote() { 
            document.getElementById('insurance-type').value = 'renters'
            document.getElementById('quote-form').scrollIntoView({ behavior: 'smooth' })
        }
        function quickLifeQuote() { 
            document.getElementById('insurance-type').value = 'vida'
            document.getElementById('quote-form').scrollIntoView({ behavior: 'smooth' })
        }
        
        // Initialize everything
        window.onload = function() {
            initializeTailwind()
            console.log('%c✅ AseguraFL prototipo cargado correctamente para hispanos en Florida!', 'color:#1e40af; font-family:monospace;')
            // Easter egg for Joel
            console.log('%cHola Joel de Miami Beach 👋 Este sitio está listo para que lo publiques y empieces a referir hoy mismo.', 'color:#1e40af;')
        }
    </script>
</body>
</html>
