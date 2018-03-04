---
title: Object Assign
date: "2018-03-03T22:40:32.169Z"
---

# Immutability With Objects

#### what is Immutable Data

Immutable data presents a mutative API which does not update the data in-place, but instead yields new updated data.

##### Example of mutable object

                const toggleTodo = (todos) => {
                    todos.completed = !s.completed;
                    return todos;
                }

##### Immutable Object with new object literal.

                const toggleTodo = (todos) => {
                    return {
                        id: todos.id,
                        text: todos.text,
                        completed: !todos.completed
                    };
                }

**Immutability** immutability allows you to optimize your application by making use of reference and value equality. This makes it easy to see if anything has changed. For example a state change in a React component. The **_shouldComponentUpate_** checks against to see if the state is identical by comparing state objects.

##### Immutable Objects with ES2015 [Object.assig()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/assign)

assign properties of several object onto target object. The argument order corresponds to the assign operator. The left argument is the ones whose property will be assigned to every further arguments will represent one of the source objects whose properties will be copied to the target object. If several sources represent the same properties the last one wins.

                            const toggleTodo = (todos) => {
                                return Object.assign({}, todos, {
                                    completed: !todo.completed
                                });
                            }

##### Immuatable Objecs with ES2016 [Spread operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_operator).

The spread operator allows an expression to be expanded in places where multiple arguments

                            const toggleTodo = (todos) => {
                                return {
                                    ...todos,
                                    completed: !todo.completed
                                };
                            }
