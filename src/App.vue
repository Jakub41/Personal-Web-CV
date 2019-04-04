<template>
  <div class="main-wrapper">
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary fixed-top" id="sideNav">
      <a class="navbar-brand js-scroll-trigger" href="#about">
        <span class="d-block d-lg-none">Start Bootstrap</span>
        <span class="d-none d-lg-block">
          <img class="img-fluid img-profile rounded-circle mx-auto mb-2" src="static/profile.jpg" alt="">
        </span>
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#about">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#experience">Experience</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#education">Education</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#skills">Skills</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#interests">Interests</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#awards">Awards</a>
          </li>
        </ul>
      </div>
    </nav>

    <div class="container-fluid p-0">
      <section class="resume-section p-3 p-lg-5 d-flex d-column" id="about">
        <div class="my-auto">
          <p class="mb-1" id="aboutMe">
             <span class="text-primary" id="hi">{{ hi }}</span>
          </p>
          <h1 class="mb-0">
            {{ name }}
            <span class="text-primary">{{ surname }}</span>
          </h1>
          <div class="subheading mb-5">
            <i class="fa fa-laptop stroke" style="color: white;"></i>
            {{ position }}
            <i class="fa fa-home stroke" style="color: white;"></i>
            {{ address }}
            <i class="fa fa-envelope stroke" style="color: white;"></i>
            <a href="mailto:lemiszewski@gmx.com">{{ email }}</a>
          </div>
          <ul class="list-inline list-social-icons mb-0">
            <li class="list-inline-item">
              <a href="https://www.linkedin.com/in/jakublemiszewski/" target="_blank">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-linkedin fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="https://github.com/Jakub41/" target="_blank">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-github fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
          </ul>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column relative" id="experience">
          <div class="glass"></div>
          <div class="my-auto absolute">
            <h2 class="mb-5">Experience</h2>

            <div
              class="resume-item d-flex flex-column flex-md-row mb-5"
              v-for="job in experience"
              :key="job.description"
            >
              <div class="resume-content mr-auto">
                <h3 class="mb-0">{{ job.position }}</h3>
                <div class="subheading mb-3">{{ job.company }}</div>
                <p>{{ job.description }}</p>
              </div>
              <div class="resume-date text-md-right">
                <span class="text-primary stroke">{{ job.startDate }} - {{ job.endDate }}</span>
              </div>
            </div>
          </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column relative" id="education">
        <div class="glass"></div>
        <div class="my-auto absolute">
          <h2 class="mb-5">Education</h2>

          <div class="resume-item d-flex flex-column flex-md-row mb-5">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">KEA Denmark</h3>
              <div class="subheading mb-3">Bachelor in Web Development</div>
              <div>Computer Science - Web Development Track</div>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary stroke">July 2016</span>
            </div>
          </div>

          <div class="resume-item d-flex flex-column flex-md-row">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">University of Pisa Italy</h3>
              <div class="subheading mb-3">Bachalor in Computer Science</div>
              <div>Computer Science - Web Security and Server Administration Track</div>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary stroke">June 2009</span>
            </div>
          </div>
          <br>
          <div class="resume-item d-flex flex-column flex-md-row">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">Maritime High School Viareggio Italy</h3>
              <div class="subheading mb-3">Junior Deck Officer</div>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary stroke">June 2003</span>
            </div>
          </div>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column relative" id="skills">
          <div class="glass"></div>
        <div class="my-auto absolute">
          <h2 class="mb-5">Skills</h2>

          <div class="subheading mb-3">Programming Languages &amp; Tools</div>
          <ul class="list-inline list-icons">
            <li class="list-inline-item">
              <i class="devicons devicons-ruby"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-ruby_on_rails"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-php"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-database"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-html5"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-css3"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-javascript"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-jquery"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-sass"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-less"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-bootstrap"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-git"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-github_badge"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-trello"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-jira"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-stackoverflow"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-terminal"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-code"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-aws"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-docker"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-heroku"></i>
            </li>

          </ul>

          <div class="subheading mb-3">Workflow</div>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-check"></i>
              Mobile-First, Responsive Design
            </li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Cross Browser Testing &amp; Debugging
            </li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Cross Functional Teams
            </li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Agile Development &amp; Scrum
            </li>
          </ul>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="interests">
        <div class="my-auto">
          <h2 class="mb-5">Interests</h2>
          <p>Apart from being a web developer, I enjoy most of my time being outdoors. In the winter, I am an avid skiier and novice ice climber. During the warmer months here in Colorado, I enjoy mountain biking, free climbing, and kayaking.</p>
          <p
            class="mb-0"
          >When forced indoors, I follow a number of sci-fi and fantasy genre movies and television shows, I am an aspiring chef, and I spend a large amount of my free time exploring the latest technolgy advancements in the front-end web development world.</p>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="awards">
        <div class="my-auto">
          <h2 class="mb-5">Awards &amp; Certifications</h2>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              Google Analytics Certified Developer
            </li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              Mobile Web Specialist - Google Certification
            </li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              1
              <sup>st</sup>
              Place - University of Colorado Boulder - Emerging Tech Competition 2009
            </li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              1
              <sup>st</sup>
              Place - University of Colorado Boulder - Adobe Creative Jam 2008 (UI Design Category)
            </li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              2
              <sup>nd</sup>
              Place - University of Colorado Boulder - Emerging Tech Competition 2008
            </li>
            <li></li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              1
              <sup>st</sup>
              Place - James Buchanan High School - Hackathon 2006
            </li>
            <li>
              <i class="fa-li fa fa-trophy text-warning"></i>
              3
              <sup>rd</sup>
              Place - James Buchanan High School - Hackathon 2005
            </li>
          </ul>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "JL-CV",
      hi: "HELLO, I'M",
      name: "Jakub",
      surname: "Lemiszewski",
      address:
        "Copenhagen DK",
      email: "lemiszewski@gmx.com",
      aboutMe:"Senior Developer",
      position: "Senior Developer",

      experience: [
        {
          position: "Senior Ruby Engineer",
          company: "Cargoflux",
          description:
            "Lead selection of appropriate technology for each component with the focus on security and scalability." +
            "Work closely with the client to develop a product solution that would suit their needs and be easily translated into a web application." +
            "Worked closely with the product manager throughout the development cycle ensuring the proposed solution met the requirements." +
            "Utilize appropriate process management tools including Jira, GitHub to support new feature implementation and maintenance on a highly compressed schedule." +
            "Successfully increased the stability of code base through effective adoption of iterative and agile methodologies" +
            "Served as a crucial team member to build solid scalable API integrations." +
            "Deploy new version releases to multiple environments including Heroku while ensuring adherence to established SLAs.",
          startDate: "January 2019",
          endDate: "April 2019"
        },
        {
          position: "Lead Ruby Developer",
          company: "S-CUBED / A3Informatics",
          description:
            "Complete Rails stack development. " +
            "Developing and Implementing solutions for the Glandon project. " +
            "Write functional, unit, and integration tests for application quality assurance. " +
            "Use version control tool Git and code storage tool Github for added application functionality. " +
            "Complete database migrations with Ruby on Rails and ActiveRecord. " +
            "PostgreSQL Database Infrastructure. " +
            "Complete database migrations with Neo4j and ActiveNode " +
            "Build custom Gems for application specific features " +
            "Managed projects with agile methodologies in JIRA " +
            "Designed user-interface pages using Twitter Bootstrap, custom CSS, JavaScript/JQuery, and JQuery UI. " +
            "DevOps and IT administration. " +
            "Linux/Ubuntu server administration " +
            "Build Java, Solr and Ruby tools for searching optimization for PDF documents",
          startDate: "September 2017",
          endDate: "December 2018"
        },
        {
          position: "Freelance Developer",
          company: "",
          description:
            "Back end and front end development.",
          startDate: "2014",
          endDate: "Present"
        }
      ]
    };
  },
  mounted() {
    const $ = this.jquery;
    this.$nextTick(() => {
      // our custom jQuery code goes here
      $('a.js-scroll-trigger[href*="#"]:not([href="#"])').click(function() {
        if (
          location.pathname.replace(/^\//, "") ===
            this.pathname.replace(/^\//, "") &&
          location.hostname === this.hostname
        ) {
          var target = $(this.hash);
          target = target.length
            ? target
            : $("[name=" + this.hash.slice(1) + "]");
          if (target.length) {
            $("html, body").animate(
              {
                scrollTop: target.offset().top
              },
              1000,
              "easeInOutExpo"
            );
            return false;
          }
        }
      });

      // Closes responsive menu when a scroll trigger link is clicked
      $(".js-scroll-trigger").click(function() {
        $(".navbar-collapse").collapse("hide");
      });

      // Activate scrollspy to add active class to navbar items on scroll
      $("body").scrollspy({
        target: "#sideNav"
      });
    });
  }
};
</script>

<style>

body {
  font-family: "Open Sans", serif;
  padding-top: 54px;
  color: #ffffff;
}

@media (min-width: 992px) {
  body {
    padding-top: 0;
    padding-left: 17rem;
  }
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: "Saira Extra Condensed", serif;
  font-weight: 700;
  text-transform: uppercase;
  color: #ffffff;
}

h1 {
  font-size: 6rem;
  line-height: 5.5rem;
}

h2 {
  font-size: 3.5rem;
}

.subheading {
  text-transform: uppercase;
  font-weight: 500;
  font-family: "Saira Extra Condensed", serif;
  font-size: 1.35rem;
}

.list-social-icons a {
  color: #495057;
}

.list-social-icons a:hover {
  color: #98123A;
}

.list-social-icons a .fa-lg {
  font-size: 1.75rem;
}

.list-icons {
  font-size: 3rem;
}

.list-icons .list-inline-item i:hover {
  color: #bd5d38;
}

#sideNav .navbar-nav .nav-item .nav-link {
  font-weight: 600;
  text-transform: uppercase;
}

