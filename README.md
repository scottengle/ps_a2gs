# Course Work for Pluralsight Course 'Angular 2: Getting Started'

https://app.pluralsight.com/library/courses/angular-2-getting-started-update

## "It's Just Angular"

This course makes some comparisons between AngularJS (Angular 1) and Angular (Angular 2 and beyond). Whenever I reference Angular 1, I'll refer to it as "AngularJS". The title of the course is slightly incorrect since it was created before the switch to "It's Just Angular". 

For more information:

http://angularjs.blogspot.com/2016/12/ok-let-me-explain-its-going-to-be.html

# External Resources

*Angular Documentation*: https://angular.io/

*Angular Quick Start*: https://angular.io/docs/ts/latest/quickstart.html

*AngularCLI*: https://cli.angular.io

*Angular Library Packages*: https://www.npmjs.com/~angular

*Course Blog Site*: http://blogs.msmvps.com/deborahk/angular-2-getting-started-problem-solver

*GitHub Repo*: https://github.com/DeborahK/Angular2-GettingStarted

*TypeScript Playground*: http://www.typescriptlang.org/Playground/

*Standard HTML Element Events (MDN)*: https://developer.mozilla.org/en-US/docs/Web/Events

*Array Filter Function (MDN)*: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter

*Rx Marbles*: http://rxmarbles.com

# Why AngularJS

* Expressive HTML
* Powerful data binding
* Modular by design
* Built-in back-end integration

# Why Angular

* Built for speed
* Modern
* Simplified API
* Enhances Productivity

# Angular Is...

* A JavaScript Framework for building client-side applications using HTML, CSS and JavaScript
* A platform supporting
  * Multiple languages
    * ES5, TypeScript
  * Multiple templating syntaxes
    * HTML, XML
  * Multiple rendering targets
    * DOM, native
* Mobile Web
  * Material Design
  * Angular Universal
  * Web Workers
* Native Mobiles Apps
  * Ionic
  * Native Script

# Anatomy of an Angular Application

* An *Application* is comprised of several *Components* and some *Services* that provide functionality across those *Components*
* A *Component* is a *View* defined by a *Template*, its associated code defined with a *Class*, and additional information defined with *MetaData*
* Angular *Modules* help organize an application into cohesive blocks of functionality
* Each application has a single *Root Module*
* Each application can have zero to many *Feature Modules*

# What is TypeScript

* Open source language
* Superset of ES 2015
* Transpiles to plain JavaScript
* Strongly Typed
  * TypeScript type definition files (*.d.ts)
* Class-based object-orientation

# Running the Sample Application

Code available at https://github.com/DeborahK/Angular2-GettingStarted

    npm i
    npm start

# Checklists

* Something is Wrong!
  * Press `F12` or `Cmd+Option+i` for browser console
  * Recheck your code
    * HTML
      * close tags
      * Angular directives are case sensitive
    * TypeScript
      * Close braces
      * TypeScript is case sensitive
  * Check *Course Blog Site* post for a solution

* Components
  * Create class for the component with some code to support the view
  * Use a decorator to define the metadata
  * import what we need from 3rd party modules or our app modules
  * Class
    * Use a clear name
      * Use `PascalCasing` for name
      * Append `Component` to the name
    * Add `export` keyword to class signature
    * Data in properties
      * Elements defined as properties of the class
      * Add appropriate data types for TypeScript
      * Add appropriate default values
      * Use `camelCase` for names
    * Logic in methods
      * Use `camelCase` for names
    * Metadata
      * Component decorator
        * Prefix with `@`
      * `selector`
        * Not needed if component isn't used in HTML
        * Prefix for clarity
      * `template`
        * The View's HTML
        * Correct HTML syntax
    * Import
      * Defines where to find the member that this component needs
      * `import` keyword
      * Member name
        * Correct spelling/casing
      * Module Path
        * Enclose in quotes
        * Correct spelling/casing
  * Encapsulating Styles in a Component
    * `styles` property of decorator
      * Specify an array of style strings
    * `styleUrls` property
      * Specify an array of stylesheet paths
  * Lifecycle Hooks
    * `import` the lifecycle hook interface
    * `implement` the lifecycle hook interface
    * Write the code for the lifecycle hook method
  * Nested Components
    * `@Input` decorator for arguments passed from container to nested component
      * Attached to a property of any type
      * Prefix with `@`
      * Suffix with `()`
    * `@Output` decorator for data passed from the nested component to a container
      * Attached to a property declared as an EventEmitter
      * Use the generic argument to define the event payload type
      * Use the `new` keyword to create an instance of EventEmitter
      * Prefix with `@`
      * Suffix with `()`
  * Container Component
    * Use the directive
      * The Directive name is nested component's selector
    * Use property bindings to pass data to the nested component
    * Use event binding to respond to events from the nested component
      * Use `$event` to access the event payload passed from the nested component
  * Relative Paths with Module ID
    * Set the moduleId property of the component decorator to module.id
    * Change the URLs to a component relative path
      * `templateUrl` property
      * `styleUrls` property

