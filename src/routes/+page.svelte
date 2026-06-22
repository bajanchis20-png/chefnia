<script>
    import Icon from "@iconify/svelte"
</script>

<section class="relative w-full h-[80vh] md:h-[85vh] flex items-center justify-center bg-black overflow-hidden">
    
    <!-- Video de fondo: Ajustado para cubrir bien en móvil -->
    <div class="absolute inset-0 z-0">
        <video 
            autoplay 
            loop 
            muted 
            playsinline 
            class="w-full h-full object-cover brightness-[0.4]"
        >
            <source src="/fondovideo.mp4" type="video/mp4" />
        </video>
        <div class="absolute inset-0 bg-black/40"></div>
    </div>

    <!-- Contenido Principal -->
    <div class="relative z-10 text-center flex flex-col items-center w-full px-6">
        
        <h1 class="text-4xl md:text-6xl font-bold text-white uppercase tracking-[0.2em] mb-4">
            NChef
        </h1>
        <p class="text-[10px] md:text-[12px] text-zinc-300 uppercase tracking-[0.4em] font-medium mb-12 max-w-sm">
           Privacidad absoluta, excelencia absoluta. Alta cocina en tu mesa.
        </p>
        
        <!-- Botones: Flex-col en móvil, Row en escritorio -->
        <div class="flex flex-col w-full max-w-[280px] gap-4">
            
            <!-- Botón Reservar -->
            <a href="/reservas" class="w-full py-4 text-[10px] uppercase tracking-[0.3em] font-bold text-black bg-white hover:bg-zinc-200 transition-all duration-300 shadow-lg">
                Reservar tu fecha
            </a>

            <!-- Botón Servicios -->
            <a href="/servicios" class="w-full py-4 text-[10px] uppercase tracking-[0.3em] font-bold text-white border border-white/50 hover:bg-white hover:text-black transition-all duration-300">
                Ver servicios
            </a>
            
        </div>
    </div>
</section>

<section class="py-20 md:py-24 bg-[#0a0a0a] px-6">
    <div class="max-w-4xl mx-auto text-center">
        <!-- Título -->
        <h2 class="text-2xl md:text-3xl font-light text-white uppercase tracking-[0.2em] mb-12">
            La Experiencia NChef
        </h2>

        <!-- Filosofía principal -->
        <p class="text-zinc-300 font-light leading-relaxed text-base md:text-lg italic mb-16 max-w-2xl mx-auto">
            "Elevamos el producto local a su máxima expresión. Técnica, autenticidad y exclusividad, directo a tu mesa."
        </p>

        <!-- Grid de Servicios (SEO & Conversión) -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 text-zinc-400">
            <div class="border-t border-zinc-800 pt-6">
                <h3 class="text-white font-medium mb-3">Chef Privado</h3>
                <p class="text-[13px] leading-relaxed">Alta cocina personalizada para eventos íntimos y veladas inolvidables.</p>
            </div>
            <div class="border-t border-zinc-800 pt-6">
                <h3 class="text-white font-medium mb-3">Parrilladas Premium</h3>
                <p class="text-[13px] leading-relaxed">El ritual del fuego en su máxima expresión. Cortes seleccionados y acompañamientos de autor.</p>
            </div>
            <div class="border-t border-zinc-800 pt-6">
                <h3 class="text-white font-medium mb-3">Eventos Especiales</h3>
                <p class="text-[13px] leading-relaxed">Desde cenas privadas hasta celebraciones exclusivas en la comodidad de tu hogar.</p>
            </div>
        </div>

    </div>
</section>