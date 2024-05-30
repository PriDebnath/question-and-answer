
Questions

1. What is angular ?
2. Explain Angular modules :
3. Explain data binding :
4. What is Angular CLI?
5. Explain Angular directives
6. What is dependency injection in Angular?
7. What are Angular components?
8. What is Angular routing and how does it work?
9. What is Angular HttpClient?
10. What are pipes in Angular?
11. Explain Angular forms and form validation
12. What is Angular testing and what are the different testing utilities provided by Angular?
13. What are Angular guards and why are they used?
14. Explain intercept
15. How do you deploy an Angular application?
16. Authentication and authorization
17. What is angular template ?
18. Explain life cycle hooks 
19. Annotations and decorators
20. Explain expression, javaScript vs angular expression
21. ng-content
22. ViewChild() vs ContentChild()
23. Bootstrapping in angular
24. Zone.js
25. Change detection
26. Oporator in Rxjs
27. Subject and BehaviourSubject
28. Host listener
29. Explain all data binding in angular
30. How can we pass data from one component to another component ? 


Questions and answers

1. What is angular ?
    Angular is a typescript based  open-source ( a software which is freely available to public, they can use or modify it ) web application framework for creating single page application .


2. Explain Angular modules :
     Angular modules are containers for a group of related components, directives, pipes or services . We can make modules that is dedicated to a specific part of an application . Some of the benefits are they encapsulates components, directives, pipes and services preventing them to leak in global scope . 
They are reuseable in multiple applications.
Angular modules can be lazy loaded meaning they can be loaded on-demand rather then upfront which helps application performance . 


3. Explain data binding :
    Data binding in angular is like bridge between application's code ( mainly ts files ) and application's view ( mainly html files ) .
There are two types of data binding in angular 
 1. One way data binding
 2. Two way data binding . 
In one way data binding when model data changes the view data get changed as well .  On the other hand in two data binding model and view stay in sync if view value get changed by user model value will change as well and vice versa .
```
 [(ngModel)]="modelName"
```

4. What is Angular CLI?
   Angular  CLI ( command line interface ) is a command line tool . Using this we can create an angular project, its components, pipe or services .  
CLI commands like
```
 "ng g c component-name" 
```
can be used to create component .


5. Explain Angular directives
    Using directives we can add specific behaviour to html elements . There are three types of directives 1. component, 2. Attribute and 3. Structure directives . 

Component directives: we can create them using @component and pass selector-name and template . 
```
@component({
  selector: 'app-example',
   template: '<p>This is a component directive</p>' 
})
```
Attribute Directives: we can attach  them to html elements to control it . Like here controling its class . Like [ngClass]
```
<p [ngClass]={}> Text </p>
```
Structure Directives: we can use them to control the structure of html elements like we can use
```
*ngIf="condition"
```
 to conditionally render it or we can use ngFor to loop to iterate over something . 


6. What is dependency injection in Angular?
  Dependency injection is a design pattern where a class gets dependency from external source rather than creating on its own . Like we can create a service which gets data from backend and later we can inject the service to multiple components where ever needed . It is reusable and testable . 


7. What are Angular components?
   Angular components are one of the most important building block on angular application .  They are responsible for rendering data and responding to user's action  . They represent ui control . Components can be module based or standalone .


8. What is Angular routing and how does it work?
    Routing helps  navigate to different component of the application without refreshing the page  . Using routing we create single page application .


9. What is Angular HttpClient?
   Http is a built in angular module we can use to perform http requests like GET, POST patch delete  .



10. What are pipes in Angular?
    Pipes are a feature of angular which help us transforming data . Like "number"  or "date" pipe . There are two types of pipe pure and impure . We can set a pipe to impure by setting its "pure" property to false .  
Pure pipe are solely dependent on input data and they are stateless, whereas impure pipes are not fully dependent on input data and it can has asynchronous task or API call  . Like async pipe to display an observable data



11. Explain Angular forms and form validation
   We use angular form to take input from user and validate the input data .
There are two types of forms in angular template driven form and reactive form . We can import formBuilder and form group to create a reactive form  .


12. What is Angular testing and what are the different testing utilities provided by Angular?
   Testing in angular involves writing and executing tests to verify the behaviour of a component, service or a pipe . Angular provides testBed to configure and create testing module to test component, service and other things . Later we can use Jasmine  testing library for javaScript which provides functions "describe" , "it" and "except"   to define test cases and assertion . Then use Karma test runner which helps run our test in different environments .


13. What are Angular guards and why are they used?
    Guards are used to control access of certain routes , we can use it implement authentication, authorization or we can control any security related activity .
Angular provides classes like CanActivate, CanActivateChild, CanDeactivate, CanLoad we can use them to create guards and attach it to routes .


14. Explain intercept
  We use it to modify request and response of api call . Also to set the header of request and add authentication token  to it . 



15. How do you deploy an Angular application?
  We can use ng build command and then take the built folder and host it on a server . And we can automate this with github action .


16. Authentication and authorization 
   Using Authentication we can verify a valid user .
