<template>
  <main class="portfolio">
    <nav class="navbar">
      <a href="#" class="logo">Eduardo Ramírez</a>

      <div class="nav-links">
        <a href="#about">Sobre mí</a>
        <a href="#experience">Experiencia</a>
        <a href="#projects">Proyectos</a>
        <a href="#contact">Contacto</a>
      </div>
    </nav>

    <section class="hero">
      <div class="hero-content">
        <p class="eyebrow">Desarrollador Full Stack</p>

        <h1>Construyo aplicaciones web y móviles.</h1>

        <p class="hero-text">
          Soy Eduardo Ramírez, desarrollador con experiencia en Laravel, Vue,
          PHP, bases de datos y aplicaciones móviles. Me enfoco en crear
          soluciones claras, estables y fáciles de usar.
        </p>

        <div class="hero-actions">
          <a href="#projects" class="btn primary">Ver proyectos</a>
          <a href="#contact" class="btn secondary">Contacto</a>
        </div>
      </div>

      <div class="photo-card">
        <div class="photo-placeholder">
          <!-- <span>Tu foto</span> -->

          <img :src="'./images/profile.jpg'" alt="Foto de Eduardo Ramírez">
        </div>
      </div>
    </section>

    <section id="about" class="section split">
      <div>
        <p class="section-label">Sobre mí</p>
        <h2>Perfil</h2>
      </div>

      <p>
        Ingeniero en Sistemas Computacionales con más de 4 años de experiencia
        en desarrollo web y móvil. He participado en la creación, mantenimiento
        y optimización de aplicaciones empresariales, plataformas web, APIs y
        sistemas móviles, trabajando principalmente con Laravel, Vue, PHP,
        Flutter y bases de datos relacionales.
      </p>
    </section>

    <section class="section">
      <p class="section-label">Tecnologías</p>
      <h2>Herramientas con las que trabajo</h2>

      <div class="skills-grid">
        <span>Laravel</span>
        <span>PHP</span>
        <span>Vue</span>
        <span>JavaScript</span>
        <span>React</span>
        <span>Angular</span>
        <span>Flutter</span>
        <span>Python</span>
        <span>MySQL</span>
        <span>PostgreSQL</span>
        <span>SQL Server</span>
        <span>SQLite</span>
        <span>Oracle</span>
        <span>Git</span>
        <span>APIs REST</span>
        <span>Cordova</span>
        <span>Android Studio</span>
        <span>Xcode</span>
      </div>
    </section>

    <section id="experience" class="section">
      <p class="section-label">Experiencia</p>
      <h2>Donde he trabajado</h2>

      <div class="timeline">
        <article class="experience-card">
          <div>
              <p>
                <img :src="'./images/icons/bennetts.png'" height="60px" alt="">
            </p>
            <h3>Grupo Bennetts</h3>
            <p class="role">Programador Jr · septiembre 2022 - marzo 2026</p>
            <a href="https://grupobennetts.com.mx" target="_blank">
              grupobennetts.com.mx
            </a>

          </div>

          <div>
            <ul>
              <li>
                Desarrollo y mejora de aplicaciones web y móviles utilizando
                Laravel, Vue, React, Angular, Cordova y Flutter.
              </li>

              <li>
                Desarrollo backend con PHP (Laravel) y Python, además de
                administración y optimización de bases de datos MySQL,
                SQL Server, SQLite, PostgreSQL y Oracle.
              </li>

              <li>
                Corrección de errores críticos y optimización de aplicaciones
                web y móviles para clientes externos.
              </li>

              <li>
                Gestión de código fuente mediante Git y preparación de versiones
                para despliegue en producción y tiendas móviles.
              </li>

              <li>
                Diseño de recursos gráficos y apoyo en la experiencia visual de
                diversos proyectos digitales.
              </li>
            </ul>

            <div class="achievement">
              <strong>Logro destacado</strong>

              <p>
                Participé en el desarrollo y optimización de un sistema de
                control de asistencia biométrica web y móvil, mejorando APIs y
                procesos de autenticación mediante código QR y huella digital.
              </p>
            </div>
          </div>
        </article>

        <article class="experience-card">
          <div>
             <p>
                <img :src="'./images/icons/sedlogo.png'" height="60px" alt="">
            </p>
            <h3>SED México</h3>
            <p class="role">Desarrollador Web · octubre 2021 - julio 2022</p>
            <a href="https://www.sedmexico.com.mx" target="_blank">
              sedmexico.com.mx
            </a>

          </div>

          <div>
            <ul>
              <li>
                Desarrollo de sitios web en WordPress, HTML y PHP adaptados a
                los requerimientos de cada cliente.
              </li>

              <li>
                Optimización de rendimiento y velocidad de carga mediante
                mejoras en backend, librerías y componentes del sistema.
              </li>

              <li>
                Desarrollo e integración de Web Services utilizando Spring Boot
                para comunicación con plataformas externas.
              </li>
            </ul>

            <div class="achievement">
              <strong>Logro destacado</strong>

              <p>
                Integración de pasarelas de pago mediante Mercado Pago en
                múltiples sitios web y tiendas en línea desarrolladas con
                WordPress y PHP, permitiendo transacciones seguras con tarjetas
                de crédito y débito.
              </p>
            </div>
          </div>
        </article>
      </div>
    </section>

    <section id="projects" class="section">
      <div class="section-header">
        <div>
          <p class="section-label">Proyectos</p>
          <h2>Algunos trabajos</h2>
        </div>

        <p>
          Aquí puedo mostrar proyectos personales, prácticas o trabajos donde
          participé. Las imágenes se pueden cambiar fácilmente desde la carpeta
          pública del proyecto.
        </p>
      </div>

      <div class="projects-grid">
        <article v-for="project in projects" :key="project.title" class="project-card">
          <div class="project-image">
            <img :src="project.image" :alt="project.title">
          </div>

          <div class="project-content">
            <p class="project-type">{{ project.type }}</p>
            <h3>{{ project.title }}</h3>
            <p>{{ project.description }}</p>

            <div class="project-tags">
              <span v-for="tag in project.tags" :key="tag">
                {{ tag }}
              </span>
            </div>
          </div>
        </article>
      </div>
    </section>

    <section id="contact" class="section contact">
      <p class="section-label">Contacto</p>

    <!--   <h2>Hablemos</h2>

      <p>
        Estoy abierto a oportunidades como desarrollador web, full stack,
        Laravel developer o desarrollador móvil.
      </p> -->

      <a href="mailto:eduardocastro1997@gmail.com" class="btn primary">
        Enviar correo
      </a>

      <div class="contact-links">
        <a href="tel:+525549611009" class="contact-card">
          <span class="icon">📞</span>

          <div>
            <small>Teléfono</small>
            <strong>55 4961 1009</strong>
          </div>
        </a>

        <a
          href="https://wa.me/525549611009"
          target="_blank"
          class="contact-card whatsapp"
        >
          <img
             :src="'./images/icons/whatsapp.png'"
            alt="WhatsApp"
            class="contact-icon"
          >

          <div>
            <small>WhatsApp</small>
            <strong>Enviar mensaje</strong>
          </div>
        </a>
      </div>
    </section>
  </main>
