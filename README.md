Angular is a JavaScript framework to build reactive Single Page Applications.

Angular 1 was created in 2010. It is now populary known as __AngularJS__. Angular 2 was a completely new code with no relation with version 1. Then other versions came till Angular 7. Angular 2 to 7 is popularly known as __Angular__.

### Installing Angular CLI
```
npm install -g @angular/cli@latest
```

### Create new Angular Project
```
ng new my-first-app
```
This command might ask few questions. Mark the relevant options.

### Running Angular Project
Navigate to the Angular project directory.
```
ng serve
```

## Binding with an input
We need to import FormsModule to use binding with forms.

__app.module.ts__
```javascript
...
import { FormsModule } from '@angular/forms';
...
imports: [
    BrowserModule,
    FormsModule
  ],
...
```
__app.component.html__
```html
<input type="text" [(ngModel)]="name"/>
<p>{{name}}</p>
```

## Adding extra styles to project
First we need to install the css framework like Bootstrap. Then add reference in _angular.json_ config file.

__angular.json__
```javascript
...
"styles": [
  "node_modules/bootstrap/dist/css/bootstrap.min.css",
  "src/styles.css"
],
...
```

## Angular Compiler Flow
When an App starts, Angular CLI starts with `main.ts` file. There we are saying to `bootstrapModule` with `AppModule`. `AppModule` is a reference to `app.module.ts` file. Inside `app.module.ts` file, we are pointing to `AppComponent`. This is how the app displays the html from app.component.html.

## Creating a New Component
It is good to have the component folder name match component name.
