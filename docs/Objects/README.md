# Objects

[<-Home](../../README.md)

## Contents
[Component](#component)<br>
[Interface](#interface)<br>
[Rectangle](#rectangle)<br>
[Actor](#actor)<br>
[Artifact](#artifact)<br>

<a name="component"/>

## Component

```plantuml
@startuml
component [component] as myComponent
@enduml
```

![Component](component.png)

<a name="interface"/>

## Interface

```plantuml
@startuml
() "This is an interface" as myInterface
@enduml
```

![Interface](interface.png)

<a name="rectangle"/>

## Rectangle

```plantuml
@startuml
rectangle "This is a Rectangle"
@enduml
```

![Rectangle](rectangle.png)

Rectangles can group other objects:

```plantuml
@startuml
rectangle "This is a Rectangle with things in it" {
    () " " as o1
    () " " as o2
    :Actor:
    [Component]
}
@enduml
```
![Rectangle](rectangle2.png)

<a name="actor"/>

## Actor

Note that if you use keyword 'actor', it will assume format of a sequence diagram. Use colons around actor name instead.

```plantuml
@startuml
:"Alice":
@enduml
```

![Actor](actor.png)

Can change colour etc with skinparams:

```plantuml
@startuml
skinparam ActorBorderColor black
skinparam ActorBackgroundColor white
:"Alice":
actor "Bob"
@enduml
```

![Actor](actor2.png)

<a name="artifact"/>

## Artifact

An artifact in UML is generally a file

```plantuml
@startuml
artifact "config.json"
@enduml
```

![Actor](artifact.png)


