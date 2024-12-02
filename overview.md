# Overview

Glimmer is a set of libraries to create user interfaces using various UI toolkits. It's meant to use the unique attributes of Ruby to create readable / testable and consice code to produce an user interface. There exist UI toolkit backends for the following toolkits:

| UI Toolkit | Ruby variant | Level of support | Relevant versions |
| GTK+       | RMI          | non-binding      |                   |
| LibUI      | RMI          | 2-way binding    |                   |
| WxWindows  | RMI          | 2-way binding    |                   |
| SWT        | JRuby        | 2-way binding    |                   |
| Web        | Opal         | 2-way binding    | < Rails 7.1       |

## Operating Principles

One of the main operting principles is to make it easy to create UIs.  It is inspired by \_whytheluckystiff's UI library Shoes. Some of the improvements over Shoes is the usage of 2-way binding. 2-way binding allows it easy to support complex user interfaces with complex interactions that are easy to think about.
