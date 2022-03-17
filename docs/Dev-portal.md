# Developer portal

- **Repo**: https://gitlab.com/tatum-io/websites/docs
- **Deployment guide:**  https://docs.google.com/document/d/1EPaWzWl8_7vn1NriKqd1cpUGMbedDj5uRdKcm2wljNw/edit#heading=h.9583zrq68fqy
- **Available at:** https://docs.tatum.io/ 

![image.png](https://stoplight.io/api/v1/projects/cHJqOjExMTMxNA/images/f7wcV4BbB78)

Developer portal was created to merge and replace multiple documentation sources used in Tatum separated in several modules:
- **API references** rendered via **Stoplight studio** (3rd party tool)
- **Markdown renderer** to visualize guides & tutorial coming from **Strapi CMS**
- **Products** with references to repositories and community projects 
- **Support** module to guide users to discord, help with blockchain terminology and show most recent updates 
- **Websockets** module with method documentation and Websocket playground to test functionality 

---

Descoped modules waiting for implementation:
- **GraphqQL** - DataAPI documentation with gql playground to explore exposed data
- **Buidl buddy** - Tool to guide user through docs and pick services based on demanded use case

## UI Design
Original design could be found at [Tatum Figma project](https://www.figma.com/file/zyaCU2Qr1R0sSXcNaKQBy7/Tatum-%7C-Devportal?node-id=2871%3A44952)

High probability of redesign after setting new brand guidelines 

## Deployment
Dev portal app client currently deployed on Heroku, to gain access ask Pavel Franc. 
- Deployment process currently is manual
- Current PR approvers: Oleg Antonyak, Jan Dočekal, Michal Každan
- Heroku access: Pavel France, Jan Dočekal, Michal Každan

## Repo structure

Described main sections to follow and learn to overview what's inside the app

### A. Components
Components styled with Tailwind v3.x

#### Base components

`Implementation task: Storybook to expose elements and behavior for other frontend products`

- Buttons
- Cards
- Dropdown
- Input
- Modal
- NavigationDropdown
- ProgressBar
- Tabs

#### Section components
Page sections composed from base elements and functions into visual/functional groups

- **Buidl buddy**= Use case explorer (not released)
- **CodeExporter** = GraphQL utility to export gql query into javascript template (not released)
- **Documentation** =  Template for markdown guides and tutorials
- **Hero**
- **Layouts** = Footer, Header, Navigation
- **Networks** = Components to show which blockchain network Tatum supports
- **Services** = Used card components in specific context
- **TableOfContents** = Markdown element to render table of contents based on title/subtitle tags
- **TimeLine** = Release log timeline
- **UseCasesSection** = Table with supported use cases (not released)

### B. Hooks
Universal helpers throughout various sections
- **useIntersectionObserver** - using observer to make page more dynamic
- **useKeyClick** - using keyboard interaction with specific elements
- **useMarkdownHeadings** - Parse headings from CMS markdown to object
- **useMediaQuery** 
- **useOutisedClick**
- **useStrapi** - Use CMS source address from environment variable
- **useWindowResize** - Resize components

### C. Pages
Main displayed routes
- **ChangeLog** = Release log with Tatum prodcuts to track changes and new features
- **Community** = Initiatives and products made by Tatum community with love (not released)
- **GraphQL** = Module with Data API docs and GraphQL explorer (not released)
- **API** = API references using Stoplight tooling to design and display OpenApi specifications
- **Products** = Page with references to Tatum product
- **Terminology** = Blockchain Glossary
- **Guides**
- **Tutorials**
- **404** - Page not found

## Integrations

### Stoplight
Stoplight products are used to design and render openapi specifications into interactive docs with all API endpoints and mock server to play with. 

We use two specific products

#### Stoplight studio
- Design API 
- Automated sync with repository
- Interface for content creators

#### Stoplight dev portal 
- NPM package to render UI as a service

Needed to just define space for UI inside app, import `StoplightProject` from [library](https://www.npmjs.com/package/@stoplight/elements-dev-portal) and defined unique project key exposed in Stoplight Studio.

- **Advantage** of this approach is low complexity of implementation
- Main **disadvantage** is limited possibility to override provided css styles and UI unless open source library is forked. Fork of Stoplight library is NOT recommended as repository is under active development by Stoplight team and its community - forked solution would lost benefits of “free” bugfixes and feature improvements

### CMS
[Link to repo with readme.md](https://gitlab.com/tatum-io/websites/cms)