* Templates
  * Use inline template
    * For short templates
    * Specify the `templateUrl` property
    * Use the ES 2015 backticks for multi-line
    * Watch syntax
  * Use linked templates
    * For longer templates
    * Specify the `templateUrl` property
    * Define path to external template file
  * Component as Directive
    * Use component `selector` as an element in the template as a directive
    * Define `selector` in `Component` metadata
    * Declare `Component` to make it available in the Angular Module
      * Add `Component` to `Declarations` array of Angular Module 
  * Interpolation
    * One-way binding form component class property to element property
    * Defined with double curly braces
      * Contains a template expression
      * No quotes needed

* Directives
  * Structural Directives
    * *ngIf and *ngFor
    * Prefix with asterisk
    * Assign to a quoted string expression
    * *ngIf
      * Conditionally adds or removes elements from the template
      * Expression is evaluated as true/false
      * When evaluated as true, the element is added to the DOM
      * When evaluated as false, the element is removed from the DOM
      * Declared in the Browser module
    * *ngFor
      * Repeats a portion of the DOM tree once for each item in an iterable list
      * Define local variable with `let`
      * Specify `of` (not `in`)
        * "let product of products"
      * Declared in the Browser module

* `ngModel`
  * Define with "football in a box", "banana in a box", etc.
    * `[(ngModel)]="listFilter"`
  * Add FormsModule to your Module
    * `import { FormsModule } from '@angular/forms'`
    * Add to imports array of Module (probably AppModule)
      * `imports: [BrowserModule, FormsModule],`

* Interfaces
  * Defines custom types
  * Promotes strong typing
  * Creating
    * Use `interface` keyword
    * `export` the interface
  * Implementing
    * `implements` keyword and interface name
    * Write code for each property and method required by the interface
    
* Pipes
  * Pipe Character: `|`
  * Pipe Name
  * Pipe Parameters
    * Separate with colons
      * `{{ product.price | currency: 'USD':true:'1.2-2' }}`
  * Custom Pipes
    * Building Custom Pipe
      * `import` Pipe and PipeTransform
      * Create a class that implements the PipeTransform
        * `export` the class
      * Write code for the Transform method
      * Decorate the class with the `Pipe` decorator
    * Using a Custom Pipe
      * `import` the custom pipe
      * Add the pipe to the declarations array of an Angular module
      * Any template associated with a component that is also declared in that Angular module can use the Pipe
      * Use the pipe in the template
        * Pipe character
          * `|`
        * Pipe name
        * Pipe arguments (separated by colons)

* Services
  * Service class
    * Clear name
    * Use PascalCasing
    * Append `Service` to the name
    * `export` keyword
  * Service decorator
    * Use `@Injectable()`
      * Prefix with `@`
      * Suffix with `()`
    * Import what you need
  * Registering a Service
    * Select the appropriate level in the hierarchy
      * Root component if service is used throughout the application
      * Specific component if only that component uses the service
      * Otherwise, common ancestor
    * Component Metadata
      * Set the providers property
      * Pass in an array
    * Import what you need
  * Dependency Injection
    * Specify the service as a dependency
    * Use a constructor parameter
    * Service is injected when component is instantiated

