# js prototypes

- every objects have \[\[prototype]]
  - implemented as `__proto__` attribute
  - \[\[prototype]] has attributes, and reference to next prototype in the chain
- every functions have a `prototype` attribute
  - object constructor are type of function
  - `prototype` becomes the new object's `__proto__` created with the constructor
- when accessing an attribute or method
  - js goes through the prototype chain until it reaches null
    - which is end of chain
