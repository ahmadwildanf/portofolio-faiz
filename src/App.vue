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
          <a href="#education">Education</a>
          <a href="#certificates">Certificates</a>
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
  I am a dedicated Web Developer with experience in IT Support, Programming, and Full-Stack Web Development. My professional background includes developing and maintaining web applications, optimizing existing systems, and deploying applications to cloud environments. I have worked with modern technologies such as PHP, CodeIgniter, Laravel, React.js, Vue.js, Node.js, MySQL, MongoDB, and Alibaba Cloud. I am highly motivated to create innovative digital solutions, continuously learn new technologies, and contribute to impactful projects that deliver real business value.
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

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

      <!-- Experience 1 -->
      <div
        class="bg-white rounded-2xl shadow-lg p-6 hover:-translate-y-2 hover:shadow-2xl transition"
      >
        <div class="text-5xl mb-4">
          💻
        </div>

        <h3 class="font-bold text-xl mb-2">
          Web Developer Intern
        </h3>

        <p class="text-blue-600 font-semibold mb-4">
          PT Dharma Controlcable Indonesia
          <p class="text-gray-500 text-sm mb-4">
          24 Oktober 2025 – 24 April 2026 (6 Bulan)
        </p>
        </p>

        <ul class="list-disc ml-5 text-gray-600">
          <li>Maintenance Website Company Profile</li>
          <li>Analisis React.js</li>
          <li>Deployment Alibaba Cloud</li>
          <li>Integrasi MongoDB</li>
        </ul>
      </div>

      <!-- Experience 2 -->
      <div
        class="bg-white rounded-2xl shadow-lg p-6 hover:-translate-y-2 hover:shadow-2xl transition"
      >
        <div class="text-5xl mb-4">
          🏢
        </div>

        <h3 class="font-bold text-xl mb-2">
          Programmer Intern
        </h3>

        <p class="text-blue-600 font-semibold mb-4">
          PT Kawasan Industri Jababeka Tbk
           <p class="text-gray-500 text-sm mb-4">
           16 Februari 2024 – 30 Juni 2024 (5 Bulan)
        </p>
        </p>

        <ul class="list-disc ml-5 text-gray-600">
          <li>Membuat Website Training</li>
          <li>Maintenance Website Purchasing</li>
          <li>Analisis dan Optimasi Sistem</li>
        </ul>
      </div>

      <!-- Experience 3 -->
      <div
        class="bg-white rounded-2xl shadow-lg p-6 hover:-translate-y-2 hover:shadow-2xl transition"
      >
        <div class="text-5xl mb-4">
          🖥️
        </div>

        <h3 class="font-bold text-xl mb-2">
          IT Support Intern
        </h3>

        <p class="text-blue-600 font-semibold mb-4">
          PT Sucofindo Cirebon
          <p class="text-gray-500 text-sm mb-4">
          5 Desember 2018 – 28 Februari 2019 (3 Bulan)
        </p>
        </p>

        <ul class="list-disc ml-5 text-gray-600">
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

      <div class="bg-white p-4 rounded-xl shadow text-center hover:shadow-lg transition">
        PHP
      </div>

      <div class="bg-white p-4 rounded-xl shadow text-center hover:shadow-lg transition">
        CodeIgniter 4
      </div>

      <div class="bg-white p-4 rounded-xl shadow text-center hover:shadow-lg transition">
        Laravel
      </div>

      <div class="bg-white p-4 rounded-xl shadow text-center hover:shadow-lg transition">
        React.js
      </div>

      <div class="bg-white p-4 rounded-xl shadow text-center hover:shadow-lg transition">
        Vue.js
      </div>

      <div class="bg-white p-4 rounded-xl shadow text-center hover:shadow-lg transition">
        Node.js
      </div>

      <div class="bg-white p-4 rounded-xl shadow text-center hover:shadow-lg transition">
        MySQL
      </div>

      <div class="bg-white p-4 rounded-xl shadow text-center hover:shadow-lg transition">
        MongoDB
      </div>

      <div class="bg-white p-4 rounded-xl shadow text-center hover:shadow-lg transition">
        Alibaba Cloud
      </div>

    </div>

  </div>
