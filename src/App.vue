<script setup>
const experienceItems = [
  {
    title: 'Desenvolvimento de aplicações web | Projetos independentes',
    activities: [
      'Construção de aplicações completas, da interface às regras de negócio no servidor.',
      'Criação de interfaces funcionais e responsivas para diferentes tamanhos de tela.',
      'Implementação e manutenção de funcionalidades com foco em organização e usabilidade.',
    ],
  },
  {
    title: 'APIs e integração de dados | Projetos independentes',
    activities: [
      'Desenvolvimento de APIs REST com Node.js e Express para comunicação entre sistemas.',
      'Integração com PostgreSQL, autenticação de usuários e aplicação de regras de negócio.',
      'Organização e versionamento do código com Git e GitHub durante o desenvolvimento.',
    ],
  },
  {
    title: 'Painéis administrativos | Projetos independentes',
    activities: [
      'Criação de dashboards para consulta e acompanhamento de informações da aplicação.',
      'Conexão das interfaces com serviços e dados armazenados no PostgreSQL.',
      'Uso de Docker e integração entre sistemas para apoiar o desenvolvimento e a execução.',
    ],
  },
]

const skills = ['Node.js e Express', 'APIs REST', 'PostgreSQL', 'Docker', 'Git e GitHub', 'Desenvolvimento front-end']
</script>

<template>
  <main class="resume" aria-label="Currículo de Gabriel Macêdo">
    <div class="resume__main">
      <header class="profile">
        <div class="profile__monogram" aria-hidden="true">GM</div>
        <div class="profile__intro">
          <h1>Gabriel Macêdo</h1>
          <p>Desenvolvedor júnior back-end e front-end · UniFAP</p>
        </div>
      </header>

      <p class="summary">
        Desenvolvedor Júnior Back-end e Front-end, formado pela UniFAP, com conhecimentos no desenvolvimento de aplicações web completas, atuando tanto na construção da interface do usuário quanto na lógica e estrutura do sistema no lado do servidor. Possuo experiência com tecnologias de front-end para criação de interfaces funcionais, responsivas e intuitivas, além de conhecimentos em back-end para desenvolvimento de APIs, integração com bancos de dados, autenticação e gerenciamento de regras de negócio. Tenho perfil proativo, foco em aprendizado contínuo, resolução de problemas e interesse em criar soluções digitais eficientes e escaláveis.
      </p>

      <section class="experience" aria-labelledby="experience-title">
        <h2 id="experience-title">Experiências Profissionais</h2>
        <article v-for="(job, index) in experienceItems" :key="`${job.title}-${index}`" class="job">
          <h3>{{ job.title }}</h3>
          <ul>
            <li v-for="activity in job.activities" :key="activity">{{ activity }}</li>
          </ul>
        </article>
      </section>
    </div>

    <aside class="resume__sidebar">
      <section class="education" aria-labelledby="education-title">
        <h2 id="education-title">FORMAÇÃO</h2>
        <article class="education__item">
          <h3>2028 | Universidade Paraíso — UniFAP</h3>
          <p>Ensino superior completo</p>
          <ul><li>Foco em desenvolvimento de softwares</li></ul>
        </article>
      </section>

      <section class="skills" aria-labelledby="skills-title">
        <h2 id="skills-title">COMPETÊNCIAS</h2>
        <ul><li v-for="skill in skills" :key="skill">{{ skill }}</li></ul>
      </section>

      <section class="contacts" aria-labelledby="contacts-title">
        <h2 id="contacts-title">CONTATOS</h2>
        <p><strong>ENDEREÇO:</strong> Rua Padre Conceição, 1167</p>
        <p><strong>EMAIL:</strong> <a href="mailto:gabrielmacedomktd@gmail.com">gabrielmacedomktd@gmail.com</a></p>
      </section>
    </aside>
  </main>
</template>
