<!-- AUTHOR : YANICE TRECH
     UPDATE DATE : 10/12/2019
     ABOUT : Sample portofolio made for Web Design U.E purposes
     TECHNOLOGIES : VUE JS + Vue Now UI Kit
     NB : <STYLE> balise in his own view, because It's not a good practice to segregate it in Vue JS using a components based frameworks
     in fact, lookng for an .css different may increase slightly the loading times, It also negates a bit of Vue JS performance
--> 

<template>
<div>
  <header>
    <title>Yanice TRECH's Portoflio</title>
    <navbar
      position="fixed"
      type="primary"
      :transparent="transparent"
      :color-on-scroll="colorOnScroll"
      menu-classes="ml-auto"
    >
      <template slot-scope="{ toggle, isToggled }">
        <a v-popover:popover1 class="navbar-brand" href="#main">
          <p>Profile</p>
        </a>
        <el-popover
          ref="popover1"
          popper-class="popover"
          placement="bottom"
          width="200"
          trigger="hover"
        >
          <div class="popover-body">Designed with Vue JS and Vue Now UI kit</div>
        </el-popover>
      </template>
      <template slot="navbar-menu">
        <li class="nav-item">
          <a class="nav-link" href="#about">
            <i class="now-ui-icons business_badge"></i>
            <p>About Me</p>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#projects">
            <i class="now-ui-icons business_chart-bar-32"></i>
            <p>Projects</p>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#skills">
            <i class="now-ui-icons design-2_html5"></i>
            <p>Skills</p>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#experiences">
            <i class="now-ui-icons business_briefcase-24"></i>
            <p>Experiences</p>
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#graduation">
            <i class="now-ui-icons education_hat"></i>
            <p>Graduation</p>
          </a>
        </li>
      </template>
    </navbar>
  </header>
  <body>
    <div id="main" class="page-header clear-filter" filter-color="orange">
      <parallax class="page-header-image" style="background-image:url('img/portfolio-bg.jpeg')"></parallax>
      <div class="container">
        <div class="photo-container">
          <img src="img/profile-picture.jpeg" alt="Profile Picture" />
        </div>
        <h3 class="title">Yanice TRECH</h3>
        <p class="category">Unity/.NET Developer</p>
      </div>
    </div>
    <div class="section">
      <div class="container">
        <div class="button-container">
          <a
            href="https://www.linkedin.com/in/yanice-trech-5b4280172/"
            class="btn btn-default btn-round btn-lg btn-icon"
            rel="tooltip"
            title="Follow me on Twitter"
            target="_blank"
          >
            <i class="fab fa-linkedin"></i>
          </a>
          <a
            href="https://github.com/yanicetrech"
            class="btn btn-default btn-round btn-lg btn-icon"
            rel="tooltip"
            title="Follow me on Instagram"
            target="_blank"
          >
            <i class="fab fa-github"></i>
          </a>
        </div>
        <!-- Begin About Me -->
        <h4 id="about" class="title text-center">About me</h4>
        <h5 class="description">
          Really passionated about development.
          I am very polyvalent, I worked in several projects of different meaning such as Web and Software development.
          I am Currently in Master degree and I want to specialize myself in video gaming development industry.
        </h5>
        <!-- End About Me -->
        <!-- Begin Projects -->
        <div class="section" id="carousel">
          <div class="container">
            <h4 id="projects" class="title text-center">Projects</h4>
            <div class="row justify-content-center">
              <div class="col-8">
                <el-carousel height="500px">
                  <el-carousel-item>
                    <img class="d-block" src="img/vr-menu.jpeg" alt="First slide" />
                    <div class="carousel-caption d-none d-md-block">
                      <h5>Last Fools, VR shooter</h5>
                    </div>
                  </el-carousel-item>
                  <el-carousel-item>
                    <img class="d-block" src="img/coe-menu.jpeg" alt="Second slide" />
                    <div class="carousel-caption d-none d-md-block">
                      <h5>Crystals Of Empathy, 3D Mobile RPG</h5>
                    </div>
                  </el-carousel-item>
                  <el-carousel-item>
                    <img class="d-block" src="img/logo-rmd.jpeg" alt="Third slide" />
                    <div class="carousel-caption d-none d-md-block">
                      <h5>Rushing My Degree, 2D Platformer</h5>
                    </div>
                  </el-carousel-item>
                </el-carousel>
              </div>
            </div>
          </div>
        </div>
        <!-- End My Projects -->
        <!-- Begin Skills -->
        <div class="row">
          <div class="col-md-10 ml-auto mr-auto">
            <h4 id="skills" class="title text-center">Skills</h4>
            <div class="col-md-20 ml-auto mr-auto">
              <div class="row collections">
                <div class="col-md-4">
                  <div style="height: 40px;">
                    <h6>.NET</h6>
                    <n-progress :value="40" type="danger" show-value></n-progress>
                  </div>
                  <div style="height: 40px;">
                    <h6>WPF</h6>
                    <n-progress :value="60" type="danger" show-value></n-progress>
                  </div>
                  <div style="height: 40px;">
                    <h6>Windows Forms</h6>
                    <n-progress :value="70" type="danger" show-value></n-progress>
                  </div>
                  <div style="height: 40px;">
                    <h6>ASP.NET Core</h6>
                    <n-progress :value="80" type="danger" show-value></n-progress>
                  </div>
                  <div style="height: 40px;">
                    <h6>ASP.NET MVC</h6>
                    <n-progress :value="40" type="danger" show-value></n-progress>
                  </div>
                </div>
                <div class="col-md-4">
                  <div style="height: 40px;">
                    <h6>Unity</h6>
                    <n-progress :value="40" type="danger" show-value></n-progress>
                  </div>
                  <div style="height: 40px;">
                    <h6>Unity 2D</h6>
                    <n-progress :value="50" type="danger" show-value></n-progress>
                  </div>
                  <div style="height: 40px;">
                    <h6>Unity 3D</h6>
                    <n-progress :value="60" type="danger" show-value></n-progress>
                  </div>
                  <div style="height: 40px;">
                    <h6>Unity VR</h6>
                    <n-progress :value="35" type="danger" show-value></n-progress>
                  </div>
                  <div style="height: 40px;">
                    <h6>Unreal Engine 4</h6>
                    <n-progress :value="10" type="danger" show-value></n-progress>
                  </div>
                </div>
                <div class="col-md-4">
                  <div style="height: 40px;">
                    <h6>Web</h6>
                    <n-progress :value="60" type="danger" show-value></n-progress>
                  </div>
                  <div style="height: 40px;">
                    <h6>React JS</h6>
                    <n-progress :value="65" type="danger" show-value></n-progress>
                  </div>
                  <div style="height: 40px;">
                    <h6>Angular</h6>
                    <n-progress :value="45" type="danger" show-value></n-progress>
                  </div>
                  <div style="height: 40px;">
                    <h6>Vue JS</h6>
                    <n-progress :value="25" type="danger" show-value></n-progress>
                  </div>
                  <div style="height: 40px;">
                    <h6>Bootstrap</h6>
                    <n-progress :value="70" type="danger" show-value></n-progress>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- End Skills -->
        <!-- Begin Experiences -->
        <div class="row">
          <div class="col-md-10 ml-auto mr-auto">
            <h4 id="experiences" class="title text-center">Professional Experiences</h4>
            <div class="col-md-20 ml-auto mr-auto">
              <div class="row collections">
                <collapse :animation-duration="500">
                  <div class="col-md-14">
                    <collapse-item title="Accord 139 - Vinci Autoroutes" name="1">
                      <div>Sample tool for management purpose made with WindowsForms framework and VBA with excel suite for Escota (06) area.</div>
                    </collapse-item>
                  </div>
                  <div class="col-md-14">
                    <collapse-item title="Cage - Scientific Games" name="2">
                      <div>International project made in .NET with WPF and ASP.NET Core frameworks used by casino employees.</div>
                    </collapse-item>
                  </div>
                  <div class="col-md-14">
                    <collapse-item title="CubeMX - STMicroElectronics" name="3">
                      <div>Large wispan project made with ReactJS, existing was in C# but very hard to maintain due to the lack of documentation, it's about micro electronics motor manipulation.</div>
                    </collapse-item>
                  </div>
                </collapse>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- End Experiences -->
      <!-- Begin Graduation -->
      <div class="row">
        <div class="col-md-10 ml-auto mr-auto">
          <h4 id="graduation" class="title text-center">Graduation</h4>
          <div class="col-md-10 ml-auto mr-auto">
            <div class="row collections">
              <div class="col-md-4">
                <card style="width: 20rem;">
                  <img
                    slot="image"
                    class="card-img-top"
                    src="img/logo-graduate.jpeg"
                    alt="Graduation logo picture"
                  />
                  <div>
                    <h4 class="card-title">BTS SN IR</h4>
                    <p class="card-text">BAC + 2 - Software Development</p>
                  </div>
                </card>
              </div>
              <div class="col-md-4">
                <card style="width: 20rem;">
                  <img
                    slot="image"
                    class="card-img-top"
                    src="img/logo-graduate.jpeg"
                    alt="Graduation logo picture"
                  />
                  <div>
                    <h4 class="card-title">LP IDSE</h4>
                    <p class="card-text">BAC + 3 - Web Development</p>
                  </div>
                </card>
              </div>
              <div class="col-md-4">
                <card style="width: 20rem;">
                  <img
                    slot="image"
                    class="card-img-top"
                    src="img/logo-graduate.jpeg"
                    alt="Graduation logo picture"
                  />
                  <div>
                    <h4 class="card-title">MASTER MAJIC</h4>
                    <p class="card-text">BAC + 5 - Game Development</p>
                  </div>
                </card>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- End Graduation -->
    </div>
  </body>
  <footer
    class="footer"
    :class="{ [`footer-${type}`]: type }"
    :data-background-color="backgroundColor"
  >
    <div class="container">
      <div class="copyright">&copy; {{ year }}, Made with VUE JS and Now UI kit</div>
    </div>
  </footer>
</div>
</template>
<script>
import {
  Tabs,
  TabPane,
  Progress,
  Collapse,
  CollapseItem,
  Card,
  Badge,
  DropDown,
  NavbarToggleButton,
  Navbar,
  NavLink
} from "@/components";

import { Carousel, CarouselItem, Popover } from "element-ui";

export default {
  name: "profile",
  props: {
    transparent: Boolean,
    colorOnScroll: Number,
    backgroundColor: String,
    type: String
  },

  data() {
    return {
      year: new Date().getFullYear()
    };
  },

  bodyClass: "profile-page",
  components: {
    Tabs,
    TabPane,
    [Progress.name]: Progress,
    [Carousel.name]: Carousel,
    [CarouselItem.name]: CarouselItem,
    [Badge.name]: Badge,
    Collapse,
    CollapseItem,
    Card,
    DropDown,
    Navbar,
    NavbarToggleButton,
    NavLink,
    [Popover.name]: Popover
  }
};
</script>

<style/>
