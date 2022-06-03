# The Conditional Clause

## Learning Goals

- Explain boolean expressions
- Use conditional clauses

## Introduction

A Java "conditional clause" is an expression that evaluates (i.e. returns) either true or false. These are the only two valid
values for a conditional clause, no in-between.

In the example above, `age > 18` can only return two values: "either `age` is larger than `18` or it's not". Notice that I didn't say
"either `age` is larger than `18` or it's smaller than `18`", and that's because the latter wording would leave open a third
possibility, which is that "age could be equal to 18", which would then lead to a third possible value.

Expressions that can only evaluate to either `true` or `false` are called `boolean` expressions. Similarly, variables of type
`boolean` are variables that can only hold the value `true` or the value `false`. For example:

```java
boolean userIsAdult = age > 18; 
```

Defines a variable named `userIsAdult` of type `boolean` and assigns it the values that the expression `age > 18` returns.
With that, we could rewrite our `if` statement as follows:

```java
if (userIsAdult) {
    System.out.println("Look at you, all grown up");
}
```

Boolean variables can also be assigned a hard-coded value of either `true` or `false`: 

```java
boolean thisVariableIsTrue = true; 
boolean thisVariableIsFalse = false; 
```

Or a version with simpler names: 

```java
boolean trueVar = true; 
booelan falseVar = false; 
```

Boolean expressions support the following comparison operators:

* `==` compares two values and returns `true` if they are equal or `false` if they are not equal
* `!=` compares two values and returns `true` if they are not equal or `false` if they are equal
* `>` return true if the left-hand side operand is strictly greater than the right-hand side operand, or false otherwise
* `<` return true if the left-hand side operand is strictly smaller than the right-hand side operand, or false otherwise
* `>=` return true if the left-hand side operand is greater than or equal to the right-hand side operand, or false otherwise
* `<=` return true if the left-hand side operand is smaller than or equal to the right-hand side operand, or false otherwise

These comparison operators can be combined with the following logical operators:

* `&&` returns true if and only if both sides of the operator are true, so `trueVar && trueVar` returns `true` while `trueVar && falseVar` returns `false` 
* `||` returns true if either side of the operator is true, so `trueVar || falseVar` return `true` while `falseVar || falseVar` returns `false`
* `!` is a unary operator that returns the reverse of its single operand, so `!trueVar = false` and `!falseVar = true`
