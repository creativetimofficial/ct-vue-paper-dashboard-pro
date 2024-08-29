# Change Log

##[2.4.2] 2024-08-21

- Update dependencies

##[2.4.1] 2022-11-30

- Update dependencies
- Fix the installation issue when running `npm i`

##[2.4.0] 2021-10-18

### Updates

- Vue Router Prefetch remove
- SweetAlert fix
- Update dependencies to latest version
- FullCalendar syntax update

## [2.3.0] 2020-06-03

- Update all dependencies to latest versions
- `FullCalendar`, `Vee-Validate`, `Google Maps` plugins updated to new syntax

## [2.2.1] 2019-02-12

- Package updates
- Bundle size improvements
- Accessibility & best practices improvements
- UI bug fixes for Wizard

## [2.2.0] 2019-01-07

#### Breaking

- Updated to fullcalendar 4.0.0-alpha.3 which no longer uses jquery. If you used fullcalendar please check their detailed release notes https://fullcalendar.io/docs/v4/release-notes
  Some api parts changed
- Removed jVectorMaps in favor of [datamaps](http://datamaps.github.io/). Check the WorldMap component for more details. If you used the world map, you could simply migrate by installing
  d3, datamaps and topojson libraries and copying the WorldMap component over.
- Removed jquery from the code (fullcalendar and world map)

### Improvements & bug fixes

- Update packages (Vue cli, element, ui, bootstrap, vue & others)
- 60 Make all charts reactive by default
- 66 Add wizard complete event which is triggered when "finish" button is clicked
- 67 Upgrade to fullcalendar 4.0.0-alpha and removed jquery dependency
- 68 Fix topnavbar menu button not showing on mobile
- 70 Migrate to latest bootstrap version
- 71 Fix switch disabled state
- 73 Fix required attribute for fg-input component
- Cleanups

## [2.1.0] 2018-08-09

- #55 Fix select arrow issues
- #29 Add loading bar (nprogress)
- Optmize imports inside routes.js
- Add helper mixins to change checkbox/radio colors
- Add extra sections in documentation (auth, requests, changing checkbox/radio colors)
- Style tweaks to documentation

## [2.0.0] 2018-07-11

2.0.0 includes 2 major changes:

- #### upgrade to Vue CLI 3
- #### upgrade from Bootstrap 3 to Bootstrap 4.

  2.0.0 also includes lots of new custom components, bug fixes and style tweaks.

The changes below might seem a bit painful at first sight and they might require
1 or 2 hours of your time but the end benefits are pretty big especially for the Vue CLI 3 upgrade.
You won't have to worry about webpack stuff anymore, complicated config files as well as tons of dependencies.
This is all handled by Vue CLI 3. You can add new plugins such as PWA support only by typing
`vue add pwa`. For more details check out [the docs for that](https://cli.vuejs.org/guide/plugins-and-presets.html#installing-plugins-in-an-existing-project)

A more easy update could be to use this project structure as it is and copy paste
your own `src/components/Dashboard`, `routes` folder and `sidebarLinks.js` file.

If you had extra dependencies installed, make sure you add them. Same applies to modified/added
css assets or images.

Also please follow the changes. Due to the fact that Bootstrap introduced quite a lot of changes from
version 3 to 4, make sure you go through the Bootstrap 4 related changes below (especially grid and card changes)

If the above doesn't work, please follow the detailed changes and try to update step by step.
If you have troubles, feel free to contact us via [support](https://www.creative-tim.com/contact-us).

#### Vue CLI 3 related changes:

- We recommend using `yarn`. Latest `npm` versions are a bit buggy. Also a strong recommendation is
  to not use npm and yarn together as it will cause ugly issues. Use only one of them.

- Move `static` folder and `index.html` to `public` folder. Add images from dashboard `public/static/img` to your project.

- Replace `devDependencies` and `scripts` in package.json with those from version 2.0.0. If you have some extra dependencies added, make sure you add them as well along with the list of dev dependencies from v2.

- Copy over `.bablerc`, `vue.config.js` file from version v2.0.0

- Delete `build` and `config` folders. If you have custom webpack configuration, please visit the
  documentation of [Vue CLI](https://github.com/vuejs/vue-cli/blob/dev/docs/README.md) on how to change
  webpack related stuff.

- Copy over `src/components/UIComponents`, `src/globalComponents.js`, `src/assets` from v2.0.0 in your project

#### Bootstrap 4 related changes:

- Update bootstrap version in index.html "https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.1.1/css/bootstrap.min.css"

- Package additions: `vue2-transitions`

- All `col-xs-` should be converted to `col-`. Bootstrap 4 is mobile first and therefore `col-` will affect all screen sizes including the smallest.

- We added new components for cards, buttons. Please make sure you use them. If you have
  plain html for cards. Change `card-content` class with `card-body`. This is necessary so we are inline with
  Bootstrap 4 cards.

- If you used the timeline, make sure you import it from the base components folder.
  `import {TimeLine, TimeLineItem} from 'src/components/UIComponents'`.
  The `body` slot changed to `content` slot. Also, make sure you use the new provided set of icons. A small change regarding timeline is that old plain labels can now be replaced with badges.
  For example `<span class="label label-success">Another Title</span>` -> `<badge type="success">Another Title</badge>`
  Badge component can be imported like this: `import {Badge} from 'src/components/UIComponents'`

- We provided custom components for collapse, collapse item. They have the same behaviour as those from
  element ui so you can simply replace `<el-collapse>` with `<collapse>` and `<el-collapse-item>` with
  `<collapse-item>`. To import Collapse components just use `import {Collapse, CollapseItem} from 'src/components/UIComponents'`

- For tabs we created new components located right in the project.
  Import the components `import {Tabs, TabPane} from 'src/components/UIComponents'`
  Simply replace. `vue-tabs` with `tabs` and `v-tab` with `tab-pane`. For vertical tabs, change
  `direction="vertical"` prop to `vertical`. E.g `<tabs vertical>`

- For dropdown menus links, use `class="dropdown-item"`. Example `<a class="dropdown-item" href="#">Action</a>`

## [1.1.0] 2017-11-07

- Package updates
- Improve overall webpack config to be as minimal as possible on top of vue-cli.
  The dashboard currently adds only a single file on top of vue cli `webpack.custom.js` which is imported in `webpack.base.conf.js`
  This allows for seamless vue-cli upgrades.
- Fix horizontal scroll on mobile (#1)
- Add tips about chartist tooltip in the docs (#3)
- Add inline support for radio buttons (#6)
- Simplify sidebar plugin and reduce it to minimum. Prefer composition of components through slots which basically allows
  having menus with sub-menus
  Example through js configuration `$sidebarLinks`:

```js
let links = [
  {
    name: "Dashboard",
    icon: "ti-panel",
    collapsed: false,
    children: [
      {
        name: "Overview",
        icon: "ti-package",
        children: [
          {
            name: "Grid System",
            path: "/components/grid-system",
          },
        ],
      },
    ],
  },
];
```

- Sidebar now allows declaration of routes through components
  Example:

```html
<side-bar>
  <template slot-scope="props" slot="links">
    <sidebar-item
      :link="{name: 'Dashboard', icon: 'ti-panel', path: '/admin/dashboard'}"
    >
    </sidebar-item>

    <sidebar-item :link="{name: 'Save units', icon: 'ti-star'}" :menu="true">
      <sidebar-item
        v-for="unit in mappedStarredUnits"
        :key="unit.name"
        :link="{name: unit.name, path: unit.path}"
      >
      </sidebar-item>
    </sidebar-item>
  </template>
</side-bar>
```

Note that this behaviour will override `$sidebarLinks` being passed as a prop. Please choose only 1, preferred approach.

- Fix unit test setup issues on some OS (#23)
- Add unit tests for Pagination and SidebarStore (more tests will be added soon)
- Upgrade to latest vue-cli

## [1.0.0] 2017-09-05

### Stable Original Release
