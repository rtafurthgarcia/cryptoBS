# CryptoBS

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 16.2.1.

## Basics 

Thats how the structure of an angular app should look like:
```
.
├── src
│   ├── app.component.html
│   ├── app.component.scss
│   ├── app.component.spec.ts
│   ├── app.component.ts
│   ├── app.module.ts
│   ├── app-routing.module.ts
│   ├── core
│   │   ├── auth -> for authentication services
│   │   ├── services -> for general services
│   │   └── other-small-dumb-component
│   ├── environment.service.ts
│   ├── features
│   │   └── add-blog-page -> each smart component has to be a page and has to have a module 
│   │       ├── new-blog-page.component.html
│   │       ├── new-blog-page.component.scss
│   │       ├── new-blog-page.component.spec.ts
│   │       ├── new-blog-page.component.ts
│   │       └── new-blog-page.module.ts
│   └── shared -> all dumb components, so without a module
│       └── add-blog-form
│           ├── add-blog-form.component.html
│           ├── add-blog-form.component.scss
│           ├── add-blog-form.component.spec.ts
│           └── add-blog-form.ts
├── environments -> for our env files
│   ├── environment.development.ts
│   ├── environment.ts
│   └── ienvironment.ts -> if possible an interface setting the minimum requirements for a proper env file
├── favicon.ico
├── index.html -> nothing but the app skelleton and the <app-root\>
├── main.ts
└── styles.scss -> for global styles
```

### Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

### Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

### Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

### Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Create new components 

- To create new environments config file: `ng generate environments`
- To create a core component: `ng generate component core/header -c "OnPush"`
- To create a new smart component:
    - first register a module: `ng generate module features/blogOverviewPage -m app.module`
    - then create the other basic component files related to this module: `ng generate component features/blog-overview-page/blogOverviewPage --flat -m features/blog-overview-page/blog-overview-page.module --export`
- To create a service: `ng generate service core/services/api.state.service`