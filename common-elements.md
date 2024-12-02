# Glimmer Common Elements

While support for the various UI toolkits require different sets of methods 
that correspond with the toolkit's terminology and sets of controls, there is 
a common way of handling 2-way binding. 

## 2-Way binding

The glimmer library uses operator overriding to define a unique syntax for
one way and two way bindings. The basic structure is an aspect of an control 
(or element in the web UI), and object it is associated with. An example 
from the LibUI adapter.

```ruby
label do
  text <=> [car, :color]
end
```
In the case above, the label control's text attribute (i.e. what is displayed
for the label) is bound to the car object and color attribute. The method
named above needs to be like an attr_accessor, that is, there needs to be a
method called :color and a method called :color=.
