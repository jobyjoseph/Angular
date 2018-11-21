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
