CNeff_of_Asgard
===============

This is for the Create Personal Github/BitBucket Repo assignment.

//Here's the code of Step-2 of Angular-Phonecat that I've modified.

'use strict';

/* Controllers */

var phonecatApp = angular.module('phonecatApp', []);

phonecatApp.controller('PhoneListCtrl', function($scope) {
  $scope.phones = [
    {'name': 'IronMan Jarvis Phone',
     'snippet': 'The smartphone that really is smarter than you.'},
    {'name': 'Thor Phone: Hammer Edition',
     'snippet': 'Brings magic and science into one electrifying phone.'},
    {'name': 'The Hulk Smash',
     'snippet': 'Featuring the largest screen ever made for a tablet.'},
    {'name': 'Black Widow 2.0',
     'snippet': 'This phone is ideal for undercover work.'},
    {'name': 'Hawkeye Galaxy S4',
     'snippet': 'This popular Samsung phone has been upgraded to include a expandable bow (arrows not included).'},
    {'name': 'Captain America Retrophone',
     'snippet': 'All of the latest features in an old-school design.'}
  ];
});

//Here's the modified code so that the unit test passes.

'use strict';

/* jasmine specs for controllers go here */
describe('PhoneCat controllers', function() {

  describe('PhoneListCtrl', function(){

    beforeEach(module('phonecatApp'));

    it('should create "phones" model with 6 phones', inject(function($controller) {
      var scope = {},
          ctrl = $controller('PhoneListCtrl', {$scope:scope});

      expect(scope.phones.length).toBe(6);
    }));

  });
});

