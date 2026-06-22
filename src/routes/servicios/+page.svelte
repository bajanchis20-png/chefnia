<section class="py-24 px-6 bg-[#0a0a0a]">
  <div class="max-w-6xl mx-auto">
    
    <h2 class="text-white text-4xl font-extralight uppercase tracking-[0.3em] text-center mb-20">
      Experiencias Privadas
    </h2>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
      
      {#each [
        {img: "/cenaintima.png", title: "Cenas Íntimas", desc: "El restaurante de 5 estrellas en tu comedor."},
        {img: "/parrilla2.jpg", title: "Parrillada con Amigos", desc: "Gourmet con cortes premium y guarniciones."},
        {img: "/bruch2.png", title: "Brunch Gourmet", desc: "Platos frescos y sofisticados para empezar el día."},
        {img: "/evento.png", title: "Eventos Especiales", desc: "Gestión integral para celebraciones exclusivas."}
      ] as service}
      
      <a href="/reservas" class="group relative h-[450px] w-full overflow-hidden block border border-zinc-800/50 hover:border-zinc-600 transition-colors duration-500">
        <!-- Imagen -->
        <img src={service.img} alt={service.title} class="w-full h-full object-cover transition-transform duration-[2000ms] ease-out group-hover:scale-110">
        
        <!-- Degradado refinado -->
        <div class="absolute inset-0 bg-gradient-to-t from-[#0a0a0a] via-[#0a0a0a]/20 to-transparent"></div>
        
        <!-- Contenido -->
        <div class="absolute bottom-0 left-0 p-10 w-full transform transition-transform duration-500">
          <h3 class="text-white text-2xl uppercase tracking-[0.2em] font-light mb-3">{service.title}</h3>
          <p class="text-zinc-400 font-light text-sm leading-relaxed mb-6 opacity-0 group-hover:opacity-100 transition-opacity duration-500">
            {service.desc}
          </p>
          
          <!-- Botón elegante -->
          <div class="flex items-center space-x-3 text-white">
            <span class="text-[10px] uppercase tracking-[0.3em] border-b border-white pb-1">
              Reservar ahora
            </span>
            <svg class="w-4 h-4 transform group-hover:translate-x-2 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1" d="M17 8l4 4m0 0l-4 4m4-4H3"></path>
            </svg>
          </div>
        </div>
      </a>
      
      {/each}
    </div>
  </div>
</section>