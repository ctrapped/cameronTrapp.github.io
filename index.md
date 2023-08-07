---
layout: page
name: index
title: Caleb Choban
description: >
  Personal Website of Caleb Choban, a PhD student in Physics at UC San Diego.
hide_description: true
cover: true
---
<!-- <script type="text/javascript">
	document.getElementsByClassName("page-title")[0].classList.add("sr-only");
</script> -->

<style type="text/css">
	.page-title {
		position: absolute;
		width: 1px;
  		height: 1px;
  		margin: -1px;
  		border: 0;
  		padding: 0;
  		clip: rect(0 0 0 0);
  		overflow: hidden;
	}
</style>

<h2 class="h1" style="color: {{site.theme_color}}" id="about">About Me </h2>

 I'm Caleb Choban, a PhD candidate in [Physics](https://physics.ucsd.edu/) and [Astronomy](https://astronomy.ucsd.edu/) at UC San Diego working in collaboration with Prof. [Dušan Kereš](https://cass.ucsd.edu/index.php/faculty:Dkeres). My research focuses on modeling dust, its life cycle, and its effects on and interactions with the interstellar medium (ISM), utilizing cosmological zoom-in simulations as part of the Feedback in Realistic Environments ([FIRE](https://fire.northwestern.edu/)) project. I am currently interested in how incorporating 'live' dust evolution models affects how galaxies evolve and utilizing these models to determine the expected dust extinction curves and emission spectra in various gas and galactic environments to help interpret and guide observations. I am also interested in how we model ISM physics, particularly chemical networks and radiative transfer in the ISM. 


<figure>
    <img align="right"  width="500" height="100" src="./assets/img/2019_space_day.jpg">
</figure>

