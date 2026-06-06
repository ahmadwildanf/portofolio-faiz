<script setup>
import { ref } from 'vue'
import foto from './assets/foto.png'

const selectedProject = ref(null)
const currentImageIndex = ref(0)

const openProject = (project) => {
  selectedProject.value = project
  currentImageIndex.value = 0
}

const closeProject = () => {
  selectedProject.value = null
}

const nextImage = () => {
  if (
    currentImageIndex.value <
    selectedProject.value.images.length - 1
  ) {
    currentImageIndex.value++
  } else {
    currentImageIndex.value = 0
  }
}

const prevImage = () => {
  if (currentImageIndex.value > 0) {
    currentImageIndex.value--
  } else {
    currentImageIndex.value =
      selectedProject.value.images.length - 1
  }
}

const projects = [
  {
    id: 1,
    name: 'Website Klinik Kecantikan',
    description: 'Website Klinik Kecantikan Laquisha Medcare',
    tech: 'CodeIgniter 4, MySQL, Bootstrap',
    images: [
      '/klinik1.png',
      '/klinik2.png',
      '/klinik3.png',
      '/klinik4.png',
      '/klinik5.png',
      '/klinik6.png',
      '/klinik7.png',
      '/klinik8.png',
    ]
  },
  {
    id: 2,
    name: 'Website Purchasing Jababeka',
    description: 'Maintenance purchasing system',
    tech: 'Laravel, Javascript, MySQL',
    images: [
      '/purchasing1.png',
      '/purchasing2.png',
      '/purchasing3.png',
      '/purchasing4.png',
      '/purchasing5.png',
      '/purchasing6.png',
      '/purchasing7.png',
      '/purchasing8.png'

    ]
  },
  {
    id: 3,
    name: 'Website Company Profile DCBattery',
    description: 'Maintenance company profile DCBattery',
    tech: 'React.js, Node.js, MongoDB, Alibaba Cloud',
    images: [
      '/dcbattery1.png',
      '/dcbattery2.png',
      '/dcbattery3.png',
      '/dcbattery4.png',
      '/dcbattery5.png',
      '/dcbattery6.png'
    ]
  }
]
</script>

<template>
  <div class="bg-gray-100 min-h-screen">

    <!-- Navbar -->
    <nav class="bg-white shadow fixed w-full z-50">
      <div class="max-w-6xl mx-auto px-6 py-4 flex justify-between">

        <h1 class="font-bold text-xl text-blue-600">
          Portfolio
        </h1>

        <div class="space-x-5 hidden md:block">
          <a href="#home">Home</a>
          <a href="#about">About</a>
          <a href="#experience">Experience</a>
          <a href="#skills">Skills</a>
          <a href="#project">Projects</a>
          <a href="#contact">Contact</a>
        </div>

      </div>
    </nav>

    <!-- Hero -->
    <section
      id="home"
      class="h-screen flex items-center justify-center bg-gradient-to-r from-blue-600 to-indigo-700 text-white"
    >
      <div class="text-center">

        <img
          :src="foto"
          class="w-40 h-40 rounded-full mx-auto border-4 border-white object-cover shadow-lg"
        />

        <h1 class="text-5xl font-bold mt-6">
          Achmad Wildan Alfarizky
        </h1>

        <p class="text-xl mt-4">
          Web Developer | Full Stack Developer
        </p>

        <a
          href="#project"
          class="inline-block mt-8 bg-white text-blue-600 px-6 py-3 rounded-lg font-semibold hover:bg-gray-200"
        >
          View Portfolio
        </a>

        <div class="mt-6 flex flex-wrap justify-center gap-4">

  <a
    href="/cv-achmad-wildan.pdf"
    download
    class="bg-green-500 hover:bg-green-600 text-white px-6 py-3 rounded-lg font-semibold"
  >
    📄 Download CV
  </a>

