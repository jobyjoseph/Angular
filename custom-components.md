All files needed as part a custom component will be in folder. Here we are creating a `server` component.

__server/server.component.ts__
```javascript
import { Component } from '@angular/core';

@Component({
  selector: 'app-server',
  templateUrl: './server.component.html'
})
export class ServerComponent {

}
```

__server/server.component.html__
```html
<h1>This is a server component</h1>
```

After creating the above 2 files, we need to attach the new component to our _module_.
__app.module.ts__
```javascript
...
import { ServerComponent } from './server/server.component';
@NgModule({
  declarations: [
    AppComponent,
    ServerComponent
  ],
  ...
})
export class AppModule { }
```

Now we can use our new component in any components inside `AppModule` like:
```html
...
<h1>Inside App Component</h1>
<hr />
<app-server></app-server>
...
```

## Creating Custom Components Using CLI
We can generate a boilerplate to create new component from command line. Go to the project folder in terminal.
```
ng generate component <component-name>
```
It will create the component inside `app` folder.

## Selectors in Custom Components
__As element__
When we write
```javascript
selector: 'app-servers'
```
we use it as an element
```html
<app-servers></app-servers>
```

__As attribute__
When we write
```javascript
selector: '[app-servers]'
```
we use it as an attribute
```html
<div app-servers></div>
```

__As class__
When we write
```javascript
selector: '.app-servers'
```
we use it with class
```html
<div class="app-servers"></div>
```
