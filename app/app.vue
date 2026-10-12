
<script setup lang="ts">
import { ref } from 'vue'

const menuOpen = ref(false)

const technologies = [
  'PHP', 'Laravel', 'JavaScript', 'TypeScript',
  'Vue.js', 'Nuxt', 'Go', 'PostgreSQL', 'REST API', 'Docker',
]

const projects = [
  {
    number: '01',
    category: 'HEALTHCARE SYSTEM',
    title: 'Hospital Management System',
    description:
      'Pengembangan dan pemeliharaan aplikasi manajemen rumah sakit, termasuk alur pelayanan, integrasi antarmodul, dan optimasi query database.',
    stack: ['Laravel', 'PHP', 'PostgreSQL', 'REST API'],
    color: 'mint',
  },
  {
    number: '02',
    category: 'SYSTEM INTEGRATION',
    title: 'Digital Signature Integration',
    description:
      'Integrasi layanan tanda tangan elektronik untuk mendukung proses penandatanganan dokumen digital dan pengelolaan hasil PDF.',
    stack: ['Laravel', 'API Integration', 'PDF'],
    color: 'blue',
  },
  {
    number: '03',
    category: 'INVENTORY MANAGEMENT',
    title: 'Inventory Workflow',
    description:
      'Pengembangan alur pengelolaan stok dan perpindahan barang dengan validasi proses bisnis serta konsistensi data.',
    stack: ['PHP', 'Laravel', 'SQL'],
    color: 'purple',
  },
]

const experiences = [
  {
    role: 'Fullstack Web Developer',
    period: 'Sesuaikan dengan periode kerja',
    description:
      'Mengembangkan fitur aplikasi, mengintegrasikan layanan, menangani bug, serta menjaga performa dan keandalan sistem.',
  },
]
</script>