@media (min-width: 992px) {
  #sideNav {
    text-align: center;
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    flex-direction: column;
    width: 17rem;
    height: 100vh;
  }
  #sideNav .navbar-brand {
    display: flex;
    margin: auto auto 0;
    padding: 0.5rem;
  }
  #sideNav .navbar-brand .img-profile {
    max-width: 10rem;
    max-height: 10rem;
    border: 0.1rem solid rgba(0,0,0);
  }
  #sideNav .navbar-collapse {
    display: flex;
    align-items: flex-start;
    flex-grow: 0;
    width: 100%;
    margin-bottom: auto;
  }
  #sideNav .navbar-collapse .navbar-nav {
    flex-direction: column;
    width: 100%;
  }
  #sideNav .navbar-collapse .navbar-nav .nav-item {
    display: block;
  }
  #sideNav .navbar-collapse .navbar-nav .nav-item .nav-link {
    display: block;
  }
}

section.resume-section {
  border-bottom: 1px solid #dee2e6;
  padding-top: 5rem !important;
  padding-bottom: 5rem !important;
}

section.resume-section .resume-item .resume-date {
  min-width: none;
}

@media (min-width: 768px) {
  section.resume-section {
    min-height: 100vh;
  }
  section.resume-section .resume-item .resume-date {
    min-width: 18rem;
  }
}

