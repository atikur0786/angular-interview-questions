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