Authorization is a way to control the access of data for different users . Suppose once we post login credentials to an authetincate api then the api returns a jwt token which  will be used next time to identify the user this is called authentication .  Now we can look into the permissions a user has and the user may  not have the permission to visit a certain routes so we can control the access accordingly  . This is called authorization .



17. What is angular template ?
   Angular template are written in html and  may contains a angular related elements, attributes and data from model .
    

18. Explain life cycle hooks 
   Angular provides few lifecycle hooks to look into the key moments in the lifecycle of a component or directive . For component it is   "ngOnIt", "ngOnChanges", "ngViewInIt" "ngOnDestroy"  .
ngOnInit: use it for initializing data of the component or fetching some data . It gets calls once while constructing the component .
ngOnChanges: it gets called whenever data of a input property of a component changes
ngAfterViewInit: it gets called when the html fully loaded .
ngOnDestroy: when a component is about to destroy and getting removed from dom . mostly we use it for clean up task like  unsubscribe ovserables 
or cancel timer .


19. Annotations and decorators
  Annotations and decorators are used in angular to provide meta data to classes, component, services and other things . An annotation is represented as "@" and we write the decorators name after that . 
"@decoratorName" example could be @component decorator to define a component with its meta data .


20. Explain expression  javaScript vs angular expression .
   Expression is a combination of values, variable, operator and functions which return some result . Manipulating data make decisions comes under this . Like 5 + 6 
could be a expression .   The significant difference are like javaScript expression can be written anywhere with valid js syntex and   angular expression should be written within curly braces {{ expression }} . Js expression will be executed by js engine and angular expression will be executed by angular template engine . 





21. ng-content 
When we use a sub component inside a parent component, while invoking that sub component on parent component we can pass more html contents  which will be visible in  sub component using below code .
```
// parent.html
<h1> I am parent </h1>
<app-sub-com>
   <p> extra content from parent </p>
<app-sub-com>
```
```
//sub-com.html
<h1> I am sub com </h1>
<ng-content>
  <!-- extra content will appear here-->
</ng-content>
```


22. ViewChild() vs ContentChild()
Viewchild is a decorator which enables you to get access to a child component or a DOM element .
ContentChild is also a decorator which give access to the content "projected" or passed from parent component . The passed content can be inserted latter using a placeholder named <ng-content> .



23. Bootstrapping in angular 
In Angular, bootstrapping refers to the process of initializing and running an Angular application. It involves loading the root module of the application which mostly is app.module.ts and then compiling and launching the component tree. 


24. Zone.js
Zone.js is a library that helps Angular to detect and react to asynchronous events .
Whenever an asynchronous operation occurs (like a setTimeout or an HTTP request), Zone.js detects it and triggers Angular's change detection mechanism. 
This ensures that Angular components are updated accordingly.



25. What is  Change detection in angular
In Angular, change detection works by comparing the current state of the application  with its previous state. If it detects any difference it update UI .  After each event or asynchronous operation (such as HTTP requests, setTimeout, etc.), Angular runs change detection. 




26. Oporator in Rxjs
We use them to create or transform  stream of observables . 
Creation Operators (of, interval, throwError),
Transformation Operators (map, switchMap),
Filtering Operators (filter),
Error Handling Operators (catchError),
Conditional and Boolean Operators (take),
    switchMap will only emit the result of the latest operation and cancel the previous ones
   ForkJoin takes last values emitted by multiple observables and combine then into a single value .



27. Subject and BehaviourSubject
Subjects and BehaviorSubjects are a bit different from the operators . They are
special types of observables that act as both observers and observables themselves . We can also push new values into the observable stream .
Example:
```
const behaviorSubject$ = new BehaviorSubject<number>(1);

behaviorSubject$.next(2);  

behaviorSubject$.subscribe(value => console.log('New BehaviorSubject:', value)); 
```

28. Host listener
host listeners are used to listen to events on the host element of a component. .
It allows you to interact with the DOM and perform actions based on user interactions.


29. Explain how we can bind  data  in angular application .
    Interpolation ({{ }}): Used to output a component property value within the HTML template. For example : {{ myProperty }}.

    Property binding ([property]="value"): Sets an HTML element property value to the value of a component property. For example, [src]="imageUrl".

     Event binding ((event)="handler()"): Listens for specific events emitted by HTML elements and executes the specified component method. For example (click)="onClick()".

    Two-way binding ([(ngModel)]): Combines property binding and event binding in a single notation to update both the model and the view. Used primarily with form elements like <input> and <textarea>.

    Attribute binding ([attr.attributeName]="value"): Binds an element attribute to a component property.

    Class binding ([class.className]="condition"): Binds CSS classes to an element based on the evaluation of a condition .


    Style binding ([style.styleName]="value"): Binds CSS styles to an element based on the value of a component property.



30. How can we pass data from one component to another component ? 
  To pass data from parent to child we can use "@Input()" in child component to access the passed data .
To pass data from child to parent we can use "@Output()" and emit some data to parent . Other then that we can make a subject or behaviour subject and put in into a service then any component can push or consume data from it .

