# Demo on how to allow parametrizing deep inside a template hierarchy

The problem was how to be able to pass in optional links, buttons, etc. into an x-box
from the parent template in a reusable fashion

The structure is

 * x-box
   * x-box-header
     * x-box-tools
   * x-box-body


where `x-box-tools` is the conditionally displayed 'tools' display location. It shouldn't
display


## the 'solutions' - as commit hashes

* `327f97ffebe53ed80369f06d951992cf1c4c796e` - one level deep params passing/yielding 
* `9e717d6d232a7ba2baa91338136df90c25391807` - deep yielding & box overrides
* `20bf54f2e1899fb3e42d030ac0bf0cf4fe6536b7` - using `ember-component-helpers`' `array` template helper to pass
  in links - get rid of all the `yields` and don't allow customization (in an app, one would like the elements to
  be consistent)

## Running

* check out the interesting commits
* `cd tests/dummy/`
* `ember serve`
* Visit your app at [http://localhost:4200](http://localhost:4200).

## Useful links

* [https://github.com/emberjs/ember.js/blob/v2.18.1/](the ember source code)
* the ember guide
  * [https://guides.emberjs.com/v2.18.0/components/wrapping-content-in-a-component/](wrap content in a component)
  * [https://guides.emberjs.com/v2.18.0/components/block-params/](supporting both block & inline params)
  * [https://emberjs.com/api/ember/2.18/classes/Ember.Templates.helpers/methods/hash?anchor=hash](the hash template helper)
* ember-bootstrap custom tabs implementation
  * [https://github.com/kaliber5/ember-bootstrap/blob/master/addon/templates/components/common/bs-tab.hbs](bs-tab.hbs)
  * [http://www.ember-bootstrap.com/api/classes/Components.Tab.html](its usage under 'Custom Tabs' section)

For more information on using ember-cli, visit [https://ember-cli.com/](https://ember-cli.com/).