Beyond research, I serve as a class representative on the Physics Graduate Council ([PGC](https://sites.google.com/a/physics.ucsd.edu/physics-graduate-council/)) interfacing with department committees and chair to advocate for the graduate population. My recent endeavors include backing an increase in graduate stipends to reduce rent burden and improving work-life balance for first-year students by establishing a flexible teaching workload. During my tenure, I founded a physics mentorship program pairing undergraduate mentees with graduate mentors to provide students guidance on various challenges ranging from graduate school applications to course selection. I am also interested in community outreach, teaching extracurricular labs for local public schools, leading Python coding and research workshops for transfer and local community college students, and running astronomy and physics demonstrations at numerous public science events.

In my spare time I enjoy camping and hiking in national parks, cycling and walking around the beautiful California coastline, and playing a good board game.


![Expo Day 2020](./assets/img/2020_expo_day.jpg){: width="500" height="100" loading="lazy"} 


<div class="body-social sidebar-social">
  <ul>
    <li> <a href="https://www.linkedin.com/in/cchoban" title="LinkedIn" class="no-mark-external" target="_blank"> <span class="icon-linkedin2"></span> <span aria-hidden="true">LinkedIn </span><span class="sr-only">LinkedIn profile</span></a></li>
    <li> <a href="https://orcid.org/0000-0001-9200-169X" title="Orcid" class="no-mark-external" target="_blank"> <span class="icon-orcid2"></span> <span aria-hidden="true">Orcid </span><span class="sr-only">LinkedIn profile</span></a></li>
    <li> <a href="https://twitter.com/cchoban" title="Twitter" class="no-mark-external" target="_blank"> <span class="icon-twitter"></span> <span aria-hidden="true">Twitter </span><span class="sr-only">Twitter profile</span></a></li>
    
  </ul>
</div>

[![FIRE logo](./assets/img/FIRE_logo.jpg){: width="250" height="100" loading="lazy"}](https://fire.northwestern.edu/)




---
<h2 class="h1" style="color: {{site.theme_color}}" id="research">Research </h2>

<h3 class="h2">Interstellar Dust</h3>


Although it constitutes only 1% of the ISM by mass, dust is integral to the physics within. It provides a surface for astrochemistry such as H<sub>2</sub> formation, facilitating the formation of molecular clouds and indirectly stars. It is a key coolant in extremely dense environments, is the primary heat source via the photoelectric effect in neutral phases of the ISM, and can reduce the abundance of important gas coolants which allow gas to cool and collapse. Dust also affects how the ISM reacts to radiation pressure and might help drive galactic winds, which can be crucial for shaping galaxy evolution. Observationally, dust absorbs ultraviolet/optical light and emits in the infrared affecting all astronomical observations to varying degree (check out the image below to see what a Milky Way-like galaxy looks like with and without dust). For instance, the amount of dust and its spatial distribution relative to stars affects the galactic stellar spectral energy distribution (SED) and influences how we interpret observed SEDs.

For a cool animated video explaining dust check out the video below featuring Prof. [Karin Sandstrom](http://karinsandstrom.github.io/), one of my collaborators.


<!-- Put image and youtube video in a table to make them side by side -->
<table><tr>
<td style="width:50%;background:transparent;border:none;" >
<img width="500" height="600" src="./assets/img/dust_no_dust_galaxy.jpg"></td>
<td style="width:50%;background:transparent;border:none;">
<iframe width="560" height="315" src="https://www.youtube.com/embed/8bRy5VDJsTI" frameborder="0" allow="encrypted-media;" allowfullscreen></iframe></td>
</tr></table>





Interstellar dust also has a complicated life cycle composed of processes during which they can be created, destroyed, grown, or eroded. 

<figure>
    <img align="right" width="600" height="100" src="./assets/img/dust_lifecycle.jpg" style="margin:0px 50px">
</figure>

  * **Dust Creation**: The initial seeds' of the dust population are created in the stellar ejecta of SNe and AGB winds where a portion of ejected metals condense into dust. Once these 'seeds' have been created they spend their life in the ISM and/or the galactic halo where they are exposed to various processes. 
  * **Gas-Dust Accretion**: In cool, dense phases of the ISM, gas-phase metals accrete onto the surface of preexisting dust grains growing the grains over time. This is believed to be the main source of dust mass in the MW. 
  * **SNe Shocks**: As supernovae remnants propagate through the ISM they destroy and shatter dust grains residing in the ISM via grain-grain collisions, thermal sputtering, and non-thermal sputtering. This is believed to be the main destroyer of dust in the MW. 
  * **Astration**: As gas cools and collapses forming stars, dust residing in said gas is also destroyed and contributes to the stellar metallicity. 
  * **Thermal Sputtering**: Dust grains residing in hot gas, such as in the galactic halo, are eroded and destroyed by energetic atoms.


<h3 class="h2">Modeling Dust Evolution in Cosmological Zoom-In Simulations</h3>



Observations find diverse dust scaling relations which suggest a complex dust system depending heavily on local gas properties, but many galaxy formation models do not capture this, treating dust in post-processing or assume a constant dust-to-metals ratio (D/Z=0.4). Recent strides have been made developing dust evolution models for galaxy formation simulations but these approaches vary in their assumptions and degree of complexity. Based on these approaches I developed two separate dust evolution models (labelled 'Elemental’ and 'Species’) which include the main mechanisms comprising the dust life cycle mentioned above and incorporated them into the magneto-hydrodynamics GIZMO code coupled to the FIRE-2 model for stellar feedback and ISM physics. The “Elemental” model tracks the evolution of generalized dust species and utilizes a simple, ‘tunable’ dust growth routine, while the “Species” model tracks the evolution of specific dust species with set chemical compositions and incorporates a physically motivated, two-phase dust growth routine. Utilizing idealized Milky Way-like galaxy simulations, I demonstrated that while both models can produce reasonable galaxy-integrated results, the dust by 'Species' approach reproduces the diverse dust scaling relations observed in the MW.



Currently I am investigating how dust evolves over cosmic time utilizing fully cosmological simulations of Milky Way-like and dwarf galaxies and how incoporating 'live' dust evolution and physics in these simulations affects how galaxies evolve.








<!-- <h3 class="h2">Past Projects</h3>
**FILL IN**    
*Advisor: [Adam Burgasser](https://cass.ucsd.edu/index.php/faculty:Aburgasser)*

Description -->

---
<h2 class="h1" style="color: {{site.theme_color}}" id="publications">Publications </h2>

A full list of my publications can be found on ADS [here](https://ui.adsabs.harvard.edu/public-libraries/-Gcrfa83Qq2xs8ndJylF0A).


<!--   
<h3 class="h2">First Author Publications</h3>



<h3 class="h2">Presentations</h3>
 -->
  

---
<h2 class="h1" style="color: {{site.theme_color}}" id="contact">Contact </h2>



Center for Astrophysics and Space Sciences (CASS)   
University of California San Diego   
9500 Gilman Drive   
La Jolla, CA 92093, USA

**cchoba<!-- tyewcnpy -->n [a<!-- juygv -->t] u<!-- tregbijd -->cs<!-- rzyjide --->d [dot] edu**
{:.lead}


<style type="text/css">
  .body-social > ul {
    display: inline-block;
    list-style-type: none;
    margin-bottom: 0;
    overflow: hidden;
    padding: 0;
  }

  .body-social > ul > li {
    float: left;
    
    /* padding-left: 5px; */
    padding-right: 10px;
    
    /* display: inline-block; */
  }


  .body-social > ul > li > a {
    display: inline;
    text-align: center;
    font-size: 0.95rem;
    font-weight: 600;
    /*width: 3rem;*/
    /*height: 4rem;*/
    padding: 4px;
    
    /* line-height: 3rem; */
    
    text-decoration: none;
    border-width: 1px;
    border-style: solid;
    border-radius: 5px;
    transition: background-color 250ms, color 250ms, text-decoration-color 250ms, border-color 250ms;
    
    /* border-bottom: none; */
  }

  .body-social > ul > li > a:not(.btn):not(.no-hover) {
    border-color: var(--accent-color);
  }

  .body-social > ul > li > a:hover {
    color: white;
    background-color: var(--accent-color);
    border-radius: 5px;
    padding: 4px;
    transition: background-color 250ms, color 250ms, text-decoration-color 250ms, border-color 250ms;
  }
</style>
