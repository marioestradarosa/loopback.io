---
lang: en
title: 'Add the Todo Model'
keywords: LoopBack 4.0, LoopBack 4
sidebar: lb4_sidebar
permalink: /doc/en/lb4/todo-tutorial-model.html
summary: LoopBack 4 Todo Application Tutorial - Add the Todo Model
---

### Models

Now we can begin working on the representation of our data for use with
LoopBack 4. To that end, we're going to create a Todo model that can represent
instances of a task for our Todo list. The Todo model will serve both as a
[Data Transfer Object](https://en.wikipedia.org/wiki/Data_transfer_object) (also
known as a DTO) for representing incoming Todo instances on requests, as well as
our data structure for use with loopback-datasource-juggler.

A model describes business domain objects and defines a list of properties with
name, type, and other constraints.

Models are used for data exchange on the wire or between different systems.

For more information about Models and how they are used in LoopBack, see
[Models](https://loopback.io/doc/en/lb4/todo-tutorial-model.html).

> **NOTE:** LoopBack 3 treated models as the "center" of operations; in LoopBack
> 4, that is no longer the case. While LoopBack 4 provides many of the helper
> methods and decorators that allow you to utilize models in a similar way, you
> are no longer _required_ to do so!

### Building your Todo model

A todo list is all about tracking tasks. For this to be useful, it will need to
let you label tasks so that you can distinguish between them, add extra
information to describe those tasks, and finally, provide a way of tracking
whether or not they're complete.

For our Todo model to represent our Todo instances for our business domain, it
will need:

- a unique id
- a title
- a description that details what the todo is all about
- a boolean flag for whether or not we've completed the task

We can use the `lb4 model` command and answer the prompts to generate the model
for us. Press `return` with an empty property name to generate the model. Follow
these steps:

```sh
lb4 model
? Model class name: todo

Let's add a property to Todo
Enter an empty property name when done

? Enter the property name: id
? Property type: number
? Is ID field? Yes
? Required?: No
? Default value [leave blank for none]:

Let's add another property to Todo
Enter an empty property name when done

? Enter the property name: title
? Property type: string
? Required?: Yes
? Default value [leave blank for none]:

Let's add another property to Todo
Enter an empty property name when done

? Enter the property name: desc
? Property type: string
? Required?: No
? Default value [leave blank for none]:

Let's add another property to Todo
Enter an empty property name when done

? Enter the property name: isComplete
? Property type: boolean
? Required?: No
? Default value [leave blank for none]:

Let's add another property to Todo
Enter an empty property name when done

? Enter the property name:

   create src/models/test.model.ts
   update src/models/index.ts

Model todo was created in src/models/
```

Now that we have our model, it's time to add a
[datasource](todo-tutorial-datasource.md) so we can perform real CRUD
operations!

### Navigation

Previous step: [Create your app scaffolding](todo-tutorial-scaffolding.md)

Next step: [Add a datasource](todo-tutorial-datasource.md)
