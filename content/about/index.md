---
title: "Sobre mí"
description: "Conoce a tu profesor de física y química."
summary: "description"
date: 2025-12-13
layout: "simple"     # <--- ESTA ES LA CLAVE
showTableOfContents: false
---


<div class="text-center mt-6">

## ¡Hola! Soy Juan

Soy profesor de Física y Química. He creado esta web para que mis alumnos tengan acceso a todo el material que voy creando.

</div>

<div class="my-10"></div> 

### Mi trayectoria

* 🎓 Graduado en Física
* 🏫 Máster en Formación del Profesorado
* 💻 Profesor en activo durante

<div class="flex flex-wrap justify-center gap-4 my-8 font-sans">    
    <div class="flex flex-col items-center p-4 bg-white dark:bg-gray-800 rounded-xl shadow-md border border-gray-200 dark:border-gray-700 min-w-[80px]">
        <span id="count-days" class="text-3xl font-bold text-blue-600 dark:text-blue-400 font-mono">0</span>
        <span class="text-xs uppercase tracking-wider text-gray-500 mt-1">Días</span>
    </div>
    <div class="flex flex-col items-center p-4 bg-white dark:bg-gray-800 rounded-xl shadow-md border border-gray-200 dark:border-gray-700 min-w-[80px]">
        <span id="count-hours" class="text-3xl font-bold text-blue-600 dark:text-blue-400 font-mono">00</span>
        <span class="text-xs uppercase tracking-wider text-gray-500 mt-1">Horas</span>
    </div>
    <div class="flex flex-col items-center p-4 bg-white dark:bg-gray-800 rounded-xl shadow-md border border-gray-200 dark:border-gray-700 min-w-[80px]">
        <span id="count-minutes" class="text-3xl font-bold text-blue-600 dark:text-blue-400 font-mono">00</span>
        <span class="text-xs uppercase tracking-wider text-gray-500 mt-1">Min.</span>
    </div>
    <div class="flex flex-col items-center p-4 bg-white dark:bg-gray-800 rounded-xl shadow-md border border-gray-200 dark:border-gray-700 min-w-[80px]">
        <span id="count-seconds" class="text-3xl font-bold text-red-500 dark:text-red-400 font-mono">00</span>
        <span class="text-xs uppercase tracking-wider text-gray-500 mt-1">Seg.</span>
    </div>
</div>

<script>
    (function() {
        // -------------------------------------------------
        // CONFIGURACIÓN: CAMBIA LA FECHA AQUÍ
        // Formato: AÑO, MES (0=Enero, 11=Diciembre), DÍA
        // Ejemplo: 2015, 8, 15 (15 de Septiembre de 2015)
        // -------------------------------------------------
        const fechaInicio = new Date(2023, 8, 1, 8, 0, 0).getTime(); 

        function actualizarContador() {
            const ahora = new Date().getTime();
            const diferencia = ahora - fechaInicio;

            // Cálculos matemáticos
            const dias = Math.floor(diferencia / (1000 * 60 * 60 * 24));
            const horas = Math.floor((diferencia % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutos = Math.floor((diferencia % (1000 * 60 * 60)) / (1000 * 60));
            const segundos = Math.floor((diferencia % (1000 * 60)) / 1000);

            // Actualizar el HTML
            document.getElementById("count-days").innerText = dias;
            document.getElementById("count-hours").innerText = horas < 10 ? "0" + horas : horas;
            document.getElementById("count-minutes").innerText = minutos < 10 ? "0" + minutos : minutos;
            document.getElementById("count-seconds").innerText = segundos < 10 ? "0" + segundos : segundos;
        }

        // Actualizar cada segundo
        setInterval(actualizarContador, 1000);
        actualizarContador(); // Ejecutar una vez al inicio para no esperar 1s
    })();
</script>




### ¿Qué encontrarás aquí?
En esta web recopilo mis apuntes personales, ejercicios resueltos y simulaciones interactivas para ayudarme a apreHender.

<div class="flex justify-center my-8">
  <img 
    src="profe.jpg" 
    alt="Foto del profesor" 
    class="w-48 h-48 rounded-full object-cover shadow-xl border-4 border-blue-100 dark:border-blue-900"
  >
</div>

{{< button href="mailto:tuemail@ejemplo.com" target="_blank" >}}
📧 Contacta conmigo
{{< /button >}}