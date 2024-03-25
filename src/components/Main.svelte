<script>
  import Step from "./Step.svelte";
  import { benefits, projects } from "../lib/data";
  import Footer from "./Footer.svelte";
  import Header from "./Header.svelte";
  import Layout from "../routes/+layout.svelte";
  import Skills from "./Skills.svelte";
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
        Hi! I'm <span class="poppins text-violet-400">Alvaro</span> García
        <br />Full Stack
        <span class="poppins text-violet-400">Developer</span>
      </h2>
      <div class="flex flex-col gap-4">
        <Skills
          pre="My"
          title="programming languages stack"
          nameList={[
            "Golang",
            "Python",
            "Javascript + TypeScript",
            "C#",
            "SQL",
          ]}
        />

        <Skills
          pre="The"
          title="Frameworks and tecnhologies that I use the most"
          nameList={[
            "Fiber",
            "Gin",
            "Sveltekit",
            "Angular",
            "Linux",
            "Docker",
            "Kubernetes",
            "Pub/Sub",
          ]}
        />

        <Skills
          pre="The"
          title="databases that I use the most"
          nameList={["MongoDB", "Redis", "SQL Server", "MySQL"]}
        />

        <Skills
          pre="The"
          title="cloud services that I use the most"
          nameList={["GPC", "Redis cloud", "Mongo Atlas", "AWS"]}
        />
      </div>
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
        What am I <span class="poppins text-violet-400">currently doing</span>?
      </h3>
      <p class="text-lg pt-8">
        I am currently <span class="poppins text-violet-400"
          >seeking employment as a full stack developer</span
        >. Additionally, I am serving as the lead collaborator for an
        <span class="poppins text-violet-400">emerging startup</span> called
        "Velticare," which will be a web application dedicated to automating
        administrative healthcare services.
        <span class="poppins text-violet-400">My role</span> in this venture has
        been the
        <span class="poppins text-violet-400">full stack development</span> of
        the application, creating microservices for various needs of the
        application. I have also been involved in the development of the web
        application. I would love to show you more of my work, so I invite you
        to stay tuned for our
        <span class="poppins text-violet-400">launch on April 1st</span>. (<a
          href="https://www.velticare.com/"
          class="text-violet-400 underline">Velticare website link</a
        >) and (<a
          href="https://www.instagram.com/velticare/"
          class="text-violet-400 underline">Velticare Instagram link</a
        >)
      </p>
    </div>
  </section>
  <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
    <div class="flex flex-col gap-2 text-center">
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Some of my <span class="poppins text-violet-400">projects</span>
      </h3>
    </div>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={projects[0]}>
        <p>
          This is one of my favorite projects made with one of my favorite
          languages, Golang. This monorepo contains a client built with the
          Sveltekit framework for JS and the RESTFUL API with Go using Fiber (a
          framework for Go based on NodeJS's Express). The interpreter is
          heavily based on Swift syntax, where it is possible to interpret basic
          functionalities such as arithmetic operations, logical operations,
          variable declaration, conditionals, loops, functions, structs, and
          arrays.
        </p>
      </Step>

      <Step step={projects[1]}>
        <p>
          This is a project of a REST API with MySQL and Docker. The API was
          built using the NestJS framework. The logical, conceptual, and
          physical model was created based on a problem statement, and the
          Oracle SQL Developer Data Modeler software was used.
        </p>
      </Step>

      <Step step={projects[2]}>
        <p>
          This university project was carried out to create a database that
          allows the management of a course management system, students, and
          teachers at the University of San Carlos of Guatemala. The logical,
          conceptual, and physical model was created based on a problem
          statement, and the Oracle SQL Developer Data Modeler software was
          used. For the implementation of the database, MySQL and Docker were
          used. An important feature of this project was the use of Stored
          Procedures, Triggers, and Functions for a more efficient, secure, and
          industry-aligned working environment.
        </p>
      </Step>

      <Step step={projects[3]}>
        <p>
          This university project was carried out to create a desktop
          application that allows the creation of deterministic and
          non-deterministic finite automata. The application was built in Java
          using the NetBeans IDE. The application allows the creation of
          deterministic and non-deterministic finite automata, simulation of
          strings, and conversion of a DFA to an NFA from a grammar.
        </p>
      </Step>

      <Step step={projects[4]}>
        <p>
          This manager was developed as a monorepo, where the frontend was built
          with React JS and the backend using Fast API as the Python framework.
          The backend was deployed on an AWS VM (EC2), and an AWS bucket (S3)
          was used to store files. The application allows creating folders,
          uploading files, downloading files, deleting files and folders,
          sharing files and folders, among other functionalities.
        </p>
      </Step>
    </div>
  </section>
  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
  >
    <div
      class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        About <span class="poppins text-violet-400">me</span>
      </h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
      I am . . .
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
      The <span class="text-violet-400">Complete</span> package
    </h5>
    <div
      class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
    >
      <table class="bg-white text-slate-700 rounded text-center">
        <thead class="border-b border-solid border-slate-200">
          <tr>
            <th></th>
            <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
            <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
            <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
            <th class="bg-violet-700 text-white whitespace-nowrap p-4 px-8"
              >Me</th
            >
          </tr>
        </thead>
        <tbody>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
              >Dedication</td
            >
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
              >Logical Thinking</td
            >
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr>
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
              >Soft Skills</td
            >
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr class="border-t border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
              >Self-taught</td
            >
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr class="border-t border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
              >Programming Skills</td
            >
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
      <p>Scroll down to se more &rarr;</p>
    </div>
    <p class="mx-auto text-lg">So why not invest in me?</p>

  </section>
</main>
