# Diagram Types

[<-Home](../../README.md)

PlantUML auto-detects the diagram type based on the first unique item in the code

## Contents
[Sequence Diagram](#sequence-diagram)<br>
[Use Case Diagram](#use-case-diagram)<br>
[Class Diagram](#class-diagram)<br>
[Activity Diagram](#activity-diagram)<br>

UNDER CONSTRUCTION

<a name="sequence-diagram"/>

## Sequence Diagram

Sequence diagrams present ordered events that occur between participants (actors) over time (which runs top-to-bottom)

Here is a simple example:

```plantuml
@startuml
title Alice and Bob do a 3-Way TCP Handshake
Alice -> Bob: SYN
Bob --> Alice: SYN+ACK
Alice -> Bob: ACK
@enduml
```

![Sequence Simple](sequence-simple.png)

There are multiple types of participant that can be used to trigger a sequence diagram, as per the types in the example below:

```plantuml
@startuml
title Sequence Participants
' Specify the participants left to right:
participant Participant
actor Actor
boundary Boundary
control Control
entity Entity
database Database
collections Collections
' Specify the events (in order):
group authentication
    Actor -> Boundary: Request Logon
    Boundary -> Actor: Provide Credentials
    Actor -> Boundary: username: actor, password: example123
    Boundary -> Actor: Accepted
end
Actor -> Boundary: List all options
Boundary -> Control: List all options (actor)
Control -> Entity: List all options (actor)
@enduml
```

![Sequence Simple](sequence-participants.png)

The order that that participants is declared determines their order left to right in the diagram, and the order of the events is the order top to bottom

<a name="use-case-diagram"/>

## Use Case Diagram

TBD

Auto detect use case diagram type by TBD

<a name="class-diagram"/>

## Class Diagram

TBD

Auto detect class diagram type by use of line type:
* <|--
* *--
* o--
* ..
* --

<a name="activity-diagram"/>

## Activity Diagram

TBD

Auto detect activity diagram type by lines that start with : and end with ;

