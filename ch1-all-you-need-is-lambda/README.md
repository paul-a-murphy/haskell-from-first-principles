All you need is Lambda

A calculus is a method of calculation or reasoning; the lambda calculus is one process for formalizing a method.


## What is functional programming

Functional programming is a computer programming paradigm that relies on functions modeled on mathematical functions. The essence of functional programming is that programs are a combination of expressions. Expressions include concrete values, variables and also functions.

Functions have a more specific definition: they are expressions that are applied to an argument or input, and once applied, can be _reduced_ or _evaluated_.

### Referential Transparency

The word purity in functional programming is sometimes used to mean what is more properly called _referential transparency_. Referential Transparency means that the same function, given the same values, will always return the same results in pure functional programming.

## What is a function

A function is a relation between a set of possible inputs and a set of possible outputs. The function itself defines and represents the relationship. When you apply a function such as addition to two inputs, it maps those two inputs to an output - the sum of those numbers.

## The structure of lambda terms

The lambda calculus has three basic components, or lambda terms: expressions, variables, and abstractions. The word expressions refers to a superset of all those things: an expression can be a variables name, an abstraction, or a combination or those things.

The simplest expression is a single _variables_. Variables have no meaning or value; they are just names for potential inputs to functions.

An _abstraction_ is a _function_. It is a lambda term that has a head and a body and is applied to an argument. An _argument_ is an input value.

Abstractions consist of two parts: the _head_ and the _body_. The head of the function is a λ (lambda) followed by a variables name. The body of the function is another expressions. So, a simple function might look like this:

```
λx.x
```
The variables named in the head is the parameter and binds all instancesof that same variable in the body function. That means when we apply this function to an argument, each _x_ in the body of the function will have the value of that argument.

The above lambda abstraction has no name and is an _anonymous function_. Let's break down the basic structure:

```
λ x . x
^___^
  |
  ------- the extend of the head of the lambda.

λ x . x
  ^------- the single parameter of the function

λ x . x
    ^---- the body, the expressions the lambda returns when applied.
```

The dot (.) separates the parameters of the lambda from the function body.

## Beta reduction

When we apply a function to an argument, we substitute the input expressions for all instances of bound variables within the body of the abstraction. This is called beta reduction.

Beta Reduction is this process of applying a lambd term to an argument, replacing the bound variables with the value of the argument, and eliminating the head.

Applications in te lambda calculus are _left associative_. That is, unless specific parentheses suggest otherwiser, they associate to the left.

## Free variables

The purposes of the head of the function is to tell us which variables to replace when we apply our function, that is, to bind the variables. But sometimes the body expression has variables that are not named in the head. These are called _free variables_. In the following expressions:

```
_x_._xy_
```

The _x_ in the body is bound, while the y is a free variables. When we apply this function to an argument, nothing can be done with the _y_. It remains unreducible.  
