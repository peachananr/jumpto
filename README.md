#Jump To by Pete R.
Create a smooth jump to sub navigational menu in one JS call
Created by [Pete R.](http://www.thepetedesign.com), Founder of [BucketListly](http://www.bucketlistly.com)

[![Jump To Menu](http://www.thepetedesign.com/images/jumpto_image.png "Jump To Menu")](http://www.thepetedesign.com/demos/jumpto_demo.html)

## Demo
[View demo](http://www.thepetedesign.com/demos/jumpto_demo.html)

## Compatibility
Modern browsers such as Chrome, Firefox, and Safari have been tested. Not tested on IE.

## Basic Usage
Jump To let you create a jump to sub navigational menu automatically with 1 line of JS call. The menu can be used to assist your navigation for pages with a lot of content.

To add this to your website, simply include the latest jQuery library together with `jquery.jumpto.js`, and `jumpto.css` into your document's `<head>` and make sure your content have a mark up that matches the structure below:

````html
<div class="page_container">
  <div class="jumpto-block">
    <h2>Header 1</h2>
    <h3>SubHeader 1</h3>
    ....
    <h3>SubHeader 2</h3>
    ....
  </div>
  <div class="jumpto-block">  
    <h2>Header 2</h2>
    <h3>SubHeader 1</h3>
    ...
  </div>
</div>
````
All you need is simply wrap everything with a container, in this case I wrapped it with a 'page_container', and make sure you wrap each section with another div, in this case it's the 'jumpto-block' div. These 'jumpto-block' will let the plugin knows how many first level links it should show on the menu. Once this is done, simply call:
 
````javascript
$(".page_container").jumpto({
  firstLevel: "> h2", // You can define which tag will represent your first level header. The default value is the <h2> tag. Any <h2> tag will automatically be used as a first level link in the menu.
  secondLevel: false, // We also support submenu. Like above, you can define the selector for the second level header to be used in the submenu. Default is false.
  innerWrapper: ".jumpto-block", // In case you want to switch the section wrapper class name to something else
  offset: 400, // You can define how many pixels until the jump to menu starts to follow you on scroll. Default is 400 pixels.
  animate: 1000, // You can define how fast/slow the page will scroll when the jump to menu is clicked. Set to false to turn off animation.
  navContainer: false, // If you want to place your jump to menu somewhere else, simply add a selector to your predefined jump to menu container here. The default is false and it will automatically be generated.
  anchorTopPadding: 20, // This option let you set the top padding when the jump to menu is clicked. This will let you control the space between your header and the top of the page. Default is 20 pixels.
  showTitle: "Jump To", // You can customize the title of the jump to menu here. Set to false if you want to hide the title
  closeButton: true // You can choose to show/hide the close button by toggling this to true/false respectively
});
````

And that's all you need to do to add an Jump To menu to your website.

If you want to see more of my plugins, visit [The Pete Design](http://www.thepetedesign.com/#design), or follow me on [Twitter](http://www.twitter.com/peachananr) and [Github](http://www.github.com/peachananr).

## Other Resources
- Tutorial (Coming Soon)