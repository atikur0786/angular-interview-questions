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
  constructor(private authService: AuthService, private router: Router) {}

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
