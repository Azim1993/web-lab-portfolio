<template>
  <section class="portfolio-content">
    <section class="portfolio-section" style="margin-top: -2em" id="summary">
      <h2>Summary</h2>
      <p>
        Fullstack Laravel developer with 8+ years of experience, proficient in system design and developing maintainable large-scale web applications. I have developed the ICDDRB COBRA suggestion engine and UK user credit score to APR calculation engine algorithm and accomplished RND and implemented micro-service at DocTime. Also, I have experience in taking responsibility for a small team and optimizing query performance, and improving code quality with design patterns. I love creating distributed systems, prototyping with new technology, and automating the tedious.
      </p>
    </section>
    <section class="portfolio-section" id="skills">
      <h2>Skills and Specialties</h2>
      <ul>
        <li>PHP, Javascript, Go Lang</li>
        <li>Microservice, OOP, Design Pattern, Clean code, REST, Docker, Unit-Test</li>
        <li>Learning stack: TypeScript, C++, Distributed system architecture, Kafka, Solr</li>
        <li>Laravel, Express, Lumen, Slim, Vue.js, Nuxt.js, Socket.io, TailwindCss</li>
        <li>ELK, Beanstalkd, RabbitMQ, Pusher, Git</li>
        <li>MYSQL, Redis, MongoDB</li>
        <li>LAMP with Nginx, Digital Ocean, AWS(EC2, S3, RDS)</li>
        <li>ES6, Sass, HTML5, CSS3, Bootstrap, jQuery, Vite, webpack</li>
      </ul>
    </section>
    <section class="portfolio-section" id="experience">
      <h2>Experience</h2>
      <div class="experience">
        <h3>Miaki Media Limited/ MyGP <span>Senior Software Engineer</span> <span class="date">Nov 2023 – Current</span></h3>
        <ul>
          <li>Design and develop 10 Million User base Application</li>
          <li>Working on 60+ micro-services</li>
          <li>Integrate JS bridge function on MYGP application</li>
          <li>Integrate Global search function with ES with suggestions</li>
        </ul>
        <h3>DocTime Limited <span>Senior Software Engineer</span> <span class="date">Mar 2021 – Oct 2023</span></h3>
        <ul>
          <li>Design and develop COBRA algorithm for ICDDRB</li>
          <li>Analysis patient information, design and develop EHR module for DocTime</li>
          <li>Integrate doctor automated payment distribution and report generation</li>
          <li>Optimize code with domain base and SQL query performance optimization</li>
          <li>Bkash SDK, API integration and Amazon chime and Agora video streaming integration</li>
          <li>Diagnostic module and complex doctor search handle with smooth transition frontend handle</li>
          <li>Lead frontend team</li>
          <li>Design and develop both offline and online campaign</li>
        </ul>
        <h3>Media365 Limited <span>Senior Software Engineer</span> <span class="date">Feb 2019 – Feb 2021</span></h3>
        <ul>
          <li>Analyze and architect personal loan dispatch with multiple lender bidding</li>
          <li>Develop user credit score with multiple lender apr offer algorithm</li>
          <li>Maintain car loan and car delivery with user credit score for UK user</li>
          <li>Handle multiple requests at same time with queue</li>
          <li>Integrate ekyc for UK user</li>
          <li>Handle automated car stock update</li>
          <li>Core role in developing surprise gift with anonymous chat</li>
        </ul>
        <h3>Advance Apps Bangladesh Limited <span>Senior Software Engineer</span> <span class="date">Sep 2018 - Dec 2019</span></h3>
        <ul>
          <li>Develop group and single chat project with pusher and integrate user story with other social network events. Also handle area base friend suggestion</li>
          <li>Maintain customer survey project with Laravel GraphQL and Vue</li>
          <li>Develop ecommerce project for gift card and offer</li>
        </ul>
        <h3>SparkBit Solution <span>Software Engineer</span> <span class="date">Mar 2017 – Aug 2018</span></h3>
        <ul>
          <li>Develop MLM base ecommerce with multi label inventory and warehouse with transport dispatch. Also integrate refer user reward and point with POS</li>
          <li>Develop Janata tower seminar hall book and rent system. Also automate approval permission transfer table to table for hi-Tech park</li>
        </ul>
      </div>
    </section>
    <section class="portfolio-section" id="education">
      <h2>Educations</h2>
      <ul>
        <li>SouthEast University Bangladesh - Bachelor in Computer Science and Engineering</li>
        <li>Cox’s Bazar Government College (2009 – 2011) - Higher Secondary Certificate</li>
      </ul>
    </section>
    <section class="portfolio-section" id="address">
      <h2>Address</h2>
      <p>ABC Cottage; Plot: 6/Z; Road: 03; Block: G; Bashundhara Residential Area, Dhaka.</p>
    </section>
  </section>
</template>

<style scoped>
.portfolio-content {
  max-width: 800px;
  margin: 2rem auto;
  padding: 2rem;
  background: #fff;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
}
.portfolio-content h1 {
  font-size: 2.2rem;
  margin-bottom: 0.2em;
}
.portfolio-content .subtitle {
  font-size: 1.1rem;
  color: #888;
  margin-left: 0.5em;
}
.contact-info {
  list-style: none;
  padding: 0;
  margin-bottom: 1.5em;
}
.contact-info li {
  display: inline-block;
  margin-right: 1.5em;
  font-size: 1.1em;
}
.portfolio-section {
  max-width: 800px;
  margin: 2.5rem auto;
  padding: 2rem 2.5rem;
  background: #fff;
  border-radius: 14px;
  box-shadow: 0 2px 12px rgba(44,62,80,0.07);
}
.portfolio-section:not(:last-child) {
  margin-bottom: 2.5rem;
}
.portfolio-section h2 {
  font-size: 1.7rem;
  color: #2c3e50;
  margin-bottom: 1.2rem;
  font-weight: 600;
}
.portfolio-section ul {
  margin: 0.5em 0 1em 1.5em;
}
.portfolio-section p {
  font-size: 1.1rem;
  color: #444;
}
.experience h3 {
  margin-top: 1.2em;
  font-size: 1.15em;
  color: #34495e;
  font-weight: 500;
}
.experience .date {
  font-size: 0.95em;
  color: #888;
  margin-left: 0.5em;
}
</style>