</template>

<script setup>
const projects = [
  {
    title: 'Multiservicios API',
    type: 'Backend / API REST',
    description:
      'API multiservicios con Laravel para gestionar negocios y conectar información con una aplicación móvil.',
    image: './images/projects/sed.png',
    tags: ['Laravel', 'MySQL', 'API REST'],
    },

    {
  title: 'Aplicación de Gestión en Campo',
  type: 'Mobile App',
  description: 'Desarrollo de una aplicación para operaciones en campo, permitiendo el registro y consulta de información en tiempo real.',
  image: './images/projects/field.png',
  tags: ['Angular', 'TypeScript', 'API REST'],
},
  {
    title: 'Aplicación móvil híbrida',
    type: 'Mobile App',
    description:
      'Aplicación móvil conectada a backend, creada con tecnologías web y preparada para despliegue.',
    image: './images/projects/unib.png',
    tags: ['Flutter', 'Cordova', 'PHP'],
  },
  {
    title: 'Sistema administrativo',
    type: 'Web App',
    description:
      'Panel web para gestión interna, consultas, usuarios y mejora de procesos administrativos.',
    image: './images/projects/people.png',
    tags: ['Vue', 'Laravel', 'SQL'],
    },
  {
  title: 'Optimización de Aplicaciones Empresariales',
  type: 'Web & Mobile',
  description:
    'Mejora de rendimiento, corrección de incidencias e implementación de nuevas funcionalidades en plataformas web y móviles.',
  image: './images/projects/code.png',
  tags: ['Laravel', 'Flutter', 'APIs'],
    },
{
  title: 'Integración de Pasarelas de Pago',
  type: 'E-commerce',
  description:
    'Implementación de pagos en línea mediante Mercado Pago para sitios web y tiendas virtuales, permitiendo transacciones seguras con tarjetas de crédito y débito.',
  image: './images/projects/mp.png',
  tags: ['PHP', 'WordPress', 'Mercado Pago'],
},
]
</script>

<style scoped>
.portfolio {
  width: min(1180px, 92%);
  margin: auto;
  color: #e5e7eb;
}

