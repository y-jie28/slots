# slots

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

<hr />

## Notes

### The Problem
- The form component is reusable, but not flexible enough for different kinds of forms. 

### Slots
- A way for markup from the parent component to the child component. 

If no content is passed from the parent, the child will render default content. 

v-slot directive is used with names assigned to slots. It can only be used on __template__ tags. 

A combination of __slots__ and __named slots__ can be used. 

