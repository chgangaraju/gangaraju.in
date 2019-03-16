<template>
  <div class="main-wrapper">
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary fixed-top" id="sideNav">
      <a class="navbar-brand js-scroll-trigger" href="#about">
        <span class="d-block d-lg-none">Gangaraju</span>
        <span class="d-none d-lg-block">
          <img
            class="img-fluid img-profile rounded-circle mx-auto mb-2"
            src="./assets/profile.jpg"
            alt
          >
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
            <a class="nav-link js-scroll-trigger" href="#achievements">Achievements</a>
          </li>
        </ul>
      </div>
    </nav>

    <div class="container-fluid p-0">
      <section class="resume-section p-3 p-lg-5 d-flex d-column" id="about">
        <div class="my-auto">
          <h1 class="mb-0">
            {{ name }}
            <span class="text-primary">{{ surname }}</span>
          </h1>
          <div class="subheading mb-5">
            {{ address }}
            <a href="mailto:gangaraju.chaganti@gmail.com">{{ email }}</a>
          </div>
          <p class="mb-5">{{ aboutMe }}</p>
          <ul class="list-inline list-social-icons mb-0">
            <li class="list-inline-item">
              <a href="https://www.facebook.com/gangaraju.chaganti">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-facebook fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="https://twitter.com/ImGangaraju">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-twitter fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="https://www.linkedin.com/in/chgangaraju">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-linkedin fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="https://github.com/chgangaraju">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-github fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="https://stackoverflow.com/users/1986826/gangaraju">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-stack-overflow fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="https://www.instagram.com/Im_Gangaraju">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-instagram fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="https://plus.google.com/+GangarajuChaganti">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-google-plus fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
          </ul>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="experience">
        <div class="my-auto">
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
              <span class="text-primary">{{ job.startDate }} - {{ job.endDate }}</span>
            </div>
          </div>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="education">
        <div class="my-auto">
          <h2 class="mb-5">Education</h2>

          <div class="resume-item d-flex flex-column flex-md-row mb-5">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">B.V.Raju Institute of Computer Education</h3>
              <div class="subheading mb-3">Andhra University</div>
              <div>Master of Computer Applications</div>
              <p>GPA: 8.18</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">June 2010 - May 2013</span>
            </div>
          </div>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="skills">
        <div class="my-auto">
          <h2 class="mb-5">Skills</h2>

          <div class="subheading mb-3">Programming Languages &amp; Tools</div>
          <ul class="list-inline list-icons">
            <li class="list-inline-item">
              <i class="devicon-java-plain-wordmark colored"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicon-docker-plain-wordmark colored"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicon-amazonwebservices-plain-wordmark colored"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicon-python-plain-wordmark colored"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicon-angularjs-plain colored"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicon-javascript-plain colored"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicon-jquery-plain-wordmark colored"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicon-git-plain-wordmark colored"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicon-nginx-original-wordmark colored"></i>
            </li>
          </ul>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="achievements">
        <div>
          <h2 class="mb-5">Awards &amp; Certifications</h2>
          <div style="width: 50%; float:left">
            <ul class="fa-ul mb-0">
              <li>
                <i class="fa-li fa fa-trophy text-warning"></i>
                AWS Cerfied Solutions Architect - Professional
              </li>
              <li>
                <i class="fa-li fa fa-trophy text-warning"></i>
                AWS Cerfied DevOps Engineer - Professional
              </li>
              <li>
                <i class="fa-li fa fa-trophy text-warning"></i>
                AWS Cerfied Solutions Architect - Associate
              </li>
              <li>
                <i class="fa-li fa fa-trophy text-warning"></i>
                AWS Cerfied Developer - Associate
              </li>
              <li>
                <i class="fa-li fa fa-trophy text-warning"></i>
                AWS Cerfied SysOps Administrator - Associate
              </li>
              <li>
                <i class="fa-li fa fa-trophy text-warning"></i>
                Young Achiever - 2015 @Pramati Technologies
              </li>
              <li>
                <i class="fa-li fa fa-trophy text-warning"></i>
                Mission R&D Course
              </li>
              <br>
              <br>
            </ul>
          </div>
          <div style="width: 50%; float:right">
            <img src="./assets/aws_certified.png" style="max-width:70%" alt="aws_certified">
          </div>
        </div>
      </section>
    </div>
    <p id="footer">All Rights Reserved @ Gangaraju Chaganti 2019</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "Gangaraju Chaganti",
      name: "Gangaraju",
      surname: "Chaganti",
      address: "[ Bhimavaram, Hyderabad, Bengaluru ]",
      email: "gangaraju.chaganti@gmail.com",
      aboutMe:
        "Software Developer with around 6 years experience in Java, AWS, Docker, Python, Angular, Terraform and Serverless",
      experience: [
        {
          position: "Senior Software Developer",
          company: "Syncron Services India Private Limited",
          description: "",
          startDate: "April 2018",
          endDate: "Present"
        },
        {
          position: "Software Developer",
          company: "Syncron Services India Private Limited",
          description: "",
          startDate: "July 2016",
          endDate: "March 2018"
        },
        {
          position: "Development Engineer",
          company: "Wavemaker Inc",
          description: "",
          startDate: "Feb 2016",
          endDate: "July 2016"
        },
        {
          position: "Development Engineer",
          company: "Pramati Technologies Private Limited",
          description: "",
          startDate: "June 2013",
          endDate: "July 2016"
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