@media (min-width: 992px) {
  section.resume-section {
    padding-top: 3rem !important;
    padding-bottom: 3rem !important;
  }
}

.bg-primary {
  background-color: rgba(224, 224, 224, 0) !important;
}

.text-primary {
  color: #98123A !important;
}

a {
  color: rgb(255, 255, 255);
}

a:hover,
a:focus,
a:active {
  color: #ffffff;
}

/*Custom Style*/
#jl-background {
  background-image: url('~@/assets/back.jpg');
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
}

#aboutMe {
  /* WebKit (Safari/Chrome) Only */
  -webkit-text-stroke: 1px black;

  /* If we weren't using text-shadow, we'd set a fallback color
     and use this to set color instead
    -webkit-text-fill-color: white; */

  color: white;

  text-shadow:
    3px 3px 0 #000,
    /* Simulated effect for Firefox and Opera
       and nice enhancement for WebKit */
   -1px -1px 0 #000,
    1px -1px 0 #000,
   -1px  1px 0 #000,
    1px  1px 0 #000;

    font-size: 30px;
}

#hi {
  font-size: 50px;
}

.stroke {
  /* WebKit (Safari/Chrome) Only */
  -webkit-text-stroke: 1px black;

  /* If we weren't using text-shadow, we'd set a fallback color
     and use this to set color instead
    -webkit-text-fill-color: white; */
  color: white!important;
  font-weight: bold;
  text-shadow:
    1px 1px 0 #000,
    /* Simulated effect for Firefox and Opera
       and nice enhancement for WebKit */
   -1px -1px 0 #000,
    1px -1px 0 #000,
   -1px  1px 0 #000,
    1px  1px 0 #000;
}

.subheading {
  /* WebKit (Safari/Chrome) Only */
  -webkit-text-stroke: 1px black;

  /* If we weren't using text-shadow, we'd set a fallback color
     and use this to set color instead
    -webkit-text-fill-color: white; */

  color: white;

  text-shadow:
    3px 3px 0 #000,
    /* Simulated effect for Firefox and Opera
       and nice enhancement for WebKit */
   -1px -1px 0 #000,
    1px -1px 0 #000,
   -1px  1px 0 #000,
    1px  1px 0 #000;

    font-size: 30px;

    margin-left: 5px;
}
.relative {
  position: relative;
  background-color: rgba(34,34,34,0.75);
}

.absolute{
   position: absolute;
   top: 0;
   padding: 2px 2px 2px 2px;
}

.glass {
  background-size: cover;
  overflow: hidden;
  filter: blur(13px);
  position: absolute;
  height: 100%;
  top: 5px;
  left: 0;
  right: 0;
  bottom: 0;
}

.text-md-right {
  position: relative;
  right: 200px;
}
</style>
