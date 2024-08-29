# [Vue Paper Dashboard PRO](https://www.creative-tim.com/product/vue-paper-dashboard-pro) [![version][version-badge]][changelog]

![alt text](https://s3.amazonaws.com/creativetim_bucket/products/63/original/opt_pkp_vue_thumbnail.jpg)

**[Vue Paper Dashboard PRO](https://www.creative-tim.com/product/vue-paper-dashboard-pro)** is a beautiful resource built over Bootstrap and Vue.
It will help you get started developing dashboards in no time.

Vue Paper Dashboard Pro is the Vue.js ported version of the [Original Paper Dashboard Pro](https://www.creative-tim.com/product/paper-dashboard-pro).
Using the Dashboard is pretty simple but requires basic knowledge of Javascript, [Vue](https://vuejs.org/v2/guide/) and [Vue-Router](https://router.vuejs.org/en/).
Vue Paper Dashboard was coded by [Cristi Jora](https://github.com/cristijora) and the design was made by [Creative Tim](https://www.creative-tim.com/).
It combines soft colors with beautiful typography and spacious cards and graphics.

It is a powerful tool, but it is light and easy to use.
It has enough features to allow you to get the job done, but it is not crowded to the point where you can't find the files for a specific plugin.

We like consistency and design that blends into its purpose.
Vue Paper Dashboard PRO is a perfect example of our most thoughtful work. It combines Vue.js components and plugins, while looking like everything fits together.
For an easy start or inspiration for you project, we have also create a set of example pages, like the user settings or usage graphics.

Vue Paper Dashboard PRO is built using the same design language as [Paper Kit](http://www.creative-tim.com/product/paper-kit).
You can easily use them together, or pick between them depending on the project you have.

## Links:

- [Live Preview](https://cristijora.github.io/paper-dashboard-pro/#/admin/overview)

## Quick Start:

Quick start options:

- [Download from Creative Tim](https://www.creative-tim.com/product/vue-paper-dashboard-pro).
- Make sure you have [Node js](https://nodejs.org/en/) installed
- Go to the downloaded folder and open a terminal
- Type `npm install` or `yarn install` if you use [yarn](https://yarnpkg.com/en/)
- Type `npm run dev` to start a development server

The repo uses [vue-cli](https://github.com/vuejs/vue-cli) scaffolding which takes care of the development setup with webpack and all the necessary modern tools to make web development faster and easier.

Other Products:

- [Download FREE Vue Version](https://www.creative-tim.com/product/vue-paper-dashboard).

### What's included

Within the download you'll find the following directories and files:

```
|-- src
    |   |-- App.vue
    |   |-- gloablComponents.js
    |   |-- globalDirectives.js
    |   |-- main.js
    |   |-- pollyfills.js
    |   |-- sidebarLinks.js
    |   |-- assets
    |   |   |-- sass
    |   |       |-- demo.scss
    |   |       |-- element_variables.scss
    |   |       |-- paper-dashboard.scss
    |   |       |-- paper
    |   |-- components
    |   |   |-- Dashboard
    |   |   |   |-- Layout
    |   |   |   |   |-- Content.vue
    |   |   |   |   |-- ContentFooter.vue
    |   |   |   |   |-- DashboardLayout.vue
    |   |   |   |   |-- LoadingMainPanel.vue
    |   |   |   |   |-- SidebarSharePlugin.vue
    |   |   |   |   |-- TopNavbar.vue
    |   |   |   |-- Views
    |   |   |       |-- Charts.vue
    |   |   |       |-- Calendar
    |   |   |       |   |-- Calendar.vue
    |   |   |       |   |-- CalendarRoute.vue
    |   |   |       |-- Components
    |   |   |       |   |-- Buttons.vue
    |   |   |       |   |-- GridSystem.vue
    |   |   |       |   |-- Icons.vue
    |   |   |       |   |-- Notifications.vue
    |   |   |       |   |-- Panels.vue
    |   |   |       |   |-- SweetAlert.vue
    |   |   |       |   |-- Typography.vue
    |   |   |       |-- Dashboard
    |   |   |       |   |-- Overview.vue
    |   |   |       |   |-- Stats.vue
    |   |   |       |   |-- Stats
    |   |   |       |       |-- Task.vue
    |   |   |       |       |-- TaskList.vue
    |   |   |       |       |-- TimeLine.vue
    |   |   |       |       |-- TimeLineItem.vue
    |   |   |       |-- Forms
    |   |   |       |   |-- ExtendedForms.vue
    |   |   |       |   |-- RegularForms.vue
    |   |   |       |   |-- ValidationForms.vue
    |   |   |       |   |-- Wizard.vue
    |   |   |       |   |-- ValidationForms
    |   |   |       |   |   |-- LoginForm.vue
    |   |   |       |   |   |-- RegisterForm.vue
    |   |   |       |   |   |-- TypeValidationForm.vue
    |   |   |       |   |-- Wizard
    |   |   |       |       |-- FirstStep.vue
    |   |   |       |       |-- SecondStep.vue
    |   |   |       |-- Maps
    |   |   |       |   |-- API_KEY.js
    |   |   |       |   |-- FullScreenMap.vue
    |   |   |       |   |-- GoogleMaps.vue
    |   |   |       |   |-- VectorMaps.vue
    |   |   |       |   |-- VectorMapsPage.vue
    |   |   |       |   |-- WorldMap.vue
    |   |   |       |   |-- world_map.js
    |   |   |       |-- Pages
    |   |   |       |   |-- background-2.jpg
    |   |   |       |   |-- Lock.vue
    |   |   |       |   |-- Login.vue
    |   |   |       |   |-- Register.vue
    |   |   |       |   |-- TimeLinePage.vue
    |   |   |       |   |-- UserProfile.vue
    |   |   |       |   |-- UserProfile
    |   |   |       |       |-- EditProfileForm.vue
    |   |   |       |       |-- MembersCard.vue
    |   |   |       |       |-- UserCard.vue
    |   |   |       |-- Tables
    |   |   |           |-- ExtendedTables.vue
    |   |   |           |-- PaginatedTables.vue
    |   |   |           |-- RegularTables.vue
    |   |   |           |-- users.js
    |   |   |-- GeneralViews
    |   |   |   |-- NotFoundPage.vue
    |   |   |-- UIComponents
    |   |       |-- Dropdown.vue
    |   |       |-- Pagination.vue
    |   |       |-- Progress.vue
    |   |       |-- Switch.vue
    |   |       |-- Cards
    |   |       |   |-- ChartCard.vue
    |   |       |   |-- CircleChartCard.vue
    |   |       |   |-- StatsCard.vue
    |   |       |-- Inputs
    |   |       |   |-- Checkbox.vue
    |   |       |   |-- formGroupInput.vue
    |   |       |   |-- Radio.vue
    |   |       |-- SidebarPlugin
    |   |           |-- index.js
    |   |           |-- MobileMenu.vue
    |   |           |-- SideBar.vue
    |   |           |-- SidebarItem.vue
    |   |           |-- UserMenu.vue
    |   |-- routes
    |       |-- routes.js
```

## Useful Links

Documentation: https://demos.creative-tim.com/vue-paper-dashboard-pro/documentation

More products from Creative Tim: <https://www.creative-tim.com/bootstrap-themes>

Tutorials: <https://www.youtube.com/channel/UCVyTG4sCw-rOvB9oHkzZD1w>

Freebies: <https://www.creative-tim.com/products>

Affiliate Program (earn money): <https://www.creative-tim.com/affiliates/new>

Social Media:

Twitter: <https://twitter.com/CreativeTim>

Facebook: <https://www.facebook.com/CreativeTim>

Dribbble: <https://dribbble.com/creativetim>

Google+: <https://plus.google.com/+CreativetimPage>

Instagram: <https://instagram.com/creativetimofficial>

[changelog]: ./CHANGELOG.md
[version-badge]: https://img.shields.io/badge/version-2.4.2-blue.svg
