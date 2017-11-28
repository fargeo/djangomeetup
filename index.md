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

## Farallon Geographics
.row[
.col-4[
[<img src="http://fargeo.com/cms/wp-content/uploads/2015/09/logo.png" alt="Farallon Geographics" height="80px" style="float:right;margin-right:20px;">](http://www.fargeo.com)
]
.col-8[
- Focus on Geospatial
- Business Analysis/Needs Assessment
- Web, Mobile, Desktop Solutions Developers
]
]

## Today's Team
.row[
.col-2[
<img src="http://fargeo.com/cms/wp-content/uploads/2015/12/jeff-gray.jpg" alt="Jeff Munowitch" height="170px" style="float:right;margin-right:20px;">
]
.col-4.bio[
Jeff Munowitch <!-- GIS Generalist, Web Developer -->
]
.col-2[
<img src="http://fargeo.com/cms/wp-content/uploads/2015/12/rob-gray.jpg" alt="Rob Gaston" height="170px" style="float:right;margin-right:20px;">
]
.col-4.bio[
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

- Backstory: Data management with no set data model
- A open-source (GNU AGPL) platform for building geospatial applications [without custom code]
- Designed for cultural heritage inventory, but widely applicable to other use cases
- Joint effort by Getty Conservation Institute and World Monuments Fund

---
## What Arches Provides

- A UI to develop complex data models (graphs)
- Search interface - keyword, numeric, boolean, temporal, geospatial, or combination thereof
- A thesauri management interface (optionally using ontology standards)
- Geospatial vector tile caching/services via TileStache
- A means of extension through custom widgets and datatypes
- Language localization

---
<!-- Rob -->
# Arches in action
As a business system, Arches has three main purposes:

1. Data discovery and visualization
    <!-- - Contextual search and visualization tools (strings, concepts, geospatial, temporal) -->
    <!-- - Reports -->
2. Data management
    <!-- - dynamic forms for managing business data -->
    <!-- - "Reference Data Manager" for managing shared thesauri -->
    <!-- - "Arches designer" for creating custom schema and forms without coding -->
3. Data integration and analysis

---
<!-- Ryan -->
# How Arches Does it with Django

Django is a high-level Python Web framework that encourages rapid development and clean, pragmatic design

---
## MVT Pattern

[FILL IN TEXT]
---
## Migrations

[FILL IN TEXT]
---
## Security

- Arches uses Django security to authenticate users, and provide different levels of user permissions.

- Permissions are managed in the Arches permissions manager and in the Django admin interface.

- Arches utilizes both Django-included and custom password validators. Extends default validators to use custom help text.

---
<span style="font-size: 0.7em;">
```
AUTH_PASSWORD_VALIDATORS = [
    {
        'NAME': 'arches.app.utils.password_validation.NumericPasswordValidator',
    },
    {
        'NAME': 'arches.app.utils.password_validation.SpecialCharacterValidator',
        'OPTIONS': {
            'special_characters': ('!','@','#',')','(','*','&','^','%','$'),
        }
    },
    {
        'NAME': 'arches.app.utils.password_validation.HasNumericCharacterValidator',
    },
    {
        'NAME': 'arches.app.utils.password_validation.HasUpperAndLowerCaseValidator',
    },
    {
        'NAME': 'arches.app.utils.password_validation.MinLengthValidator',
        'OPTIONS': {
            'min_length': 9,
        }
    },
]
```
</span>


---
## Localization

- MegaJ included localization to Arabic, but using .NET framework.

- Arches developers can easily internationalize static content with Django.

- Internationalization allows Arches to be instantly ready for localization.


---
## Project Paradigm

- Arches itself designed to be customized. Not just the data model.

- We created a command, inspired by Django, to deploy the framework of your own Arches project.

- Allows implementors to create and modify their own templates without overwriting core Arches code.

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
<!-- Jeff -->
# Future Challenges

- Ongoing Community Building
- Containerization in Production/Development
- Python 3/Django 2
- ????
