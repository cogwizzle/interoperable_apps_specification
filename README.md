# Interoperable Applications Specification
## Version 0.5

## Preface
This document is meant to be a living document to further the development of interoperable web and desktop applications.  Interoperable applications are applications that have requirements of working with other applications.  RESTful web driven services offer an easy connectivity between applications.  It is not meant to be the spoken word of the programming gods, however it is a series of beliefs and best practices developed over years of experience with desktop, mobile, and web application development.  This document is free to be commited to and improved upon by any individuals looking to deepen the specification.

## Software Design
This section will outline best practices when designing interoperable software.  This section will go over the layered application approach to software development, how to design effective user interfaces, and how to link multiple applications together.  We will also touch on Design Patterns and Testing.

### Layered Architecture
The Layered Architecture design approach involves subdividing your software into four different sections.  The presentation layer, the business layer, the persistence layer, and the database layer.  Each of these layers should of a clear Division of Responsibility.  Division of responsibility is a principle that each module or class should have only one responsiblity.  The following example is a good representation of what good layered applications look like.

1. Database - MySQL
2. Persistence - PersonDao class : Data access object for Person entity.
3. Businesss
  * Person - Representation of a person.
  * PersonService - Layer for interacting with person objects.
4. Presentation Layer - RESTful web API for accessing data.

Even though the presentaiton layer in this example doesn't have a traditional user interface as the presentation layer it still has clear division of responsiblity at each level of the design.  Each piece in this example has only one responsibility.

### User Interfaces
Division of responsibility is also very important when it comes to designing a user interface.  When building a user interface it is generally a good idea to break down the interface into smaller reusable components.  It is no wonder that libraries like React, RiotJS, Vue, and Angular have taken such a hold with modern JavaScript engineers.  As oposed to the older technologies it is much easier to write small components that are testable and more relaible.  It is still possible to use component based design with older frameworks like jQuery, or even Java Swing.  Using the jQuery example you can use jQuery plugins to add the dynamic flare to your web pages.  And as far as Java Swing allows you to extend the functionality of the base Swing classes in a way that can meet modern component based design.

It should also be noted that your user interface should be completely seperate from your backend.  A new user should be able to create a completely different user interface for you application wihtout the backend ever being able to tell.  This wll allow developers to include data from multiple sources in a user interface that is multi system inclusive.  This is where all of the power of interoperable software applications comes from.

### Prefer Design Patterns
Design patterns are proven solutions to common software development problems.  When designing software it is generally a good idea to use these patterns when applicable.  A new developer working on your project can save time reading through code by learning common design patterns for a given language.  This will increase productivity and allow developers to easily communicate the value of classes.  The pattern also has a proven track record of success.  Always prefer common design patterns where possible and always learn the most common patterns for the languages you work in.

### Test
This point should go without saying, but in my experience this is still up for debate among some developers.  You should always test your code as completely as possible.  No matter what!  If you were a customer you wouldn't buy a bike that wasn't tested.  If you were a bik manufacturer you wouldn't by a wheel for a bike that wasn't tested.  As a wheel manufacturer you woudn't buy rubber from someone who did not rate the material for making bike wheels.  These principles still apply to software development.  Yes testing is hard.  It takes time, but it also saves time later down the road.  Automated test are the fastest and prefered method for testing.  In the event that this is not possible because of legacy code then I recomend writing a matrix of class dependencies and writing test cases for your application.  Once you have done all of that work move to automated test as soon as possible.  Don't let your customers fall on their face by using your poorly test product.

### Wire it up
Generally the prefered way to wire applications up is through a RESTful API.  Your front end should talk to one or more RESTful applications and load without the dependency on the data existing.  This will allow you to create unique experiences for you customer using multiple services in one application.  If your front end and back end are completely separate as spoken about before you can write the front end or the back end in the langauge of your choice.  It works in a similar manner to microservices in the sense that the language doesn't matter as the API is the language in which you communicate with the application.  RESTful APIs are our applications common language.

// TODO continue here.

## Wind up
// TODO write wind up.