</div>

      </div>
    </section>

    <!-- About -->
    <section
      id="about"
      class="max-w-6xl mx-auto py-20 px-6"
    >
      <h2 class="text-4xl font-bold text-center mb-10">
        About Me
      </h2>

      <div class="bg-white p-8 rounded-2xl shadow">

        <p class="leading-relaxed text-gray-700">
          Saya memiliki pengalaman di bidang IT Support,
          Programmer dan Web Developer. Berpengalaman
          dalam pengembangan aplikasi web menggunakan
          PHP, CodeIgniter, Laravel, React.js, Vue.js,
          Node.js, MySQL, MongoDB serta deployment
          menggunakan Alibaba Cloud.
        </p>

      </div>
    </section>

    <!-- Experience -->
    <section
      id="experience"
      class="bg-white py-20"
    >
      <div class="max-w-6xl mx-auto px-6">

        <h2 class="text-4xl font-bold text-center mb-12">
          Experience
        </h2>

        <div class="space-y-8">

          <div class="border-l-4 border-blue-500 pl-6">
            <h3 class="font-bold text-xl">
              Web Developer Intern
            </h3>

            <p class="text-gray-500">
              PT Dharma Controlcable Indonesia
            </p>

            <ul class="list-disc ml-5 mt-3">
              <li>Maintenance Website Company Profile</li>
              <li>Analisis React.js</li>
              <li>Deployment Alibaba Cloud</li>
              <li>Integrasi MongoDB</li>
            </ul>
          </div>

          <div class="border-l-4 border-blue-500 pl-6">
            <h3 class="font-bold text-xl">
              Programmer Intern
            </h3>

            <p class="text-gray-500">
              PT Kawasan Industri Jababeka Tbk
            </p>

            <ul class="list-disc ml-5 mt-3">
              <li>Membuat Website Training</li>
              <li>Maintenance Website Purchasing</li>
              <li>Mengaplikasikan ke server lokal</li>
            </ul>
          </div>

          <div class="border-l-4 border-blue-500 pl-6">
            <h3 class="font-bold text-xl">
              IT Support Intern
            </h3>

            <p class="text-gray-500">
              PT Sucofindo Cirebon
            </p>

            <ul class="list-disc ml-5 mt-3">
              <li>Troubleshooting Hardware</li>
              <li>Troubleshooting Software</li>
              <li>Maintenance Jaringan</li>
            </ul>
          </div>

        </div>

      </div>
    </section>

    <!-- Skills -->
    <section
      id="skills"
      class="py-20 bg-gray-100"
    >
      <div class="max-w-6xl mx-auto px-6">

        <h2 class="text-4xl font-bold text-center mb-10">
          Skills
        </h2>

        <div class="grid md:grid-cols-3 gap-5">

          <div class="bg-white p-4 rounded-xl shadow text-center">PHP</div>
          <div class="bg-white p-4 rounded-xl shadow text-center">CodeIgniter 4</div>
          <div class="bg-white p-4 rounded-xl shadow text-center">Laravel</div>
          <div class="bg-white p-4 rounded-xl shadow text-center">React.js</div>
          <div class="bg-white p-4 rounded-xl shadow text-center">Vue.js</div>
          <div class="bg-white p-4 rounded-xl shadow text-center">Node.js</div>
          <div class="bg-white p-4 rounded-xl shadow text-center">MySQL</div>
          <div class="bg-white p-4 rounded-xl shadow text-center">MongoDB</div>
          <div class="bg-white p-4 rounded-xl shadow text-center">Alibaba Cloud</div>

        </div>

        <section class="py-20 bg-white">
  <div class="max-w-6xl mx-auto px-6">

    <h2 class="text-4xl font-bold text-center mb-10">
      Certificates
    </h2>

    <div class="grid md:grid-cols-3 gap-6">

      <a
        href="/sertifikat magang jababeka.pdf"
        target="_blank"
        class="bg-gray-100 p-6 rounded-xl shadow hover:shadow-lg"
      >
        <h3 class="font-bold">
          MSIB Batch 6
        </h3>

        <p class="text-gray-600 mt-2">
          PT Kawasan Industri Jababeka Tbk
        </p>
      </a>

      <a
        href="/sertifikat BNSP.pdf"
        target="_blank"
        class="bg-gray-100 p-6 rounded-xl shadow hover:shadow-lg"
      >
        <h3 class="font-bold">
          Analisis Program
        </h3>

        <p class="text-gray-600 mt-2">
          Sertifikat Kompetensi BNSP
        </p>
      </a>

      <a
        href="/sertifikat maganghub.pdf"
        target="_blank"
        class="bg-gray-100 p-6 rounded-xl shadow hover:shadow-lg"
      >
        <h3 class="font-bold">
         MagangHub Batch 1
        </h3>

        <p class="text-gray-600 mt-2">
          PT DharmaControlCable Indonesia
        </p>
      </a>

    </div>

  </div>
</section>

      </div>
    </section>

   <!-- Projects -->
<section
  id="project"
  class="py-20"
>
  <div class="max-w-6xl mx-auto px-6">

    <h2 class="text-4xl font-bold text-center mb-12">
      My Projects
    </h2>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

      <div
        v-for="project in projects"
        :key="project.id"
        class="bg-white rounded-2xl shadow-lg overflow-hidden hover:-translate-y-2 hover:shadow-2xl transition-all duration-300 cursor-pointer"
        @click="openProject(project)"
      >

        <img
          :src="project.images[0]"
          :alt="project.name"
          class="w-full h-52 object-cover"
        />

        <div class="p-5">

          <h3 class="font-bold text-xl mb-2">
  {{ project.name }}