<template>
  <div class="min-h-screen bg-[#080D0C] text-[#E8F0EC]">
    <!-- Navbar -->
    <header class="site-header">
      <nav class="container-shell nav-shell">
        <a href="#home" class="brand" @click="menuOpen = false">
          <span class="brand-mark">&lt;/&gt;</span>
          <span>portfolio<span class="text-mint">.dev</span></span>
        </a>

        <button
          class="mobile-toggle"
          type="button"
          :aria-expanded="menuOpen"
          aria-label="Buka atau tutup navigasi"
          @click="menuOpen = !menuOpen"
        >
          {{ menuOpen ? 'Tutup' : 'Menu' }}
        </button>

        <div class="nav-links" :class="{ 'nav-open': menuOpen }">
          <a href="#about" @click="menuOpen = false">Tentang</a>
          <a href="#projects" @click="menuOpen = false">Project</a>
          <a href="#experience" @click="menuOpen = false">Pengalaman</a>
          <a href="#contact" class="nav-contact" @click="menuOpen = false">
            Hubungi saya <span aria-hidden="true">↗</span>
          </a>
        </div>
      </nav>
    </header>

    <main>
      <!-- Hero -->
      <section id="home" class="container-shell hero-section">
        <div class="hero-copy">
          <div class="availability">
            <span class="availability-dot"></span>
            FULLSTACK & BACKEND DEVELOPER
          </div>

          <h1>
            Membangun solusi digital yang
            <span class="gradient-text">andal dan bermakna.</span>
          </h1>

          <p class="hero-description">
            Saya seorang developer yang berfokus pada pengembangan aplikasi
            web, integrasi sistem, dan backend yang terstruktur, dengan
            perhatian pada kualitas kode serta kebutuhan bisnis.
          </p>

          <div class="hero-actions">
            <a class="button-primary" href="#projects">
              Lihat project <span aria-hidden="true">↗</span>
            </a>
            <a class="button-secondary" href="#contact">
              Mari terhubung
            </a>
          </div>

          <div class="hero-meta">
            <span><span class="meta-icon">⌘</span> Laravel & Vue</span>
            <span><span class="meta-icon">⌘</span> Backend & API</span>
            <span><span class="meta-icon">⌘</span> Go enthusiast</span>
          </div>
        </div>

        <div class="hero-visual" aria-label="Ilustrasi kode program">
          <div class="orb orb-one"></div>
          <div class="orb orb-two"></div>

          <div class="code-window">
            <div class="window-top">
              <div class="window-dots">
                <span></span><span></span><span></span>
              </div>
              <span class="window-file">developer.ts</span>
              <span class="window-symbol">TS</span>
            </div>

            <div class="code-content">
              <div><span class="line-number">01</span><span class="syntax-purple">const</span> developer = {</div>
              <div><span class="line-number">02</span>&nbsp;&nbsp;name: <span class="syntax-green">'Fullstack Developer'</span>,</div>
              <div><span class="line-number">03</span>&nbsp;&nbsp;focus: [</div>
              <div><span class="line-number">04</span>&nbsp;&nbsp;&nbsp;&nbsp;<span class="syntax-green">'Backend'</span>,</div>
              <div><span class="line-number">05</span>&nbsp;&nbsp;&nbsp;&nbsp;<span class="syntax-green">'Scalable Systems'</span>,</div>
              <div><span class="line-number">06</span>&nbsp;&nbsp;&nbsp;&nbsp;<span class="syntax-green">'Clean Code'</span>,</div>
              <div><span class="line-number">07</span>&nbsp;&nbsp;],</div>
              <div><span class="line-number">08</span>&nbsp;&nbsp;build: () =&gt; {</div>
              <div><span class="line-number">09</span>&nbsp;&nbsp;&nbsp;&nbsp;<span class="syntax-purple">return</span> <span class="syntax-green">'Something useful'</span></div>
              <div><span class="line-number">10</span>&nbsp;&nbsp;}</div>
              <div><span class="line-number">11</span>}</div>
              <div><span class="line-number">12</span><span class="syntax-muted">// Always learning.</span><span class="cursor"></span></div>
            </div>

            <div class="window-footer">
              <span><span class="status-dot"></span> Ready to build</span>
              <span>UTF-8 · TypeScript</span>
            </div>
          </div>

          <div class="floating-card floating-top">
            <span class="floating-icon">⌘</span>
            <div>
              <strong>Clean code</strong>
              <small>Maintainable by design</small>
            </div>
          </div>

          <div class="floating-card floating-bottom">
            <span class="floating-icon">↗</span>
            <div>
              <strong>Problem solver</strong>
              <small>Focus on real impact</small>
            </div>
          </div>
        </div>

        <a href="#about" class="scroll-cue">
          <span></span> Gulir untuk mengenal saya
        </a>
      </section>

      <!-- About -->
      <section id="about" class="section-block">
        <div class="container-shell">
          <div class="section-heading">
            <span class="eyebrow">01 / TENTANG SAYA</span>
            <h2>Teknologi yang baik dimulai dari <span>masalah yang tepat.</span></h2>
          </div>

          <div class="about-grid">
            <div class="about-copy">
              <p>
                Saya berfokus pada pengembangan aplikasi web dari sisi
                backend hingga frontend. Saya terbiasa mengembangkan fitur,
                mengintegrasikan API, mengelola database, dan melakukan
                pemeliharaan aplikasi yang digunakan dalam proses bisnis.
              </p>
              <p>
                Bagi saya, menulis kode bukan hanya tentang membuat fitur
                berjalan, tetapi juga menjaga agar sistem mudah dipahami,
                aman, dan dapat dikembangkan di kemudian hari.
              </p>
            </div>

            <div class="tech-panel">
              <div class="tech-panel-heading">
                <span class="panel-dot"></span>
                <span>TECHNOLOGIES I WORK WITH</span>
              </div>
              <div class="tech-list">
                <span v-for="tech in technologies" :key="tech" class="tech-chip">
                  {{ tech }}
                </span>
              </div>
              <p class="tech-note">
                Fokus pengembangan: backend, integrasi sistem, dan aplikasi web.
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- Projects -->
      <section id="projects" class="section-block projects-section">
        <div class="container-shell">
          <div class="section-heading section-heading-row">
            <div>
              <span class="eyebrow">02 / PROJECT PILIHAN</span>
              <h2>Beberapa hal yang <span>saya bangun.</span></h2>
            </div>
            <span class="section-count">SELECTED WORKS · 03</span>
          </div>

          <div class="project-grid">
            <article
              v-for="project in projects"
              :key="project.number"
              class="project-card"
            >
              <div class="project-card-top">
                <span class="project-number">{{ project.number }}</span>
                <span class="project-arrow">↗</span>
              </div>

              <div class="project-art" :class="`art-${project.color}`">
                <div class="art-window">
                  <span></span><span></span><span></span>
                  <div class="art-lines">
                    <i></i><i></i><i></i><i></i>
                  </div>
                </div>
                <div class="art-orbit"></div>
              </div>

              <span class="project-category">{{ project.category }}</span>
              <h3>{{ project.title }}</h3>
              <p class="project-description">{{ project.description }}</p>

              <div class="project-stack">
                <span v-for="tech in project.stack" :key="tech">{{ tech }}</span>
              </div>
            </article>
          </div>

          <p class="project-disclaimer">
            Catatan: project di atas merupakan contoh deskripsi awal berdasarkan
            jenis pekerjaan. Sesuaikan dengan project nyata, kontribusi pribadi,
            dan informasi yang boleh dipublikasikan.
          </p>
        </div>
      </section>

      <!-- Experience -->
      <section id="experience" class="section-block">
        <div class="container-shell">
          <div class="section-heading">
            <span class="eyebrow">03 / PENGALAMAN</span>
            <h2>Pengalaman yang membentuk <span>cara saya bekerja.</span></h2>
          </div>

          <div class="experience-list">
            <article
              v-for="(item, index) in experiences"
              :key="item.role"
              class="experience-item"
            >
              <div class="experience-index">0{{ index + 1 }}</div>
              <div class="experience-main">
                <h3>{{ item.role }}</h3>
                <p class="experience-period">{{ item.period }}</p>
                <p class="experience-description">{{ item.description }}</p>
              </div>
              <span class="experience-symbol">↗</span>
            </article>
          </div>
        </div>
      </section>

      <!-- Contact -->
      <section id="contact" class="section-block contact-section">
        <div class="container-shell">
          <div class="contact-card">
            <span class="eyebrow">04 / KONTAK</span>
            <h2>Ada project atau peluang menarik?</h2>
            <p>
              Saya terbuka untuk berdiskusi tentang peluang kerja,
              kolaborasi, dan tantangan pengembangan aplikasi web.
            </p>

            <!-- Ganti alamat email ini dengan email kamu -->
            <a class="button-primary" href="mailto:emailkamu@example.com">
              Hubungi saya melalui email <span aria-hidden="true">↗</span>
            </a>

            <div class="contact-links">
              <a href="https://github.com/" target="_blank" rel="noreferrer">GitHub ↗</a>
              <a href="https://www.linkedin.com/" target="_blank" rel="noreferrer">LinkedIn ↗</a>
            </div>
          </div>
        </div>
      </section>
    </main>

    <footer class="site-footer">
      <div class="container-shell footer-inner">
        <span>© {{ new Date().getFullYear() }} · Portfolio Developer</span>
        <span>Dibuat dengan <span class="text-mint">Vue & Nuxt</span></span>
        <a href="#home">Kembali ke atas ↑</a>
      </div>
    </footer>
  </div>
</template>
