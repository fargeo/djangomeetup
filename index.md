title: <img src="https://www.archesproject.org/wp-content/uploads/2017/03/arches-logo-tm-only.svg" alt="Arches:" id="logo" width="86vw"> a look under the hood of a platform that allows the deployment of custom apps without writing code
class: animation-fade
layout: true

<!-- This slide will serve as the base layout for all your slides -->
.bottom-bar[
  {{title}}
]

---

class: impact

<img src="https://www.archesproject.org/wp-content/uploads/2017/03/arches-logo-tm-only.svg" alt="Arches:" id="logo" data-height-percentage="10" data-actual-width="300" data-actual-height="67">
## a look under the hood of a platform that allows the deployment of custom apps without writing code
## Nov. 29, 2017, Django Meetup

---
<!-- Adam -->

# Farallon Geographics
.row[
.col-4[
[<img src="http://fargeo.com/cms/wp-content/uploads/2015/09/logo.png" alt="Farallon Geographics" height="80px" style="float:right;margin-right:20px;">](http://www.fargeo.com)
]

]
- Focus on Geospatial
- Business Analysis/Needs Assessment
- Web, Mobile, Desktop Solutions Developers

## Today's Team
.row[
.col-4[
<img src="http://fargeo.com/cms/wp-content/uploads/2015/12/jeff-gray.jpg" alt="Jeff Munowitch" height="80px" style="float:right;margin-right:20px;">
]
.col-8[
Jeff Munowitch <!-- GIS Generalist, Web Developer -->
]
]

.row[
.col-4[
<img src="http://fargeo.com/cms/wp-content/uploads/2015/12/rob-gray.jpg" alt="Rob Gaston" height="80px" style="float:right;margin-right:20px;">
]
.col-8[
Rob Gaston <!-- Master Front-end Developer, but really also quite good at everything else -->
]
]




---
<!-- Adam -->

# What we want from this talk
- Show off Arches
- Solicit Ideas and Technical Improvements
- Grow the Community by getting more people deploying, using, developing on and knowing about Arches

---
<!-- Cyrus -->
# What is Arches?

Arches is an open-source, geospatially-enabled software platform for cultural heritage inventory and management, developed jointly by the Getty Conservation Institute and World Monuments Fund. 

Fill in more

## What Arches Does

"Arches is a platform for building applications [without custom code]"

Brief Backstory on problem to solve: Data Management with no set Data Model 

FILL IN INFO

---
<!-- Ryan -->
# How Arches Does it with Django

Django is a high-level Python Web framework that encourages rapid development and clean, pragmatic design

FILL IN INFO

---
<!-- Jeff -->
## Full Technology Stack

and where django fits in
PostgreSQL/PostGIS
ElasticSearch
Django
Knockout/Backbone
Mapbox GL JS

FILL IN IMAGES of all the tech

---
<!-- Rob -->
# Arches in action
As a business system, Arches has three main purposes:

1. Data discovery and visualization
    - Contextual search and visualization tools (strings, concepts, geospatial, temporal)
    - Reports
2. Data management
    - dynamic forms for managing business data
    - "Reference Data Manager" for managing shared thesauri
    - "Arches designer" for creating custom schema and forms without coding
3. Data integration and analysis
    - "Map layer manager" for integrating mapping UI with GIS assets
    - data export tools
    - API and geospatial services

---
<!-- Jeff -->
# Future Challenges

- Ongoing Community Building
- Containerization in Production/Development
- Python 3/Django 2
- ????
