
## Content management

Any user with access to CMS [GUI](https://cms.tatum.io/) is able to use content structure defined by devs and fill related content

- **Manage published** /unpublished articles
- Manage content for different **locales**
- **Filter articles** based on any attribute to overview your content

<div class="toolbar-note">
You can find more information about content types builder [here](https://strapi.io/features/content-types-builder).
</div>


## Requirements to use

- Granted role by application administrator
- Basic knowledge of Markdown language

## How to create article

Write something cool with online editors like [Dillinger](https://dillinger.io/) or rather [DXH Markdown editor](https://happy-blackwell-bcd781.netlify.app/)

Flavored elements
Class | Usecase | 
---------|----------|
 toolbar-note | Green toolbox  
 toolbar-tip | Blue toolbox 
 toolbar-warning | Red toolbox 
 toolbar-caution | Yellow toolbox
 tabbed-code-blocks | Tabbed code example
 youtube-url | Embedded youtube video

Examples: 
<div class="toolbar-note">
You can find more information about content types builder [here](https://strapi.io/features/content-types-builder).
</div>

<div class="tabbed-code-blocks">
```Code item 1
{"json1":"value1"}
```
```Code item 2
{"json2":"value2"}
```
</div>

<div youtube-url="https://www.youtube.com/watch?time_continue=209&v=CGgyyTTv0yw&feature=emb_title&ab_channel=Tatum"></div>


### Current usage in Dev portal

#### Markdown guides
Guides and tutorials coming from CMS could be flavoured with additional visual elements not existing in basic Markdown syntax.

Categories broke down into collections
- **Guides-virtual** = Guides related to [Virtual accounts](https://docs.tatum.io/guides/ledger-and-off-chain/how-to-support-fiat-currencies)
- **Guides-blockchain** = Blockchain specific [articles](https://docs.tatum.io/guides/blockchain/how-to-send-a-bitcoin-transaction)
- **Introduction** = Articles accessible from main page
- **Tutorials** = [Tutorials](https://docs.tatum.io/tutorials/how-to-create-a-peer-to-peer-nft-auction)

#### Release log

Release log is currently used to inform users about new functionalities that Tatum releases over time.
There is a specific template in this log and it is necessary to specify mandatory parameters: date of release, version of release and content (new functionalities, support for new blockchains,...)

![50CSHzew2O.png](https://stoplight.io/api/v1/projects/cHJqOjExMTMxNA/images/PYUnQKQjjQM)

#### Terminology

The world of blockchain is specific and contains dozens of different terms that new users may not understand. Therefore, via CMS we manage teminology dictionary, which contains explained most used terms.

The structure of CMS template is very simple. It contains only parameters (all mandatory) `Title`, `Description` and `Category` of new term.

![5ehqGB3PhK.png](https://stoplight.io/api/v1/projects/cHJqOjExMTMxNA/images/wwfAA1AKjp8)


#### Websockets

Section describing how to use Tatum WebSockets with interactive playground and list of all supported methods.

From CMS perspective:
- `title` = Display name in left menu
- `slug` = Defined URL. Mandatory not to use 
- `markdown` = Article content
- `category` = Section in left menu where to put article (json-rpc method, pub-sub method, general article)
- `requestPlayground` = Example to be prefilled in Websocket playground
- `blockchain` = Method supported for specific blockchain (evm = common option for Ethereum like chains or non specific methods)


#### Product
Product collection is being used to map all API endpoints inside Tatum and reuse the knowledge for general overview on main page and FAQ section to guide internal/external users

- `operation` - Unique operation id defined in openapi specs
- `docs` - Reference inside api documentation
- `name` - Service name displayed in main overview
- `credit` - credit cost of given service
- `endpoint` - API endpoint used for service
- `description` - Short description of the service
- `category` - Logical categorization used for main overview
- `subcategory` - Logical subcategorization to specify service further
- `supported` - JSON as table with supported chains per service 
- `free` - Flag to identify whether to consume "free" credits or "premium"

---

## How to use CMS at Tatum

Using CMS is divided into two basic options according to the granted permission. `Content Manager` is a section that is used to fill data while `Content-Type Builder` is used to create templates for individual documents.

Let's start with the simpler and more used one.

### Content Manager quick guide

For business owners, the Content Manager section is primarily designed. This section is used to fill data according to specified templates.

Let's take a look at this. Imagine that as a business owner you want to add a new article to the Tutorials section.

![chrome_E60mfwnPqm.gif](https://stoplight.io/api/v1/projects/cHJqOjExMTMxNA/images/nB1Ov06vuuY)

1. First of all, we have to create a new article. After creating a new article, you will see a pre-filled form according to the template, which is the same for all documents in the Tutorials section.
2. Individual fields that can be filled will appear in the new entry. Whether an individual field is required or not is indicated by a red star next to the title.
3. After you have filled in all the necessary entries, all you have to do is save the new entry. You are also offered the opportunity to publish the article. This is directly reflected in the place where the documentation is deployed in the production.

And that's all you need to create a new article.

---