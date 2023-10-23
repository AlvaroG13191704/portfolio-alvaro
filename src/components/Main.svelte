<script>
  import Step from "./Step.svelte";
  import { benefits, projects } from "../lib/data"
  import Footer from "./Footer.svelte";
  import Header from "./Header.svelte";
  import Layout from "../routes/+layout.svelte";


</script>

<main class="flex flex-col flex-1 p-4">
  <section
      id="introPage"
      class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
  >
      <div
          class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
      >
          <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
              Hi! Soy <span class="poppins text-violet-400">Alvaro</span> García
              <br />Backend
              <span class="poppins text-violet-400">Developer</span>
          </h2>
          <p class="text-base sm:text-lg md:text-xl">
            Mis <span class="text-violet-400"> tecnologías favoritas</span> son Golang , Python, Javascript y Java. 
            MySQL, MongoDB, Redis, Docker, GCP, AWS, Git y Linux.
          </p>
          <!-- <button
              class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
          >
              <div
                  class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
              />
              <h4 class="relative z-9">Date un toque &rarr;</h4>
          </button> -->
      </div>
      <div class="relative shadow-2xl grid place-items-center">
          <img
              src={"images/profile.png"}
              alt="Zetane Engine"
              class="object-cover z-[2] max-h-[70vh]"
          />
      </div>
  </section>
  <!-- Section to add what I'm doing currently-->
  <section class="py-20 lg:py-20 flex flex-col">
    <div class="flex flex-col gap-2 text-center">
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            ¿Qué <span class="poppins text-violet-400">hago</span> actualmente?
        </h3>
        <p class="text-lg pt-8">
            Actualmente me encuentro <span class="poppins text-violet-400">en busca de trabajo como desarrollador backend</span>. Además, estoy siendo colaborador principal de una 
            <span class="poppins text-violet-400">empresa emergente (startup) llamado “Velticare”</span> la cual será una aplicación web dedicada a la automatización de servicios 
            administrativos de salud, por el momento nos encontramos en fase demo haciendo pruebas con 
            un grupo selectivo de doctores. <span class="poppins text-violet-400">Mi rol</span> en este emprendimiento ha sido el <span class="poppins text-violet-400">desarrollo backend</span> de la aplicación creando 
            microservicios para diferentes necesidades de la aplicación, también he sido participe de la integración de funcionalidades 
            para el frontend. Me gustaría enseñarte más de mi trabajo en los diferentes lenguajes y tecnologías que se manejan, 
            pero <span class="poppins text-violet-400">por políticas internas</span>, no puedo compartir mi trabajo,
            unicamente antiguos repositorios que ya no tienen un uso significativo.<span class="poppins text-violet-400">Pronto proporcionaremos más información.</span>  
        </p>

    </div>
  </section>
  <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
      <div class="flex flex-col gap-2 text-center">
          <h6 class="text-large sm:text-xl md:text-2xl">
              Algunos de mis proyectos más interesantes.
          </h6>
          <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
              Curios@ <span class="poppins text-violet-400">de ver </span> mi trabajo?
          </h3>
      </div>
      <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
          <Step step={projects[0]}>
              <p>
                Este es uno de mis proyectos favoritos hecho con uno de mis lenguajes favoritos, Golang, este monorepo contiene un cliente hecho con el framework Sveltekit para JS y el RESTFUL API con Go utilizando Fiber (framework para Go basado en Express de NodeJS). El intérprete se basa fuertemente en la sintaxis de Switf, donde es posible interpretar las funcionalidades básicas, como lo son las operaciones aritmeticas, operaciones logicas, declaracion de variables, condicionales, ciclos, funciones, structs y vectores.
              </p>
          </Step>
          <Step step={projects[1]}>
              <p>
                Este es un proyecto de una API REST con MySQL y Docker, el api fue hecha con el framework NestJS. El modelo lógico, conceptual y físico fue creado a partir del planteamiento de un problema y se utilizó el software Oracle SQL Developer Data Modeler.
              </p>
          </Step>
          <Step step={projects[2]}>
              <p>
                Este proyecto universitario fue realizado con el fin de crear una base de datos que permita el manejo de un sistema de gestión de cursos, estudiantes y docentes en la Universidad de San Carlos de Guatemala. El modelo lógico, conceptual y físico fue creado a partir del planteamiento de un problema y se utilizó el software Oracle SQL Developer Data Modeler. Para la implementación de la base de datos se utilizó MySQL y Docker. Una caracteristica importante de este proyecto fue el uso de Procedimientos Almacenados, Triggers y Funciones para un entorno de trabajo más eficiente, seguro y apegado al mundo laboral.
              </p>
          </Step>
          <Step step={projects[3]}>
            <p>
                Este proyecto universitario fue realizado con el fin de crear una aplicación de escritorio que permita la creación de autómatas finitos deterministas y no deterministas. La aplicación fue hecha en Java y se utilizó el IDE NetBeans. La aplicación permite la creación de autómatas finitos deterministas y no deterministas, la simulación de cadenas, la conversión de un AFD a un AFND a partir de una gramática. 
            </p>
        </Step>
        <Step step={projects[4]}>
            <p>
                Este gestor fue desarrollado como un monorepo, donde el frontend hecho con react js y el backend utilizando Fast API como framework de python. El backend se desplego en una VM de AWS (EC2) y se utilizó un bucket de AWS (S3) para almacenar los archivos. La aplicación permite la creación de carpetas, subir archivos, descargar archivos, eliminar archivos y carpetas, compartir archivos y carpetas, entre otras funcionalidades.
            </p>
        </Step>
        <Step step={projects[5]}>
            <p>
                Este microservico fue uno de los primeros creados para el proyecto velticare, el cual fue desarrollado con el framework Fast API para python, este microservicio utiliza docker para crear contenedores que luego fueron desplegados en GCP Run Este microservicio permite el manejo de consultas y archivos generados por los doctores de velticare.
            </p>
        </Step>
      </div>
  </section>
  <section
      id="about"
      class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
  >
      <!-- <div class="z-[-1] bg-violet-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div> -->
      <div
          class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
      >
          <h6 class="text-large sm:text-xl md:text-2xl">
                Más cosas sobre mi.
          </h6>
          <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
              Un poco <span class="poppins text-violet-400">sobre</span> mi.
          </h3>
      </div>
      <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
          Yo soy . . .
      </p>
      <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
          {#each benefits as benefit, index}
              <div class="flex gap-6 sm:gap-8">
                  <p
                      class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                  >
                      0{index + 1}
                  </p>
                  <div class="flex flex-col gap-6 sm:gap-8">
                      <h3 class="text-2xl sm:text-3xl md:text-5xl">
                          {benefit.name}
                      </h3>
                      <p>{benefit.description}</p>
                  </div>
              </div>
          {/each}
      </div>
      <h5 class={" text-2xl sm:text-3xl font-semibold text-center poppins "}>
          El <span class="text-violet-400">Paquete</span> completo
      </h5>
      <div
          class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
      >
          <table class="bg-white text-slate-700 rounded text-center">
              <thead class={"border-b border-solid border-slate-200  "}>
                  <tr class="">
                      <th />
                      <th class="whitespace-nowrap p-2 px-4">Candidato #1</th>
                      <th class="whitespace-nowrap p-2 px-4">Candidato #2</th>
                      <th class="whitespace-nowrap p-2 px-4">Candidato #3</th>
                      <th
                          class="bg-violet-700 text-white whitespace-nowrap p-4 px-8"
                          >Yo</th
                      >
                  </tr>
              </thead>
              <tbody>
                  <tr class="border-b border-solid border-slate-200">
                      <td
                          class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                          >Dedicación</td
                      >
                      <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                      <td><i class="fa-solid fa-check text-slate-500" /></td>
                      <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                      <td><i class="fa-solid fa-check text-green-500" /></td>
                  </tr>
                  <tr class="border-b border-solid border-slate-200">
                      <td
                          class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                          >Pensamiento lógico</td
                      >
                      <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                      <td><i class="fa-solid fa-check text-slate-500" /></td>
                      <td><i class="fa-solid fa-check text-slate-500" /></td>
                      <td><i class="fa-solid fa-check text-green-500" /></td>
                  </tr>
                  <tr>
                      <td
                          class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                          >Habilidades blandas</td
                      >
                      <td><i class="fa-solid fa-check text-slate-500" /></td>
                      <td><i class="fa-solid fa-check text-slate-500" /></td>
                      <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                      <td><i class="fa-solid fa-check text-green-500" /></td>
                  </tr>
                  <tr class="border-t border-solid border-slate-200">
                      <td
                          class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                          >Autodidacta</td
                      >
                      <td><i class="fa-solid fa-check text-slate-500" /></td>
                      <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                      <td><i class="fa-solid fa-check text-slate-500" /></td>
                      <td><i class="fa-solid fa-check text-green-500" /></td>
                  </tr>
                  <tr class="border-t border-solid border-slate-200">
                    <td
                        class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                        >Habilidades de programación</td
                    >
                    <td><i class="fa-solid fa-check text-slate-500" /></td>
                    <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-green-500" /></td>
                </tr>
              </tbody>
          </table>
      </div>
      <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
          <p>Baja para ver más &rarr;</p>
      </div>
      <p class="mx-auto text-lg">Entonces ¿Por qué no invertir en mi?</p>
  </section>
</main>