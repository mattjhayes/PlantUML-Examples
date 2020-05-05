# Assorted Example Diagrams
Assorted examples of diagrams I've used in blog posts:

[<-Home](../../README.md)

## Contents
[IT Arch - Coupling](#itarch-coupling)<br>

<a name="itarch-coupling"/>

## IT Architecture – A Discussion on Coupling

Here are a few example diagrams from post [IT Architecture – A Discussion on Coupling](https://mattjhayes.com/2020/04/18/it-architecture-a-discussion-on-coupling/)

```plantuml
@startuml
' Diagram on Decoupling for Coupling blog post

skinparam handwritten true
skinparam RectangleBackgroundColor white
skinparam NoteBackgroundColor APPLICATION
skinparam NoteBorderColor black

caption \nDecoupling via Intermediary

rectangle "Component 1" as cp1
note right of cp1: "<i>I don't know who I'm talking to\n<i>past the intermediary</i>"

rectangle "<i>Intermediary</i>" as im #Gold

rectangle "Component 2" as cp2
note right of cp2: "<i>I don't know who's talking to me\n<i>through the intermediary</i>"

cp1 -[#black]down-> im
im -[#black]down-> cp2

@enduml
```

![decoupling](decoupling.png)

A continuum:

```plantuml
@startuml

scale 800 width

skinparam handwritten true
skinparam RectangleBackgroundColor white
skinparam RectangleBorderColor white
skinparam nodesep 100
skinparam InterfaceBackgroundColor white
skinparam InterfaceBorderColor black
caption \n\n\nContinuum of Platform Coupling

rectangle "Extremely\nTightly\nCoupled" as tight #Coral
() "Version-Specific\nProprietary\nInterface" as vspi
() "Proprietary\nInterface" as pi
() "Open\nSource\nInterface" as osi
() "Open\nStandards\nInterface" as osi2
rectangle "Extremely\nLoosely\nCoupled" as loose #YellowGreen

tight <-right-vspi #black
vspi -right- pi #black
pi -right- osi #black
osi -right- osi2 #black
osi2 -right-> loose #black

@enduml
```

![platform_continuum](platform_continuum.png)

A component diagram:

```plantuml
@startuml
left to right direction

skinparam handwritten true
skinparam RectangleBackgroundColor red
skinparam ActorBorderColor black
skinparam ActorBackgroundColor white

caption Example of Cascading Failure in Tightly Coupling System

actor "Sad User" as user

rectangle "User Application\n(cascaded failure)" as user_app

rectangle "Component 1\n(cascaded failure)" as comp_1

together {
    rectangle "Component 2\n(original failure)" as comp_2
    rectangle "Component 3\n(working)" as comp_3 #LimeGreen
}

user -[#black]-> user_app
user_app -[#OrangeRed]-> comp_1 : tight\ncoupling
comp_1 -[#OrangeRed]-> comp_2 : tight\ncoupling
comp_1 -[#OrangeRed]-> comp_3 : tight\ncoupling
comp_2 .[#red]left.> comp_1 : failure\npropagation
comp_1 .[#red]left.> user_app : failure\npropagation
@enduml
```

![tight_coupling_cascading_failure](tight_coupling_cascading_failure.png)
