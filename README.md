# LibDemo

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 6.1.5.

Demo is based on this [article](https://medium.com/@tomsu/how-to-build-a-library-for-angular-apps-4f9b38b0ed11).


## install the library

Presuming the library project folder is a sibling of this demo project, run

```angular2html
$ npm install ../example-ng6-lib/dist/example-ng6-lib/example-ng6-lib-1.0.0.tgz
```

dependencies will now look like:

```angular2html
"dependencies": {
  . . .
  "example-ng6-lib": "file:../example-ng6-lib/dist/example-ng6-lib/example-ng6-lib-0.0.1.tgz",
  . . .
},
```

**note**: always import the library `tgz` and not the directory itself.

Import the library module:

```angular2html
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';

import { AppComponent } from './app.component';
import {ExampleNg6LibModule} from 'example-ng6-lib';

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    ExampleNg6LibModule   <----
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

and use `FooComponent` in `app.component.html`:

```angular2html
<div style="text-align:center">
  <h1>
    Welcome to {{ title }}!
  </h1>
  <img width="300" alt="Angular Logo" src="data:image/svg+xml;base64,PHN2...">
  
  <enl-foo></enl-foo>  <---
  
</div>
```

and 

```angular2html
$ ng serve
```



