# inherit

Prototype inheritance made easy. Add this method to classes
so they can be easily sub-classed.

    var inherits = require('inherits');

    // Create a class
    var View = function(name){ 
      this.name = name;
    };
    View.prototype.surname = "Wayne";

    // Give it the method
    View.extend = inherits;

    // Now create sub-classes
    var Child = View.extend({
      hobbies: ['flying', 'knitting', 'cooking']
    });

    var barry = new Child('Barry');
    
    // It will inherit the properties
    barry.surname === 'Wayne';