<script lang="ts">
    import "./layout.css";
    let { children } = $props();
</script>

<svelte:head>
    <title>ChefNia | Private Dining Experience</title>
    <!-- Asegura que la escala sea correcta en móviles -->
    <meta name="viewport" content="width=device-width, initial-scale=1">
</svelte:head>

<!-- Header: Estilo Editorial Responsive -->
<nav class="flex flex-col items-center pt-12 pb-8 md:pt-20 md:pb-16 bg-[#0a0a0a]">
    <!-- Logo: Tamaño ajustado para móvil -->
    <a href="/" class="mb-8 md:mb-12 hover:scale-[1.02] transition-transform duration-700">
        <img class="w-24 h-24 md:w-32 md:h-32 object-contain" src="/nia2.png" alt="ChefNia Logo"/>
    </a>
    
    <!-- Menú: Ajuste de gap y tamaño de letra para móviles -->
    <div class="flex flex-wrap justify-center gap-6 md:gap-12 text-[10px] md:text-[13px] uppercase tracking-[0.2em] md:tracking-[0.35em] text-zinc-300 font-bold">
        <a href="/" class="hover:text-white transition-all duration-300">Inicio</a>
        <a href="/servicios" class="hover:text-white transition-all duration-300">Servicios</a>
        <a href="/chef" class="hover:text-white transition-all duration-300">El Chef</a>
        <a href="/reservas" class="text-white border-b border-white pb-1">Reservar</a>
    </div>
</nav>

<!-- Contenido -->
<main class="bg-[#0a0a0a] min-h-[60vh] text-white px-4">
    {@render children()}
</main>

<!-- Footer: Minimalista y adaptado -->
<footer class="bg-[#0a0a0a] py-16 md:py-24 border-t border-zinc-900">
    <div class="max-w-xl mx-auto px-6 text-center flex flex-col items-center">
        <!-- Eslogan: Tamaño ajustado para que no se corte -->
        <p class="text-[9px] md:text-[10px] uppercase tracking-[0.3em] md:tracking-[0.45em] text-white font-bold mb-8 leading-relaxed">
            Alta Cocina en la Intimidad de tu Espacio
        </p>
        
        <div class="w-16 h-[0.5px] bg-zinc-700 mb-8"></div>
        
        <div class="flex flex-col gap-4">
            <a href="mailto:info@chefnia.com" class="text-[9px] md:text-[10px] text-zinc-400 hover:text-white uppercase tracking-[0.2em] transition-colors">
                info@chefnia.com
            </a>
            <p class="text-[8px] md:text-[9px] text-zinc-600 uppercase tracking-[0.2em]">
                © 2026 ChefNia · Valencia, Venezuela
            </p>
        </div>
    </div>
</footer>