# 2012.02.15.BackboneSF

!SLIDE top-left

# Jasmine &amp; Backbone

}}} images/jenga.jpg::undeleterious::flickr::http://www.flickr.com/photos/undeleterious/486595732/

!SLIDE

# Hi.

## Davis W. Frank
### [Pivotal Labs](http://pivotallabs.com) | [Jasmine](http://pivotal.github.com/jasmine)

!SLIDE

# Test JS much?

!SLIDE

# Jasmine Intro

## (condensed version)


!SLIDE 

@@@ javascript
describe("Deck", function() {
  var deck;

  describe("with jokers", function() {
    beforeEach(function() {
      deck = new Deck({jokers: true});
    });	

    it("should have the correct count of cards", function() {
      expect(deck.count).toEqual(54);
    });
  });

  describe("without jokers", function() {
    beforeEach(function() {
      deck = new Deck({jokers: false});
    });	

    it("should have the correct count of cards", function() {
      expect(deck.count).toEqual(52);
    });	
  });
});
@@@

!SLIDE bottom-left

# Yes we have ...

}}} images/menu.jpg::darktek13::flickr::http://www.flickr.com/photos/darktek13/2130147274/

!SLIDE

## `jasmine.Clock`

### Test timeouts synchronously

!SLIDE

## `spyOn(obj, 'functionName');`
## `jasmine.createSpy();` 

## for test doubles

!SLIDE

# Custom Matchers

!SLIDE

# Standalone HTML Runner

## Manage your own `<script>`s

!SLIDE

# Ruby Friendly?

## `$ gem install jasmine`

## Test Like Water, my friend

!SLIDE bottom-left

# Supporting Projects

}}} images/structure.jpg::s_fenton::flickr::http://www.flickr.com/photos/s_fenton/4263417366/

!SLIDE 

# Jasmine jQuery

## Fixtures & Matchers

!SLIDE

# Jasmine Ajax

## XHR stubbing/mocking/faking

!SLIDE

@@@ javascript
describe("Deck", function() {
  var deck;

  beforeEach(function() {
    jasmine.Ajax.UseMock();
    deck = new Deck({jokers: false});
  });	

  it("requires registration before use", function() {
    expect(deck.shuffle()).toEqual(false);
		
    deck.register();
    mostRecentAjaxRequest().response(successfulRegistrtaion);

    expect(deck.shuffle()).toEqual(true);
  });
});
@@@

!SLIDE bottom-right

# What about Backbone.js?

}}} images/clothespins.jpg::Rob Crusoe::flickr::http://www.flickr.com/photos/26094818@N06/2641000361/

!SLIDE

# Data & Logic in _Objects_

## get'em out of the DOM

!SLIDE

# Test Behavior
## not frameworks

!SLIDE

# Models?

!SLIDE

# Models?

## What do they _do_?

!SLIDE

# Collections?

!SLIDE

# Collections?

## What do they _do_?

!SLIDE

# Collections?

## Verify you send the right URL

!SLIDE

# Routers?

!SLIDE

# Routers?

## What do they _do_?

!SLIDE

# Routers?

## default route, initial DOM state

!SLIDE

# Views?

!SLIDE

# Yes, Views

## they do a LOT

!SLIDE

## (don't go crazy)

!SLIDE left

# Hard to test in Jasmine

* Visibility
* Focus
* Event firing
* Keyboard events
* Mouse Events

!SLIDE left

# Easy to test in Jasmine

* Interfaces of your objects
* Client/server interactions
* _Presence_ of DOM nodes

!SLIDE

# Everything Else?

## Integration Tests

!SLIDE

# Selenium

## There. I said it.

!SLIDE bottom-right

# Other thoughts

}}} images/rodin.jpg::maiac::flickr::http://www.flickr.com/photos/maiac/3476481538/

!SLIDE

# You're writing an _app_

## Not just a 'stateless' server

!SLIDE

# POJSO's have their place

## Extract code into objects 

### (and test them)

!SLIDE

# Miss Controllers?

## MVC works pretty well

!SLIDE

# Separate your View logic

## Read [The Humble Dialog Box](http://www.objectmentor.com/resources/articles/TheHumbleDialogBox.pdf)

!SLIDE

# Enough with `bindAll`

## Constructors as closures?

!SLIDE left

# Show Notes

* Watch Yehuda Katz's [Rails 3 for Mobile Applications](http://www.engineyard.com/video/12678746)
* Michael Feathers's [The Humble Dialog Box](http://www.objectmentor.com/resources/articles/TheHumbleDialogBox.pdf)
* [Bulldog](http://github.com/infews/bulldog), a single-page 'app' for [todo.txt](http://todotxt.com) - how I use Backbone
* [Jasmine Google group](http://groups.google.com/jasmine-js)

!SLIDE

# Thanks!

### [@dwfrank](http://twitter.com/dwfrank) | [Bio](http://dwf.bigpencil.net)



