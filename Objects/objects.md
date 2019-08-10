# Objects

[<-Home](../README.md)

## Contents
[Component](#component)<br>

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

<a name="actor"/>

## Actor

Note that if you use keyword 'actor', it will assume format of a sequence diagram. Use colons around actor name instead.

```plantuml
@startuml
:"Alice":
@enduml
```

![Actor](actor.png)



