# Other Layout Tricks

[<-Home](../README.md)

Here are some other tricks for fixing layout issues that may help.

## Change Component Order

Let's assume we want Class 1 on the left. We used the 'right' tag, however this isn't working:

```plantuml
@startuml

skinparam monochrome true
skinparam handwritten true

title Wrong layout

rectangle "Application" {
    rectangle "Class 1" {
        rectangle "function" as fx1
    }
    rectangle "Class 2" {
        rectangle "internal function" as fx2
    }
}

fx1 -right-> fx2

@enduml
```

![wrong_way_around](wrong_way_around.png)

A fix is to reverse the order of the components in the code:

```plantuml
@startuml

skinparam monochrome true
skinparam handwritten true

title Layout fixed by changing order

rectangle "Application" {
    rectangle "Class 2" {
        rectangle "internal function" as fx1
    }
    rectangle "Class 1" {
        rectangle "function" as fx2
    }
}

fx1 <-left- fx2

@enduml
```

![wrong_order](reversed_order.png)