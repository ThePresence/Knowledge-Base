
- [Angular](#angular)
  - [To change default startup page -](#to-change-default-startup-page)
  - [Components Basics](#components-basics)
  - [Angular Start-up Loading](#angular-start-up-loading)

# Angular

## To change default startup page -

- try changing the redirectTo in app-routing.module.ts: redirectTo: 'auth/login'

## Components Basics

```
selector: 'ngx-app    // tag
template: '<h2>Hello</h2>' 	//HTML Code
```

## Angular Start-up Loading

- Main.ts --> Passes as an argument to app.module.ts --> loads component.ts --> angular analyses selector tag -->and it loads html