* Http
  * Setup
    * Add HttpModule to the imports array of one of the application's Angular Modules
  * Service
    * Import what we need
    * Define dependency for the http client service
      * Use a constructor parameter
    * Create a method for each http request
    * Call the desired http method, such as get
      * Pass in the URL for the desired endpoint
    * Map the Http response to a JSON object
    * Add error handling
  * Subscribing
    * Call `subscribe` method of the returned observable
    * Provide a function to handle an emitted item
      * Normally assigns a property to the returned JSON object
    * Provide an error function to handle any returned errors

* Routing
  * Displaying Components
    * Nest-able Components
      * Requires a selector
      * Nest in another component
      * Does not need a route
    * Routed components
      * No selector
      * Configure the routes
      * Tie routes to actions
  * Doing Routing
    * Configure route definitions
      * Define the base element in index.html
      * Import RouterModule into AppModule
        * Add each route (RouterModule.forRoot)
        * Order matters
      * Route definitions require
        * `path`
          * No leading slash
          * `''` for default route
          * `'**'` for wildcard route
        * `component`
          * Not a string
          * Not enclosed in quotes
    * Tie routes to actions
      * Add RouterLink directive as an attribute
        * Clickable element
        * Enclose in square brackets
      * Bind to a link parameters array
        * First element is the path
        * All other elements are route parameters
    * Place the view
      * Add RouterOutlet directive
        * Identify where to display the routed component's view
        * Specified in the host component's template
  * Passing Parameters
    * Add param to route configuration path
      * `{ path: 'product/:id', component: ProductDetailComponent }`
    * Add param to router link
      * `<a [routerLink]="['/product', product.productId]">{{product.productName}}</a>`
    * Import the `ActivatedRoute` service into the component
      * `import { ActivatedRoute } from '@angular/router';`
    * Add the `ActivatedRoute` service to the component constructor
      * `constructor(private _route: ActivatedRoute) { }`
    * Read out the route parameter
      * `console.log(this._route.snapshot.params['id']);`
      * The parameter name must match the one in the route definition (i.e. 'id')
  * Activate a Route with Code
    * Use the Router service
      * Import the service
      * Define it as a dependency
    * Create a method that calls the navigate method of the Router service
      * Pass in the link parameters array
    * Add a user interface element
      * Use event binding to bind to the created method
  * Route Guards
    * Build a Guard service
      * Implement the guard type (i.e. CanActivate)
      * Create the method (canActivate())
    * Register the guard service provider
      * Must be registered in a Module (not a component)
    * Add the guard to the desired route

* Module Structure
  * Every application must have a root application Module
    * `AppModule` by convention
  * Every application must have a root application component
    * `AppComponent` by convention
    * `AppModule` will bootstrap `AppComponent`
  * Define separate Angular modules for each feature
    * Enforces separation of concerns
    * Helps keep `AppModule` from getting too large
  * Create shared modules (`SharedModule`) for components, directives and pipes you want to share
    * Primarily use the `exports` and `declarations` array
  * Create core modules (`CoreModule`) for services you want to ensure are loaded on application start
    * Ensure that core modules are imported only once in `AppModule`
    * Primarily have `providers`, none of which are exported
  * Create routing modules for routes
  * Decorate modules with `NgModule` metadata
    * Includes:
      * Bootstrap array
        * Startup components
      * Declarations array
        * Components, directives and pipes that belong to the module
      * Exports array
        * Components, directives and pipes that an importing module can use
      * Imports array
        * Components, directives and pipes used by the module
      * Providers array
        * Service providers
        * Angular registers each provider with Angular's root application injector

# Modules

## ES 2015 Modules

    // in product.ts
    export class Product { }

    // in product-list.ts
    import { Product } from './product' // <= don't add the file extension

## Angular Modules

* Root Angular Module
* Feature Angular Module
* Shared Module

## Angular Components

Each component belongs to a single module.

## Difference between ES Modules and Angular Modules

    ES Modules                Angular Modules
    -----------------------   ------------------------------
    Code files that import    Code files that organize
    or export something       the application into cohesive
                              blocks of functionality

    Organize our code files   Organize our application

    Modularize our code       Modularize our application

    Promote code reuse        Promote application boundaries

# Angular Components

*Components* have a *Template* (the *View), *Class* (the behavior) and *MetaData* (extra information for Angular).

