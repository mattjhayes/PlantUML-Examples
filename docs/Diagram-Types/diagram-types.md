# Diagram Types

[<-Home](../../README.md)

PlantUML auto-detects the diagram type based on the first unique item in the code

## Contents
[Sequence Diagram](#sequence-diagram)<br>
[Mind Map](#mindmap-diagram)<br>
[Mind Map of Tasks](#mindmap-diagram-tasks)<br>
[Deployment Diagrams](#deployment-diagrams)<br>
[Component Diagrams](#component-diagrams)<br>
[C4 Model Diagrams](../Examples/README.md#c4-model)<br>
[Use Case Diagram](#use-case-diagram)<br>
[Class Diagram](#class-diagram)<br>
[Activity Diagram](#activity-diagram)<br>

UNDER CONSTRUCTION

<a name="sequence-diagram"/>

## Sequence Diagram

Sequence diagrams present ordered events that occur between participants (actors) over time (which runs top-to-bottom)

Here is a simple example:

![Sequence Simple](sequence-simple.png)

```plantuml
@startuml
title Alice and Bob do a 3-Way TCP Handshake

skinparam ParticipantBackgroundColor SkyBlue
skinparam ParticipantBorderColor Black

' Set default colours for the horizontal arrows and vertical traces: 
skinparam sequence {
    ArrowColor blue
    LifeLineBorderColor black
}

Alice -> Bob: SYN
Bob --> Alice: SYN+ACK
Alice -> Bob: ACK

@enduml
```

There are multiple types of participant that can be used to trigger a sequence diagram, as per the types in the example below:

![Sequence Participants](sequence-participants.png)

```plantuml
@startuml
title Sequence Participants

' Set colors:
skinparam ParticipantBackgroundColor skyblue
skinparam ParticipantBorderColor black
skinparam ArrowColor darkblue
skinparam ActorBorderColor black
skinparam ActorBackgroundColor skyblue
skinparam BoundaryBorderColor black
skinparam BoundaryBackgroundColor skyblue
skinparam ControlBorderColor black
skinparam ControlBackgroundColor skyblue
skinparam EntityBorderColor black
skinparam EntityBackgroundColor skyblue
skinparam DatabaseBorderColor black
skinparam DatabaseBackgroundColor skyblue
skinparam CollectionsBorderColor black
skinparam CollectionsBackgroundColor skyblue

skinparam Sequence {
    LifelineBorderColor gray
}

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

The order that that participants is declared determines their order left to right in the diagram, and the order of the events is the order top to bottom

Here is the same diagram, but with simpler set-up code, thanks to use of a theme:

![Sequence Participants](sequence-participants-theme.png)

```plantuml
@startuml
!theme bluegray
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


Another example showing setting colours etc:

![Sequence Another Example](sequence-another-example.png)

```plantuml
@startuml

Title Another Sequence Diagram Example

skinparam ParticipantBackgroundColor SkyBlue
skinparam ParticipantBorderColor Black

' Set default colours for the horizontal arrows and vertical traces: 
skinparam sequence {
    ArrowColor blue
    LifeLineBorderColor black
}

' disable the bottom boxes for aesthetic reasons:
hide footbox 

' Set default colors for notes:
skinparam NoteBackgroundColor Yellow
skinparam NoteBorderColor black

' Participants:
participant “Alice\nin\nWonderland” as alice
participant “Bob\n\n” as bob
participant “Mad\nHatter\n” as hatter

alice -> bob: what this means
note right: Written by Lewis Carroll

bob -[#red]> hatter: this arrow is red

hatter -[#black]> alice: This is all\nnonsense!
@enduml
```

## Mind Map Diagram

Mind map diagrams are a great way to quickly break a problem or concept down into smaller parts.

Here is a simple example:

![Mind Map Simple](mindmap.png)

```plantuml
@startmindmap
skinparam ArrowColor DarkGrey
<style>
mindmapDiagram {
  node {
    Padding 15
    Margin 15
    BackGroundColor YellowGreen
    FontColor DarkSlateGrey
    LineColor white
    LineThickness 1.0
    MaximumWidth 180
  }
  rootNode {
    Padding 15
    Margin 15
    BackGroundColor DeepSkyBlue
    FontColor DarkSlateGrey
    FontSize 18
    LineColor DodgerBlue
    LineThickness 1.0
  }
  leafNode {
    Padding 15
    Margin 15
    BackGroundColor Thistle
    FontColor DarkSlateGrey
    FontSize 15
    LineColor Plum
    LineThickness 1.0
  }
}
</style>
* World
 * Continents
  * North America
   * Canada
   * United States
   * Mexico
  * Antarctica
   * Antarctica
  * Others TBD
 * Oceans
  * **Pacific**. Largest Ocean
  * Atlantic
  * Others TBD

@endmindmap
```

<a name="mindmap-diagram-tasks"/>

## Mind Map Diagram of Tasks

Here we create a Mind Map to track tasks, with visual tags for urgent and completed:

![Mind Map Simple](mind_map_tasks.png)

```plantuml
@startmindmap
skinparam ArrowColor DarkGrey
<style>
mindmapDiagram {
  node {
    Padding 15
    Margin 15
    BackGroundColor YellowGreen
    FontColor DarkSlateGrey
    LineColor white
    LineThickness 1.0
    MaximumWidth 180
  }
  rootNode {
    Padding 15
    Margin 15
    BackGroundColor DeepSkyBlue
    FontColor DarkSlateGrey
    FontSize 18
    LineColor DodgerBlue
    LineThickness 1.0
  }
  leafNode {
    Padding 15
    Margin 15
    BackGroundColor Thistle
    FontColor DarkSlateGrey
    FontSize 15
    LineColor Plum
    LineThickness 1.0
  }
  .completed {
    BackgroundColor lightslategrey
    LineColor limegreen
    FontStyle italic
    LineThickness 2.0
  }
  .urgent {
    BackgroundColor orangered
    LineColor yellow
    FontStyle bold
    LineThickness 2.0
  }
}
</style>
* Documentation
** PlantUML Examples
*** Mind Map Example 1 <<completed>>
*** Mind Map Task Example <<urgent>>
*** Another Mind Map Example
** Other Task Group
*** Another Task

@endmindmap
```

<a name="deployment-diagrams"/>

## Deployment Diagrams

This isn't strictly a UML Deployment Diagram, but is similar:

![Deployment-Like Diagram](source/deployment-like-diagram/deployment-like-diagram.png)
[source code](source/deployment-like-diagram.md)

<a name="component-diagrams"/>

## Component Diagrams

TBD

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

<a name="mindmap-diagram"/>