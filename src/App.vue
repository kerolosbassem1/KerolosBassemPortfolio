<script setup>
import heroImage from './assets/kerolos-portrait.jpeg'

const contactLinks = [
  { label: 'Email', value: 'Kerolosbassem3@gmail.com', href: 'mailto:Kerolosbassem3@gmail.com' },
  { label: 'Phone', value: '+20 120 572 5854', href: 'tel:+201205725854' },
  { label: 'LinkedIn', value: 'linkedin.com/in/kerolos-bassem-30aa0a251', href: 'https://www.linkedin.com/in/kerolos-bassem-30aa0a251' },
  { label: 'GitHub', value: 'github.com/kerolosbassem1', href: 'https://github.com/kerolosbassem1' },
]

const skills = [
  'HTML5',
  'CSS3',
  'JavaScript',
  'TypeScript',
  'React.js',
  'Next.js',
  'Vue.js',
  'Tailwind CSS',
  'Bootstrap',
  'Vite',
  'REST APIs',
  'Responsive Design',
  'Git',
  'GitHub',
  'Linux',
  'Codex',
]

const experience = [
  {
    company: 'Cepro AI',
    location: 'Riyadh',
    role: 'Frontend Engineer',
    date: 'Feb 2026 - Present',
    points: [
      'Develop and maintain scalable web applications using React.js, Next.js, Vue.js, and TypeScript.',
      'Build reusable Vue.js components across multiple dashboards to improve maintainability.',
      'Integrate frontend components with backend APIs and collaborate with cross-functional teams.',
      'Use Git and AI-assisted development tools for debugging, refactoring, documentation, and faster delivery.',
    ],
  },
  {
    company: 'Coach Academy',
    location: 'Cairo',
    role: 'Problem-Solving Instructor',
    date: 'Jul 2022 - Aug 2022',
    points: ['Supported students with problem-solving fundamentals and programming practice.'],
  },
  {
    company: 'Masa Company',
    location: 'Cairo',
    role: 'Frontend Developer Intern',
    date: 'Jan 2022 - Apr 2022',
    points: [
      'Developed interactive UI components using HTML5, CSS3, JavaScript, and Bootstrap.',
      'Implemented a calculator project to strengthen JavaScript logic and DOM manipulation skills.',
    ],
  },
  {
    company: 'Masa Company',
    location: 'Cairo',
    role: 'Flutter Developer Intern',
    date: 'Jan 2022 - Apr 2022',
    points: [
      'Integrated REST APIs and implemented state management solutions for scalable mobile experiences.',
    ],
  },
]

const projects = [
  {
    title: 'Executive Monitoring Dashboard',
    company: 'Cepro AI',
    points: [
      'Developed responsive dashboards using Vue.js and Tailwind CSS with advanced data visualization.',
      'Improved UI/UX, integrated backend APIs, and increased UI consistency with reusable components.',
    ],
  },
  {
    title: 'Dark Web Monitoring Platform',
    company: 'Cepro AI',
    points: [
      'Rebuilt the dark web page from scratch and integrated it with backend services.',
      'Added new client pages and enhanced frontend performance.',
    ],
  },
  {
    title: 'Client & Partner Dashboard System',
    company: 'Cepro AI',
    points: [
      'Developed dashboards and search features.',
      'Enhanced reporting and take-down status functionality.',
    ],
  },
]
</script>

