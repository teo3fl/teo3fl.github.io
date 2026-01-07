---
layout: default
title: About
permalink: /about
---

<style>
  .about-layout {
    display: flex;
    gap: 32px;
    align-items: flex-start;
    margin-top: 20px;
  }

  .about-text {
    flex: 2;
  }

  .about-photo {
    flex: 1;
    display: flex;
    justify-content: center;
  }

  .about-photo img {
    display: block;
    max-width: 220px;
    width: 100%;
    border-radius: 4px;
    border: 1px solid var(--green);
    box-shadow: 0 0 10px var(--green-alpha-25);
  }

  @media (max-width: 800px) {
    .about-layout {
      flex-direction: column;
      align-items: stretch;
    }

    .about-photo {
      margin-top: 16px;
      justify-content: center;
      width: 100%;
    }

    .about-photo img {
      max-width: 180px;
      width: 100%;
      margin: 0 auto;
    }
  }

  .closing-links {
    margin-top: 14px;
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }

  .closing-links a {
    display: inline-flex;
    padding: 5px 12px;
    border-radius: 4px;
    border: 1px solid var(--green);
    color: var(--green);
    text-decoration: none;
    font-size: 0.85rem;
    transition:
      box-shadow 0.25s ease,
      border-color 0.25s ease,
      transform 0.25s ease,
      opacity 0.25s ease;
  }

  .closing-links a:hover {
    border-color: var(--green);
    box-shadow:
      0 0 4px var(--green-alpha-45),
      0 0 8px var(--green-alpha-30),
      0 0 12px var(--green-alpha-12);
    transform: translateY(-1px);
    opacity: 0.9;
  }
</style>

<section>
  <h1>About Me</h1>

  <div class="about-layout">
    <div class="about-text">
      <p>
        I have graduated from Transylvania University of Brașov with a Bachelor’s Degree 
        in Informatics (2021), and I chose to study this field because I wanted to become 
        a game developer. I would say that games are the point where art meets programming, 
        and I'm an artsy person as much as I'm interested in the technical aspect of games.
      </p>
      <p>
        In terms of Unity development, I am most familiar with systems programming, gameplay 
        programming, UI implementation, AI behavior implementation for NPCs, and the 3D 
        environment (though I have also worked on 2D projects).
      </p>
      <p>
        Although my main area of expertise is Unity, I have also made a few games using C++ 
        and the SFML library, and one in Unreal. I am also interested in artificial intelligence, 
        as my Bachelor's Degree thesis and some of my personal projects are strongly based on it.
      </p>
      <p>
        Besides programming, I have been teaching myself sound editing and music theory as well. 
        This skill has proven useful for both work projects and personal ones, as I was able to 
        provide sound effects on a short notice and within a short amount of time. I also produced 
        music for many of my personal projects.
      </p>
      <div class="closing-links">
        {% assign cv = site.socials | where: "name", "cv" | first %}
        <a href="{{ cv.url }}">Resume</a>
        {% assign linkedin = site.socials | where: "name", "linkedin" | first %}
        <a href="{{ linkedin.url }}" target="_blank" rel="noopener noreferrer">LinkedIn</a>
      </div>
    </div>
    <div class="about-photo">
      <img
        src="/assets/images/profile.png"
        alt="Portrait of author"
        loading="lazy"
      >
    </div>
  </div>
</section>