.navbar {
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo {
  color: #ffffff;
  font-weight: 700;
  text-decoration: none;
  letter-spacing: -0.04em;
}

.nav-links {
  display: flex;
  gap: 28px;
}

.nav-links a {
  color: #94a3b8;
  text-decoration: none;
  font-size: 14px;
}

.nav-links a:hover {
  color: #ffffff;
}

.hero {
  min-height: calc(100vh - 80px);
  display: grid;
  grid-template-columns: 1.3fr 0.7fr;
  gap: 56px;
  align-items: center;
}

.hero-content {
  max-width: 820px;
}

.eyebrow,
.section-label,
.project-type {
  color: #38bdf8;
  font-size: 13px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.16em;
}

h1 {
  font-size: clamp(42px, 6vw, 74px);
  line-height: 1;
  letter-spacing: -0.06em;
  margin: 18px 0 24px;
}

h2 {
  font-size: clamp(30px, 4vw, 46px);
  line-height: 1;
  letter-spacing: -0.05em;
  margin: 10px 0 0;
}

h3 {
  font-size: 24px;
  margin: 8px 0 10px;
  letter-spacing: -0.04em;
}

p {
  color: #94a3b8;
  line-height: 1.8;
}

.hero-text {
  max-width: 680px;
  font-size: 18px;
}

.hero-actions {
  display: flex;
  gap: 14px;
  margin-top: 28px;
}

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 13px 18px;
  border-radius: 999px;
  text-decoration: none;
  font-weight: 700;
  font-size: 14px;
}

.primary {
  background: #ffffff;
  color: #020617;
}

.secondary {
  border: 1px solid #334155;
  color: #ffffff;
}

.photo-card {
  border: 1px solid #1e293b;
  border-radius: 32px;
  padding: 14px;
  background: rgba(15, 23, 42, 0.6);
}

.photo-placeholder {
  aspect-ratio: 4 / 5;
  border-radius: 24px;
  background: #111827;
  display: grid;
  place-items: center;
  color: #64748b;
  border: 1px dashed #334155;
  overflow: hidden;
}

.photo-placeholder img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.section {
  padding: 90px 0;
  border-top: 1px solid #1e293b;
}

.split {
  display: grid;
  grid-template-columns: 0.8fr 1.2fr;
  gap: 60px;
}

.skills-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-top: 30px;
}

.skills-grid span,
.project-tags span {
  border: 1px solid #334155;
  color: #cbd5e1;
  padding: 9px 14px;
  border-radius: 999px;
  font-size: 14px;
}

.timeline {
  display: grid;
  gap: 20px;
  margin-top: 36px;
}

.experience-card {
  display: grid;
  grid-template-columns: 0.8fr 1.2fr;
  gap: 40px;
  background: rgba(15, 23, 42, 0.68);
  border: 1px solid #1e293b;
  border-radius: 26px;
  padding: 28px;
}

.experience-card a {
  color: #38bdf8;
  text-decoration: none;
  font-size: 14px;
}

.role {
  margin: 0 0 10px;
  color: #cbd5e1;
}

ul {
  margin: 0;
  padding-left: 18px;
}

li {
  color: #94a3b8;
  line-height: 1.75;
  margin-bottom: 10px;
}

.achievement {
  margin-top: 20px;
  padding: 18px;
  border-radius: 16px;
  background: rgba(56, 189, 248, 0.08);
  border: 1px solid rgba(56, 189, 248, 0.18);
}

.achievement strong {
  display: block;
  margin-bottom: 8px;
  color: #38bdf8;
}

.achievement p {
  margin: 0;
}

.section-header {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  margin-bottom: 36px;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 22px;
}

.project-card {
  background: #0f172a;
  border: 1px solid #1e293b;
  border-radius: 26px;
  overflow: hidden;
  transition: transform 0.2s ease, border-color 0.2s ease;
}

.project-card:hover {
  transform: translateY(-4px);
  border-color: #334155;
}

.project-image {
  aspect-ratio: 16 / 10;
  background: #1e293b;
  overflow: hidden;
}

.project-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.project-content {
  padding: 24px;
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-top: 18px;
}

.contact {
  text-align: center;
  max-width: 720px;
  margin: auto;
  padding-bottom: 120px;
}

.contact .btn {
  margin-top: 20px;
}

.contact-links {
  margin-top: 32px;
  display: flex;
  justify-content: center;
  gap: 16px;
  flex-wrap: wrap;
}

.contact-card {
  display: flex;
  align-items: center;
  gap: 14px;
  min-width: 240px;
  padding: 16px 20px;
  border-radius: 18px;
  text-decoration: none;
  color: white;
  border: 1px solid #1e293b;
  background: rgba(15, 23, 42, 0.7);
  transition: all 0.25s ease;
}

.contact-card:hover {
  transform: translateY(-3px);
  border-color: #334155;
}

.contact-card small {
  display: block;
  color: #94a3b8;
  margin-bottom: 4px;
}

.contact-card strong {
  font-size: 15px;
}

.icon {
  font-size: 26px;
}

.contact-icon {
  width: 32px;
  height: 32px;
  object-fit: contain;
}

.whatsapp:hover {
  border-color: #22c55e;
}

@media (max-width: 900px) {
  .nav-links {
    display: none;
  }

  .hero,
  .split,
  .section-header,
  .projects-grid,
  .experience-card {
    grid-template-columns: 1fr;
  }

  .hero {
    padding: 60px 0;
  }

  .photo-card {
    max-width: 340px;
  }

  .hero-actions {
    flex-direction: column;
    align-items: flex-start;
  }

  h1 {
    letter-spacing: -0.05em;
  }
}
</style>
