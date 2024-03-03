---
layout: page
permalink: /organizers/
title: Organizers
description:
nav: true
nav_order: 8

people:
  - name: Mariona Taulé
    description: CLiC Research Group
    uni: Universitat de Barcelona
    website: https://clic.ub.edu/m_taule
    picture: m_taule.jpg

  - name: Simona Frenda
    description:
    uni: Universitá Degli Studi di Torino
    website: https://www.di.unito.it/~frenda/
    picture: s_frenda.jpeg

  - name: Wolfgang S. Schmeisser-Nieto
    description: CLiC Research Group
    uni: Universitat de Barcelona
    website: https://clic.ub.edu/ws_schmeisser
    picture: w_schmeisser.jpg

  - name: Pol Pastells
    description: CLiC Research Group
    uni: Universitat de Barcelona
    website: https://pastells.github.io
    picture: p_pastells.jpg

  - name: Alejandro Ariza-Casabona
    description: CLiC Research Group
    uni: Universitat de Barcelona
    website: https://clic.ub.edu/a_ariza
    picture: a_ariza.jpg

  - name: Mireia Farrús
    description: CLiC Research Group
    uni: Universitat de Barcelona
    website: https://clic.ub.edu/m_farrus
    picture: m_farrus.jpg

  - name: Paolo Rosso
    description: PRHLT Research Center
    uni: Universitat Politècnica de València
    website: https://personales.upv.es/prosso/
    picture: p_rosso.jpg
---

<div class="grid">
    {%- for person in page.people -%}
    <article class="grid-item card">
        {% if person.picture -%}
        <img class="avatar" src="/assets/img/{{person.picture}}" alt="Portrait ({{person.name}})" width="auto" height="auto">
            {%- else -%}
        <img class="avatar" src="/assets/img/mainlp-logo-500.png" alt="Portrait ({{person.name}})" width="auto" height="auto">
            {%- endif -%}
        <div class="card-body">
            <!-- <h2 class="card-title">{{person.name}}</h2> -->
            <h2 class="card-title">
                {% if person.website -%}
                <a href="{{person.website}}">{{person.name}}</a>
                {%- else -%}
                {{person.name}}
                {%- endif -%}
            </h2>
            <div class="card-text">
                {{person.description}}
                {{person.uni}}
                <!-- <p style="margin-bottom: 0rem;">{{person.description}}</p>
                <ul class="network-icon" aria-hidden="true">
                {% if person.website -%}
                <li><a href="{{person.website}}"><i class="fas fa-globe"></i></a></li>
                {%- endif -%}
                {% if person.email -%}
                <li><a role="button" class="email" style="color: var(--global-theme-color)"><i class="fas fa-envelope"></i></a></li>
                {%- endif -%}
                {% if person.googlescholar -%}
                <li><a href="{{person.googlescholar}}"><i class="ai ai-google-scholar"></i></a></li>
                {%- endif -%}
                {% if person.github -%}
                <li><a href="{{person.github}}"><i class="fab fa-github"></i></a></li>
                {%- endif -%}
                {% if person.twitter -%}
                <li><a href="{{person.twitter}}"><i class="fab fa-twitter"></i></a></li>
                {%- endif -%}
                </ul>
                {% if person.email -%}
                <div class="email hidden">
                <p>{{ person.email }}</p>
                </div>
                {%- endif -%} -->
            </div>
        </div>
    </article>
    {%- endfor -%}
  </div>

## Funding

STERHEOTYPES: STudying European Racial Hoaxes and sterEOTYPES (S129542). Program: Challenge for Europe.
Participants: Universitat de Barcelona (UB). International project funded by Compagnia di San Paolo.
{% include figure.html path="assets/img/sanpaolo.png" class="img-fluid rounded z-depth-1" width="200"%}

FairTransNLP-Language: Analysing toxicity and stereotypes in language for unbiased, fair and transparent
systems (PID2021-124361OB-C33). Funded by Ministerio de Ciencia, Innovación y Universidades, programa de
I+D de Generación de Conocimiento. MCIN/AEI/10.13039/501100011033/FEDER,UE.
{% include figure.html path="assets/img/logos-ministerio.png" class="img-fluid rounded z-depth-1" width="400"%}
