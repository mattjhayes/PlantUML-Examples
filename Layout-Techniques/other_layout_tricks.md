# Other Layout Tricks

[<-Home](../README.md)

Use hidden lines as a work-around to give hints to PlantUML as to how to lay out the diagram

## Change Component Order

This isn't working, Class 1 should be on left:

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