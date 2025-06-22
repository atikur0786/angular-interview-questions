# Angular Interview Questions & Answers – Beginner Level (Conceptual Foundation)

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
