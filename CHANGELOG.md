# Change Log

## [1.0.0] 2017-09-05
### Stable Original Release

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
    let links = 
    [{
        name: 'Dashboard',
        icon: 'ti-panel',
        collapsed: false,
        children: [{
          name: 'Overview',
          icon: 'ti-package',
          children: [{
             name: 'Grid System',
             path: '/components/grid-system'
          }]
        }]
     }]
  ```
  - Sidebar now allows declaration of routes through components
  Example: 
  ```html
  <side-bar>
      <template slot-scope="props" slot="links">
        <sidebar-item :link="{name: 'Dashboard', icon: 'ti-panel', path: '/admin/dashboard'}">
        </sidebar-item>
        
        <sidebar-item :link="{name: 'Save units', icon: 'ti-star'}" :menu="true">
          <sidebar-item v-for="unit in mappedStarredUnits"
                        :key="unit.name"
                        :link="{name: unit.name, path: unit.path}">
          </sidebar-item>
        </sidebar-item>
        
      </template>
    </side-bar>
  ```
  Note that this behaviour will override `$sidebarLinks` being passed as a prop. Please choose only 1, preferred approach.
  
  - Fix unit test setup issues on some OS (#23)
  - Add unit tests for Pagination and SidebarStore (more tests will be added soon)
  - Upgrade to latest vue-cli 
