# Angular2-demo

## A sample demo with Angular2

### HTML

```html
<my-app>Loading...</my-app>
```

### System.config

```JS
System.config({
        transpiler: 'typescript',
        typescriptOptions: { emitDecoratorMetadata: true },
        packages: {'app': {defaultExtension: 'ts'}}
      });
      System.import('/app/environment_main')
            .then(null, console.error.bind(console));
```
### Component.ts

```JS
import {Component, View} from "angular2/core";

@Component({
   selector: 'my-app'
})

@View({
  template: '<h2>Angular 2 </h2>'
})

export class AppComponent {

}

```

### Environment Main.ts

```JS
import {bootstrap} from "angular2/platform/browser"
import {AppComponent} from "./environment_app.component"

bootstrap(AppComponent);

```
