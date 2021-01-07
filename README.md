# portfolio-do-hackathon #

<!--- See https://shields.io for others or to customize this set of shields.  --->

![GitHub repo size](https://img.shields.io/github/repo-size/dennislwm/portfolio-do-hackathon?style=plastic)
![GitHub language count](https://img.shields.io/github/languages/count/dennislwm/portfolio-do-hackathon?style=plastic)
![GitHub top language](https://img.shields.io/github/languages/top/dennislwm/portfolio-do-hackathon?style=plastic)
![GitHub last commit](https://img.shields.io/github/last-commit/dennislwm/portfolio-do-hackathon?color=red&style=plastic)
![GitHub stars](https://img.shields.io/github/stars/dennislwm/portfolio-do-hackathon?style=social)
![GitHub forks](https://img.shields.io/github/forks/dennislwm/portfolio-do-hackathon?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/dennislwm/portfolio-do-hackathon?style=social)
![GitHub followers](https://img.shields.io/github/followers/dennislwm?style=social)
<span class="badge-buymeacoffee"><a href="https://ko-fi.com/dennislwm" title="Donate to this project using Buy Me A Coffee"><img src="https://img.shields.io/badge/buy%20me%20a%20coffee-donate-yellow.svg" alt="Buy Me A Coffee donate button" /></a></span>
<span class="badge-patreon"><a href="https://patreon.com/dennislwm" title="Donate to this project using Patreon"><img src="https://img.shields.io/badge/patreon-donate-yellow.svg" alt="Patreon donate button" /></a></span>

# Getting Started #

These steps will get this sample application running for you using DigitalOcean.

**Note: Following these steps will result in charges for the use of DigitalOcean services**

## Table of Contents
- [portfolio-do-hackathon](#portfolio-do-hackathon)
- [Getting Started](#getting-started)
  - [Table of Contents](#table-of-contents)
  - [Requirements](#requirements)
  - [Forking the Sample App Source Code](#forking-the-sample-app-source-code)
  - [Deploying the App](#deploying-the-app)
  - [Making Changes to Your App](#making-changes-to-your-app)
  - [Learn More](#learn-more)
  - [Deleting the App](#deleting-the-app)
- [Customizing the Homepage](#customizing-the-homepage)
    - [Project Structure](#project-structure)
  - [Enabling a Section](#enabling-a-section)
- [Advanced Customization](#advanced-customization)
    - [Themes Structure](#themes-structure)
  - [Adding a Section](#adding-a-section)
  - [📫 How to reach me](#-how-to-reach-me)
  - [Python, R and Metatrader for Happi Traders](#python-r-and-metatrader-for-happi-traders)
  - [FREE $100 CREDIT](#free-100-credit)
  
## Requirements

* You need a DigitalOcean account. If you don't already have one, you can sign up at [DigitalOcean.com](https://yourls.fxgit.work/001affdo)
    
## Forking the Sample App Source Code

To use all the features of App Platform, you need to be running against your own copy of this application. To make a copy, click the Fork button above and follow the on-screen instructions. In this case, you'll be forking this repo as a starting point for your own app (see [Github documentation](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo) to learn more about forking repos.

After forking the repo, you should now be viewing this README in your own github org (e.g. `https://github.com/<your-org>/sample-hugo`)

**Note:** You can skip forking this repo and select the "Hugo" sample from the app creation page, however do notice that certain features will be disabled.

## Deploying the App ##

Click this button to deploy the app to the DigitalOcean App Platform.

 [![Deploy to DO](https://mp-assets1.sfo2.digitaloceanspaces.com/deploy-to-do/do-btn-blue.svg)](https://cloud.digitalocean.com/apps/new?repo=https://github.com/dennislwm/portfolio-do-hackathon/tree/main)

## Making Changes to Your App ##

As long as you left the default Autodeploy option enabled when you first launched this app, you can now make code changes and see them automatically reflected in your live application. During these automatic deployments, your application will never pause or stop serving request because the App Platform offers zero-downtime deployments.

## Learn More ##

You can learn more about the App Platform and how to manage and update your application at https://www.digitalocean.com/docs/app-platform/.

## Deleting the App #

When you no longer need this sample application running live, you can delete it by following these steps:
1. Visit the Apps control panel at https://cloud.digitalocean.com/apps
1. Navigate to the sample-hugo app
1. Choose "Settings"->"Destroy"

This will delete the app and destroy any underlying DigitalOcean resources.

**Note: If you don't delete your app, charges for the use of DigitalOcean services will continue to accrue.**

# Customizing the Homepage #

You can customize the homepage by editing the **homepage.yml** file located in the folder *data*.

### Project Structure
     root/                            <-- Root of your project
       |- config.black-and-light.toml <-- Config file for black-and-light theme
       |- config.toml                 <-- Config file for somrat theme (DEFAULT)
       +- .do/                        <-- Holds any DO deployment file
       +- content/                    <-- Holds any blog articles (NOT USED by somrat theme)
       +- data/                       <-- Holds any homepage file (copied from somrat exampleSite)
       +- layouts/                    <-- Holds any partial file (NOT USED by somrat theme)
       +- resources/                  <-- Holds any resource file (NOT USED by somrat theme)
       +- static/                     <-- Holds any static file (copied from somrat exampleSite)
       +- themes/                     <-- Holds any Hugo theme

## Enabling a Section ##

It is trivial to enable or disable a section within the homepage.

Open the file **homepage.yml**, find the relevant section and edit the setting to **true** or **false**. For example:

```
portfolio:
  enable : true
```

The menu must be enabled or disabled separately within the config.

Open the file **config.toml**, find the relevant menu and comment or uncomment the setting. For example, to disable the menu:

```
#[[menu.main]]
#URL = "#portfolio"
#name = "Portfolio"
#weight = 4
```

---
# Advanced Customization #

If you require more advanced customization, such as HTML/JS/CSS, than is permissible from the config file, you will have to modify the files under *themes* folder.

### Themes Structure
     root/                            <-- Root of your project
       +- themes/                     <-- Holds any Hugo theme
          +- somrat/                  <-- Theme as a git submodule
             |- index.html            <-- Default HTML index file used to render homepage.yml
             |- 404.html              <-- Default HTML error file
             +- assets/               <-- Holds any CSS/JS file
                +- css/               <-- Holds any CSS file
                +- js/                <-- Holds any JS file
             +- layouts/              <-- Holds any partial file

## Adding a Section ##

To add a new section within the homepage:

* Add a new section in **homepage.yml**
* Add a new section in **index.html**
* Add a new menu in **config.toml**

1. Open the file **homepage.yml**, copy and paste a new section. For example:

```
############################## rank #################################
rank:
  enable: true
  title: "GLOBAL RANK"
  rank_list:
    - name: "Summary"
      link: https://cr-ss-service.azurewebsites.net/api/ScreenShot?widget=summary&username=dennislwm

    - name: "Skills Chart"
      link: https://cr-skills-chart-widget.azurewebsites.net/api/api?username=dennislwm
```

2. Open the file **index.html**, copy and paste a new section. For example:

```
<!-- =============================
      Start Rank
    =============================== -->
<section class="rank" id="rank">
  {{ if $data.homepage.rank.enable }}
  {{ with $data.homepage.rank }}
  <div class="container">
    <div class="row">
      <div class="col-lg-12 mx-auto col-sm-10">
        <div class="wow fadeInUp" data-wow-duration="1.5s">
          <div class="rank-heading">
            <div class="bar"></div>
            <h1>{{ .title }}</h1>
          </div>
          <div class="row">
            {{ range .rank_list }}
            <div class="col-lg-12 mx-auto col-sm-10">
              <div class="rank-label">
                <h4 style="margin-top:10px">{{ .name | markdownify }}</h4>
                <img class="rank-img img-fluid" src="{{ .link | absURL }}" alt="{{ .name | markdownify }}">
              </div>
              <!--<div class="rank-label">{{ .name | markdownify }}</div>-->
            </div>
            {{ end }}
          </div>
        </div>
      </div>
    </div>
  </div>
  {{ end }}
  {{ end }}

</section>
<!-- =============================
           End Rank
        =============================== -->
```

3. Open the file **config.toml**, copy and paste a new menu. For example:

```
[[menu.main]]
URL = "#rank"
name = "Rank"
weight = 4
```

## 📫 How to reach me ##
<p>
<a href="https://yourls.fxgit.work/a006"><img src="https://img.shields.io/badge/twitter-%231DA1F2.svg?&style=for-the-badge&logo=twitter&logoColor=white" height=25></a> 
<a href="https://yourls.fxgit.work/a008"><img src="https://img.shields.io/badge/medium-%2312100E.svg?&style=for-the-badge&logo=medium&logoColor=white" height=25></a> 
<a href="https://yourls.fxgit.work/a004"><img src="https://img.shields.io/badge/DEV.TO-%230A0A0A.svg?&style=for-the-badge&logo=dev-dot-to&logoColor=white" height=25></a>
<a href="https://yourls.fxgit.work/a007"><img src="https://img.shields.io/badge/-YouTube-red?&style=for-the-badge&logo=youtube&logoColor=white" height=25></a>
</p>
<p>
<span class="badge-buymeacoffee"><a href="https://ko-fi.com/dennislwm" title="Donate to this project using Buy Me A Coffee"><img src="https://img.shields.io/badge/buy%20me%20a%20coffee-donate-yellow.svg" alt="Buy Me A Coffee donate button" /></a></span>
<span class="badge-patreon"><a href="https://patreon.com/dennislwm" title="Donate to this project using Patreon"><img src="https://img.shields.io/badge/patreon-donate-yellow.svg" alt="Patreon donate button" /></a></span>
</p>

* 🔭 I’m currently working on Github Actions for Python and publish on Netlify
* 🌱 I’m currently learning [freecodecamp](https://freecodecamp.org)
* 👯 I’m looking to collaborate on [Darwinex ZeroMq Connector](https://github.com/dennislwm/dwx-zeromq-connector) 
* 🤔 I’m looking for help with [Blender](https://blender.org)
* 💬 Ask me about Any Geek stuff
* 😄 Pronouns: happi, grateful
* ⚡ Fun fact: I'm a Star Wars fan

![GitHub metrics](https://metrics.lecoq.io/dennislwm?isocalendar=1&languages=1&followup=1&pagespeed=1&pagespeed.detailed=true)

## Python, R and Metatrader for Happi Traders

[https://fxgit.work](https://yourls.fxgit.work/a001)

## FREE $100 CREDIT

[https://digitalocean.com](https://yourls.fxgit.work/001affdo)