</h3>

<p class="text-gray-600 text-sm mb-2">
  {{ project.description }}
</p>

<p class="text-blue-600 text-sm font-medium mb-4">
  {{ project.tech }}
</p>

          <button
            class="bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition"
          >
            View Gallery
          </button>

        </div>

      </div>

    </div>

  </div>
</section>

    <!-- Modal Slider -->
    <div
      v-if="selectedProject"
      class="fixed inset-0 bg-black/80 flex items-center justify-center z-50 p-4"
    >
      <div class="bg-white rounded-2xl p-6 max-w-5xl w-full">

        <div class="flex justify-between items-center mb-5">
          <h2 class="text-2xl font-bold">
            {{ selectedProject.name }}
          </h2>

          <button
            @click="closeProject"
            class="bg-red-500 text-white px-4 py-2 rounded"
          >
            Close
          </button>
        </div>

        <div class="relative">

          <img
            :src="selectedProject.images[currentImageIndex]"
            class="w-full max-h-[70vh] object-contain rounded-xl"
          />

          <button
            @click="prevImage"
            class="absolute left-2 top-1/2 -translate-y-1/2 bg-white rounded-full shadow w-12 h-12 text-xl"
          >
            ❮
          </button>

          <button
            @click="nextImage"
            class="absolute right-2 top-1/2 -translate-y-1/2 bg-white rounded-full shadow w-12 h-12 text-xl"
          >
            ❯
          </button>

        </div>

        <div class="text-center mt-4 text-gray-600">
          {{ currentImageIndex + 1 }} /
          {{ selectedProject.images.length }}
        </div>

        <div class="flex gap-2 mt-5 overflow-x-auto">

          <img
            v-for="(img,index) in selectedProject.images"
            :key="index"
            :src="img"
            @click="currentImageIndex = index"
            class="w-24 h-16 object-cover rounded cursor-pointer border-2"
            :class="
              currentImageIndex === index
                ? 'border-blue-500'
                : 'border-transparent'
            "
          />

        </div>

      </div>
    </div>

    <!-- Contact -->
<section
  id="contact"
  class="bg-gradient-to-b from-white to-gray-100 py-24"
>
  <div class="max-w-6xl mx-auto px-6">

    <h2 class="text-5xl font-bold text-center mb-6">
      Contact Me
    </h2>

    <p class="text-center text-xl text-gray-600 mb-16">
      Mari berdiskusi mengenai project, peluang kerja,
      atau kolaborasi pengembangan website.
    </p>

    <div class="grid md:grid-cols-3 gap-8">

      <!-- Email -->
      <div
        class="bg-white rounded-3xl shadow-lg p-10 text-center hover:-translate-y-2 hover:shadow-2xl transition duration-300"
      >

        <i
          class="fa-solid fa-envelope text-6xl text-red-500 mb-6"
        ></i>

        <h3 class="text-2xl font-bold mb-4">
          Email
        </h3>

        <a
          href="mailto:awildan170@gmail.com"
          class="text-lg text-gray-600 hover:text-blue-600"
        >
          awildan170@gmail.com
        </a>

      </div>

      <!-- WhatsApp -->
      <div
        class="bg-white rounded-3xl shadow-lg p-10 text-center hover:-translate-y-2 hover:shadow-2xl transition duration-300"
      >

        <i
          class="fa-brands fa-whatsapp text-6xl text-green-500 mb-6"
        ></i>

        <h3 class="text-2xl font-bold mb-4">
          WhatsApp
        </h3>

        <a
          href="https://wa.me/62895337080857"
          target="_blank"
          class="text-lg text-gray-600 hover:text-green-600"
        >
          0895337080857
        </a>

      </div>

      <!-- Location -->
      <div
        class="bg-white rounded-3xl shadow-lg p-10 text-center hover:-translate-y-2 hover:shadow-2xl transition duration-300"
      >

        <i
          class="fa-solid fa-location-dot text-6xl text-blue-500 mb-6"
        ></i>

        <h3 class="text-2xl font-bold mb-4">
          Location
        </h3>

        <p class="text-lg text-gray-600">
          Cirebon, Jawa Barat
        </p>

      </div>

    </div>

  </div>
</section>

    <footer class="bg-gray-900 text-white text-center py-5">
      © 2026 Achmad Wildan Alfarizky
    </footer>

  </div>
</template>