## Templates

* View layout
* Created with HTML
* Includes binding and directives

## Class (Properties and Methods)

* Code supporting the View
* Created with TypeScript
* Properties: data
* Methods: logic

## MetaData

* Extra data for Angular
* Defined with a decorator

## Creating Components with Decorators

* Decorators are a function that adds metadata to a class, its members or its method arguments
* Prefixed with `@`
* Angular provides built-in decorators
* Components should always have a template

## Importing what we need

Before we use an external function or class, we define where to find it using an import statement.

Import allows us to use exported members from eternal ES modules.

## Completed Component

    import { Component } from '@angular/core';

    @Component({
      selector: 'pm-app',
      template: `
      <div><h1>{{pageTitle}}</h1>
        <div>My Component</div>
      </div>
      `
    })
    export class AppComponent {
      pageTitle: string = 'Acme Product Management';
    }

## Bootstrapping the App Component

* Load the root component (bootstrapping)
* Host the application

## Single Page App (SPA)

* index.html contains the main page for the application
* this is often the only web page of the app
* An Angular app is often called an SPA

## Angular Application Startup

`index.html` holds the root application component.

    System.import('app')...;

    <body>
      <pm-app>Loading ...</pm-app>
    </body>

SystemJS imports the ES module from the `app` folder, specifying the `main.js` file as the default starting location.

    packages: { 
      app: {
        main: './main.js',
        defaultExtension: 'js'
      }
    }

`main.ts` has the bootsrapping code in it.

    import { platformBrowserDynamic } from '@angular/platform-browser-dynamic';
    import { AppModule } from './app.module';

    platformBrowserDynamic().bootstrapModule(AppModule);

`app.module.ts` contains some bootstrapping code in it.

    import { NgModule } from '@angular/core';
    import { BrowserModule } from '@angular/platform-browser';
    import { AppComponent } from './app.component';

    @NgModule({
      imports: [ BrowserModule ],
      declarations: [ AppComponent ],
      bootstrap: [ AppComponent ]
    })
    export class AppModule { }

`app.component.ts` is the root app component.

    ...
    @Component({
      selector: 'pm-app',
      template: `
      <div>{{pageTitle}}</div>
      `
    })
    export class AppComponent {
      ...
    }

# Templates, Interpolation and Directives

## Types of `Template`s:

* Inline Template 
  * Single-line with single quotes
  * Multi-line with backticks
* Linked Template
  * Use `templateUrl` in `Component` metadata

## Binding with Interpolation

Coordinates communication between the component's class and its template and often involves passing data.

Interpolation and one-way bindings with template expressions:

    // in Template
    <h1>{{pageTitle}}</h1>

    // in Class 
    export class AppComponent {
      pageTitle: string = 'Acme Product Management';
    }

## Directives

Custom HTML element or attribute used to power up and extend HTML.

* Custom
* Built-In

*Built-In Directives*

* *ngIf
  * Structural directive
  * Identified by an asterisk before the directive name
  * Declared in the Browser module
  * conditionally adds or removes elements from the template
* *ngFor
  * Identified by an asterisk before the directive name
  * Declared in the Browser module
  * Repeats a portion of the DOM tree once for each item in an iterable list

## For ... Of vs. For ... In

*For ... Of*
Iterates over iterable objects such as an array.

*For ... In*
Iterates of the properties of an object.
Think of `in` as iterating over the `index`.

Take this example:

    let nicknames = ['foo', 'bar', 'baz'];

    for (let nickname of nicknames) {
      console.log(nickname);
    }

    // outputs:
    // foo
    // bar
    // baz

    for (let nickname in nickname) {
      console.log(nickname);
    }

    // outputs:
    // 0
    // 1
    // 2

# Data Binding and Pipes

Types:

* Interpolation
  * `{{pageTitle}}`
* Property Binding
  * `<img [src]="product.imageUrl">`
* Event Binding
  * `<button (click)="toggleImage()"></button>`
* Two-Way Binding
  * `<ingput [(ngModel)]="listFilter"/>`

## Property Binding

Allows us to set a template expression to the value of an element property.

The binding target is enclosed in square brackets on left of the equals.

