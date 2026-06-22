<script>
  let nombre = "";
  let fecha = "";
  let servicio = "Chef Privado";
  const numeroWhatsApp = "584120000000"; 

  function realizarReserva() {
    const mensaje = `Hola, me gustaría solicitar una reserva:%0A%0A` +
                    `👤 Cliente: ${nombre}%0A` +
                    `📅 Fecha: ${fecha}%0A` +
                    `🍽️ Servicio: ${servicio}`;
    
    const url = `https://wa.me/${numeroWhatsApp}?text=${mensaje}`;
    window.open(url, '_blank');
  }
</script>

<!-- Hero Section unificado -->
<section class="relative h-[50vh] flex items-center justify-center bg-black overflow-hidden">
  <img src="/reservas2.jpg" alt="" class="absolute w-full h-full object-cover opacity-60 scale-105">
  <div class="absolute inset-0 bg-gradient-to-t from-[#0a0a0a] via-transparent to-transparent"></div>

  <div class="relative z-10 text-center">
    <h2 class="text-zinc-500 uppercase tracking-[0.4em] text-[10px] mb-4 font-bold">Experiencia Gastronómica</h2>
    <h1 class="text-4xl md:text-6xl font-bold text-white uppercase tracking-[0.2em]">Reservas</h1>
  </div>
</section>

<!-- Formulario con tipografía consistente -->
<section class="py-20 px-6 bg-[#0a0a0a]">
  <div class="max-w-xl mx-auto">
    <div class="mb-12 text-center">
      <p class="text-zinc-300 font-light leading-relaxed text-base italic">"La cocina es el corazón del hogar, yo pongo el arte."</p>
    </div>

    <div class="bg-zinc-900/30 p-10 border border-zinc-800/60 shadow-2xl backdrop-blur-sm">
      <div class="space-y-8">
        <!-- Campo Nombre -->
        <div>
          <label class="block text-zinc-500 text-[10px] uppercase tracking-[0.3em] mb-3 font-bold">Nombre del anfitrión</label>
          <input type="text" bind:value={nombre} placeholder="Ingrese su nombre" 
                 class="w-full bg-transparent border-b border-zinc-800 py-3 text-white placeholder-zinc-700 focus:border-white outline-none transition-all duration-500">
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <!-- Campo Fecha -->
          <div>
            <label class="block text-zinc-500 text-[10px] uppercase tracking-[0.3em] mb-3 font-bold">Fecha</label>
            <input type="date" bind:value={fecha} 
                   class="w-full bg-transparent border-b border-zinc-800 py-3 text-white focus:border-white outline-none transition-all duration-500 [color-scheme:dark]">
          </div>
          
          <!-- Campo Servicio -->
          <div>
            <label class="block text-zinc-500 text-[10px] uppercase tracking-[0.3em] mb-3 font-bold">Servicio</label>
            <div class="relative">
              <select bind:value={servicio} 
                      class="w-full bg-zinc-900 border border-zinc-700 py-3 px-4 text-white text-[12px] uppercase tracking-[0.1em] focus:border-white outline-none transition-all cursor-pointer appearance-none">
                <option class="bg-black text-white p-4">Chef Privado</option>
                <option class="bg-black text-white p-4">Parrillada Premium</option>
                <option class="bg-black text-white p-4">Cena Especial en Casa</option>
                <option class="bg-black text-white p-4">Eventos Especiales</option>
              </select>
              <div class="absolute inset-y-0 right-0 flex items-center px-4 pointer-events-none text-zinc-500">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
              </div>
            </div>
          </div>
        </div>

        <!-- Botón de Envío -->
        <button on:click={realizarReserva}
                class="w-full border border-white text-white py-4 uppercase tracking-[0.3em] text-[10px] font-bold 
                       hover:bg-white hover:text-black transition-all duration-500 mt-6">
          Confirmar Solicitud
        </button>
      </div>
    </div>
  </div>
</section>