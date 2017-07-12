# How to manage menus in cloudcms
[This tutorial](https://idealley.gitbooks.io/cloud-cms-how-to-manage-menus/content/) walks you trough the different steps to create a menu graph that is connected to your content graph.

This repo is a JSON only version of the original [Manage menus with Cloud CMS](https://github.com/idealley/cloudcms-manage-menus) repo. It is intended as a backend for [Cloudcms + webpack + Vuejs](https://github.com/idealley/cloudcms-webpack-vuejs). All routes return JSON.

This is a **basic** setting, caching is needed as well as error handling for example. It is meant to get up and running quickly.

## Aim
* Manage menus
* Generate sitemaps
* maintain a consitant breadcrumb/pathway (you are here: page > page > ...)

## Setup
The setup of Cloud CMS is handled by a CLI. You need to provide API Keys. If you do not have any [check the documentation](https://www.cloudcms.com/apikeys.html).
Then clone this repository and:
* `$ npm install`
* `$ node setup`
    * select **Setup Cloud CMS for the tutorial**
* run again `$ node setup` (soon option will be back)
    * select **Import sample content**
This will create all the necessary content for the demo, but you will still have to link items. This is explained in the tutorial (coming soon).

## Run the app
`$ node app.js`
You have now few routes available:
* `/main-menu` -> displays the menu and you can click on the menu items
* `/a-category`
* `/a-category/article-1`
* `/article-1`
* `/article-2`
* `/article-3`

Basically anything that you pass after `/` will be sent as a `slug` to Cloud CMS. If content matches Cloud CMS will respond with the documents.

Normally you can add new pages/menu item, there is a simplistic automatic routing included.