</section>

<!-- Education -->
<section
  id="education"
  class="py-20 bg-gradient-to-b from-blue-50 to-white scroll-mt-24"
>
  <div class="max-w-6xl mx-auto px-6">

    <h2 class="text-4xl font-bold text-center mb-12">
      Education
    </h2>

    <div class="flex justify-center">

      <div
        class="bg-gradient-to-r from-blue-600 to-indigo-600 text-white rounded-3xl shadow-xl p-10 max-w-2xl w-full text-center hover:scale-105 transition duration-300"
      >

        <div class="text-6xl mb-5">
          🎓
        </div>

        <h3 class="text-3xl font-bold mb-3">
          Universitas Bina Sarana Informatika
        </h3>

        <p class="text-xl font-semibold mb-2">
          S1 Information System
        </p>

        
        <p class="text-xl font-semibold mb-2">
          GPA
        </p>

        <p class="text-blue-100 text-lg">
          2021 - 2025
        </p>

        <div class="mt-6">
          <span
            class="bg-white text-blue-600 px-4 py-2 rounded-full font-semibold"
          >
            Bachelor Degree
          </span>
        </div>

      </div>

    </div>

  </div>
</section>

<!-- Certificates -->
<section
  id="certificates"
  class="py-20 bg-white scroll-mt-24"
>
  <div class="max-w-6xl mx-auto px-6">

    <h2 class="text-4xl font-bold text-center mb-12">
      Certificates
    </h2>

    <div class="grid md:grid-cols-3 gap-8">

      <!-- Certificate 1 -->
      <a
        href="/sertifikat magang jababeka.pdf"
        target="_blank"
        class="bg-gray-50 rounded-2xl shadow-lg p-8 text-center hover:-translate-y-2 hover:shadow-xl transition"
      >
        <div class="text-5xl mb-4">
          🏆
        </div>

        <h3 class="font-bold text-xl">
          MSIB Batch 6
        </h3>

        <p class="text-gray-600 mt-3">
          PT Kawasan Industri Jababeka Tbk
        </p>
      </a>

      <!-- Certificate 2 -->
      <a
        href="/sertifikat BNSP.pdf"
        target="_blank"
        class="bg-gray-50 rounded-2xl shadow-lg p-8 text-center hover:-translate-y-2 hover:shadow-xl transition"
      >
        <div class="text-5xl mb-4">
          📜
        </div>

        <h3 class="font-bold text-xl">
          Analisis Program
        </h3>

        <p class="text-gray-600 mt-3">
          Sertifikat Kompetensi BNSP
        </p>
      </a>

      <!-- Certificate 3 -->
      <a
        href="/sertifikat maganghub.pdf"
        target="_blank"
        class="bg-gray-50 rounded-2xl shadow-lg p-8 text-center hover:-translate-y-2 hover:shadow-xl transition"
      >
        <div class="text-5xl mb-4">
          🚀
        </div>

        <h3 class="font-bold text-xl">
          MagangHub Batch 1
        </h3>

        <p class="text-gray-600 mt-3">
          PT Dharma Controlcable Indonesia
        </p>
      </a>

    </div>

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
  <div class="flex justify-center gap-8 mt-16">

  <a
    href="https://github.com/ahmadwildanf"
    target="_blank"
    class="text-5xl text-gray-700 hover:text-black transition"
  >
    <i class="fa-brands fa-github"></i>
  </a>

  <a
    href="https://linkedin.com/in/achmadwildanfaiz"
    target="_blank"
    class="text-5xl text-blue-600 hover:scale-110 transition"
  >
    <i class="fa-brands fa-linkedin"></i>
  </a>

 <a
    href="https://instagram.com/ahmad_wildan86"
    target="_blank"
    class="text-5xl text-pink-500 hover:scale-110 transition"
  >
    <i class="fa-brands fa-instagram"></i>
  </a>
</div>
</section>

    <footer class="bg-gray-900 text-white text-center py-5">
    
      © 2026 Achmad Wildan Alfarizky
    </footer>

  </div>
</template>