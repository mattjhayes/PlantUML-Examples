# Hidden Lines

Use hidden lines as a work-around to give hints to PlantUML as to how to lay out the diagram

## Without Hidden Lines

```plantuml
@startuml
skinparam monochrome true

component [component 1] as myComponent
component [component 2] as myComponent2
component [component 3] as myComponent3
component [component 4] as myComponent4

myComponent - myComponent2
myComponent2 --> myComponent3
myComponent2 --> myComponent4
myComponent - myComponent4

@enduml
```

![Diagram layout without hidden lines](no-hidden-lines.png)

## With Hidden Lines to align components 2 & 4

```plantuml
@startuml
skinparam monochrome true

component [component 1] as myComponent
component [component 2] as myComponent2
component [component 3] as myComponent3
component [component 4] as myComponent4

myComponent - myComponent2
myComponent2 --> myComponent3
myComponent2 --> myComponent4
myComponent - myComponent4

' Hidden line to help layout:
myComponent2 -[hidden]--> myComponent4

@enduml
```

![Diagram layout with hidden lines](hidden-lines.png)

## Types of Hidden Line

TBD