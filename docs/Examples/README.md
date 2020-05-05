# Assorted Example Diagrams
Assorted examples of diagrams I've used in blog posts:

[<-Home](../../README.md)

## Contents
[IT Arch - Coupling](#itarch-coupling)<br>

<a name="itarch-coupling"/>

## IT Architecture – A Discussion on Coupling

A couple of diagrams from post [IT Architecture – A Discussion on Coupling](https://mattjhayes.com/2020/04/18/it-architecture-a-discussion-on-coupling/)

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

