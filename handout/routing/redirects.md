# Route Redirections #

When your application starts, it navigates to the empty route by default.
We can configure the router to redirect to a named route by default:

```javascript
export const routes: RouterConfig = [
  { path: '', redirectTo: 'component-one', pathMatch: 'full' },
  { path: 'component-one', component: ComponentOne },
  { path: 'component-two', component: ComponentTwo }
];
```

This tells the router to redirect to component-one when matching the empty path ('').

When starting the application, it will automatically navigate to the route for `component-one`.

> pathMatch is an optional property that defaults to 'prefix' which determines whether to match full URLs or just the beginning. When defining a route with empty path string we must set pathMatch to 'full', otherwise it would match all paths.