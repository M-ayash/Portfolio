<template>
  <div class="CV">
    <section class="cv-left">
      <div class="header-left">
        <h1 class="left-title">Mohammad</h1>
        <div class="cv-img">
          <img src="@/assets/img/main-img.jpg" alt="Mohammad Ayash" class="" />
          <p class="description p-3">
            Ik ben een webontwikkelaar met frontend ervaring. Kennis van HTML,
            CSS, Javascript, Bootstrap, Wordpress Vuejs python en Java .
          </p>
        </div>
        <hr />
        <div class="activite">
          <h3>ACTIVITEITEN EN INTERESSES</h3>
          <ul>
            <li>Lezen</li>
            <li>Wandelen</li>
            <li>voetbal</li>
            <li>programmeren</li>
          </ul>
        </div>
        <div class="skills">
          <h3>VAARDIGHEDEN</h3>
          <ul>
            <li>
              <span>front-end</span>
              <div class="progress">
                <span class="progress-bar bg-info" style="width: 80%">80%</span>
              </div>
            </li>
            <li>VueJs
              <div class="progress">
                <span class="progress-bar bg-info" style="width: 70%">70%</span>
              </div>
            </li>
            <li>wordpress
              <div class="progress">
                <span class="progress-bar bg-info" style="width: 60%">60%</span>
              </div>
            </li>
            <li>software developer
              <div class="progress">
                <span class="progress-bar bg-info" style="width: 60%">60%</span>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </section>
    <!---->
    <section class="cv-right p-3">
      <div class="header-right">
        <h1 class="right-title">Ayash</h1>
        <h3 class="job-name">Front-end Developer</h3>
      </div>
      <div class="personalia-details">
        <div class="email">
          <p><i class="fa-solid fa-envelope"></i> mohammadhd1987@gmail.com</p>
        </div>
        <div class="phone"></div>
        <div class="adress">
          <p><i class="fa-solid fa-map-location-dot"></i> Tamboer 9</p>
          <p>6866 ED, Heelsum</p>
        </div>
        <hr />
      </div>

      <div class="work-exper">
        <h2>WERK ERVARING</h2>
        <div>
          <h3>front-end developer</h3>
          <p><span>ICTMaatwerk </span>|<span> 2021-heden</span></p>
          <ul>
            <li>
              Website gemaakt en beheerd met<br />
              HTML,CSS,Javascript,php,Vuejs
            </li>
            <li>Wep Applicaties ontwikkeld</li>
          </ul>
        </div>
      </div>
      <div class="opleiding">
        <h2>OPLEIDING</h2>
        <div>
          <h3>NT2 -Inburgering</h3>
          <p><span>Rijnijssel-Arnhem </span>|<span> 2019-heden</span></p>
          <ul>
            <li>
              Website gemaakt en beheerd met<br />
              HTML,CSS,Javascript,php,Vuejs
            </li>
            <li>Wep Applicaties ontwikkel</li>
          </ul>
        </div>
        <div>
          <h3>ICT-engineering onderwijs</h3>
          <p><span>Damascus-syrie </span>|<span> 2008-2012</span></p>
          <ul>
            <li>software engineering</li>
            <li>web designer,database,</li>
            <li>software developer</li>
          </ul>
        </div>
      </div>
    </section>
  </div>
</template>

<style>
.CV {
  background-color: #fff;
  min-height: 100vh;
  min-width: 100%;
}
.cv-left {
  min-height: 100vh;
  width: 40%;
  float: left;
  background-color: rgb(57, 90, 135);
  color: #fff;
}
.cv-img {
  width: 100%;
  text-align: center;
}
.cv-img img {
  border-radius: 50%;
  border: 3px solid #ddd;
  max-width: 100%;
  height: 30vh;
}
.header-left h1 {
  font: 4em sans-serif;
  text-align: center;
  font-weight: bolder;
  color: #fff;
}
.description {
  font-size: 20px;
  text-align: justify;
}
.activite,
.skills {
  margin: 20px 10px;
}
.activite h3,
.skills h3 {
  text-align: center;
}
.progress {
  display: inline-flex;
  width: 10em;
  float: right;
}

/*///////////////*/

.cv-right {
  width: 60%;
  float: left;
  color: rgb(57, 90, 135);
}
.right-title {
  font: 4em sans-serif;
  text-align: center;
  font-weight: bolder;
}
.job-name {
  text-align: center;
}
.personalia-details {
  padding: 20px;
}
.personalia-details h1 {
  color: rgb(57, 90, 135);
  padding-bottom: 10px;
  text-decoration: underline;
}
.solliciteren-text {
  text-align: justify;
  white-space: normal;
}

.work-exper,
.opleiding {
  color: #000;
}
.work-exper h2,
.opleiding h2 {
  text-align: center;
  color: rgb(57, 90, 135);
}
.work-exper h3,
.opleiding h3 {
  color: rgb(0, 22, 51);
}
.work-exper p,
.opleiding p {
  color: gray;
  padding-left: 10px;
}
@media print{
 .cv{
   min-height: 100%;
   max-width: 100%;
 } 
 .cv-img img {
   height: 20vh;
 }
}
</style>