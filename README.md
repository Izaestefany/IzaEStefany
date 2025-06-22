## Hi there 👋

<!--
**Izaestefany/IzaEStefany** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portafolio Interactivo</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
        }
        .hotspot {
            position: absolute;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.9);
            color: #4f46e5;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            border: 2px solid white;
        }
        .hotspot:hover {
            transform: scale(1.15);
            background-color: #4f46e5;
            color: white;
        }
        .hotspot-pulse {
            animation: pulse 2s infinite;
        }
        @keyframes pulse {
            0% {
                box-shadow: 0 0 0 0 rgba(79, 70, 229, 0.7);
            }
            70% {
                box-shadow: 0 0 0 20px rgba(79, 70, 229, 0);
            }
            100% {
                box-shadow: 0 0 0 0 rgba(79, 70, 229, 0);
            }
        }
        .modal {
            transition: opacity 0.3s ease;
        }
    </style>
</head>
<body class="bg-gray-100 flex items-center justify-center min-h-screen p-4">

    <!-- Contenedor Principal -->
    <div class="relative w-full max-w-lg mx-auto text-center">
        
        <!-- Encabezado -->
        <div class="mb-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-800">Tu Nombre Aquí</h1>
            <p class="text-lg text-gray-600 mt-2">Haz clic en mis servicios para saber más</p>
        </div>

        <!-- Contenedor de la Imagen y Hotspots -->
        <div class="relative inline-block">
            <!-- Imagen de Avatar -->
            <!-- IMPORTANTE: Reemplaza el 'src' con el enlace a tu propia imagen de avatar -->
            <img 
              src="https://placehold.co/400x400/e2e8f0/4a5568?text=Tu+Avatar+Aqu%C3%AD" 
              alt="Avatar animado personal" 
              class="rounded-full w-64 h-64 md:w-80 md:h-80 object-cover shadow-2xl border-8 border-white"
              onerror="this.onerror=null;this.src='https://placehold.co/400x400/e0e0e0/757575?text=Error+cargando+imagen';"
            >
            
            <!-- Hotspot 1: Redacción Creativa -->
            <button class="hotspot hotspot-pulse" style="top: 10%; left: 0%;" data-modal="modal-redaccion">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15.232 5.232l3.536 3.536m-2.036-5.036a2.5 2.5 0 113.536 3.536L6.5 21.036H3v-3.536L16.732 3.732z" /></svg>
            </button>

            <!-- Hotspot 2: Diseño de Imágenes -->
            <button class="hotspot hotspot-pulse" style="top: 40%; right: -10%;" data-modal="modal-diseno">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z" /></svg>
            </button>

            <!-- Hotspot 3: Servicios Administrativos -->
            <button class="hotspot hotspot-pulse" style="bottom: 10%; left: 0%;" data-modal="modal-admin">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" /></svg>
            </button>
        </div>
    </div>

    <!-- Modales (Ocultos por defecto) -->
    <!-- Modal para Redacción Creativa -->
    <div id="modal-redaccion" class="modal fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center p-4 hidden opacity-0">
        <div class="bg-white rounded-lg shadow-xl w-full max-w-md p-6 relative transform transition-all scale-95">
            <button class="close-modal absolute top-4 right-4 text-gray-500 hover:text-gray-800">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" /></svg>
            </button>
            <h2 class="text-2xl font-bold text-indigo-600 mb-4">Redacción Creativa</h2>
            <p class="text-gray-700">Transformo ideas en palabras que conectan, inspiran y venden. Desde storytelling para marcas hasta contenido para blogs y redes sociales, creo textos que dejan huella y cumplen objetivos.</p>
        </div>
    </div>

    <!-- Modal para Diseño de Imágenes -->
    <div id="modal-diseno" class="modal fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center p-4 hidden opacity-0">
        <div class="bg-white rounded-lg shadow-xl w-full max-w-md p-6 relative transform transition-all scale-95">
            <button class="close-modal absolute top-4 right-4 text-gray-500 hover:text-gray-800">
                 <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" /></svg>
            </button>
            <h2 class="text-2xl font-bold text-indigo-600 mb-4">Diseño de Imágenes</h2>
            <p class="text-gray-700">Creo soluciones visuales impactantes para tu marca. Diseño de logos, banners, posts para redes sociales y cualquier material gráfico que necesites para destacar y comunicar tu mensaje de forma efectiva.</p>
        </div>
    </div>

    <!-- Modal para Servicios Administrativos -->
    <div id="modal-admin" class="modal fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center p-4 hidden opacity-0">
        <div class="bg-white rounded-lg shadow-xl w-full max-w-md p-6 relative transform transition-all scale-95">
            <button class="close-modal absolute top-4 right-4 text-gray-500 hover:text-gray-800">
                 <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" /></svg>
            </button>
            <h2 class="text-2xl font-bold text-indigo-600 mb-4">Servicios Administrativos</h2>
            <p class="text-gray-700">Optimizo tu tiempo para que te enfoques en crecer. Ofrezco soporte administrativo remoto, gestión de agenda, organización de documentos y atención al cliente, garantizando eficiencia y profesionalismo.</p>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // Selecciona todos los hotspots y modales
            const hotspots = document.querySelectorAll('.hotspot');
            const modals = document.querySelectorAll('.modal');
            const closeButtons = document.querySelectorAll('.close-modal');

            // Función para abrir un modal
            const openModal = (modalId) => {
                const modal = document.getElementById(modalId);
                if (modal) {
                    modal.classList.remove('hidden');
                    setTimeout(() => {
                        modal.classList.remove('opacity-0');
                        modal.querySelector('div').classList.remove('scale-95');
                    }, 10);
                }
            };

            // Función para cerrar un modal
            const closeModal = (modal) => {
                modal.classList.add('opacity-0');
                modal.querySelector('div').classList.add('scale-95');
                setTimeout(() => {
                    modal.classList.add('hidden');
                }, 300); // Coincide con la duración de la transición
            };

            // Añade evento de clic a cada hotspot
            hotspots.forEach(hotspot => {
                hotspot.addEventListener('click', () => {
                    const modalId = hotspot.getAttribute('data-modal');
                    openModal(modalId);
                });
            });

            // Añade evento de clic a cada botón de cierre
            closeButtons.forEach(button => {
                button.addEventListener('click', () => {
                    const modal = button.closest('.modal');
                    closeModal(modal);
                });
            });

            // Cierra el modal si se hace clic fuera del contenido
            modals.forEach(modal => {
                modal.addEventListener('click', (e) => {
                    if (e.target === modal) {
                        closeModal(modal);
                    }
                });
            });
            
            // Cierra el modal con la tecla Escape
            document.addEventListener('keydown', (e) => {
                if (e.key === "Escape") {
                    modals.forEach(modal => {
                        if (!modal.classList.contains('hidden')) {
                            closeModal(modal);
                        }
                    });
                }
            });
        });
    </script>
</body>
</html>
