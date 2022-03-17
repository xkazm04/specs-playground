# Strapi CMS at Tatum

Initial document to describe concept how to use Strapi in Tatum Dev portal or any other web product.

## Introduction

![diagram-how-strapi-headless-cms-node-js-works.png](https://stoplight.io/api/v1/projects/cHJqOjExMTMxNA/images/i5LapX5c7lw)

Main motivation of using headless CMS (Content management system) are

- Content management by **non-devs** (marketing, business, copywriters)
- **Scalable** solution to manage hundreds of articles in various languages

#### Advantages of headless CMS

- **Omnichannel architecture** - Tatum is able to control via Strapi main Web, Dev portal or mobile apps as it uses API-driven approach which is programming language agnostic.
- **Cost effective** - Strapi CMS is free to use without performance limitations with ability to be deployed on local server &amp; database

#### Main disadvantages 

- **Dev dependency** - Even content could be managed by business, there is need initially to set rules how to create content, to deploy and maintain servers CMS is running on - these activities require developer attention with each major change in content structure
- **Adoption** - In comparison with Wordpress modules there are limited features created by the community as headless CMS experienced growth in the last 2-3 years while Wordpress is used frequently for almost two decades.

---

## Roles & Permissions

Available application roles:

- `Admin` - Able to invite new users into application, change their roles and set visibility of API endpoints. Any developer participating in CMS should have this role also to add new features or enhance existing with new parameters.
- `Editor` - Allows to create or edit any content for existing CMS templates. It means if some feature is already implemented - you can manage its content.

To become `Admin` or `Editor` access link is required from current administrator in Slack channel "**developers**". 


## Modules

**Content-types builder** - Module for devs to create database collections, create API and display in web application

How to create/update collection

```
1. Get current version

$ git clone --branch feature/strapi https://gitlab.com/tatum-io/developer-tools/dev-portal-strapi-cms.git

2. Fill .env (on request)

3. Run local environment

$ npm install
$ npm run develop

4. Create collection fields from specific data types*
5. Configure view for content managers in logical order (optional)
6. Set visibility of collection, authentication rules. Define API endpoint for collection
7. Push changes into repository

$ git add .
$ git commit
$ git push origin
```

<div class="toolbar-note">
Strapi CMS supports follow api methods: Create, Delete, Update, FindOne, Find
</div>

#### Collection data types 

Data types | Usage example | 
---------|----------|
 Short text | Titles | 
 Long text | Descriptions | 
 Rich text | Markdown articles |
 Number | Article order | 
 Enum | Article categorization | 
 Boolean | Environment specification |  
 JSON | Hiearchical tree representation | 

---


## Strapi references

- https://strapi.io/
- https://www.youtube.com/strapi



