jquery-ui-memory-game
=====================

Jquery plugin (widget) for creating "memory" cards games from a list of links and images.

See it in action: http://matteosistisette.github.io/jquery-ui-memory-game


Requirements
------------

To be able to use the plugin, place the downloaded `css` and `js` folders in the webroot of your page, and paste this code into the `<head>` of your html:

    <!-- DEPENDENCIES: jQuery and jQuery-UI -->
    <script src="https://code.jquery.com/jquery-2.2.4.js"></script>
    <script src="https://code.jquery.com/ui/1.11.4/jquery-ui.js"></script>
    
    <!-- INCLUDE THE PLUGIN (js and css) -->
    <link rel="stylesheet" href="css/jquery.memory-game.css">
    <script src="js/jquery.memory-game.js"></script>

    
Basic usage
-----------
There are two ways of building a "Memory" card game using this plugin:
- Build the list of cards through **HTML markup** (links wrapped around images), and convert it into a Memory game with one simple line of JavaScript
- or, define the list of cards as a **JavaScript object** and pass it as a parameter to the plugin constructor

###Defining the list of cards through HTML markup (minimal JavaScript code)###

