# Angular Interview Questions & Answers

This open-source guide covers foundational Angular interview questions with clear, concise answers. Great for beginners and as a revision tool before interviews.

---

## Table of Contents

1. [What is Angular and how is it different from AngularJS?](#1-what-is-angular-and-how-is-it-different-from-angularjs)
2. [What are components, and how do you create one?](#2-what-are-components-and-how-do-you-create-one)
3. [What is a module in Angular? What is `NgModule`?](#3-what-is-a-module-in-angular-what-is-ngmodule)
4. [What are services in Angular and how are they injected?](#4-what-are-services-in-angular-and-how-are-they-injected)
5. [What is the difference between `constructor()` and `ngOnInit()`?](#5-what-is-the-difference-between-constructor-and-ngoninit)
6. [What is two-way data binding and how do you use it?](#6-what-is-two-way-data-binding-and-how-do-you-use-it)
7. [Explain interpolation, property binding, and event binding.](#7-explain-interpolation-property-binding-and-event-binding)
8. [What is the role of `@Input()` and `@Output()`?](#8-what-is-the-role-of-input-and-output)
9. [How does Angular detect changes? What is `ChangeDetectionStrategy`?](#9-how-does-angular-detect-changes-what-is-changedetectionstrategy)
10. [How do Angular forms differ: Template-driven vs Reactive Forms?](#10-how-do-angular-forms-differ-template-driven-vs-reactive-forms)
11. [What is an observable, and how is it used with HttpClient?](#11-what-is-an-observable-and-how-is-it-used-with-httpclient)
12. [What is async pipe and how does it simplify observable usage?](#12-what-is-async-pipe-and-how-does-it-simplify-observable-usage)
13. [How does routing work in Angular? What is RouterModule?](#13-how-does-routing-work-in-angular-what-is-routermodule)
14. [What are guards in Angular (CanActivate, CanDeactivate)?](#14-what-are-guards-in-angular-canactivate-candeactivate)
15. [What are resolvers in routing?](#15-what-are-resolvers-in-routing)
16. [What is lazy loading and how do you implement it?](#16-what-is-lazy-loading-and-how-do-you-implement-it)
17. [What are pipes? How do you create a custom pipe?](#17-what-are-pipes-how-do-you-create-a-custom-pipe)
18. [What are directives? Difference between structural and attribute directives.](#18-what-are-directives-difference-between-structural-and-attribute-directives)
19. [What is a ViewChild / ContentChild? When to use each?](#19-what-is-a-viewchild--contentchild-when-to-use-each)
20. [How does Angular handle forms validation?](#20-how-does-angular-handle-forms-validation)
21. [Explain the role and lifecycle of Angular Interceptors.](#21-explain-the-role-and-lifecycle-of-angular-interceptors)
22. [How does Angular handle dependency injection under the hood?](#22-how-does-angular-handle-dependency-injection-under-the-hood)
23. [What is a module federation / micro frontend architecture in Angular?](#23-what-is-a-module-federation--micro-frontend-architecture-in-angular)
24. [How do you optimize performance in Angular apps?](#24-how-do-you-optimize-performance-in-angular-apps)
25. [What are pure and impure pipes? How do they affect performance?](#25-what-are-pure-and-impure-pipes-how-do-they-affect-performance)
26. [Explain `ngZone` and `zone.js` – how do they relate to change detection?](#26-explain-ngzone-and-zonejs--how-do-they-relate-to-change-detection)
27. [What is `Renderer2` and why would you use it instead of direct DOM manipulation?](#27-what-is-renderer2-and-why-would-you-use-it-instead-of-direct-dom-manipulation)
28. [How do you unit test components, services, and interceptors?](#28-how-do-you-unit-test-components-services-and-interceptors)
29. [What is a dynamic component and how do you load one at runtime?](#29-what-is-a-dynamic-component-and-how-do-you-load-one-at-runtime)
30. [Explain the Angular compilation process: AoT vs JIT.](#30-explain-the-angular-compilation-process-aot-vs-jit)
31. [How would you implement a global error handler?](#31-how-would-you-implement-a-global-error-handler)
32. [How would you build a role-based authentication system in Angular?](#32-how-would-you-build-a-role-based-authentication-system-in-angular)
33. [How do you protect certain routes based on user roles?](#33-how-do-you-protect-certain-routes-based-on-user-roles)
34. [How would you implement a retry mechanism for failed API calls?](#34-how-would-you-implement-a-retry-mechanism-for-failed-api-calls)
35. [How do you manage global state in Angular (e.g., using NgRx or a shared service)?](#35-how-do-you-manage-global-state-in-angular-eg-using-ngrx-or-a-shared-service)
36. [How would you share data between unrelated components in Angular?](#36-how-would-you-share-data-between-unrelated-components-in-angular)
37. [How do you handle file upload and preview in Angular?](#37-how-do-you-handle-file-upload-and-preview-in-angular)
38. [How would you integrate a third-party chart library or rich text editor in Angular?](#38-how-would-you-integrate-a-third-party-chart-library-or-rich-text-editor-n-angular)
39. [How do you handle environment-based configurations (dev/prod) in Angular?](#39-how-do-you-handle-environment-based-configurations-devprod-in-angular)
40. [How would you lazy load and preload Angular modules?](#40-how-would-you-lazy-load-and-preload-angular-modules)

---

## 1. What is Angular and how is it different from AngularJS?

**Angular** is a modern, TypeScript-based, front-end web application framework developed and maintained by **Google**. It is a complete rewrite of **AngularJS** (version 1.x), designed to build scalable and performant single-page applications (SPAs).

#### ✅ Key Features of Angular:

- **Component-based architecture**
- **TypeScript support**
- **Powerful CLI for scaffolding and automation**
- **RxJS for reactive programming**
- **Dependency Injection (DI) system**
- **Modular development with NgModules**
- **Built-in routing and lazy loading**
- **Ahead-of-Time (AOT) compilation**
- **Unit and integration testing support**

---

#### 🆚 Angular vs AngularJS: Key Differences

| Feature                  | AngularJS (1.x)              | Angular (2+)                                 |
| ------------------------ | ---------------------------- | -------------------------------------------- |
| **Language**             | JavaScript                   | TypeScript                                   |
| **Architecture**         | MVC (Model-View-Controller)  | Component-based                              |
| **Mobile Support**       | Limited                      | Designed for mobile apps                     |
| **Performance**          | Slower due to dirty checking | Faster with unidirectional data flow         |
| **Data Binding**         | Two-way by default           | Unidirectional by default + two-way opt-in   |
| **Dependency Injection** | Custom implementation        | Hierarchical DI using TypeScript decorators  |
| **DOM Manipulation**     | Direct DOM manipulation      | Abstracted via `Renderer2`                   |
| **Tooling**              | Manual setup                 | Angular CLI provides powerful tooling        |
| **Modularity**           | Less modular                 | Encourages modular development via NgModules |
| **Testing**              | Less structured              | Built-in testing tools and best practices    |

---

#### 🎯 Summary for Interviews:

- Angular is **not a new version** of AngularJS — it's a **complete rewrite**.
- Angular uses **TypeScript**, improving code quality and maintainability.
- Angular improves **performance, scalability**, and supports modern web standards.
- Angular supports **enterprise-level applications**, unlike AngularJS which was suited for smaller apps.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 2. What are components, and how do you create one?

In Angular, a **component** is the **fundamental building block** of the UI. Every Angular application is made up of components arranged in a tree-like structure, starting from the **root component** (`AppComponent`).

A component controls:

- A **template** (HTML for view rendering)
- A **class** (TypeScript for logic and data)
- **CSS/SCSS styles** (optional styling)

Each component is **encapsulated** and **reusable**, which supports modular and maintainable architecture.

---

#### ✅ Anatomy of a Component

```ts
import { Component } from "@angular/core";

@Component({
  selector: "app-hello",
  templateUrl: "./hello.component.html",
  styleUrls: ["./hello.component.css"],
})
export class HelloComponent {
  message = "Hello, Angular!";
}
```

| Part          | Description                                        |
| ------------- | -------------------------------------------------- |
| `selector`    | The custom HTML tag used to embed the component    |
| `templateUrl` | Points to the HTML file for the component          |
| `styleUrls`   | Links to the component's styles                    |
| `class`       | Contains logic, data, methods, and lifecycle hooks |

---

#### 🛠️ How to Create a Component

Use Angular CLI for easy scaffolding:

```bash
ng generate component my-component
# or shorthand
ng g c my-component
```

This creates:

```
src/app/my-component/
├── my-component.component.ts      // Component class
├── my-component.component.html    // Template
├── my-component.component.css     // Styles
└── my-component.component.spec.ts // Test file
```

---

#### 📌 How to Use a Component

Once created, you can use the component selector (`<app-my-component></app-my-component>`) inside any template, such as `app.component.html`.

---

#### 🎯 Summary for Interviews:

- A **component** in Angular is a **self-contained UI unit** made of template, class, and style.
- Components follow a **modular structure** and support **reuse and testing**.
- You create components using `@Component()` decorator.
- Angular CLI makes component generation fast and consistent.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 3. What is a module in Angular? What is `NgModule`?

In Angular, a **module** is a mechanism to group related parts of an application together — such as components, directives, pipes, and services — into **a cohesive block of functionality**.

Angular uses **NgModules** to define these blocks. Every Angular app has at least **one root module** called `AppModule`, and can have multiple **feature modules** for better modularity and lazy loading.

---

#### ✅ What is `@NgModule`?

`@NgModule` is a **decorator function** that takes a **metadata object** and tells Angular how to compile and launch the application.

```ts
import { NgModule } from "@angular/core";
import { BrowserModule } from "@angular/platform-browser";
import { AppComponent } from "./app.component";

@NgModule({
  declarations: [
    AppComponent, // Components, directives, pipes
  ],
  imports: [
    BrowserModule, // Other Angular modules
  ],
  providers: [], // Services or global providers
  bootstrap: [AppComponent], // Root component to bootstrap
})
export class AppModule {}
```

---

#### 🔑 Key Properties of `NgModule`:

| Property       | Purpose                                                                 |
| -------------- | ----------------------------------------------------------------------- |
| `declarations` | Declares components, directives, and pipes owned by the module          |
| `imports`      | Imports other Angular modules (e.g., `FormsModule`, `HttpClientModule`) |
| `providers`    | Registers services and injectables                                      |
| `bootstrap`    | Lists the root component (only in the root module)                      |
| `exports`      | Makes components/directives/pipes available to other modules            |

---

#### 📦 Why Use Modules?

- Encourages **separation of concerns**
- Enables **lazy loading** of features
- Makes the application **more scalable and maintainable**
- Supports **reusability** of shared modules across features

---

#### 🧱 Types of Angular Modules

1. **Root Module** – The main app module (`AppModule`)
2. **Feature Modules** – Domain-specific modules (e.g., `UserModule`)
3. **Shared Module** – Common components/pipes used across multiple modules
4. **Core Module** – Singleton services and global utilities

---

#### 🛠️ Creating a Module via CLI

```bash
ng generate module user
# or shorthand
ng g m user
```

This will generate a new file: `user.module.ts`.

---

#### 🎯 Summary for Interviews:

- An Angular **module** is a container for a cohesive block of functionality.
- The `@NgModule` decorator defines how the module behaves.
- Modules allow for **code organization**, **reuse**, **scalability**, and **lazy loading**.
- Every Angular app must have a **root module**, and can have multiple **feature/shared modules**.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 4. What are services in Angular and how are they injected?

In Angular, a **service** is a **reusable class** that contains business logic, data access methods, or shared functionality — **independent of any component**.

Services help:

- Keep components clean and focused on the UI
- Promote code reuse
- Enable separation of concerns
- Facilitate testing

Angular uses a **Dependency Injection (DI)** system to **inject services** where they are needed.

---

#### ✅ Creating a Service

Use the Angular CLI:

```bash
ng generate service user
# or shorthand
ng g s user
```

This generates:

```bash
src/app/user.service.ts
```

---

#### 🛠️ Example Service

```ts
// user.service.ts
import { Injectable } from "@angular/core";

@Injectable({
  providedIn: "root", // Makes the service available app-wide
})
export class UserService {
  getUsers() {
    return ["Alice", "Bob", "Charlie"];
  }
}
```

- The `@Injectable()` decorator tells Angular that this class can be injected as a dependency.
- `providedIn: 'root'` makes it a **singleton**, available throughout the app without needing to register it in a module manually.

---

#### 📥 Injecting a Service into a Component

```ts
import { Component, OnInit } from "@angular/core";
import { UserService } from "./user.service";

@Component({
  selector: "app-user-list",
  template: `<ul>
    <li *ngFor="let user of users">{{ user }}</li>
  </ul>`,
})
export class UserListComponent implements OnInit {
  users: string[] = [];

  constructor(private userService: UserService) {}

  ngOnInit() {
    this.users = this.userService.getUsers();
  }
}
```

---

#### 🔍 How Dependency Injection Works in Angular

- Angular maintains an **injector tree**.
- When a class requires a dependency (like a service), Angular looks for a **provider** of that dependency in the injector hierarchy.
- Services declared with `providedIn: 'root'` are registered in the **root injector**, making them **singletons** shared across the app.

---

#### 🧱 Alternative: Providing Services in a Module

If you don’t want to use `providedIn: 'root'`, you can register a service in a module manually:

```ts
@NgModule({
  providers: [UserService],
})
export class AppModule {}
```

---

#### 🎯 Summary for Interviews:

- A **service** in Angular is a class that holds shared logic (e.g., fetching data, utilities, state).
- Use the **`@Injectable()` decorator** to make it available for DI.
- Angular uses **Dependency Injection** to inject services into components, pipes, or other services.
- Services with `providedIn: 'root'` are **singletons** across the entire app.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 5. What is the difference between `constructor()` and `ngOnInit()`?

In Angular, both `constructor()` and `ngOnInit()` are used in component classes — but they serve **different purposes** in the component lifecycle.

Understanding their roles is key to writing maintainable and performant Angular code.

---

### 🏗️ `constructor()`

The `constructor()` is a **TypeScript feature** (not Angular-specific) that gets called when the class is instantiated. It’s mainly used to **inject dependencies** via Angular's **Dependency Injection (DI)** system.

```ts
constructor(private userService: UserService) {
  console.log('Constructor called');
}
```

> ✅ Use `constructor()` only for **dependency injection** or simple initializations that don't rely on Angular bindings.

---

### ⚙️ `ngOnInit()`

`ngOnInit()` is a **lifecycle hook** provided by Angular. It's called **after Angular has initialized all data-bound properties** of the component.

It is the ideal place to:

- Perform initialization logic
- Call APIs
- Access `@Input()` properties
- Set up observables or timers

```ts
ngOnInit() {
  console.log('ngOnInit called');
  this.users = this.userService.getUsers();
}
```

To use it, the class must implement the `OnInit` interface:

```ts
import { OnInit } from "@angular/core";

export class MyComponent implements OnInit {
  ngOnInit() {
    // logic here
  }
}
```

---

### 🔍 Comparison Table

| Feature                  | `constructor()`                          | `ngOnInit()`                                    |
| ------------------------ | ---------------------------------------- | ----------------------------------------------- |
| Type                     | TypeScript feature                       | Angular lifecycle hook                          |
| Called when?             | When the component class is instantiated | After input properties are set (component init) |
| Use for DI?              | ✅ Yes                                   | ❌ No                                           |
| Safe to access bindings? | ❌ No                                    | ✅ Yes                                          |
| Typical uses             | Dependency injection, minimal setup      | API calls, data initialization, logic execution |

---

### 🎯 Summary for Interviews:

- `constructor()` is used for **injecting dependencies** and basic setup.
- `ngOnInit()` is used for **initializing component logic**, fetching data, or interacting with `@Input()` values.
- Always prefer `ngOnInit()` for logic that depends on Angular bindings or services.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 6. What is two-way data binding and how do you use it?

**Two-way data binding** is a mechanism in Angular that allows automatic synchronization of data **between the component class and the view (HTML template)**.

When the user updates the input in the UI, the model updates in the component class, and vice versa — **instantly reflecting changes in both directions**.

---

### 🔁 How Two-Way Binding Works

Angular achieves two-way binding using a **combination of property binding and event binding**:

```html
<input [value]="name" (input)="name = $event.target.value" />
```

To simplify this, Angular provides the **banana-in-a-box syntax**:

```html
<input [(ngModel)]="name" />
```

---

### 🛠️ How to Use Two-Way Binding in Angular

1. Import `FormsModule` in your module:

```ts
import { FormsModule } from "@angular/forms";

@NgModule({
  imports: [FormsModule],
})
export class AppModule {}
```

2. Use `[(ngModel)]` in your component template:

```ts
<!-- app.component.html -->
<input [(ngModel)]="username" placeholder="Enter your name" />
<p>Hello, {{ username }}!</p>
```

3. Define the property in your component class:

```ts
// app.component.ts
export class AppComponent {
  username: string = "";
}
```

As the user types, `username` is updated in real-time, and any programmatic update to `username` is instantly reflected in the UI.

---

### ⚠️ When to Use Two-Way Binding

- Form inputs
- Filters and search bars
- Editable fields
- Real-time UI updates based on user input

---

### 🔍 Best Practices

- Use `[(ngModel)]` only for **form inputs or editable UI elements**.
- Avoid overusing two-way binding for large-scale data, which may hurt performance.
- Prefer **Reactive Forms** for complex, scalable form handling in large apps.

---

### 🎯 Summary for Interviews:

- Two-way data binding keeps the **component and view in sync** automatically.
- Achieved using `[(ngModel)]`, which is syntactic sugar for `[value]` and `(input)` binding.
- Requires importing `FormsModule`.
- Ideal for **simple forms and interactive UI elements**.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 7. Explain interpolation, property binding, and event binding.

In Angular, **data binding** is the mechanism to coordinate the data between your component class and the view. Angular supports several types of data binding depending on the direction of data flow.

This question is commonly asked to evaluate your understanding of Angular's **unidirectional and bidirectional data flow**.

---

### 🟡 Interpolation (`{{ ... }}`)

Interpolation is used to **display data from the component class into the HTML template**.

```html
<p>Welcome, {{ username }}!</p>
```

- `username` is a property in the component class.
- Angular replaces `{{ username }}` with the actual value.

✅ **One-way data binding**: Component → View
❌ Cannot be used for HTML element properties (like `disabled`, `src`, etc.)

---

### 🟡 Property Binding (`[property]`)

Property binding allows you to **bind DOM element properties** to values in the component.

```html
<img [src]="profileImage" /> <button [disabled]="isLoading">Submit</button>
```

- The value of `profileImage` is bound to the `src` attribute.
- The button is disabled when `isLoading` is `true`.

✅ Safe and dynamic
✅ Works with DOM and Angular component input properties

---

### 🟡 Event Binding (`(event)`)

Event binding is used to **handle events raised by DOM elements** (e.g., click, input, change) and trigger methods in your component class.

```html
<button (click)="submitForm()">Submit</button>
<input (input)="onNameChange($event)" />
```

- When the button is clicked, `submitForm()` is called.
- `(event)` captures events like `click`, `input`, `change`, etc.

✅ **One-way data binding**: View → Component
✅ Ideal for responding to user actions

---

### 🔄 Combine All for Two-Way Binding

Two-way data binding is a combination of property and event binding:

```html
<input [(ngModel)]="username" />
```

It’s equivalent to:

```html
<input [value]="username" (input)="username = $event.target.value" />
```

---

### 🔍 Comparison Table

| Type             | Syntax                | Data Flow        | Use Case                           |
| ---------------- | --------------------- | ---------------- | ---------------------------------- |
| Interpolation    | `{{ value }}`         | Component → View | Displaying strings or variables    |
| Property Binding | `[prop]="value"`      | Component → View | DOM or custom component properties |
| Event Binding    | `(event)="handler()"` | View → Component | Handling user interactions         |

---

### 🎯 Summary for Interviews:

- **Interpolation**: Binds string values into the template.
- **Property binding**: Dynamically updates DOM element or component properties.
- **Event binding**: Listens for user actions and handles them in the component.
- Together, they form the basis for powerful UI interactions in Angular.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 8. What is the role of `@Input()` and `@Output()`?

In Angular, `@Input()` and `@Output()` are **decorators** that enable **communication between parent and child components**.

They are essential tools for **component interaction** in a modular architecture.

---

### 🔁 When Are They Used?

- Use `@Input()` when the **parent needs to pass data to a child**.
- Use `@Output()` when the **child needs to emit an event to the parent**.

This maintains a **unidirectional data flow**, which is a best practice in Angular.

---

### 🟡 `@Input()` – Passing Data from Parent to Child

Used to bind a property in the **child component** that gets its value from the **parent**.

```ts
// child.component.ts
import { Component, Input } from "@angular/core";

@Component({
  selector: "app-child",
  template: `<p>Welcome, {{ name }}!</p>`,
})
export class ChildComponent {
  @Input() name: string = "";
}
```

```html
<!-- parent.component.html -->
<app-child [name]="'Alice'"></app-child>
```

---

### 🟡 `@Output()` – Sending Data from Child to Parent

Used with an `EventEmitter` to notify the **parent component** when something happens in the **child**.

```ts
// child.component.ts
import { Component, Output, EventEmitter } from "@angular/core";

@Component({
  selector: "app-child",
  template: `<button (click)="notify()">Notify Parent</button>`,
})
export class ChildComponent {
  @Output() clicked = new EventEmitter<string>();

  notify() {
    this.clicked.emit("Button clicked!");
  }
}
```

```html
<!-- parent.component.html -->
<app-child (clicked)="handleChildClick($event)"></app-child>
```

```ts
// parent.component.ts
handleChildClick(message: string) {
  console.log('Child says:', message);
}
```

---

### 🔍 Summary Table

| Decorator   | Direction      | Type             | Purpose                             |
| ----------- | -------------- | ---------------- | ----------------------------------- |
| `@Input()`  | Parent → Child | Property binding | Receive data into a child component |
| `@Output()` | Child → Parent | EventEmitter     | Emit events/data to a parent        |

---

### 🎯 Summary for Interviews:

- `@Input()` is used to **accept values** from a parent component.
- `@Output()` is used to **emit custom events** from child to parent using `EventEmitter`.
- They help in **modular and maintainable component design**.
- Promote **unidirectional data flow**, which simplifies debugging and improves performance.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 9. How does Angular detect changes? What is `ChangeDetectionStrategy`?

Angular uses a powerful **change detection mechanism** to keep the UI in sync with the application state. This mechanism runs automatically and ensures that the DOM updates when component data changes.

---

### 🔁 How Angular Detects Changes

Angular uses **Zone.js** to hook into browser events like clicks, input, timeouts, and HTTP responses. When such events occur, Angular triggers the **Change Detection** cycle to update the view.

**Default Process:**

1. Angular runs the component tree from the root.
2. It checks each component’s template for updated values.
3. If any value has changed, Angular updates the DOM accordingly.

This happens:

- On user events (e.g., input, click)
- After API responses
- Inside `setTimeout()`, `setInterval()`, or Promises

---

### 🧠 What is `ChangeDetectionStrategy`?

Angular provides the `ChangeDetectionStrategy` enum to control **how and when a component should be checked for changes**.

It can be set on a component like this:

```ts
import { Component, ChangeDetectionStrategy } from "@angular/core";

@Component({
  selector: "app-profile",
  templateUrl: "./profile.component.html",
  changeDetection: ChangeDetectionStrategy.OnPush,
})
export class ProfileComponent {
  @Input() user!: User;
}
```

---

### 🟡 Types of Change Detection Strategies

| Strategy  | Description                                                                                                         |
| --------- | ------------------------------------------------------------------------------------------------------------------- |
| `Default` | Angular checks the **entire component tree** every time a change is triggered                                       |
| `OnPush`  | Angular checks the component **only when its `@Input()` reference changes** or an event occurs within the component |

---

### ✅ When to Use `OnPush`

- Your component uses **immutable objects** or observables.
- You want to **optimize performance** by skipping unnecessary checks.
- You are working with **large component trees** or **high-frequency data updates**.

---

### 🔍 Example of `OnPush` Optimization

```ts
@Component({
  selector: "app-optimized",
  template: `{{ user.name }}`,
  changeDetection: ChangeDetectionStrategy.OnPush,
})
export class OptimizedComponent {
  @Input() user!: { name: string };
}
```

If `user` is mutated directly, the view **won't update**:

```ts
this.user.name = "New Name"; // ❌ won't trigger change detection
```

Instead, you must **assign a new object**:

```ts
this.user = { ...this.user, name: "New Name" }; // ✅ triggers change detection
```

---

### 🎯 Summary for Interviews:

- Angular uses **Zone.js** and its own **change detection mechanism** to update the view automatically.
- `ChangeDetectionStrategy` helps control how often Angular checks a component for changes.
- `Default`: checks all components (safe but can be inefficient).
- `OnPush`: checks only when `@Input()` references change or an internal event occurs (highly efficient for performance).

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 10. How do Angular forms differ: Template-driven vs Reactive Forms?

Angular provides two ways to handle user input through forms:

- **Template-driven Forms** – suitable for simple, declarative forms
- **Reactive Forms** – suitable for complex, dynamic, and scalable forms

Both approaches are built on the same `FormControl`, `FormGroup`, and `FormArray` classes but differ in how they are implemented.

---

### 🟢 Template-driven Forms

- Defined **in the HTML template**
- Uses Angular directives like `[(ngModel)]`, `#form="ngForm"`
- Two-way data binding (`[(ngModel)]`)
- Minimal TypeScript code
- Easier to use for simple forms

#### Example:

```html
<form #userForm="ngForm" (ngSubmit)="onSubmit(userForm.value)">
  <input name="username" [(ngModel)]="user.username" required />
  <button type="submit">Submit</button>
</form>
```

#### Setup:

Import `FormsModule` in your module.

```ts
@NgModule({
  imports: [FormsModule]
})
```

---

### 🔵 Reactive Forms

- Defined **programmatically in the component class**
- Uses `FormControl`, `FormGroup`, `FormBuilder`
- Provides **more control** over validation and form state
- Supports **dynamic forms**, nested groups, and custom validation
- Better suited for **large-scale enterprise apps**

#### Example:

```ts
form = new FormGroup({
  username: new FormControl('', Validators.required)
});

onSubmit() {
  console.log(this.form.value);
}
```

```html
<form [formGroup]="form" (ngSubmit)="onSubmit()">
  <input formControlName="username" />
  <button type="submit">Submit</button>
</form>
```

#### Setup:

Import `ReactiveFormsModule` in your module.

```ts
@NgModule({
  imports: [ReactiveFormsModule]
})
```

---

### 🔍 Comparison Table

| Feature         | Template-driven             | Reactive Forms                   |
| --------------- | --------------------------- | -------------------------------- |
| Form setup      | In HTML template            | In TypeScript component class    |
| Data flow       | Two-way binding (`ngModel`) | Explicit via `FormControl`       |
| Best suited for | Simple forms                | Complex and dynamic forms        |
| Validation      | HTML + Angular directives   | Fully programmatic, customizable |
| Testability     | Harder to test              | Easy to test                     |
| Dynamic forms   | Difficult                   | Easy and flexible                |
| Scalability     | Limited                     | High                             |

---

### 🎯 Summary for Interviews:

- **Template-driven forms** are simple, declarative, and great for small forms.
- **Reactive forms** offer more flexibility, better structure, and are ideal for complex or enterprise-level forms.
- Choose based on your use case: **simplicity vs control**.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 11. What is an observable, and how is it used with HttpClient?

In Angular, an **observable** is a key part of **reactive programming** using the **RxJS library**. Observables are used to **handle asynchronous data streams**, such as HTTP requests, user input, or real-time updates.

The **`HttpClient` service** in Angular returns data as observables, making it powerful and flexible for handling API calls.

---

### 🔁 What is an Observable?

An **Observable** is a stream of data that can be observed over time. It supports:

- Asynchronous data flows
- Operators (e.g., `map`, `filter`, `retry`)
- Subscriptions and unsubscriptions
- Emission of multiple values over time

> Think of it like a **promise**, but with **multiple values** and **cancellation support**.

---

### 📡 Using Observables with `HttpClient`

1. Import `HttpClientModule` in your root or feature module:

```ts
import { HttpClientModule } from "@angular/common/http";

@NgModule({
  imports: [HttpClientModule],
})
export class AppModule {}
```

2. Inject `HttpClient` into a service or component:

```ts
import { HttpClient } from "@angular/common/http";
import { Observable } from "rxjs";

@Injectable({ providedIn: "root" })
export class UserService {
  constructor(private http: HttpClient) {}

  getUsers(): Observable<User[]> {
    return this.http.get<User[]>("https://api.example.com/users");
  }
}
```

3. Subscribe to the observable:

```ts
export class UserComponent implements OnInit {
  users: User[] = [];

  constructor(private userService: UserService) {}

  ngOnInit() {
    this.userService.getUsers().subscribe({
      next: (data) => (this.users = data),
      error: (err) => console.error("Error fetching users:", err),
    });
  }
}
```

---

### 📌 Benefits of Using Observables with HttpClient

| Feature        | Benefit                                     |
| -------------- | ------------------------------------------- |
| Stream-based   | Can handle multiple events/data emissions   |
| Cancelable     | Unsubscribe to avoid memory leaks           |
| Composable     | Use RxJS operators to transform/filter data |
| Async handling | Easily integrate with UI lifecycle hooks    |

---

### ⚠️ Important Notes

- Always **unsubscribe** from observables when the component is destroyed (if not using `async` pipe).
- Consider using **`catchError`**, `retry`, and `finalize` for better error handling and user experience.

---

### 🎯 Summary for Interviews:

- Observables are a core part of Angular’s reactive programming model.
- `HttpClient` uses observables to return data from HTTP calls.
- Observables are powerful, composable, and cancelable — making them ideal for **API integration**, **real-time updates**, and **asynchronous workflows** in Angular.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 12. What is async pipe and how does it simplify observable usage?

The `async` pipe in Angular is a **built-in pipe** that automatically **subscribes to an observable or a promise**, gets its latest value, and returns it in the template.

It also **automatically unsubscribes** when the component is destroyed, preventing memory leaks.

---

### ✅ Why Use `async` Pipe?

Manually subscribing to observables in a component can lead to:

- Repetitive boilerplate
- Risk of memory leaks if not unsubscribed
- Messy lifecycle code

The `async` pipe solves these issues **declaratively** in the template.

---

### 🧪 Example Without `async` Pipe (Manual Subscription)

```ts
// user.component.ts
ngOnInit() {
  this.userService.getUsers().subscribe(users => {
    this.users = users;
  });
}
```

```html
<!-- user.component.html -->
<ul>
  <li *ngFor="let user of users">{{ user.name }}</li>
</ul>
```

---

### ✅ Example With `async` Pipe (Preferred)

```ts
// user.component.ts
users$ = this.userService.getUsers(); // Observable
```

```html
<!-- user.component.html -->
<ul>
  <li *ngFor="let user of users$ | async">{{ user.name }}</li>
</ul>
```

- No need to subscribe manually.
- Angular manages the subscription and unsubscription lifecycle.
- Cleaner, more readable code.

---

### 🔁 How It Works

The `async` pipe:

1. Subscribes to the observable or promise.
2. Emits the latest value to the view.
3. Unsubscribes automatically when the component is destroyed.

Works with:

- `Observable<T>`
- `Promise<T>`

---

### 📌 When to Use `async` Pipe

- In templates for displaying data from observables (e.g., HTTP data, user input, route params).
- With `*ngIf`, `*ngFor`, or simple bindings.
- In combination with `| slice`, `| date`, etc.

---

### 🔍 Best Practices

- Prefer using `async` pipe **directly in the template** to reduce code complexity.
- Avoid mixing `async` pipe with manual subscriptions on the same observable.
- For performance, consider `ChangeDetectionStrategy.OnPush` with `async`.

---

### 🎯 Summary for Interviews:

- The `async` pipe automatically **subscribes to and unsubscribes from observables/promises**.
- Simplifies code and avoids manual memory management.
- Promotes cleaner, more declarative Angular templates.
- Great for handling **asynchronous data in templates**.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 13. How does routing work in Angular? What is `RouterModule`?

In Angular, **routing** enables **navigation between different views or pages** in a Single Page Application (SPA) without reloading the page. Angular’s router maps **URL paths to components**, handles navigation, and supports route guards, lazy loading, and parameter passing.

The `RouterModule` is the **core module** Angular provides to configure and manage routing.

---

### 🧭 How Angular Routing Works

1. You define routes as an array of objects.
2. Each route maps a **URL path** to a **component**.
3. Angular uses the `<router-outlet>` directive to render the component associated with the current route.

---

### 🛠️ Basic Routing Setup

#### 1. Import `RouterModule` in `AppModule`

```ts
import { NgModule } from "@angular/core";
import { RouterModule, Routes } from "@angular/router";
import { HomeComponent } from "./home/home.component";
import { AboutComponent } from "./about/about.component";

const routes: Routes = [
  { path: "", component: HomeComponent },
  { path: "about", component: AboutComponent },
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule],
})
export class AppRoutingModule {}
```

#### 2. Use `<router-outlet>` in your AppComponent template

```html
<!-- app.component.html -->
<router-outlet></router-outlet>
```

#### 3. Navigate using `routerLink`

```html
<a routerLink="/">Home</a> <a routerLink="/about">About</a>
```

---

### 📦 What is `RouterModule`?

`RouterModule` is an Angular module that:

- Provides router directives like `<router-outlet>`, `routerLink`, and `routerLinkActive`
- Registers the route configuration (`RouterModule.forRoot(routes)`)
- Enables navigation and guards

> ✅ It’s the backbone of Angular’s routing system.

---

### 🧩 Advanced Features Supported by Router

| Feature               | Description                                         |
| --------------------- | --------------------------------------------------- |
| Route Parameters      | Pass dynamic values via URLs (`/user/:id`)          |
| Route Guards          | Protect routes using `CanActivate`, `CanDeactivate` |
| Lazy Loading          | Load feature modules only when needed               |
| Child Routes          | Nested routing inside components                    |
| Redirects & Wildcards | Handle default and unknown routes                   |
| Route Resolvers       | Pre-fetch data before loading a component           |

---

### 🔍 Example with Route Parameter

```ts
{ path: 'user/:id', component: UserComponent }
```

```ts
// In component
this.route.snapshot.paramMap.get("id");
```

---

### 🎯 Summary for Interviews:

- Angular routing enables navigation within SPAs using URL-based mapping to components.
- `RouterModule` provides the infrastructure for routing and navigation.
- Routing is configured using `RouterModule.forRoot(routes)` for the root module or `forChild()` for feature modules.
- Features like **guards**, **resolvers**, and **lazy loading** help build complex, performant applications.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 14. What are guards in Angular (CanActivate, CanDeactivate)?

In Angular, **route guards** are interfaces that allow you to **control access to routes**. They act like gatekeepers that decide whether a user can enter or leave a route.

Guards are commonly used for:

- **Authentication** and **authorization**
- **Unsaved changes warnings**
- **Role-based access control**
- **Preloading/preventing navigation based on business logic**

---

### 🛡️ Types of Guards

| Guard              | Purpose                                          |
| ------------------ | ------------------------------------------------ |
| `CanActivate`      | Checks if a route **can be activated** (entered) |
| `CanDeactivate`    | Checks if a route **can be deactivated** (left)  |
| `CanActivateChild` | Checks access to **child routes**                |
| `CanLoad`          | Prevents loading of **lazy-loaded modules**      |
| `Resolve`          | Pre-fetches data before route activation         |

This section focuses on the two most commonly used:

---

### 🔐 `CanActivate` – Protect Route Entry

Used to **prevent access** to a route unless certain conditions are met (e.g., the user is logged in).

#### ✅ Example

```ts
@Injectable({ providedIn: "root" })
export class AuthGuard implements CanActivate {
  constructor(
    private authService: AuthService,
    private router: Router
  ) {}

  canActivate(): boolean {
    if (this.authService.isLoggedIn()) {
      return true;
    } else {
      this.router.navigate(["/login"]);
      return false;
    }
  }
}
```

```ts
// app-routing.module.ts
{
  path: 'dashboard',
  component: DashboardComponent,
  canActivate: [AuthGuard]
}
```

---

### 🔄 `CanDeactivate` – Prevent Route Exit

Used to **warn or block users** from leaving a route if certain conditions are not met (e.g., unsaved form data).

#### ✅ Example

```ts
export interface CanComponentDeactivate {
  canDeactivate: () => boolean | Observable<boolean>;
}

@Injectable({ providedIn: "root" })
export class UnsavedChangesGuard
  implements CanDeactivate<CanComponentDeactivate>
{
  canDeactivate(component: CanComponentDeactivate): boolean {
    return component.canDeactivate ? component.canDeactivate() : true;
  }
}
```

```ts
// component.ts
export class FormComponent implements CanComponentDeactivate {
  hasUnsavedChanges = true;

  canDeactivate(): boolean {
    return (
      !this.hasUnsavedChanges ||
      confirm("You have unsaved changes. Leave anyway?")
    );
  }
}
```

```ts
// app-routing.module.ts
{
  path: 'form',
  component: FormComponent,
  canDeactivate: [UnsavedChangesGuard]
}
```

---

### 🧠 How Guards Work

- Guards return:
  - `true` or `false`
  - A `UrlTree` (to redirect)
  - An `Observable<boolean | UrlTree>`
  - A `Promise<boolean | UrlTree>`

> Angular **waits** for the guard to resolve before activating/deactivating the route.

---

### 🎯 Summary for Interviews:

- **Guards** in Angular allow you to **intercept route navigation**.
- `CanActivate`: checks **before entering** a route.
- `CanDeactivate`: checks **before leaving** a route.
- Useful for authentication, preventing data loss, role-based access, etc.
- Guards improve **app security**, **user experience**, and **navigation control**.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 15. What are resolvers in routing?

In Angular, a **resolver** is a service that implements the `Resolve<T>` interface and is used to **fetch data before a route is activated**.

Resolvers are useful when:

- You want a route’s component to load **only after required data is ready**
- You want to **avoid loading spinners** inside components
- You want to **fetch data in advance** so the component template can render immediately

---

### 🧠 How Does a Resolver Work?

When you assign a resolver to a route:

1. Angular runs the resolver **before** activating the route.
2. The route is **paused** until the resolver finishes.
3. The resolved data is injected into the component via the **`ActivatedRoute`**.

---

### ✅ Step-by-Step Example

#### 1. Create a Resolver Service

```ts
import { Injectable } from "@angular/core";
import { Resolve } from "@angular/router";
import { Observable } from "rxjs";
import { UserService } from "./user.service";
import { User } from "./user.model";

@Injectable({ providedIn: "root" })
export class UserResolver implements Resolve<User[]> {
  constructor(private userService: UserService) {}

  resolve(): Observable<User[]> {
    return this.userService.getUsers(); // API call
  }
}
```

#### 2. Add Resolver to Route

```ts
// app-routing.module.ts
{
  path: 'users',
  component: UserListComponent,
  resolve: { usersData: UserResolver }
}
```

#### 3. Access Resolved Data in Component

```ts
import { ActivatedRoute } from "@angular/router";

export class UserListComponent implements OnInit {
  users: User[] = [];

  constructor(private route: ActivatedRoute) {}

  ngOnInit() {
    this.users = this.route.snapshot.data["usersData"];
  }
}
```

---

### 🧪 Resolver Return Types

Resolvers can return:

- **Observable<T>**
- **Promise<T>**
- **Synchronous value** (`T`)

If the resolver fails, the route **won’t activate**, and you can handle it using error pages or redirects.

---

### 📦 Benefits of Using Resolvers

| Benefit                    | Description                                           |
| -------------------------- | ----------------------------------------------------- |
| Pre-fetch data             | Load data before component loads                      |
| Cleaner components         | No need to handle loading states inside the component |
| Centralized error handling | Easier to manage fetch failures with route redirects  |
| Seamless user experience   | Avoids flickering or "empty screen" states            |

---

### 🎯 Summary for Interviews:

- A **resolver** fetches data **before the route activates**.
- Implement the `Resolve<T>` interface and use the `resolve()` method.
- Attach the resolver in route config under the `resolve` property.
- Access resolved data using `ActivatedRoute.snapshot.data`.
- Ideal for **preloading data**, **cleaner UX**, and **maintainable components**.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 16. What is lazy loading and how do you implement it?

**Lazy loading** in Angular is a design pattern that **loads feature modules only when needed**, rather than at the initial load of the application.

This helps improve:

- **Initial load performance**
- **Scalability** of large applications
- **Separation of concerns** between app features

---

### 🚀 Why Use Lazy Loading?

By default, Angular **eagerly loads** all modules when the app starts. In large applications, this increases:

- Initial bundle size
- Time to interactive (TTI)
- Unused resources being loaded

With **lazy loading**, you load only what’s required for the current route.

---

### 📦 How to Implement Lazy Loading

#### 🛠️ 1. Create a Feature Module

```bash
ng generate module admin --route admin --module app.module
```

This command sets up lazy loading automatically (since Angular v9+ with Ivy).

If doing manually:

```bash
ng generate module admin
ng generate component admin/dashboard
```

#### 🗺️ 2. Define Routes in the Feature Module

```ts
// admin-routing.module.ts
const routes: Routes = [{ path: "", component: DashboardComponent }];

@NgModule({
  imports: [RouterModule.forChild(routes)],
  exports: [RouterModule],
})
export class AdminRoutingModule {}
```

#### 🧩 3. Register Lazy Route in App Routing

```ts
// app-routing.module.ts
const routes: Routes = [
  {
    path: "admin",
    loadChildren: () =>
      import("./admin/admin.module").then((m) => m.AdminModule),
  },
];
```

- The module and its components are **only loaded when the route `/admin` is visited**.

---

### 🧠 Key Notes

- Lazy loading works with `loadChildren` and **dynamic imports**.
- Use **`forChild()`** for feature routing (vs `forRoot()` for root module).
- Ensure that the feature module exports its components & routing.
- Guards and resolvers work the same in lazy-loaded routes.

---

### ✅ Eager vs Lazy Loading Comparison

| Feature          | Eager Loading               | Lazy Loading                               |
| ---------------- | --------------------------- | ------------------------------------------ |
| Load time        | Entire app loads at startup | Loads only required modules on demand      |
| Performance      | Slower initial load         | Faster startup, slower on first route load |
| Setup complexity | Easy (default)              | Requires modular setup                     |
| Use case         | Small apps                  | Large apps with multiple features          |

---

### 🎯 Summary for Interviews:

- **Lazy loading** loads feature modules **on-demand**, improving performance.
- Implemented using `loadChildren` with dynamic import in the routing module.
- Reduces initial bundle size and speeds up page load.
- Best used in large-scale applications with multiple routes and features.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 17. What are pipes? How do you create a custom pipe?

In Angular, **pipes** are used to **transform data directly in the template**. Pipes take in a value, process it, and return a transformed value without modifying the original data.

They are commonly used for:

- Formatting strings, numbers, and dates
- Filtering and transforming arrays
- Creating custom display logic directly in the HTML

---

### 🛠️ Built-in Pipes Examples

Angular includes several **built-in pipes**:

| Pipe        | Usage Example | Output              |                           |
| ----------- | ------------- | ------------------- | ------------------------- |
| `date`      | \`{{ today    | date:'short' }}\`   | e.g., `6/18/25, 11:30 PM` |
| `uppercase` | \`{{ name     | uppercase }}\`      | `JOHN DOE`                |
| `currency`  | \`{{ price    | currency:'INR' }}\` | `₹1,000.00`               |
| `json`      | \`{{ object   | json }}\`           | Pretty JSON string        |
| `slice`     | \`{{ list     | slice:0:3 }}\`      | First 3 items of the list |

---

### ✅ Creating a Custom Pipe

You can create a custom pipe using the `@Pipe()` decorator and implementing the `PipeTransform` interface.

#### 🧪 Example: `capitalize` Pipe

```ts
import { Pipe, PipeTransform } from "@angular/core";

@Pipe({
  name: "capitalize",
})
export class CapitalizePipe implements PipeTransform {
  transform(value: string): string {
    if (!value) return "";
    return value.charAt(0).toUpperCase() + value.slice(1).toLowerCase();
  }
}
```

#### 🧩 Using the Custom Pipe in HTML

```html
<p>{{ 'angular' | capitalize }}</p>
<!-- Output: Angular -->
```

#### 🧾 Register Pipe in a Module

```ts
@NgModule({
  declarations: [CapitalizePipe],
  exports: [CapitalizePipe],
})
export class SharedModule {}
```

---

### 🧠 Key Points About Pipes

- Pipes are **pure by default**, meaning they're only re-evaluated when the input changes.
- You can make a pipe **impure** by setting `pure: false` in the decorator, but this has performance costs.
- Pipes are **declarative**, making templates cleaner and logic reusable.

---

### 📦 When to Use Pipes

| Use Case             | Example                               |
| -------------------- | ------------------------------------- |
| Display formatting   | Dates, currency, uppercase/lowercase  |
| List transformation  | Slicing/filtering arrays in templates |
| Custom display logic | Converting roles, statuses, units     |

---

### 🎯 Summary for Interviews:

- **Pipes** transform data in templates without changing the original value.
- Angular provides **built-in pipes**, and you can create **custom pipes** using `@Pipe` and `PipeTransform`.
- Pipes improve **template readability** and **reuse formatting logic**.
- Use pipes for **formatting**, **filtering**, and **custom display transformations**.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 18. What are directives? Difference between structural and attribute directives.

In Angular, a **directive** is a class with a `@Directive()` decorator that allows you to **attach behavior to elements in the DOM**.

Directives are one of Angular’s core building blocks and are used to:

- **Manipulate the DOM**
- **Change appearance, behavior, or layout**
- **Extend HTML with custom logic**

---

### 🛠️ Types of Directives in Angular

Angular has **three types** of directives:

| Type                     | Purpose                                      | Example              |
| ------------------------ | -------------------------------------------- | -------------------- |
| **Component**            | A directive with a template                  | `@Component({...})`  |
| **Structural Directive** | Adds/removes elements from the DOM           | `*ngIf`, `*ngFor`    |
| **Attribute Directive**  | Changes appearance or behavior of an element | `ngClass`, `ngStyle` |

---

### 🧱 Structural Directives

Structural directives are used to **change the layout of the DOM** by adding, removing, or replacing elements.

> Identified with an asterisk `*` syntax.

#### Examples:

```html
<!-- *ngIf: conditionally adds element -->
<div *ngIf="isLoggedIn">Welcome!</div>

<!-- *ngFor: loops over a list -->
<li *ngFor="let user of users">{{ user.name }}</li>
```

#### Custom Structural Directive (Example):

```ts
@Directive({
  selector: "[appIfNot]",
})
export class IfNotDirective {
  constructor(
    private tpl: TemplateRef<any>,
    private viewContainer: ViewContainerRef
  ) {}

  @Input() set appIfNot(condition: boolean) {
    if (!condition) {
      this.viewContainer.createEmbeddedView(this.tpl);
    } else {
      this.viewContainer.clear();
    }
  }
}
```

---

### 🎨 Attribute Directives

Attribute directives are used to **change the appearance or behavior** of an existing element/component.

> They work by **modifying element attributes**, styles, or classes.

#### Examples:

```html
<!-- ngStyle: sets inline styles -->
<div [ngStyle]="{color: 'blue'}">Styled Text</div>

<!-- ngClass: toggles CSS classes -->
<p [ngClass]="{ active: isActive }">Highlight me</p>
```

#### Custom Attribute Directive (Example):

```ts
@Directive({
  selector: "[appHighlight]",
})
export class HighlightDirective {
  constructor(private el: ElementRef) {
    el.nativeElement.style.backgroundColor = "yellow";
  }
}
```

```html
<p appHighlight>This text is highlighted</p>
```

---

### 📌 Comparison Table

| Feature             | Structural Directive            | Attribute Directive                   |
| ------------------- | ------------------------------- | ------------------------------------- |
| Affects DOM layout? | Yes (adds/removes DOM elements) | No (modifies existing elements only)  |
| Common usage        | `*ngIf`, `*ngFor`, `*ngSwitch`  | `ngClass`, `ngStyle`, custom behavior |
| Syntax indicator    | Uses `*` prefix                 | Uses property binding or plain attr   |
| Purpose             | Template control                | Styling or behavior control           |

---

### 🎯 Summary for Interviews:

- Angular **directives** add behavior to DOM elements.
- **Structural directives** (e.g., `*ngIf`, `*ngFor`) change the DOM structure.
- **Attribute directives** (e.g., `ngClass`, `ngStyle`) change the DOM appearance or behavior.
- You can create **custom directives** to encapsulate reusable logic or styles.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 19. What is a `ViewChild` / `ContentChild`? When to use each?

Angular provides decorators like `@ViewChild()` and `@ContentChild()` to **access DOM elements, directives, or components** from the class.

They are used to get a **reference to a child element**, component, or directive in the **template or projected content**, allowing interaction directly from the component class.

---

### 🔍 What is `@ViewChild`?

`@ViewChild()` is used to **access an element, directive, or child component** that is **declared in the same template** as the component.

#### ✅ Example: Accessing a DOM Element

```html
<!-- app.component.html -->
<input #inputBox type="text" />
```

```ts
@ViewChild('inputBox') inputRef!: ElementRef;

ngAfterViewInit() {
  this.inputRef.nativeElement.focus();
}
```

#### ✅ Example: Accessing a Child Component

```html
<app-child #childRef></app-child>
```

```ts
@ViewChild('childRef') child!: ChildComponent;

ngAfterViewInit() {
  this.child.doSomething();
}
```

---

### 🔍 What is `@ContentChild`?

`@ContentChild()` is used to access content that is **projected into a component using `<ng-content>`**.

#### ✅ Example:

```ts
// parent.component.html
<app-wrapper>
  <p #projectedContent>Hello from parent</p>
</app-wrapper>
```

```html
<!-- wrapper.component.html -->
<ng-content></ng-content>
```

```ts
@ContentChild('projectedContent') content!: ElementRef;

ngAfterContentInit() {
  console.log(this.content.nativeElement.textContent);
}
```

---

### 🧠 When to Use Each

| Decorator         | Used For                                       | Lifecycle Hook         |
| ----------------- | ---------------------------------------------- | ---------------------- |
| `@ViewChild()`    | Accessing elements/components in own template  | `ngAfterViewInit()`    |
| `@ContentChild()` | Accessing content projected via `<ng-content>` | `ngAfterContentInit()` |

---

### 📌 Additional Tips

- Use `static: true` if you need access before `ngAfterViewInit()`.
  Example: `@ViewChild('el', { static: true })`

- You can also use:
  - `@ViewChildren()` to get a list of multiple elements in the view
  - `@ContentChildren()` to get multiple projected content items

---

### 🎯 Summary for Interviews:

- `@ViewChild()` is used for accessing elements or components **declared in the template**.
- `@ContentChild()` is used for accessing **projected content** inside `<ng-content>`.
- Choose based on where the child lives: inside the template → `ViewChild`; projected via `ng-content` → `ContentChild`.
- Use inside `ngAfterViewInit()` or `ngAfterContentInit()` lifecycle hooks.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 20. How does Angular handle forms validation?

Angular provides a **powerful and flexible validation system** for both **template-driven** and **reactive forms**, allowing developers to ensure form input correctness using built-in, custom, and asynchronous validators.

---

### 🧾 Validation Types in Angular

| Type             | Works In            | Description                                              |
| ---------------- | ------------------- | -------------------------------------------------------- |
| **Built-in**     | Template + Reactive | Predefined validators like `required`, `minLength`, etc. |
| **Custom**       | Template + Reactive | User-defined validation logic                            |
| **Asynchronous** | Reactive            | Validates data with server/API responses                 |

---

### ✅ Built-in Validators

#### 🧪 Template-driven Example

```html
<form #form="ngForm">
  <input name="email" ngModel required email />
  <div *ngIf="form.controls.email?.errors?.required">Email is required</div>
</form>
```

#### 🧪 Reactive Example

```ts
form = new FormGroup({
  email: new FormControl("", [Validators.required, Validators.email]),
});
```

```html
<input formControlName="email" />
<div *ngIf="form.get('email')?.errors?.email">Invalid email address</div>
```

---

### 🧑‍💻 Creating a Custom Validator

#### ✅ Sync Validator (e.g., no special characters)

```ts
function noSpecialChars(control: AbstractControl): ValidationErrors | null {
  const valid = /^[A-Za-z0-9]*$/.test(control.value);
  return valid ? null : { specialChars: true };
}
```

```ts
form = new FormGroup({
  username: new FormControl("", [noSpecialChars]),
});
```

---

### 🌐 Async Validator Example

Useful for things like **checking username availability**:

```ts
function usernameAvailable(http: HttpClient): AsyncValidatorFn {
  return (control: AbstractControl): Observable<ValidationErrors | null> => {
    return http
      .get(`/api/check-username/${control.value}`)
      .pipe(map((res) => (res["available"] ? null : { usernameTaken: true })));
  };
}
```

---

### 🔍 Accessing Validation State

| Property                | Meaning                      |
| ----------------------- | ---------------------------- |
| `valid` / `invalid`     | Overall field validity       |
| `touched` / `untouched` | Has the user interacted?     |
| `dirty` / `pristine`    | Has the field been modified? |
| `errors`                | List of validation errors    |

```ts
form.get("email")?.errors;
form.get("email")?.valid;
```

---

### 📦 Error Display Best Practices

```html
<div *ngIf="form.get('email')?.touched && form.get('email')?.invalid">
  <small *ngIf="form.get('email')?.errors?.required">Email is required</small>
  <small *ngIf="form.get('email')?.errors?.email">Invalid email</small>
</div>
```

---

### ✅ Validation Summary: Template vs Reactive

| Feature                 | Template-driven           | Reactive Forms               |
| ----------------------- | ------------------------- | ---------------------------- |
| Validators setup        | HTML with directives      | TypeScript with `Validators` |
| Validation state access | Via form references       | Via form control objects     |
| Custom validators       | Supported (less flexible) | Fully supported and flexible |

---

### 🎯 Summary for Interviews:

- Angular supports **built-in, custom, and async validators** in both form types.
- **Template-driven** forms use HTML-based validation directives.
- **Reactive forms** use class-based control objects and offer better scalability and testability.
- Use `errors`, `valid`, `dirty`, and `touched` properties to manage validation UX.
- Custom and async validators allow integration with complex logic and APIs.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 21. Explain the role and lifecycle of Angular Interceptors

In Angular, **interceptors** are part of the **HTTPClient module** and allow you to intercept and modify **outgoing HTTP requests** and **incoming HTTP responses** globally across the app.

They are ideal for implementing cross-cutting concerns like:

- Authentication (e.g., adding auth tokens)
- Logging
- Error handling
- Request transformation
- Caching

---

### 🧠 What is an Interceptor?

An **interceptor** is a service class that implements the `HttpInterceptor` interface. It provides an `intercept()` method that intercepts every HTTP request made using `HttpClient`.

```ts
intercept(
  req: HttpRequest<any>,
  next: HttpHandler
): Observable<HttpEvent<any>>
```

---

### ✅ Interceptor Example: Add Auth Token

```ts
@Injectable()
export class AuthInterceptor implements HttpInterceptor {
  intercept(
    req: HttpRequest<any>,
    next: HttpHandler
  ): Observable<HttpEvent<any>> {
    const token = localStorage.getItem("auth_token");
    const authReq = req.clone({
      setHeaders: { Authorization: `Bearer ${token}` },
    });
    return next.handle(authReq);
  }
}
```

---

### 🧾 Registering an Interceptor

You must register the interceptor using the `HTTP_INTERCEPTORS` token with `multi: true`.

```ts
@NgModule({
  providers: [
    {
      provide: HTTP_INTERCEPTORS,
      useClass: AuthInterceptor,
      multi: true,
    },
  ],
})
export class AppModule {}
```

✅ You can register **multiple interceptors**, and Angular will chain them in the order they are provided.

---

### 🔁 Interceptor Lifecycle

1. Request is initiated via `HttpClient`
2. Request passes through all registered interceptors
3. Each interceptor can:
   - **Modify** the request (e.g., add headers)
   - **Cancel** the request
   - **Forward** it to the next handler

4. The HTTP response passes **back through the interceptors** in reverse order
5. Each interceptor can:
   - **Modify** the response
   - **Handle errors** (e.g., retry logic, redirection)

---

### 🧪 Common Use Cases

| Use Case               | What You Do in Interceptor                  |
| ---------------------- | ------------------------------------------- |
| Add auth token         | Modify request headers                      |
| Show/hide loader       | Trigger loader on request start/stop        |
| Central error handling | Catch errors and handle 401s, 500s globally |
| Modify responses       | Parse or sanitize response data             |
| Retry failed requests  | Use RxJS `retry()` or `catchError()`        |

---

### 🎯 Summary for Interviews

- Angular **interceptors** intercept all HTTP requests/responses made via `HttpClient`.
- Implemented using `HttpInterceptor` interface and registered with `HTTP_INTERCEPTORS`.
- Perfect for **auth, logging, transformation, and error handling**.
- Requests pass through interceptors in **forward order**, responses in **reverse**.
- Use `req.clone()` to avoid mutating original requests (immutability principle).

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 22. How does Angular handle dependency injection under the hood?

Angular uses a **Hierarchical Dependency Injection (DI) system** to efficiently manage how services and other dependencies are created, shared, and injected across the app.

Dependency Injection in Angular:

- Promotes **loose coupling** between components and services
- Enables **testability**, **reusability**, and **separation of concerns**

---

### 🧠 What is Dependency Injection (DI)?

Dependency Injection is a **design pattern** where an object (like a component) receives its dependencies (like services) from an external source **rather than creating them internally**.

Instead of:

```ts
this.authService = new AuthService();
```

Angular does:

```ts
constructor(private authService: AuthService) {}
```

---

### 🔧 How Angular DI Works Internally

Angular uses **injectors** to manage and resolve dependencies:

#### 1. **Providers** Register Dependencies

Services are registered using:

- `@Injectable({ providedIn: 'root' })`
- `providers: [ServiceName]` in components/modules

#### 2. **Injector Tree** is Created

Angular builds a **tree of injectors** at runtime:

- **Root Injector**: created by Angular when app starts
- **Child Injectors**: created per component/module if local providers are defined

#### 3. **Dependency Resolution**

When Angular needs to inject a service:

1. It checks the current injector
2. If not found, it moves up the hierarchy (component → module → root)
3. If not found anywhere, it throws an error

---

### 🧱 Types of Providers

| Type          | Description                             |
| ------------- | --------------------------------------- |
| **Root**      | Singleton service shared across the app |
| **Module**    | Available only within that module       |
| **Component** | New instance for each component         |

---

### 🔍 Example

```ts
@Injectable({ providedIn: "root" })
export class AuthService {}

@Component({
  selector: "app-login",
  templateUrl: "./login.component.html",
})
export class LoginComponent {
  constructor(private authService: AuthService) {}
}
```

- `AuthService` is registered in the root injector
- Angular injects the singleton instance into `LoginComponent`

---

### ⚙️ DI Resolution in Lifecycle

- **During app bootstrap**, Angular parses constructors looking for dependencies
- The `Injector` class resolves and caches instances for reuse
- Services are instantiated **only once** per injector scope

---

### 🧪 Advanced: `@Inject()`, `@Optional()`, `@Self()`, `@SkipSelf()`

Angular gives fine-grained control over injection:

| Decorator     | Purpose                               |
| ------------- | ------------------------------------- |
| `@Inject()`   | Inject by token instead of type       |
| `@Optional()` | Inject if available, else pass `null` |
| `@Self()`     | Look only in current injector         |
| `@SkipSelf()` | Skip current injector, look in parent |

---

### 🎯 Summary for Interviews:

- Angular uses a **hierarchical injector system** to manage dependency lifecycles.
- Dependencies are resolved **via constructor injection** at runtime.
- Providers can be registered at **root, module, or component level**.
- Angular checks the **injector hierarchy** to resolve dependencies.
- You can fine-tune DI behavior using decorators like `@Inject`, `@Optional`, `@Self`, etc.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 23. What is a module federation / micro frontend architecture in Angular?

**Micro frontend architecture** is an architectural pattern where a frontend application is **split into smaller, independently developed and deployed apps** (called micro frontends), similar to microservices on the backend.

**Module Federation**, introduced in **Webpack 5**, is the key enabler that allows Angular apps to implement micro frontends efficiently.

---

### 🧠 What Is Micro Frontend Architecture?

Micro frontends let teams:

- Build separate features/apps in **isolation**
- Use **independent deployments**
- Maintain **autonomous codebases**
- Integrate them into a **shell or host app** dynamically at runtime

> "Each team owns a part of the UI, end-to-end."

---

### 🧩 What Is Module Federation?

**Module Federation** is a Webpack 5 feature that enables:

- Sharing code across multiple applications **at runtime**
- Loading **remote components/modules** on demand
- Reducing duplication between micro frontends (shared libraries)

---

### 🔗 Host vs Remote Applications

| Role       | Responsibility                            |
| ---------- | ----------------------------------------- |
| **Host**   | The main container app that loads others  |
| **Remote** | Feature module/app exposed to be consumed |

---

### ✅ Use Case Example

- `host-app` → Main shell
- `user-app` → Remote exposed app for user management
- `admin-app` → Remote exposed admin panel

---

### 🛠️ Setting Up Module Federation in Angular

1. **Use Angular CLI with Webpack 5**
   - Angular v13+ supports custom builders like [@angular-architects/module-federation](https://www.npmjs.com/package/@angular-architects/module-federation)

2. **Install the Plugin**

```bash
ng add @angular-architects/module-federation --project host-app
```

3. **Expose Remote Module**

```js
// user-app/webpack.config.js
exposes: {
  './UserModule': './src/app/user/user.module.ts'
}
```

4. **Consume in Host App**

```ts
// app.routes.ts in host-app
{
  path: 'user',
  loadChildren: () =>
    loadRemoteModule({
      type: 'module',
      remoteEntry: 'http://localhost:4201/remoteEntry.js',
      exposedModule: './UserModule'
    }).then(m => m.UserModule)
}
```

---

### 📦 Benefits of Micro Frontends + Module Federation

| Benefit                 | Description                                  |
| ----------------------- | -------------------------------------------- |
| Independent deployments | Teams deploy features without waiting        |
| Code isolation          | Each app has its own repo, routing, services |
| Shared libraries        | Share Angular, RxJS, etc., to reduce bundle  |
| Team autonomy           | Ideal for large-scale enterprise apps        |

---

### ⚠️ Challenges to Consider

| Challenge               | Strategy                                                   |
| ----------------------- | ---------------------------------------------------------- |
| Version conflicts       | Align Angular versions or use shared mappings              |
| Complex builds          | Use `ModuleFederationPlugin` carefully                     |
| Shared state management | Use shared services or micro frontend-specific state tools |

---

### 🎯 Summary for Interviews:

- Micro frontends split a monolithic frontend into **independent apps**.
- **Module Federation** enables runtime sharing of Angular modules across apps.
- In Angular, this is commonly implemented using **Webpack 5 + module federation plugin**.
- Great for **large teams**, **independent deployments**, and **scalable architecture**.
- Requires **careful planning** of routing, versioning, and shared libraries.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 24. How do you optimize performance in Angular apps?

Performance optimization in Angular apps involves several strategies across **build optimization**, **change detection**, **network efficiency**, and **UX responsiveness**.

Well-optimized Angular applications are:

- Fast to load (low initial bundle)
- Smooth to use (minimal re-renders)
- Efficient (low memory & CPU usage)

---

### 🚀 Key Angular Performance Optimization Techniques

---

#### ✅ 1. **Use Lazy Loading for Modules**

Load feature modules only when needed.

```ts
{
  path: 'admin',
  loadChildren: () => import('./admin/admin.module').then(m => m.AdminModule)
}
```

📈 Benefit: Smaller initial bundle size.

---

#### ✅ 2. **Enable Ahead-of-Time (AOT) Compilation**

AOT compiles Angular templates **at build time**, not in the browser.

```bash
ng build --prod
```

📈 Benefit: Faster rendering, smaller bundles, early error detection.

---

#### ✅ 3. **Use OnPush Change Detection Strategy**

```ts
@Component({
  changeDetection: ChangeDetectionStrategy.OnPush
})
```

This tells Angular to **re-render only when input changes**, instead of running on every event.

📈 Benefit: Reduces unnecessary checks and DOM updates.

---

#### ✅ 4. **Avoid Memory Leaks (Unsubscribe)**

Always unsubscribe from observables or use `async` pipe.

```ts
ngOnDestroy() {
  this.subscription.unsubscribe();
}
```

Or better:

```html
<div *ngIf="data$ | async as data">{{ data }}</div>
```

📈 Benefit: Prevents memory leaks and long GC pauses.

---

#### ✅ 5. **Use TrackBy in ngFor Loops**

```html
<li *ngFor="let item of items; trackBy: trackById"></li>
```

```ts
trackById(index: number, item: Item) {
  return item.id;
}
```

📈 Benefit: Prevents re-rendering unchanged DOM elements.

---

#### ✅ 6. **Use Pure Pipes Over Impure Pipes**

Pure pipes recalculate only when input changes.

```ts
@Pipe({ name: 'customPipe', pure: true })
```

📈 Benefit: Better performance with large lists or data-bound UIs.

---

#### ✅ 7. **Minimize DOM and Change Detection Work**

- Avoid deeply nested structures
- Avoid placing heavy logic inside templates
- Use `ngZone.runOutsideAngular()` to skip change detection when needed

---

#### ✅ 8. **Bundle Optimization**

- Enable **build optimizations** and **tree-shaking** in `angular.json`
- Use **source-map-explorer** to audit bundle sizes
- Remove unused polyfills and 3rd-party libraries

---

#### ✅ 9. **Defer Non-Critical Scripts**

Load scripts or images only when needed using:

- `loading="lazy"` for images
- Dynamic `import()` for heavy modules

---

#### ✅ 10. **Use Web Workers for Heavy Computations**

Offload CPU-heavy tasks like data processing to a separate thread.

```bash
ng generate web-worker my-worker
```

---

### 🧠 Pro Performance Tips

| Optimization                   | When to Use                               |
| ------------------------------ | ----------------------------------------- |
| `OnPush` strategy              | For smart/dumb component separation       |
| `trackBy` in `*ngFor`          | Large lists or real-time updates          |
| `async` pipe                   | Reactive, auto-unsubscribing data streams |
| PreloadingStrategy for modules | Load lazy modules in background           |
| Service workers & PWA          | For offline capability and faster load    |

---

### 🎯 Summary for Interviews:

- Angular performance is optimized via **lazy loading**, **AOT**, **OnPush**, **trackBy**, and **tree-shaking**.
- Use **async pipes**, **pure pipes**, and **web workers** to reduce CPU/memory overhead.
- Performance bottlenecks can be avoided by limiting change detection and memory leaks.
- Tools like `source-map-explorer`, `Lighthouse`, and `RxJS` best practices help analyze and improve performance.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 25. What are pure and impure pipes? How do they affect performance?

In Angular, **pipes** are used to transform data in templates. These pipes can be either **pure** or **impure**, which determines **when and how often** the pipe’s `transform()` method is called.

The distinction between the two directly affects **performance**, especially in large or dynamic UIs.

---

### 🔍 What is a Pure Pipe?

A **pure pipe** is a pipe that Angular executes **only when it detects a pure change** in the input data.

✅ By default, all Angular pipes are **pure** unless explicitly marked otherwise.

#### Pure changes include:

- Primitives (`string`, `number`, `boolean`) that are changed
- Object or array **references** changing (not just internal mutation)

```ts
@Pipe({ name: "capitalize" }) // default is pure: true
export class CapitalizePipe implements PipeTransform {
  transform(value: string): string {
    return value.charAt(0).toUpperCase() + value.slice(1);
  }
}
```

📈 **Performance Benefit:**

- Called only when input reference changes
- Efficient for use in large lists or frequent change detection cycles

---

### 🔍 What is an Impure Pipe?

An **impure pipe** is one that Angular calls **on every change detection cycle**, regardless of whether its inputs have changed.

```ts
@Pipe({ name: "filterList", pure: false })
export class FilterListPipe implements PipeTransform {
  transform(items: any[], search: string): any[] {
    return items.filter((item) => item.name.includes(search));
  }
}
```

📉 **Performance Concern:**

- Called very frequently — can lead to **laggy UIs** if the logic is expensive
- Should be used **only when necessary**, e.g., for real-time filtering

---

### 📦 Pure vs Impure Pipe Comparison

| Feature           | Pure Pipe                            | Impure Pipe                                         |
| ----------------- | ------------------------------------ | --------------------------------------------------- |
| `@Pipe({ pure })` | `true` (default)                     | `false`                                             |
| Called When       | Input reference changes              | Every change detection cycle                        |
| Use Case          | Simple transforms (e.g., formatting) | Complex transforms with internal mutations          |
| Performance       | High performance                     | Lower performance (if misused)                      |
| Example           | `uppercase`, `date`, `currency`      | `filter`, `sort`, or custom pipes with mutable data |

---

### 🧠 Best Practices

- Use **pure pipes** whenever possible for **better performance**
- Avoid **impure pipes** in large lists or high-frequency updates
- For filtering/sorting, consider:
  - Doing the operation in the component
  - Caching results to avoid recomputation

---

### 🎯 Summary for Interviews:

- Angular pipes are **pure by default**, meaning they only recalculate when inputs change by reference.
- **Impure pipes** are called on every change detection cycle, which can **negatively affect performance**.
- Use impure pipes **only when necessary**, and avoid them in performance-critical scenarios.
- Understanding pure vs impure pipes is essential for building **high-performance Angular apps**.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 26. Explain `ngZone` and `zone.js` – how do they relate to change detection?

Angular’s powerful **change detection system** relies on **`NgZone`** and **`zone.js`** to automatically track **asynchronous operations** and update the UI when needed.

These tools allow Angular to know _when to run change detection_, without the developer manually triggering it in most cases.

---

### 🔄 What is `zone.js`?

- `zone.js` is a **third-party library** used by Angular to **patch async APIs** (like `setTimeout`, `fetch`, `Promise`, etc.).
- It creates an **execution context (zone)** around your code, tracking all asynchronous tasks.

> Think of it as a "watchdog" that notifies Angular every time an async task completes.

---

### 🔧 What is `NgZone`?

`NgZone` is an Angular wrapper around `zone.js` that:

- Detects **when a task completes**
- Triggers **Angular's change detection** to update the DOM

It provides APIs like:

```ts
ngZone.run(() => { ... });          // run code inside Angular zone (triggers change detection)
ngZone.runOutsideAngular(() => { ... });  // run code outside Angular zone (skips change detection)
```

---

### 🧠 How Change Detection Works with `zone.js`

1. User triggers an action (e.g., button click)
2. Async task starts (e.g., `setTimeout`, HTTP call)
3. `zone.js` tracks the task via patched APIs
4. When the task completes, Angular is notified
5. `NgZone` runs **change detection** to check for any data changes
6. The DOM updates automatically

---

### 🧪 Example: Without `NgZone`

```ts
setTimeout(() => {
  this.counter++; // UI might not update
}, 1000);
```

Angular may not know when to update. You’d need to trigger it manually.

---

### ✅ Example: Using `NgZone.run()`

```ts
constructor(private ngZone: NgZone) {}

someAsyncTask() {
  setTimeout(() => {
    this.ngZone.run(() => {
      this.counter++; // UI updates automatically
    });
  }, 1000);
}
```

---

### ⚡ Optimization: `runOutsideAngular()`

If you want to **skip change detection** (e.g., for performance-heavy background tasks):

```ts
this.ngZone.runOutsideAngular(() => {
  // expensive or repeated tasks here (like animations or polling)
  setTimeout(() => {
    this.ngZone.run(() => {
      this.counter++; // only re-enter Angular when necessary
    });
  }, 2000);
});
```

---

### 📦 Summary Table

| Feature            | `zone.js`                        | `NgZone`                                   |
| ------------------ | -------------------------------- | ------------------------------------------ |
| Provided by        | Third-party library              | Angular framework                          |
| Role               | Tracks async tasks globally      | Controls Angular’s change detection zone   |
| Main API usage     | Behind the scenes                | `run()`, `runOutsideAngular()`             |
| Performance impact | Adds automatic tracking overhead | Can be optimized via `runOutsideAngular()` |

---

### 🎯 Summary for Interviews:

- Angular uses **`zone.js`** to automatically detect when async operations complete.
- **`NgZone`** is Angular’s abstraction to **trigger or skip** change detection.
- `NgZone.run()` ensures changes are detected and UI updates.
- `NgZone.runOutsideAngular()` is used for performance optimization by avoiding unnecessary change detection.
- Understanding `NgZone` is key for handling performance-critical operations and custom asynchronous flows.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 27. What is `Renderer2` and why would you use it instead of direct DOM manipulation?

`Renderer2` is a **platform-independent API** provided by Angular to safely perform **DOM manipulations** like creating elements, adding/removing classes, setting styles, or listening to events — **without directly accessing the browser's native DOM APIs.**

This abstraction helps Angular apps remain **compatible across platforms** (like browsers, servers, or web workers), and ensures **security, testability, and consistency**.

---

### 🧱 Why Not Use `document` or `element.nativeElement` Directly?

Direct DOM access like:

```ts
document.querySelector("#myElement").style.color = "red";
```

- **Breaks Angular’s platform independence**
- **May not work in server-side rendering (SSR)**
- **Introduces security risks like XSS**
- **Is hard to test and mock**

Angular encourages using `Renderer2` to avoid such issues.

---

### 🔧 What is `Renderer2`?

`Renderer2` is an Angular service injected into components or directives that lets you **safely interact with the DOM**.

```ts
constructor(private renderer: Renderer2) {}
```

---

### ✅ Example: Using Renderer2

```ts
@ViewChild('box') boxRef!: ElementRef;

constructor(private renderer: Renderer2) {}

ngAfterViewInit() {
  this.renderer.setStyle(this.boxRef.nativeElement, 'color', 'blue');
  this.renderer.addClass(this.boxRef.nativeElement, 'highlighted');
}
```

```html
<div #box>Hello Renderer</div>
```

---

### 📚 Common `Renderer2` Methods

| Method                         | Description                     |
| ------------------------------ | ------------------------------- |
| `createElement()`              | Create a new DOM element        |
| `createText()`                 | Create a text node              |
| `appendChild()`                | Append child to parent          |
| `setAttribute()`               | Set an attribute on an element  |
| `removeAttribute()`            | Remove attribute                |
| `addClass()` / `removeClass()` | Add/remove CSS class            |
| `setStyle()` / `removeStyle()` | Modify inline styles            |
| `listen()`                     | Attach event listeners          |
| `setProperty()`                | Set a property on a DOM element |

---

### 🚀 When Should You Use Renderer2?

| Use Case                            | Why Use Renderer2                        |
| ----------------------------------- | ---------------------------------------- |
| DOM manipulation in Angular         | Keeps SSR support and testability        |
| Building custom directives          | Safely apply behavior to host elements   |
| Writing UI libraries                | Ensures abstraction from native APIs     |
| Supporting web workers or platforms | Avoids reliance on browser-specific APIs |

---

### 🧠 Advanced Tip

You can use `Renderer2.listen()` to attach event listeners in a **platform-safe** way:

```ts
this.renderer.listen(this.boxRef.nativeElement, "click", () => {
  alert("Box clicked!");
});
```

---

### 🎯 Summary for Interviews:

- `Renderer2` is Angular’s **safe abstraction** over direct DOM manipulation.
- It’s used for modifying elements without breaking platform compatibility.
- Avoids issues with **SSR, testing, and cross-platform rendering**.
- Commonly used in **directives, dynamic components, or UI libraries**.
- Use `ElementRef` cautiously — always prefer `Renderer2` for DOM actions.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 28. How do you unit test components, services, and interceptors?

Angular provides a powerful testing ecosystem built on **Jasmine** (testing framework) and **Karma** (test runner). Unit testing ensures that each part of your application (components, services, interceptors) behaves as expected in isolation.

---

## ✅ Testing Strategy Overview

| Type        | Purpose                                       |
| ----------- | --------------------------------------------- |
| Component   | Test UI logic, DOM updates, bindings          |
| Service     | Test business logic, API calls, data handling |
| Interceptor | Test request/response modification            |

---

## 🧩 1. Unit Testing Angular Components

### 🔧 Setup

```ts
import { ComponentFixture, TestBed } from "@angular/core/testing";
import { MyComponent } from "./my.component";

describe("MyComponent", () => {
  let component: MyComponent;
  let fixture: ComponentFixture<MyComponent>;

  beforeEach(() => {
    TestBed.configureTestingModule({
      declarations: [MyComponent],
    });

    fixture = TestBed.createComponent(MyComponent);
    component = fixture.componentInstance;
    fixture.detectChanges(); // triggers ngOnInit and DOM rendering
  });

  it("should create the component", () => {
    expect(component).toBeTruthy();
  });

  it("should render title in h1", () => {
    component.title = "Hello Test";
    fixture.detectChanges();
    const compiled = fixture.nativeElement;
    expect(compiled.querySelector("h1").textContent).toContain("Hello Test");
  });
});
```

---

## 🔧 2. Unit Testing Angular Services

### Example: Testing a Service with HttpClient

```ts
import { TestBed } from "@angular/core/testing";
import { MyService } from "./my.service";
import {
  HttpClientTestingModule,
  HttpTestingController,
} from "@angular/common/http/testing";

describe("MyService", () => {
  let service: MyService;
  let httpMock: HttpTestingController;

  beforeEach(() => {
    TestBed.configureTestingModule({
      imports: [HttpClientTestingModule],
      providers: [MyService],
    });

    service = TestBed.inject(MyService);
    httpMock = TestBed.inject(HttpTestingController);
  });

  it("should fetch data from API", () => {
    const mockResponse = [{ id: 1, name: "Test" }];

    service.getData().subscribe((data) => {
      expect(data.length).toBe(1);
      expect(data[0].name).toBe("Test");
    });

    const req = httpMock.expectOne("/api/data");
    expect(req.request.method).toBe("GET");
    req.flush(mockResponse);
  });

  afterEach(() => {
    httpMock.verify();
  });
});
```

---

## 🛡️ 3. Unit Testing HTTP Interceptors

### Interceptor Example:

```ts
@Injectable()
export class AuthInterceptor implements HttpInterceptor {
  intercept(
    req: HttpRequest<any>,
    next: HttpHandler
  ): Observable<HttpEvent<any>> {
    const token = "fake-token";
    const cloned = req.clone({
      setHeaders: { Authorization: `Bearer ${token}` },
    });
    return next.handle(cloned);
  }
}
```

### Interceptor Test:

```ts
import { TestBed } from "@angular/core/testing";
import { HTTP_INTERCEPTORS, HttpClient } from "@angular/common/http";
import {
  HttpClientTestingModule,
  HttpTestingController,
} from "@angular/common/http/testing";
import { AuthInterceptor } from "./auth.interceptor";

describe("AuthInterceptor", () => {
  let http: HttpClient;
  let httpMock: HttpTestingController;

  beforeEach(() => {
    TestBed.configureTestingModule({
      imports: [HttpClientTestingModule],
      providers: [
        { provide: HTTP_INTERCEPTORS, useClass: AuthInterceptor, multi: true },
      ],
    });

    http = TestBed.inject(HttpClient);
    httpMock = TestBed.inject(HttpTestingController);
  });

  it("should add Authorization header", () => {
    http.get("/test").subscribe();

    const req = httpMock.expectOne("/test");
    expect(req.request.headers.has("Authorization")).toBeTrue();
    expect(req.request.headers.get("Authorization")).toBe("Bearer fake-token");
  });

  afterEach(() => {
    httpMock.verify();
  });
});
```

---

## 🧪 Tips for Writing Angular Unit Tests

| Best Practice                          | Why It Helps                          |
| -------------------------------------- | ------------------------------------- |
| Use `TestBed.configureTestingModule()` | Sets up the test environment          |
| Use `HttpTestingController`            | Mock and test HTTP requests cleanly   |
| Keep tests isolated                    | Avoid testing multiple things at once |
| Use spies (`jasmine.createSpy()`)      | Mock dependencies easily              |
| Call `fixture.detectChanges()`         | Sync the component and its template   |
| Verify after each HTTP test            | Ensures no pending requests remain    |

---

## ✅ Summary for Interviews

- Angular uses **TestBed** for setting up test environments.
- **Component tests** check DOM rendering, interaction, and input/output behavior.
- **Services are tested** using mocks or `HttpTestingController` for API calls.
- **Interceptors are tested** by injecting them with `HTTP_INTERCEPTORS` and inspecting request headers or bodies.
- Follow **AAA Pattern**: Arrange, Act, Assert for clean and structured tests.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 29. What is a dynamic component and how do you load one at runtime?

### ✅ Definition

A **dynamic component** in Angular is a component that is **not declared in the template statically**. Instead, it is **created and inserted into the DOM at runtime**, typically based on user actions, configuration, or data.

This is useful when:

- You want to display different components dynamically based on logic.
- You’re building modals, notifications, plugin systems, dashboards, or CMS-like UIs.

---

## 🧠 When to Use Dynamic Components

- Showing different component types in a placeholder area.
- Rendering modals or dialogs dynamically.
- Embedding components from user-generated content.
- Plugin-based architectures.

---

## 🔧 Step-by-Step: Loading a Component Dynamically

### 1. **Create the Component to Load**

```ts
// hello.component.ts
@Component({
  selector: "app-hello",
  template: `<p>Hello, I am dynamically loaded!</p>`,
})
export class HelloComponent {}
```

---

### 2. **Prepare the Container (Host)**

Use `@ViewChild()` and `ViewContainerRef` to act as a placeholder.

```ts
// dynamic-host.component.ts
@Component({
  selector: "app-dynamic-host",
  template: `<ng-template #dynamicContainer></ng-template>`,
})
export class DynamicHostComponent {
  @ViewChild("dynamicContainer", { read: ViewContainerRef, static: true })
  container!: ViewContainerRef;

  constructor(private resolver: ComponentFactoryResolver) {}

  loadComponent() {
    const factory = this.resolver.resolveComponentFactory(HelloComponent);
    this.container.clear(); // optional: clears previous views
    this.container.createComponent(factory);
  }
}
```

> ⚠️ In Angular 14+, you can skip `ComponentFactoryResolver` and use `ViewContainerRef.createComponent()` directly.

---

### ✅ Angular 14+ Modern Way (without ComponentFactoryResolver)

```ts
loadComponent() {
  this.container.clear();
  this.container.createComponent(HelloComponent);
}
```

---

## 🧪 Dynamic Component with Inputs

If the component accepts `@Input()` values:

```ts
const componentRef = this.container.createComponent(HelloComponent);
componentRef.instance.title = "Dynamic title passed!";
```

---

## 🧹 Cleanup & Lifecycle

- If components are created frequently, call `.destroy()` or `.clear()` to avoid memory leaks.
- Dynamic components also go through the full Angular lifecycle (`ngOnInit`, etc.).

---

## ✅ Summary for Interviews

| Key Point                 | Description                                    |
| ------------------------- | ---------------------------------------------- |
| **Dynamic Component**     | Loaded at runtime, not declared in template    |
| **Uses**                  | Modals, dashboards, plugin systems, CMS        |
| **Tooling**               | `ViewContainerRef`, `ComponentFactoryResolver` |
| **Modern Angular (v14+)** | Uses `createComponent()` directly              |
| **Pass Inputs**           | Via `componentRef.instance`                    |
| **Memory Management**     | Use `.clear()` or `.destroy()`                 |

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 30. Explain the Angular Compilation Process: AoT vs JIT

In Angular, templates written in HTML are **compiled into JavaScript** so the browser can understand and execute them. This compilation can happen in **two ways**:

- **AoT (Ahead-of-Time) Compilation**
- **JIT (Just-in-Time) Compilation**

---

### 🚀 What is Compilation in Angular?

Angular templates are not plain HTML — they contain Angular syntax like `*ngIf`, `{{ data }}`, `@Input()`, etc. The **Angular Compiler (ngc)** converts this template syntax + TypeScript code into efficient JavaScript at compile time.

---

## 🧠 What is JIT (Just-in-Time) Compilation?

JIT compiles Angular components **in the browser at runtime**.

### ✅ Characteristics:

- Compilation happens when the app is launched.
- Used in **development mode** by default.
- Faster build time, but **slower app start time**.
- Includes full metadata and compiler in the bundle.

### 📦 Example:

```ts
platformBrowserDynamic().bootstrapModule(AppModule);
```

---

## ⚙️ What is AoT (Ahead-of-Time) Compilation?

AoT compiles Angular templates **at build time**, before the app is run in the browser.

### ✅ Characteristics:

- Used in **production mode**.
- Templates are precompiled into efficient JS.
- Faster app startup (no compilation at runtime).
- Smaller bundle size (compiler is removed).
- Better security (detects template errors early).
- Fewer runtime surprises (fail-fast approach).

### 📦 Example:

```ts
platformBrowser().bootstrapModuleFactory(AppModuleNgFactory);
```

---

## 🆚 Comparison Table: AoT vs JIT

| Feature              | AoT (Ahead-of-Time)  | JIT (Just-in-Time)         |
| -------------------- | -------------------- | -------------------------- |
| **Compilation Time** | Build time           | Runtime (in browser)       |
| **Build Size**       | Smaller              | Larger (includes compiler) |
| **Startup Time**     | Faster               | Slower                     |
| **Error Detection**  | Early (compile-time) | Late (runtime)             |
| **Best for**         | Production           | Development                |
| **Security**         | More secure          | Less secure                |

---

## 🔍 How to Enable AoT in Angular CLI

Angular CLI uses AoT **by default** for production builds.

```bash
ng build --configuration production
```

Or:

```bash
ng build --aot
```

---

## ✅ Summary for Interviews

| Concept             | Description                                                                             |
| ------------------- | --------------------------------------------------------------------------------------- |
| **JIT**             | Compiles templates in the browser at runtime. Used in development.                      |
| **AoT**             | Compiles templates during build. Used in production for faster load and smaller bundle. |
| **Benefits of AoT** | Early error detection, faster load, better performance and security.                    |
| **When to Use JIT** | During development for faster rebuilds and debugging.                                   |

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 31. How would you implement a global error handler?\*\*

In Angular, a global error handler can be implemented using the `ErrorHandler` class provided by the framework. This allows you to catch and process all unhandled errors throughout the application — useful for logging, user notifications, or redirecting to an error page.

---

### 🔧 **Steps to Implement a Global Error Handler**

#### 1. **Create a Custom Error Handler Class**

```ts
// global-error-handler.service.ts
import { ErrorHandler, Injectable, Injector } from "@angular/core";
import { HttpErrorResponse } from "@angular/common/http";
import { Router } from "@angular/router";

@Injectable()
export class GlobalErrorHandler implements ErrorHandler {
  constructor(private injector: Injector) {} // use Injector to avoid cyclic deps

  handleError(error: any): void {
    const router = this.injector.get(Router);

    if (error instanceof HttpErrorResponse) {
      // Handle server errors
      console.error("HTTP Error:", error.status, error.message);

      if (error.status === 401) {
        // Unauthorized - redirect to login
        router.navigate(["/login"]);
      } else if (error.status === 500) {
        // Server error - show error page
        router.navigate(["/error"]);
      }
    } else {
      // Handle client-side or unknown errors
      console.error("Client Error:", error.message);
      router.navigate(["/error"]);
    }

    // Optionally log to external service
    // this.loggingService.logError(error);
  }
}
```

---

#### 2. **Provide It in Your App Module**

```ts
// app.module.ts
import { NgModule, ErrorHandler } from "@angular/core";
import { GlobalErrorHandler } from "./global-error-handler.service";

@NgModule({
  providers: [{ provide: ErrorHandler, useClass: GlobalErrorHandler }],
})
export class AppModule {}
```

---

### 🛡️ **Best Practices**

- Avoid injecting services directly in the constructor to prevent cyclic dependencies — use `Injector` instead.
- Don't swallow errors silently. Always log or report them.
- Create user-friendly error pages (e.g., `/error`, `/not-found`, etc.).
- Optionally report errors to an external monitoring tool (Sentry, LogRocket, etc.).

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 32. How would you build a role-based authentication system in Angular?\*\*

A role-based authentication system ensures that different types of users (e.g., admin, editor, viewer) can only access parts of the application appropriate to their role. This enhances security and maintains proper access control across routes, components, and UI elements.

---

### 🔐 **Step-by-Step Implementation Guide**

#### 1. **Authentication Service**

Responsible for login/logout and storing user info (like role) in a token or in-memory.

```ts
// auth.service.ts
import { Injectable } from "@angular/core";
import { Router } from "@angular/router";

@Injectable({ providedIn: "root" })
export class AuthService {
  private currentUser: any;

  constructor(private router: Router) {}

  login(userData: any) {
    // In a real app, you'd get a JWT or session token from server
    localStorage.setItem("user", JSON.stringify(userData));
    this.currentUser = userData;
  }

  logout() {
    localStorage.removeItem("user");
    this.currentUser = null;
    this.router.navigate(["/login"]);
  }

  getUser() {
    return this.currentUser || JSON.parse(localStorage.getItem("user") || "{}");
  }

  hasRole(role: string): boolean {
    const user = this.getUser();
    return user?.roles?.includes(role);
  }

  isAuthenticated(): boolean {
    return !!this.getUser();
  }
}
```

---

#### 2. **Role-Based Route Guard**

Prevent users from accessing unauthorized routes based on their role.

```ts
// role.guard.ts
import { Injectable } from "@angular/core";
import {
  CanActivate,
  ActivatedRouteSnapshot,
  RouterStateSnapshot,
  Router,
} from "@angular/router";
import { AuthService } from "./auth.service";

@Injectable({ providedIn: "root" })
export class RoleGuard implements CanActivate {
  constructor(
    private auth: AuthService,
    private router: Router
  ) {}

  canActivate(route: ActivatedRouteSnapshot): boolean {
    const expectedRoles = route.data["roles"] as string[];
    const user = this.auth.getUser();

    if (!user || !expectedRoles.some((role) => user.roles.includes(role))) {
      this.router.navigate(["/unauthorized"]);
      return false;
    }

    return true;
  }
}
```

---

#### 3. **Configure Routes with Roles**

Use `data` property to define allowed roles for each route.

```ts
// app-routing.module.ts
const routes: Routes = [
  {
    path: "admin",
    component: AdminComponent,
    canActivate: [RoleGuard],
    data: { roles: ["admin"] },
  },
  {
    path: "editor",
    component: EditorComponent,
    canActivate: [RoleGuard],
    data: { roles: ["editor", "admin"] },
  },
  {
    path: "unauthorized",
    component: UnauthorizedComponent,
  },
];
```

---

#### 4. **Control UI Elements Based on Role**

You can hide or show elements in templates using a directive or method:

```html
<!-- Example -->
<button *ngIf="authService.hasRole('admin')">Admin Panel</button>
```

---

### 🛡️ **Security Considerations**

- **NEVER** trust client-side role checks alone — also enforce them on the backend.
- Use JWT tokens or sessions securely with HTTPS.
- Refresh user role/token on app start to avoid stale state.

---

### ✅ Summary

> Role-based authentication in Angular involves:
>
> - Storing user roles securely.
> - Guarding routes via `CanActivate`.
> - Dynamically rendering UI elements based on roles.
> - Ensuring backend validation to prevent unauthorized access.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 33. How do you protect certain routes based on user roles?\*\*

Protecting routes based on user roles in Angular is done using **route guards**, particularly the `CanActivate` guard. This ensures users can only access the routes that match their assigned roles (e.g. `admin`, `editor`, `user`, etc.).

---

### 🔐 Step-by-Step Implementation

#### 1. **Assume Your User Object Has Roles**

When users log in, your backend sends a JWT or user object with assigned roles:

```ts
// Sample user object
{
  username: 'john',
  roles: ['admin', 'editor']
}
```

This is stored in localStorage or a service for easy access.

---

#### 2. **Create a Role-Based Route Guard**

```ts
// role.guard.ts
import { Injectable } from "@angular/core";
import { CanActivate, ActivatedRouteSnapshot, Router } from "@angular/router";
import { AuthService } from "./auth.service";

@Injectable({ providedIn: "root" })
export class RoleGuard implements CanActivate {
  constructor(
    private auth: AuthService,
    private router: Router
  ) {}

  canActivate(route: ActivatedRouteSnapshot): boolean {
    const expectedRoles: string[] = route.data["roles"];
    const user = this.auth.getUser();

    if (!user || !expectedRoles.some((role) => user.roles.includes(role))) {
      this.router.navigate(["/unauthorized"]); // Redirect if not allowed
      return false;
    }

    return true;
  }
}
```

---

#### 3. **Use the Guard in Your Routing Configuration**

```ts
// app-routing.module.ts
const routes: Routes = [
  {
    path: "admin-dashboard",
    component: AdminDashboardComponent,
    canActivate: [RoleGuard],
    data: { roles: ["admin"] },
  },
  {
    path: "editor-dashboard",
    component: EditorDashboardComponent,
    canActivate: [RoleGuard],
    data: { roles: ["editor", "admin"] },
  },
  {
    path: "unauthorized",
    component: UnauthorizedComponent,
  },
];
```

---

#### 4. **AuthService with Role Check**

```ts
// auth.service.ts
getUser() {
  return JSON.parse(localStorage.getItem('user') || '{}');
}

hasRole(role: string): boolean {
  const user = this.getUser();
  return user?.roles?.includes(role);
}
```

---

#### 5. **(Optional) UI Restriction for Buttons or Menus**

```html
<!-- Only show admin link if user has 'admin' role -->
<a *ngIf="authService.hasRole('admin')" routerLink="/admin-dashboard">Admin</a>
```

---

### ✅ Summary

> To protect routes based on roles:
>
> - Use `CanActivate` guard and access route metadata via `data.roles`.
> - Verify the user's role from AuthService.
> - Redirect unauthorized users to an error or login page.
> - Always validate roles on the **backend** too, for true security.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 34. How would you implement a retry mechanism for failed API calls?\*\*

In Angular, you can implement a retry mechanism for failed HTTP requests using **RxJS operators** like `retry()`, `retryWhen()`, `delay()`, and `take()` with `HttpClient`.

This is especially useful for transient failures like network issues or rate limiting.

---

### 🔁 **Basic Retry with `retry()`**

```ts
import { HttpClient } from '@angular/common/http';
import { retry, catchError } from 'rxjs/operators';
import { throwError } from 'rxjs';

constructor(private http: HttpClient) {}

getData() {
  return this.http.get('/api/data').pipe(
    retry(3), // Retry 3 times before failing
    catchError(error => {
      console.error('Request failed after retries:', error);
      return throwError(() => error);
    })
  );
}
```

---

### ⏱️ **Retry with Delay using `retryWhen()`**

```ts
import { retryWhen, delay, scan } from 'rxjs/operators';

getDataWithRetry() {
  return this.http.get('/api/data').pipe(
    retryWhen(errors =>
      errors.pipe(
        scan((acc, error) => {
          if (acc >= 2) throw error; // Retry only 3 times
          return acc + 1;
        }, 0),
        delay(2000) // Delay between retries
      )
    ),
    catchError(error => {
      console.error('Failed after retries with delay:', error);
      return throwError(() => error);
    })
  );
}
```

---

### 🔧 **Use Case in an Interceptor for Global Retry**

You can also apply retry logic **globally** using an HTTP interceptor:

```ts
// retry.interceptor.ts
@Injectable()
export class RetryInterceptor implements HttpInterceptor {
  intercept(
    req: HttpRequest<any>,
    next: HttpHandler
  ): Observable<HttpEvent<any>> {
    return next.handle(req).pipe(
      retryWhen((errors) =>
        errors.pipe(
          scan((retryCount, err) => {
            if (retryCount >= 3) {
              throw err;
            }
            return retryCount + 1;
          }, 0),
          delay(1000)
        )
      )
    );
  }
}
```

Register this interceptor in `AppModule` providers array with `multi: true`.

---

### ⚠️ **Things to Keep in Mind**

- Do **not** retry on client-side validation errors (e.g., 400 Bad Request).
- You should retry mainly on:
  - `0` (network error),
  - `503` (service unavailable),
  - `429` (rate limit).

- You can customize this using conditions inside the `scan` operator.

---

### ✅ Summary

> Use `retry()` for simple retries or `retryWhen()` with `delay` and `scan` for advanced use cases. You can also add global retry logic via HTTP interceptors. Always handle errors gracefully and avoid retrying fatal errors.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 35. How do you manage global state in Angular (e.g., using NgRx or a shared service)?\*\*

Global state management in Angular refers to **maintaining and sharing application state (like user info, theme, authentication, cart data) across multiple components** without unnecessary duplication or prop drilling.

There are two primary approaches:

---

## **1. Using a Shared Service with RxJS**

A lightweight solution for smaller apps.

### **Step 1: Create a State Service**

```ts
// app-state.service.ts
import { Injectable } from "@angular/core";
import { BehaviorSubject } from "rxjs";

@Injectable({ providedIn: "root" })
export class AppStateService {
  private userSource = new BehaviorSubject<any>(null);
  user$ = this.userSource.asObservable();

  setUser(user: any) {
    this.userSource.next(user);
  }

  clearUser() {
    this.userSource.next(null);
  }
}
```

---

### **Step 2: Use in Components**

```ts
// component.ts
constructor(private appState: AppStateService) {}

ngOnInit() {
  this.appState.user$.subscribe(user => {
    console.log('Current user:', user);
  });
}

login() {
  this.appState.setUser({ name: 'John', role: 'admin' });
}
```

✅ **Advantages:** Simple, minimal boilerplate, easy to implement.
⚠️ **Disadvantages:** Not ideal for very large apps with complex state.

---

## **2. Using NgRx (Redux Pattern for Angular)**

For enterprise apps or complex state, use **NgRx** (a state management library following the Redux pattern).

### **Core Concepts in NgRx**

- **Store** → Single source of truth for state.
- **Actions** → Describe what happened (e.g., `LOGIN_SUCCESS`).
- **Reducers** → Update state based on actions.
- **Selectors** → Retrieve slices of state.
- **Effects** → Handle side effects like API calls.

---

### **Basic Example**

#### **Define Action**

```ts
// user.actions.ts
import { createAction, props } from "@ngrx/store";

export const setUser = createAction("[User] Set", props<{ user: any }>());
```

#### **Reducer**

```ts
// user.reducer.ts
import { createReducer, on } from "@ngrx/store";
import { setUser } from "./user.actions";

export const initialState = null;

const _userReducer = createReducer(
  initialState,
  on(setUser, (state, { user }) => user)
);

export function userReducer(state: any, action: any) {
  return _userReducer(state, action);
}
```

#### **Dispatch & Select**

```ts
// component.ts
constructor(private store: Store<{ user: any }>) {}

setUser() {
  this.store.dispatch(setUser({ user: { name: 'John', role: 'admin' } }));
}

ngOnInit() {
  this.store.select('user').subscribe(user => console.log(user));
}
```

---

## ✅ **When to Use What**

| Approach                  | When to Use                                    |
| ------------------------- | ---------------------------------------------- |
| **Shared Service + RxJS** | Small to medium apps, simple state             |
| **NgRx (Redux)**          | Large, complex apps with multiple state slices |

---

### ✅ **Summary**

> - Use **Shared Service with BehaviorSubject** for simple global state.
> - Use **NgRx** for large apps needing predictable state management, time-travel debugging, and clear architecture.
> - Both rely on **RxJS** for reactive data flow.

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 36. How would you share data between unrelated components in Angular?

In Angular, unrelated components (components not in a parent-child relationship) **cannot use `@Input()` or `@Output()` to communicate** directly. Instead, Angular provides several powerful patterns to enable communication and data sharing between such components.

---

### 🔹 **1. Shared Service with RxJS (Most Common Approach)**

This is the most widely used and scalable method for sharing data across unrelated components using a singleton service and RxJS observables like `Subject` or `BehaviorSubject`.

#### ✅ Create the Shared Service

```ts
// shared-data.service.ts
import { Injectable } from "@angular/core";
import { BehaviorSubject } from "rxjs";

@Injectable({ providedIn: "root" })
export class SharedDataService {
  private sharedValue = new BehaviorSubject<string>("default");
  sharedValue$ = this.sharedValue.asObservable();

  updateValue(newVal: string) {
    this.sharedValue.next(newVal);
  }
}
```

#### ✅ Component A (Sender)

```ts
// component-a.ts
constructor(private sharedData: SharedDataService) {}

sendData() {
  this.sharedData.updateValue('Hello from A');
}
```

#### ✅ Component B (Receiver)

```ts
// component-b.ts
constructor(private sharedData: SharedDataService) {}

ngOnInit() {
  this.sharedData.sharedValue$.subscribe(val => {
    console.log('Received in B:', val);
  });
}
```

---

### 🔹 **2. State Management Libraries (NgRx, NGXS, Akita)**

For complex applications with many unrelated components needing to share or sync data, use centralized state management.

- **NgRx** provides a Redux-style store, actions, reducers, and selectors.
- Promotes **predictability**, **testability**, and **scalability**.

```ts
// With NgRx: dispatch actions and use selectors to get shared state
this.store.dispatch(updateUser({ user }));
this.store.select(selectUser).subscribe((user) => console.log(user));
```

---

### 🔹 **3. Route Parameters or Query Params**

If components are navigated via Angular Router, you can pass data through the URL.

```ts
// From Component A
this.router.navigate(["/details"], { queryParams: { id: 123 } });
```

```ts
// In Component B
this.route.queryParams.subscribe((params) => {
  const id = params["id"];
});
```

---

### 🔹 **4. LocalStorage / SessionStorage**

For simple, persistent data (non-sensitive), use browser storage:

```ts
localStorage.setItem("username", "john");
const username = localStorage.getItem("username");
```

---

### 🔹 **5. Event Bus (Custom Event Emitter Service)**

You can also build a global event bus using an RxJS `Subject`.

```ts
// event-bus.service.ts
event$ = new Subject<string>();

emit(msg: string) {
  this.event$.next(msg);
}

listen() {
  return this.event$.asObservable();
}
```

---

### ✅ **Summary Table**

| Method                  | When to Use                                    |
| ----------------------- | ---------------------------------------------- |
| Shared Service + RxJS   | Best for most cases, clean and reactive        |
| State Management (NgRx) | Large apps needing global state & traceability |
| Router Params           | When navigating and passing info via routes    |
| Local/Session Storage   | Simple persistence without services            |
| Event Bus (RxJS)        | App-wide custom event handling                 |

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 37. How do you handle file upload and preview in Angular?\*\*

In Angular, file upload and preview involves:

1. Using an `<input type="file">` element to select a file.
2. Reading the file with `FileReader` for preview.
3. Uploading the file via an Angular `HttpClient` POST request to the server.

---

### 🔹 Step-by-Step Implementation

---

#### ✅ **1. Template – File Input and Preview UI**

```html
<!-- file-upload.component.html -->
<input type="file" (change)="onFileSelected($event)" />
<div *ngIf="previewUrl">
  <img *ngIf="isImage" [src]="previewUrl" alt="Preview" width="200" />
  <p *ngIf="!isImage">Selected file: {{ file?.name }}</p>
</div>
<button (click)="uploadFile()" [disabled]="!file">Upload</button>
```

---

#### ✅ **2. Component Logic – File Handling**

```ts
// file-upload.component.ts
import { Component } from "@angular/core";
import { HttpClient } from "@angular/common/http";

@Component({
  selector: "app-file-upload",
  templateUrl: "./file-upload.component.html",
})
export class FileUploadComponent {
  file: File | null = null;
  previewUrl: string | null = null;
  isImage = false;

  constructor(private http: HttpClient) {}

  onFileSelected(event: Event) {
    const input = event.target as HTMLInputElement;
    if (input.files?.length) {
      this.file = input.files[0];
      const reader = new FileReader();

      reader.onload = () => {
        this.previewUrl = reader.result as string;
        this.isImage = this.file!.type.startsWith("image/");
      };
      reader.readAsDataURL(this.file);
    }
  }

  uploadFile() {
    if (!this.file) return;

    const formData = new FormData();
    formData.append("file", this.file);

    this.http.post("/api/upload", formData).subscribe({
      next: (res) => console.log("Upload success", res),
      error: (err) => console.error("Upload failed", err),
    });
  }
}
```

---

### 🔹 Backend Expectation

The backend (Node.js, Django, etc.) should expect a multipart/form-data upload under the key `file`.

---

### ✅ **Best Practices**

| Best Practice                    | Why Important                                        |
| -------------------------------- | ---------------------------------------------------- |
| Use `FormData`                   | To send files as multipart/form-data                 |
| Validate file size/type          | Avoid uploading large or unsupported files           |
| Show progress with `HttpRequest` | For UX, show upload status or spinner                |
| Secure backend                   | Sanitize and validate uploaded content on the server |

---

### 🔹 Extra: Show Upload Progress (Optional)

```ts
import { HttpRequest, HttpEventType } from "@angular/common/http";

const req = new HttpRequest("POST", "/api/upload", formData, {
  reportProgress: true,
});

this.http.request(req).subscribe((event) => {
  if (event.type === HttpEventType.UploadProgress && event.total) {
    const progress = Math.round((100 * event.loaded) / event.total);
    console.log(`Progress: ${progress}%`);
  }
});
```

---

### ✅ Summary

| Feature         | How                                       |
| --------------- | ----------------------------------------- |
| Select file     | `<input type="file">`                     |
| Preview file    | `FileReader.readAsDataURL()`              |
| Upload file     | `HttpClient.post()` with `FormData`       |
| Handle progress | `HttpRequest` with `reportProgress: true` |

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 38. How would you integrate a third-party chart library or rich text editor in Angular?

Angular supports seamless integration of third-party libraries like **charting tools** (e.g., Chart.js, ApexCharts) and **rich text editors** (e.g., Quill, CKEditor) using Angular wrappers or native libraries via npm.

---

### 🟦 Example 1: Integrating a Chart Library (Chart.js)

#### ✅ 1. **Install Chart.js and ng2-charts (Angular wrapper)**

```bash
npm install chart.js ng2-charts
```

#### ✅ 2. **Import in Module**

```ts
import { NgChartsModule } from "ng2-charts";

@NgModule({
  imports: [NgChartsModule],
})
export class AppModule {}
```

#### ✅ 3. **Use in Component**

```html
<!-- chart.component.html -->
<canvas baseChart [data]="chartData" [type]="'bar'" [options]="chartOptions">
</canvas>
```

```ts
// chart.component.ts
import { Component } from "@angular/core";
import { ChartOptions, ChartType, ChartData } from "chart.js";

@Component({
  selector: "app-chart",
  templateUrl: "./chart.component.html",
})
export class ChartComponent {
  chartData: ChartData<"bar"> = {
    labels: ["Jan", "Feb", "Mar"],
    datasets: [{ data: [65, 59, 80], label: "Sales" }],
  };
  chartOptions: ChartOptions = {
    responsive: true,
  };
}
```

---

### 🟦 Example 2: Integrating a Rich Text Editor (Quill)

#### ✅ 1. **Install Quill and ngx-quill**

```bash
npm install quill ngx-quill
```

#### ✅ 2. **Import Modules**

```ts
import { QuillModule } from "ngx-quill";

@NgModule({
  imports: [QuillModule.forRoot()],
})
export class AppModule {}
```

#### ✅ 3. **Use in Template**

```html
<!-- rich-text.component.html -->
<quill-editor [(ngModel)]="editorContent"></quill-editor>
<p>Preview:</p>
<div [innerHTML]="editorContent"></div>
```

```ts
// rich-text.component.ts
export class RichTextComponent {
  editorContent: string = "";
}
```

> 🔒 Don't forget to enable `FormsModule` or `ReactiveFormsModule` for `ngModel`.

---

### ✅ Best Practices

| Task                                                      | Why It’s Important                                  |
| --------------------------------------------------------- | --------------------------------------------------- |
| Use official Angular wrappers (`ng2-charts`, `ngx-quill`) | Simplifies integration, leverages Angular lifecycle |
| Lazy load heavy modules                                   | Improve initial load time                           |
| Sanitize HTML if saving rich text                         | Prevent XSS attacks                                 |
| Use `ViewChild` to access editor/chart instances          | For programmatic control                            |

---

### ✅ Summary Table

| Library Type     | Popular Packages                       | Angular Support                 |
| ---------------- | -------------------------------------- | ------------------------------- |
| Charting         | Chart.js + ng2-charts                  | ✅ Wrapper                      |
|                  | ApexCharts + ngx-apexcharts            | ✅ Wrapper                      |
| Rich Text Editor | Quill + ngx-quill                      | ✅ Wrapper                      |
|                  | CKEditor + @ckeditor/ckeditor5-angular | ✅ Official Angular Integration |

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 39. How do you handle environment-based configurations (dev/prod) in Angular?\*\*

Angular provides built-in support for managing different configurations (e.g., development, staging, production) using the **`src/environments/`** directory and **file replacements** during build time.

---

### ✅ Step-by-Step Guide

#### 1. **Define Environment Files**

Create environment-specific files under `src/environments/`:

- `environment.ts` → for development
- `environment.prod.ts` → for production
- You can also create more: `environment.staging.ts`, etc.

```ts
// environment.ts
export const environment = {
  production: false,
  apiBaseUrl: "https://dev-api.example.com",
};
```

```ts
// environment.prod.ts
export const environment = {
  production: true,
  apiBaseUrl: "https://api.example.com",
};
```

---

#### 2. **Use Environment Config in Code**

You can import and use the configuration anywhere in your app:

```ts
import { environment } from "../environments/environment";

this.http.get(`${environment.apiBaseUrl}/users`);
```

---

#### 3. **Configure File Replacements in `angular.json`**

Angular replaces `environment.ts` with `environment.prod.ts` during production builds.

```json
"fileReplacements": [
  {
    "replace": "src/environments/environment.ts",
    "with": "src/environments/environment.prod.ts"
  }
]
```

You can also add more configurations (like staging) under different configurations.

---

#### 4. **Build with the Right Configuration**

- Development:

  ```bash
  ng serve
  ```

- Production:

  ```bash
  ng build --configuration production
  ```

- Custom config (e.g., staging):

  ```bash
  ng build --configuration staging
  ```

---

### ✅ Best Practices

| Practice                                                                               | Reason                                    |
| -------------------------------------------------------------------------------------- | ----------------------------------------- |
| Keep secrets (API keys, tokens) **out** of environment files                           | Avoid exposing sensitive data in frontend |
| Use Angular CLI configurations instead of manually checking `window.location.hostname` | Cleaner and safer                         |
| Avoid hardcoding URLs                                                                  | Use `environment` consistently            |
| Consider `.env` files with build tools like `dotenv-webpack` if using custom builders  | More flexible for CI/CD                   |

---

### ✅ Example Use Case

```ts
// api.service.ts
import { HttpClient } from "@angular/common/http";
import { environment } from "../../environments/environment";

@Injectable()
export class ApiService {
  constructor(private http: HttpClient) {}

  getUsers() {
    return this.http.get(`${environment.apiBaseUrl}/users`);
  }
}
```

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>

## 40. How would you lazy load and preload Angular modules?\*\*

In Angular, **lazy loading** allows you to load feature modules **only when they're needed**, improving performance. **Preloading** helps by loading those modules in the background **after the app starts**.

---

### 🚀 **Lazy Loading**

#### ✅ Step 1: Create a Feature Module with Routing

```bash
ng generate module features/dashboard --route dashboard --module app
```

This sets up lazy loading automatically.

Or manually:

```ts
// app-routing.module.ts
const routes: Routes = [
  {
    path: "dashboard",
    loadChildren: () =>
      import("./features/dashboard/dashboard.module").then(
        (m) => m.DashboardModule
      ),
  },
];
```

> ✅ This uses **dynamic imports** to load the module only when `dashboard` route is accessed.

---

#### ✅ Step 2: Configure the Feature Module

```ts
// dashboard-routing.module.ts
const routes: Routes = [{ path: "", component: DashboardComponent }];

@NgModule({
  imports: [RouterModule.forChild(routes)],
  exports: [RouterModule],
})
export class DashboardRoutingModule {}
```

---

### ⚡️ **Preloading Modules**

Lazy loading improves initial load, but if users will visit multiple routes, preloading improves performance.

#### ✅ Enable Preloading

```ts
// app-routing.module.ts
import { PreloadAllModules } from "@angular/router";

@NgModule({
  imports: [
    RouterModule.forRoot(routes, {
      preloadingStrategy: PreloadAllModules,
    }),
  ],
  exports: [RouterModule],
})
export class AppRoutingModule {}
```

> 📦 `PreloadAllModules` tells Angular to preload **all lazy-loaded modules** in the background after app starts.

---

### 🔧 Custom Preloading Strategy (Advanced)

You can write custom logic to preload only some modules:

```ts
export class CustomPreloadingStrategy implements PreloadingStrategy {
  preload(route: Route, load: () => Observable<any>): Observable<any> {
    return route.data && route.data["preload"] ? load() : of(null);
  }
}
```

Use it in route:

```ts
{
  path: 'admin',
  loadChildren: () => import('./admin/admin.module').then(m => m.AdminModule),
  data: { preload: true }
}
```

---

### 🧠 Summary

| Feature             | Benefit                                       |
| ------------------- | --------------------------------------------- |
| **Lazy Loading**    | Reduces initial bundle size                   |
| **Preloading**      | Improves navigation speed                     |
| **Custom Strategy** | Fine-grained control over what gets preloaded |

---

<div align="right">
    <b><a href="#table-of-contents">↥ back to top</a></b>
</div>
