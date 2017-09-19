# Interoperable Applications Specification
## Version 0.5

## Preface
This document is meant to be a living document to further the development of interoperable web and desktop applications.  Interoperable applications are applications that have requirements of working with other applications.  RESTful web driven services offer an easy connectivity between applications.  It is not meant to be the spoken word of the programming gods, however it is a series of beliefs and best practices developed over years of experience with desktop, mobile, and web application development.  This document is free to be commited to and improved upon by any individuals looking to deepen the specification.

### Community of Developers
We want other developers to contribute to this project and help us make more informed decisions about writing applications.  Join and be a part of this document, but please do so in a respectful way.  We want all developers to feel welcome to contribute ideas here based on merit.  We will not tolerate bad behavior in the community.
 
## Software Development Principles
Software Development Principles are like moral guidelines for writing software.  Just like your moral compas they are a set of beliefs that guide your behavior.  Staying true to the identity of your software development principles will make the decision making pieces of software much easier.

### Single Responsibilty / Division of Responsibility
The single responsibility (or Division of Responsibility principle is about assigning one responsibility over a single part of an application to a class.  When software is written this way it generally results in smaller testable sections of code.  It also makes dependency injection or inversion of control easier as the class is easily placed in either the constructor of another class or in a builder pattern.  Single responsibility also has the benifit of only ever having one reason to change a class and that is that the requirements for that single responsibility changes.

### Layered Approach to Software Development
The layered application design or (Multitier Software Development) is designed around dividing responsibility of an application into a few common layers.  Because of this it is related to the first Single of Responsibility principle.  The most common layers in multilayered applications are Presentation, Application, Business, and Data Access Layer.

#### Presentation Layer
The presentation layer is the User Interface.

#### Application Layer
The application layer is the service layer of the application.  In RESTful applications this is the controller / router layer of the application.

#### Business Layer
The business layer is where all of the business / domain logic happens.

#### Data Access Layer
The data access layer is the persistence layer.  It interacts with your database or long term storage mechanisms.  It also handles any logging or caching.

### RESTful API Architecture
RESTful applications are applications that access a service layer through means of hitting RESTful endpoints (or URIs).  The user interface is completely separate from the remainder of the application.  An application should be able to change the entire front end without rewriting a single line of back end code.  The reason that this is important in regards to having applications work together is that the data / service your REST api provides should be able to support one or many different interfaces.  The interfaces are going to vary based on the system your user is trying to design based on one API or a series of differnt APIs.  Using RESTful APIs and a common language like JSON it allows our user to decide how to combine our services together to create unique application experiences.

### Agile Manifesto
The Agile Manifesto is a very short read that covers some very important principles of 'Agile' software development.  Agile is a buzzword that gets abused in Software Development as a substitution for the word SCRUM or XP.  It really doesn't mean any of those things.  A quick read through the agile manifesto would probably be the best way to really understand what Agile is and it is encouraged that everyone should do this.  http://agilemanifesto.org/

## Software Development Practices
Software Development practices are complimentary to your software development principles.  The practices are the embodiment of the software development principles.  They are the behaviors of Software Engineers who respectes the values of good software development principles.  These are some of the tips and tricks to leading a healthy software development lifestyle.

### The Next Developer
As a software engineer we must be cognicent that software changes.  We have all worked in poorly written spaghetti legacy code that doesn't make sense to us.  It takes hours to read through and hours to debug.  This type of software leaves a really bad taste when you have to work with it.  The Next Developer principle is an attempt to stop the perpetuation of this cycle.  When writing software always try to write both your code and your comments in a way that when the next poor sap comes to this piece of code they can understand with relative ease what is happening in any given function or class.  This means that if you do something weird explain why it was done that way and why it was the best way to sovle the problem.  Don't leave someone else a TODO without an explanation as to why it didn't get done.  TODOs that are left incomplete can make you seem like you don't respect other developers time.  Always try to leave the code with accurate comments by cleaning up prior comments.  Also always update your test and finally always write meaninful and short commit messages.  The next guy who looks at your code may not even be someone else.  It could be you three years down the road.

### Test Driven Development
Test driven development is a technique used to write software with single responsibility in mind.  TDD you write the test before you write the code.  The next step is to write the code and ensure that all test pass.  Then you refactor the code to make it better and repeat the process.  This is refered to as Red, Green, Refactor.  By doing this you can tell if the domain of what you are currently working with is too complex and if it needs to be split up into multiple classes.  The test also act as a form of documentation for the next developer explaining all of the features and corner cases associated with a class.  TDD is not always possible and really is just a tool for ensuring good software design.  When TDD can't be used always ensure that you write automated test after the fact to ensure your code is performing as expected.

#### When are test complete?
Test are complete when all cases in the software have been tested.  A good initial indication of this is using a code coverage tool to check and ensure that every line of code in a file is hit.  When lines of code can't be hit that is fine, but understand that with each line of untested code is a potential unpredictable headache later down the road.

#### How to know a test is working?
To know for sure a test is working you should write the test before any code is written.  Then run the test.  If the test passes even though the code hasn't been implemented you know that you have written a test that can't fail and you should consider reworking it before continuing.

### Comment First
Comment first is a technique that a Software Developer lays out the funcationality of the section of code they are about to write before they write it.  It is a good way to ensure that you code is documented well and it allows you to plan out and put your thoughts onto paper.  It also has the added benefit during pairing of allowing other people to understand where you are going so they can help guide you through the process of completing a feature.

### Web First
Web first development is a principle where you design the user interface of your application to work on a mobile device first.  The principle simply states that if the application looks good and works on a mobile device it will scale and work on a desktop computer or tablet no problem.

### Database Design and Effective Data Modeling
// TODO This section of the document needs extensive research done.  I did not complete this section as I haven't done the research to complete this section.  Any other epxerts in this matter please feel free to contribute or I will spend the time to figure out the best advice I can provide for this section.

### Be Excited to Learn
Being excited to learn is the biggest advantage a Software Developer can give themselves in this field.  All successful Software Engineers are excited to discover and explore new territory.  This single skill will truely make you an unstoppable force. // TODO Elaborate on this more when motivation is feeling higher.

### RESTful Endpoints Format
### Component Driven User Interface

## Wind up