The binding source is on the right of the equals in quotes.

    //Using Property Binding
    <img [src]='product.imageUrl'>

    // Using Interpolation
    <img src={{product.imageUrl}}>

Property binding allows us to controll the component's DOM from the component's class.

Prefer property binding over interpolation, unless you need something more complex:

    <img src='http://openclipart.org/{{product.imageUrl}}'>

## Event Binding

Enclose bound event in parentheses. The template statement is enclosed in single quotes on the right of the equal sign.

Refer to standard events for options (see [External Resources](#external-resources)).

## Two-Way Binding

Use the `ngModel` (i.e. `[()]`) directive. Nicknamed "banana in a box", "football in a box".

`ngModel` is part of the Angular FormsModule.

    // Template
    <input [(ngModel)]="listFilter">

    // Class
    export class ListComponent {
      listFilter: string = 'cart';
    }

## Transforming Data with Pipes

* Transform bound properties before they are displayed
* Built-in pipes
  * date
  * number
  * decimal
  * perent
  * currency
  * json
  * slice
  * etc
* Custom pipes

### Pipe Examples

    // Interpolation
    {{ product.productCode | lowercase }}

    // Property Bindings
    <img [src]="product.imageUrl" [title]="product.productName | uppercase">

    // Chaining
    {{ product.price | currency | lowercase }}

    // With Parameters
    {{ product.price | currency:'USD':true:'1.2-2' }}

# More on Components

## Interfaces

Interfaces help enforce strong typing in TypeScript.

Interfaces are a `specification` identifying a related set of properties and methods.

A class commits to supporting the specification by `implementing` the interface.

Use the interface as a data type.

Interfaces are not supported by ES 5 or ES 2015, but are supported by TypeScript.

Import the interface as a data type in the imports.

Transpiled out of the resulting javascript after transpilation.

## Encapsulating Styles

Templates sometimes require unique styles.

We can either:
* inline the styles directly into the HTML
* build an external stylesheet and link it in index.html
* use the Component decorator using the `styles` property or `stylesUrls` array property

## Lifecycle Hooks

Component Lifecycle:
* Create
* Render
* Create and render children
* Process changes
* Destroy

Component Lifecycle Hooks
* OnInit
  * Perform component initialization, retrieve data
* OnChanges
  * Perform action after change to input properties
* OnDestroy
  * Perform Cleanup

To use a lifecycle hook, implement one of the interfaces.

    import { Component, OnInit } from '@angular/core';

    export class ProductListComponent implements OnInit {
      pageTitle: string = 'Product List',
      showImage: boolean = false;
      listFilter: string = 'cart';
      products: IProduct[] = [...];

      ngOnInit() : void {
        console.log('In OnInit');
      }
    }

## Building Custom Pipes

Pipes transform bound properties before display. You can build custom pipes.

    // Class
    import { Pipe | PipeTransform } from '@angular/core';

    @Pipe({
      name: 'productFilter'
    })
    export class ProductFilterPipe implements PipeTransform {
      transform(value: IProduct[], filterBy: string): IProduct[] {
        ...
      }
    }

    // Template
    <tr *ngFor="let product of products | productFilter: listFilter">

    // Add to Module
    declarations: [
      AppComponent,
      ProductListComponent,
      ProductFilterPipe,
    ],

## Relative Paths with Module Id

To use relative paths in component metadata, define a module Id.

    @Component({
      selector: 'selector',
      moduleId: module.id,
      templateUrl: '...',
      styleUrls: ['...']
    })

The `module.id` is a "semi-global variable" available when using the CommonJS module format.

Contains the absolute URL of the component class module file.

Requires writing modules in CommonJS format.

Requires using a module loader, such as SystemJS.

# Nested Components

Two ways to use:

* As a directive
  * Within a template
* As a routing target
  * Looks as though the user has travelled to another view

A component is nest-able:

* If its template only manages a fragment of a larger view
* If it has a selector
* If it optionally communicates with its container

Building a nested component:

* The outer component is the `parent` or `container` component
* The inner component is the `child` or `nested` component
* The nested component receives information from its container using `@Input` properties
* The nested component passes information back to its container by raising events with `@Output`

You use the `@Input` decorator to specify properties in a component that are passed in.

Data is passed using property bindings.

Use the `@Output` operator to pass data back to a Component's container using events.

`@Input` and `@Output` is the Component's Public API.

# Services and Dependency Injection

## Services 

A `Service` is a class with a focused purpose.

Used for features that:

* Are independent from any particular component
* Profide shared data or logic across components
* Encapsulate external interactions

If you register the service with Angular, it will maintain a singleton that can be used throughout the application through Dependency Injection (DI).

## Dependency Injection

DI is a coding pattern in which a class receives the instances of objects it needs (called dependencies) from an external source rather than creating them itself. In Angular, the external source is the Angular injector.

Building A Service:

* Create the service class
* Define the metadata with a decorator
* Import it into other areas where needed

Note: It is recommended to always decorate services with the `@Injectable()` decorator.

    import { Injectable } from '@angular/core';

    @Injectable()
    export class ProductService {
      getProducts(): IProduct[] {
        ...
      }
    }

## Registering a Service

To Register a Service:

* You must register a `Provider`
  * Code that can create or return a service
  * Typically the service class itself
* Define in component or Angular module metadata
* Registered in component
  * Injectable to component AND its children
* Registered in root Angular module
  * Injectable everywhere in the application

# Retrieving Data Using HTTP

## Observables and Reactive Extensions

* Observables
  * Observables help us manage asynchronous data
  * Treat events as a collection
    * An array whose items arrive asynchronously over time
  * Are a proposed feature of the next version of JavaScript
  * Use Reactive Extensions (RxJS) to use them now
  * Are used within Angular
  * Support Observable Operators
    * Methods on observables that compose new observables
    * Transform the source observable in some way
    * Process each value as it is emitted
    * Examples: map, filter, take, merge

### Promises vs. Observables

    Promise                         Observable
    ------------------------------  --------------------------------------------------
    Provides a single future value  Emits multiple values over time
    Not lazy                        Lazy - will not emit values until subscribed to
    Not cancellable                 Cancellable
                                    Supports map, filter, reduce and similar operators

## Sending an HTTP Request

    // In Service
    ...

    import { Http, Response } from '@angular/http';
    import { Observable } from 'rxjs/Observable';
    import 'rxjs/add/operator/map';

    ...

    @Injectable()
    export class ProductService {
      private _productUrl = 'www.mywebservice.com/api/products';

      constructor(private _http: Http) {
      }

      getProducts(): Observable<IProduct[]> {
        return this._http.get(this._productUrl)
                   .map((response: Response) => <IProduct[]>response.json());
      }
    }

    // In AppModule
    ...
    import { HttpModule } from '@angular/http';

    @NgModule({
      imports: [
        ...
        HttpModule
      ]
      ...
    })

## Exception Handling

Use `.catch` to catch errors. You can also use the `.do` operator to do extra things (like logging to the console);

    ...
    import 'rxjs/add/operator/do';
    import 'rxjs/add/operator/catch';
    ...

    get products(): Observable<IProduct[]> {
      return this._http.get(this._productUrl)
                 .map((response: Response) => <IProduct[]>response.json())
                 .do(data => console.log('All: ' + JSON.stringify(data)))
                 .catch(this.handleError);
    }

    private handleError(error: Response) {
      ...
    }

## Subscribing to an Observable

    x.then(valueFn, errorFn)                              // Promise
    x.subscribe(valueFn, errorFn)                         // Observable
    x.subscribe(valueFn, errorFn, completeFn)             // Observable; completeFn is rarely used
    let sub = x.subscribe(valueFn, errorFn, completeFn)   // to hold the subscription for later unsubscribe

    // Example
    ngOnInit(): void {
      this._productService.getProducts()
        .subscribe(
          products => this.products = products,
          error => this.errorMessage = <any>error);
    }

# Navigation and Routing Basics

## How Routing Works

An Angular application is a Single Page Application (SPA).

* Configure a route for each component
* Define options/actions
* Tie a route to each option/action
* Activate the route based on user action
* Activating a route displays the component's view
* Angular uses HTML5-style routes by default that don't require the hash symbol
* Hash-style routing can be configured instead of HTML5-style routing

## Configuring Routes

Routing is component based.

An Angular application has one router, registered in the AppModule.

    ...
    import { RouterModule } from '@angular/router';

    @NgModule({
      imports: [
        BrowserModule,
        FormsModule,
        HttpModule,
        RouterModule.forRoot([])    // Configure routes here
      ],
      declarations: [
        ...
      ],
      bootstrap: [
        AppComponent
      ]
    })
    export class AppModule { }

Append the 'useHash' config option to specify hash-style routing.

    RouterModule.forRoot([], {useHash: true})

Specify route definitions with Route objects.

    [
      {path: 'products', component: ProductListComponent},
      {path: 'products/:id', component: ProductDetailComponent},
      {path: 'welcome', component: WelcomeComponent},
      {path: '', redirectTo: 'welcome, pathMatch: 'full'},
      {path: '**', component: PageNotFoundComponent}
    ]

Notes:

* No leading slashes
* Order of routes matters

## Tying Routes to Actions

Navigating the Application Routes

* Menu option, link, image or button that activates a route     // we need to handle this
* typing the URL in the address bar / bookmark                  // this just works
* The browser's forward or back buttons                         // this just works
* Add the `[routerLink]` directive to navigable links
  * `<a [routerLink]="['/welcome']">Home</a></li>`
  * `<a [routerLink]="['/products']">Product List</a></li>` 

## Placing the Views

When a route is activated, the corresponding component's view is displayed in the `<router-outlet></router-outlet>` directive.

# Navigation and Routing Additional Techniques

## Passing Parameters to a Route

* Configure the route with parameters
  * `{path: 'product/:id', component: ProductDetailComponent}`
* Configure the links with parameters
  * `<a [routerLink]="['/product', product.productId]">{{product.productName}}</a>`
* Add `ActivatedRoute` import to component
  * `import { ActivatedRoute } from '@angular/router';`
* Add `_route` to component constructor
  * `constructor(private _route: ActivatedRoute) {`
* Retrieve route params during construction
  * Use `snapshot` if you only need the initial value on construction
    * `console.log(this._route.snapshot.params['id']);`
  * Use observable approach if you need to subscribe to changes

## Activating a Route with Code

To route with code:

* Use the `Router` service from `@angular/router`.
* Add the Router service to the constructor
  * `constructor(private _router: Router) { }`
* Activate the route
  * `onBack(): void { this._router.navigate(['/products']); }`

## Protecting a Route with Guards

### Use guards to limit access to a route.

* CanActivate
  * Guard navigation to a route
* CanDeactivate
  * Guard navigation from a route
* Resolve
  * Pre-fetch data before activating a route
* CanLoad
  * Prevent asynchronous routing

### Building a Guard

    import { Injectable } from '@angular/core';
    import { CanActivate } from @angular/router;

    @Injectable()
    export class ProductDetailGuard implements CanActivate {
      canActivate(): boolean {    // you can return an observable or promise from here also
        ...
      }
    }

### Registering a Guard

Guards must be provided at the root Angular Module level.

    ...
    import { ProductDetailGuard } from './products/product-guard.service';

    @NgModule({
      imports: [...],
      declarations: [...],
      providers: [ ProductDetailGuard ],
      bootstrap: [ AppComponent ]
    })
    export class AppModule { }

### Using a Guard

Add the Guard to a route.

    RouterModule.forRoot([
      { path: 'products', component: ProductListComponent },
      { path: 'products/:id',
        canActivate: [ ProductDetailGuard ],
        component: ProductDetailComponent },
    ])

# Angular Modules

## What is an Angular Module

* A class with an NgModule decorator
* It's purpose:
  * Organize the pieces of our app
  * Arrange them into blocks
  * Extend our application with capabilities from external libraries
  * Provide a template resolution environment
  * Aggregate and re-export
* An Angular Module:
  * Declares all components, directives, and pipes within our application
  * Bootstraps the initial component of our app
  * Can export components, directives and pipes to other modules
  * Can import other modules, bringing in exported functionality from those other modules
  * Can register service providers with the Angular Injector
  * Defines the components, directives and pipes available to the components that belong to the module

## Angular Module Metadata

* All Angular applications have one root AppModule and one root AppComponent
* The root AppComponent is used for bootstrapping

### Bootstrap Array

* Every application must bootstrap at least one component, the root application component
* The bootstrap array should only be used in the root application module, AppModule

### Declarations Array

* Used to define components, directives and pipes that belong to the module
* Only declare components, directives and pipes
* Every component, directive and pipe we create must belong to one and only one Angular module
* Never re-declare declare components, directives and pipes that belong to another module
* All declared components, directives and pipes are private by default
  * They are only accessible to other components, directives and pipes declared in the same module
* The Angular module provides the template resolution environment for its component templates

### Exports Array

* Lets us share components, directives and pipes with other modules
* Lets us re-export other system libraries and modules
* Lets us re-export 3rd party modules
* Lets us re-export our own modules
* Export any components, directives and pipes needed by other components
* Re-export modules to re-export their components, directives and pipes
* We can re-export something without importing it first
* *Never* export a service

### Imports Array
* Lets us import supporting modules that export components, directives and pipes
* Importing a module makes available any exported components, directives and pipes from that module
* Only import what this module needs
* Imports *are not* inherited.
  * Importing a module *does not* provide access to the exports of its imported modules
  * Unless the modules re-exports its imported modules

### Providers Array
* Lets us register service providers at the module level
* Any service provider added to the providers array is registered at the root of the application
* Don't add services to the providers array of a shared module
  * This will cause multiple instances of the service
  * Consider building a CoreModule for services and import it once in the AppModule
* Routing Guards must be added to the providers array of an Angular module

## Creating a Feature Module

* Define a new feature module
* Add the appropriate components to the declarations array of the feature module
* Don't import BrowserModule if you need `*ngFor` and `*ngIf` in a feature module
  * Import the CommonModule instead
* Add related services as Providers
* Import the feature module into the root AppModule

## Defining a Shared Module

The purpose of a shared module is to organize a set of commonly used pieces into one module and export those pieces for use by any module that imports the shared module. This lets us aggregate our external components and external modules into a convenience module.

Note: we can export something without importing it first.

## Revisiting AppModule

Every application has a root Angular Module called, by convention, `AppModule`. Its purpose is to orchestrate the application as a whole.

To refactor the root application routes into their own module:

    // in app-routing.module.ts
    import { NgModule } from '@angular/core';
    import { RouterModule } from '@angular/router';

    import { WelcomeModule } from './home/welcome.component';

    @NgModule({
      imports: [
        RouterModule.forRoot([
          { path: 'welcome', component: WelcomeComponent },
          { path: '', redirectTo: 'welcome', pathMatch, 'full' },
          { path: '**', redirectTo: 'welcome', pathMatch, 'full' }
        ])
      ],
      exports: [
        RouterModule
      ]
    })
    export class AppRoutingModule { };

Something similar can be done for feature modules.

# Angular Setup Revisited

* TypeScript Configuration File
  * `tsconfig.json` specifies TypeScript compile options and settings
* TypeScript Definitions File
  * `.d.ts` files specify type definitions for 3rd party modules
  * `typings.json` specifies registry dependencies for typings
* npm Package File
  * `package.json` specifies properties about the application, scripts, dependencies and dev-dependencies
* SystemJS Configuration File
  * `systemjs.config.js` specifies SystemJS configuration settings
* index.html File Scripts

## Bootstrapping Process Revisited

Use either JIT (just in time) compiling or AOT (ahead of time) compiling.

    // in main.ts, with JIT compiling
    import { platformBrowserDynamic } from '@angular/platform-browser-dynamic';
    import { AppModule } from './app.module';
    platformBrowserDynamic().bootstrapModule(AppModule);

    // in main.ts, with AOT compiling
    import { platformBrowser } from '@angular/platform-browser';
    import { AppModuleNgFactory } from './app.module.ngfactory';
    platformBrowser().bootstrapModuleFactory(AppModuleFactory);

## Angular CLI

The Angular CLI is a command line interface for Angular.

`ng new Application` will create a working Angular application with all required starter files.

`ng g component component-name` will create a new component in the application.

Can also generate unit and e2e tests.

See the [AngularCLI](https://cli.angular.io) site for more information.