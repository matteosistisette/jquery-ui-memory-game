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
- or, define the list of cards as a **JavaScript array** and pass it as a parameter to the plugin constructor

###Using HTML markup
See complete live example here: [http://jsbin.com/kawipa](http://jsbin.com/kawipa/edit?html,output)

HTML markup:

    <div id="memory-game">
      <a href="http://en.wikipedia.org/wiki/Iguana"><img width="100" height="100" src="example-images/iguana.jpg"></a>
      <a href="http://en.wikipedia.org/wiki/Panda"><img width="100" height="100" src="example-images/panda.jpg"></a>
      <a href="http://en.wikipedia.org/wiki/Lemur"><img width="100" height="100" src="example-images/lemur.jpg"></a>
      <a href="http://en.wikipedia.org/wiki/Penguin"><img width="100" height="100" src="example-images/penguins.jpg"></a>
      <a href="http://en.wikipedia.org/wiki/Polar_bear"><img width="100" height="100" src="example-images/polarbear.jpg"></a>
      <a href="http://en.wikipedia.org/wiki/Rabbit"><img width="100" height="100" src="example-images/rabbit.jpg"></a>
      <a href="http://en.wikipedia.org/wiki/Rhinoceros"><img width="100" height="100" src="example-images/rhino.jpg"></a>
      <a href="http://en.wikipedia.org/wiki/Common_seal"><img width="100" height="100" src="example-images/seal.jpg"></a>
      <a href="http://en.wikipedia.org/wiki/Zebra"><img width="100" height="100" src="example-images/zebra.jpg"></a>
    </div>

JavaScript code:

    <script>
    $(function(){
        $("#memory-game").memoryGame();
    });
    </script>

**NOTE:** The size of the card images in pixels must be known (and fixed) when the plugin is instantiated. That's why we need the explicit `width` and `height` html attributes, at least on the first image; alternatively, CSS could be used. See below for more details and alternatives.

###Using a JavaScript array
See complete live example here: [http://jsbin.com/vonaye](http://jsbin.com/vonaye/edit?html,output)

HTML markup (just a container):

    <div id="memory-game"></div>
    
JavaScript code:

    <script>
    $(function(){
      $("#memory-game").memoryGame({
        cards: [
          {
            imageUrl: 'example-images/iguana.jpg',
            linkUrl: 'http://en.wikipedia.org/wiki/Iguana'
          },
          {
            imageUrl: 'example-images/panda.jpg',
            linkUrl: 'http://en.wikipedia.org/wiki/Panda'
          },
          {
            imageUrl: 'example-images/lemur.jpg',
            linkUrl: 'http://en.wikipedia.org/wiki/Lemur'
          },
          {
            imageUrl: 'example-images/penguins.jpg',
            linkUrl: 'http://en.wikipedia.org/wiki/Penguin'
          },
          {
            imageUrl: 'example-images/polarbear.jpg',
            linkUrl: 'http://en.wikipedia.org/wiki/Polar_bear'
          },
          {
            imageUrl: 'example-images/rabbit.jpg',
            linkUrl: 'http://en.wikipedia.org/wiki/Rabbit'
          },
          {
            imageUrl: 'example-images/rhino.jpg',
            linkUrl: 'http://en.wikipedia.org/wiki/Rhinoceros'
          },
          {
            imageUrl: 'example-images/seal.jpg',
            linkUrl: 'http://en.wikipedia.org/wiki/Common_seal'
          },
          {
            imageUrl: 'example-images/zebra.jpg',
            linkUrl: 'http://en.wikipedia.org/wiki/Zebra'
          }
        ],
        cardWidth: 100,
        cardHeight: 100
      });
    });
    </script>
    
**NOTE:** if you use this method, you have to specify the card image height and width via the `cardWidth` and `cardHeight` parameters.
