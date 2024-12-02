# Web UI Toolkit

The Web toolkit depends on running the Opal version of
ruby. 

Opal is a ruby implementation that is similar to
MRI but differs in that it has differences due to being
implemented as a complement to Javascript. For example,
strings in Opal are immutable like JS strings, so all
methods in Ruby that mutate strings are not implemented. It is like 95%
compatible with Ruby and you can write standard Ruby code with a few 
guidelines of things to avoid to maintain compatibility.

## The basics

Creating static HTML with glimmer-web uses a Domain Specific Language (DSL) to
describe the HTML to produce. A simple hellow world is given below:

```ruby
require 'glimmer-dsl-web'

include Glimmer

Document.ready? do
  div {
    'Hello, World!'
  }
end
```

This produces the following HTML:

```html
<div data-parent="body" class="element element-1">
  Hello, World!
</div>
```

## HTML Guide

### html tag

```
[tag_name](tag_attributes_hash) do
   on[event] do |event|    # zero or more event handlers
   end 
   
end
```

* tag_name - any valid HTML tag name
* tag_attributes_hash - the keys and values map to HTML attributes and values

