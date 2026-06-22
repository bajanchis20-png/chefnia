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
            ChefNia
        </h1>
        <p class="text-[10px] md:text-[12px] text-zinc-300 uppercase tracking-[0.4em] font-medium mb-12 max-w-sm">
            Alta cocina en la intimidad de tu espacio.
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
    <div class="max-w-3xl mx-auto text-center">
        <h2 class="text-xl md:text-2xl font-light text-zinc-100 uppercase tracking-[0.2em] mb-8">
            La Filosofía de ChefNia
        </h2>
        <p class="text-zinc-400 font-light leading-relaxed text-[13px] md:text-[15px] italic">
            "Combinamos la técnica culinaria más refinada con ingredientes locales para ofrecerte una experiencia única,, directamente en tu propia mesa."
        </p>
    </div>
</section>