<template>
    <!-- BEGIN NAVBAR -->
  <div class="navbar">
      <a href="#about">About</a>
      <a href="#experience">Experience</a>
      <a href="#education">Education</a>
      <a href="#projects">Projects</a>
      <a href="#skills">Skills</a>
      <a href="#contact">Contact</a>
    </div>
    <!-- END NAVBAR -->

    <div class="container">

      <!-- HEADER -->
      <div class="jumbotron">
        <div class="jumbotron-text">
          <h1>Afi kristiani</h1>
          <p>D3 Brawijaya University</p>
        </div>
        <div class="jumbotron-social">
          <ul class="ul-social">
            <li class="li-social-links">
              <a class="social" href="https://github.com/kristianiafi" target="_blank"><i class="fa fa-github" aria-hidden="true"></i></a>
            </li>
            <li class="li-social-links">
              <a class="social" href="https://www.linkedin.com/in/afi-kristiani-4540011a9/" target="_blank"><i class="fa fa-linkedin" aria-hidden="true"></i></a>
            </li>
          </ul>
        </div>
        <div id="down-arrow">
          <span><a href="#about"><i class="fa fa-chevron-down" aria-hidden="true"></i></a></span>
        </div>
      </div>
      <!-- END HEADER -->

      <!-- BEGIN ABOUT -->
      <div class="row white box-shadow">
        <div class="side-content"></div>
        <div class="main-content">
          <div class="content-header">
            <a class="anchor" name="about"></a>
            <h2>About</h2>
          </div>
          <div class="content-body">
            <p>Nama saya afi kristiani biasa dipanggil afi, umur saya 20 tahun. Saya berasal dari Bogor, Jawa Barat. Saya Mahasiswi Prodi Teknologi Informasi Universitas Brawijaya </p>
            <p>Saya suka menonton film. genre film yang sering say tonton yaitu genre trhiller,comedi, dan horor. Saya adalah pribadi yang ceria dan mudah bersosialisasi dengan orang lain.</p>
          </div>
        </div>
        <div class="side-content"></div>
      </div>
      <!-- END ABOUT -->

      <!-- BEGIN EXPERIENCE -->
      <div class="row">
        <div class="side-content"></div>
        <div class="main-content">
          <div class="content-header">
            <a class="anchor" name="experience"></a>
            <h2>Experience</h2>
          </div>
          <!-- CARD #1 -->
          <div class="content-body">
            <div class="card" v-for="experience in experiences">
              <div class="card-header">
                <h4>{{experience.company}} <span class="job-title">{{experience.job_title}}</span></h4>
              </div>
              <div class="card-content">
                <p>{{ experience.description }}</p>
              </div>
            </div>
          </div>
        </div>
        <div class="side-content"></div>
      </div>
      <!-- END EXPERIENCE -->

      <!-- BEGIN EDUCATION -->
      <div class="row white box-shadow">
        <div class="side-content"></div>
        <div class="main-content">
          <div class="content-header">
            <a class="anchor" name="education"></a>
            <h2>Education</h2>
          </div>
          <div class="content-body">

            <!-- EDUCATION DATA -->
            <div class="card" v-for="education in educations">
              <div class="card-header">
                <h4>{{education.name}} <span class="job-title">{{education.date_attended}}</span></h4>
              </div>
              <div class="card-content">
                <!-- baru deh disini dipanggil si description tadi -->
                <p>{{ education.description }}</p>
              </div>
            </div>

          </div>
        </div>
        <div class="side-content"></div>
      </div>
      <!-- END EDUCATION -->

      <!-- BEGIN PROJECTS -->
      <div class="row">
        <div class="side-content-sm"></div>
        <div class="main-content-lg">
          <div class="content-header">
            <a class="anchor" name="projects"></a>
            <h2>Projects</h2>
          </div>
          <div class="content-body">
            <!-- CARD #1 -->
            <div class="project-card" v-for="project in projects">
              <div class="project-content">
                <h4>{{project.project_name}}</h4>
                <a :href="project.link">Project repository</a>
                <p></p>
              </div>
            </div>
          </div>
        </div>
        <div class="side-content-sm"></div>
      </div>
      <!-- END PROJECTS -->

      <!-- BEGIN SKILLS -->
      <div class="row white box-shadow">
        <div class="side-content"></div>
        <div class="main-content">
          <div class="content-header">
            <a class="anchor" name="skills"></a>
            <h2>Skills</h2>
          </div>
          <div class="content-body">
            <ul class="ul-skills">
              <li class="li-skills" v-for="skill in skills">{{ skill }}</li>
            </ul>
          </div>
        </div>
        <div class="side-content"></div>
      </div>
      <!-- END SKILLS -->

      <!-- BEGIN FOOTER -->
      <div class="row">
        <div class="side-content"></div>
        <div class="main-content">
          <div class="content-header">
          </div>
          <div class="content-body">
            <p>Copyright 2024</p>
          </div>
        </div>
        <div class="side-content"></div>
      </div>
      <!-- END FOOTER -->
    </div>
</template>
<style>
@import url("~/assets/style.css");
</style>

<script>
export default {
  data(){
    return{
      // Data Personal
      skills: ["HTML", "Javascript", "PHP", "Laravel", "Python"],

      educations: [
        {name: "Universitas Brawijaya", date_attended:"2023 - Now", description:"Saya mahasiswi Prodi Teknologi Informasi Fakultas Vokasi Universitas Brawijaya "},
        {name: "SMKS PEMBANGUNAN BOGOR", date_attended:"2020 - 2023", description:"Saya Lulusan Jurusan Multimedia di SMKS PEMBANGUNAN Kota Bogor, Jawa Barat"}, 
      ],

      experiences: [
        {company: "PT. Utsman Property Indonesia", job_title: " Staff Media Sosial", description:" Saya Magang selama 3 Bulan di PT.Utsman Property Indonesia dengan jobdesk memegang akun dari perusahan dengan tanggujawab dengan konten konten yang akan diposting untuk akun tersebut "},
        {company: "SOS (SAVE OUR SOCMED)Short Movie Competition ", job_title: " clapper loader ", description:" Saya bertugas memberikan tanda awal pada pengambilan gambar dengan cara memegang clapperboard dan memperkenalkan informasí yang tertera di papam clapper"},
      ],

      projects: [
        {project_name: "Color change, Increment, Carousel using Vue JS", description: "", link: "https://github.com/kristianiafi/tugas-vue"},
        {project_name: "Contactform using PHP", description: "", link: "https://github.com/kristianiafi/contact-form"},
      ]
    }
  }
}
</script>