<template>
  <main class="portfolio-page">
    <nav class="site-nav" aria-label="Primary navigation">
      <a class="brand" href="#home" aria-label="Kerolos Bassem home">Kerolos Bassem</a>

      <div class="nav-links">
        <a href="#home">Home</a>
        <a href="#projects">Projects</a>
        <a href="#about">About Me</a>
        <a href="#contact">Contact</a>
      </div>

      <button class="menu-button" type="button" aria-label="Open navigation menu">
        <span></span>
        <span></span>
      </button>
    </nav>

    <section id="home" class="hero" aria-labelledby="hero-title">
      <div class="hero-media">
        <img :src="heroImage" alt="Kerolos Bassem portrait" />
      </div>

      <div class="hero-content">
        <p class="eyebrow">Frontend Engineer</p>

        <div class="headline-row">
          <h1 id="hero-title">My<br />Portfolio</h1>
          <span class="title-line" aria-hidden="true"></span>
        </div>

        <p class="intro">
          I am Kerolos Bassem Fekry, a frontend engineer based in Cairo, Egypt.
          I build scalable, responsive, and user-focused web applications using
          React.js, Next.js, Vue.js, TypeScript, and modern UI workflows.
        </p>

        <div class="hero-actions">
          <a class="primary-action" href="#projects">Explore Now</a>
          <a
            class="play-action"
            href="/Kerolos_Bassem_cv_20-6-2026.pdf"
            download="Kerolos_Bassem_cv_20-6-2026.pdf"
          >
            <span class="play-icon" aria-hidden="true"></span>
            Download CV
          </a>
        </div>

        <div class="page-marker" aria-label="Page 1 of 1">Page | 01</div>
      </div>
    </section>

    <section id="about" class="content-section about-section" aria-labelledby="about-title">
      <div class="section-heading">
        <p class="section-kicker">About Me</p>
        <h2 id="about-title">Production-ready frontend work with clean UI systems.</h2>
      </div>

      <div class="about-grid">
        <p>
          Frontend Engineer with hands-on experience building dashboards, reusable UI
          components, REST API integrations, and responsive web applications.
          Comfortable working in Agile teams, improving performance, debugging complex
          UI issues, and keeping code maintainable.
        </p>

        <div class="quick-facts" aria-label="Quick facts">
          <span>Cairo, Egypt</span>
          <span>B.Sc. Computer Science, Thebes Academy</span>
          <span>Arabic native</span>
          <span>English very good</span>
        </div>
      </div>
    </section>

    <section class="content-section skills-section" aria-labelledby="skills-title">
      <div class="section-heading">
        <p class="section-kicker">Skills</p>
        <h2 id="skills-title">Frontend stack and tools.</h2>
      </div>

      <div class="skill-list">
        <span v-for="skill in skills" :key="skill">{{ skill }}</span>
      </div>
    </section>

    <section id="projects" class="content-section" aria-labelledby="projects-title">
      <div class="section-heading">
        <p class="section-kicker">Projects</p>
        <h2 id="projects-title">Selected work from Cepro AI.</h2>
      </div>

      <div class="card-grid">
        <article v-for="project in projects" :key="project.title" class="info-card">
          <p class="card-meta">{{ project.company }}</p>
          <h3>{{ project.title }}</h3>
          <ul>
            <li v-for="point in project.points" :key="point">{{ point }}</li>
          </ul>
        </article>
      </div>
    </section>

    <section class="content-section" aria-labelledby="experience-title">
      <div class="section-heading">
        <p class="section-kicker">Experience</p>
        <h2 id="experience-title">Where I have worked.</h2>
      </div>

      <div class="timeline">
        <article v-for="job in experience" :key="`${job.company}-${job.role}`" class="timeline-item">
          <div>
            <p class="card-meta">{{ job.location }} | {{ job.date }}</p>
            <h3>{{ job.role }}</h3>
            <strong>{{ job.company }}</strong>
          </div>

          <ul>
            <li v-for="point in job.points" :key="point">{{ point }}</li>
          </ul>
        </article>
      </div>
    </section>

    <section id="contact" class="content-section contact-section" aria-labelledby="contact-title">
      <div class="section-heading">
        <p class="section-kicker">Contact</p>
        <h2 id="contact-title">Let's build something clean and useful.</h2>
      </div>

      <div class="contact-grid">
        <a v-for="item in contactLinks" :key="item.label" :href="item.href" target="_blank" rel="noreferrer">
          <span>{{ item.label }}</span>
          {{ item.value }}
        </a>
      </div>
    </section>
  </main>
</template>
