# Other Layout Tricks

[<-Home](../README.md)

Here are some other tricks for fixing layout issues that may help.

## Change Component Order

Let's assume we want Box 1 on the left. We used the 'right' tag, however this isn't working:

```plantuml
@startuml

skinparam monochrome true
skinparam handwritten true

title Wrong layout

rectangle "Grouping" {
    rectangle "Box 1" {
        rectangle "Apples"
    }
    rectangle "Box 2" {
        rectangle "Pears"
    }
}

Apples -right-> Pears

@enduml
```

![wrong_way_around](wrong_way_around.png)

A fix is to reverse the order of the components in the code:

```plantuml
@startuml

skinparam monochrome true
skinparam handwritten true

title Layout fixed by Changing Component Order

rectangle "Grouping" {
    rectangle "Box 2" {
        rectangle "Pears"
    }
    rectangle "Box 1" {
        rectangle "Apples"
    }
}

Apples -right-> Pears

@enduml
```

![wrong_order](reversed_order.png)