# Diagram Types

[<-Home](../../README.md)

PlantUML auto-detects the diagram type based on the first unique item in the code

## Contents

[Activity Diagram](#activity-diagram)<br>
[C4 Model Diagrams](../Examples/README.md#c4-model)<br>
[Class Diagram](#class-diagram)<br>
[Component Diagrams](#component-diagrams)<br>
[Deployment Diagrams](#deployment-diagrams)<br>
[Gantt Charts](#gantt-charts)<br>
[Mind Map](#mindmap-diagram)<br>
[Mind Map of Tasks](#mindmap-diagram-tasks)<br>
[Sequence Diagrams](#sequence-diagram)<br>
[Use Case Diagram](#use-case-diagram)<br>

<a name="activity-diagram"/>

## Activity Diagram

Auto detect activity diagram type by lines that start with : and end with ;

![Activity Diagram](source/activity-diagram/activity-diagram.png)

[(source PlantUML code)](source/activity-diagram.md)

<a name="class-diagram"/>

## Class Diagram

Auto detect class diagram type by use of line type:
* <|--
* *--
* o--
* ..
* --

![Class Diagram](source/class-diagram/class-diagram.png)

[(source PlantUML code)](source/class-diagram.md)

<a name="component-diagrams"/>

## Component Diagrams

TBD

<a name="deployment-diagrams"/>

## Deployment Diagrams

This isn't strictly a UML Deployment Diagram, but is similar:

![Deployment-Like Diagram](source/deployment-like-diagram/deployment-like-diagram.png)

[(source PlantUML code)](source/deployment-like-diagram.md)

<a name="gantt-charts"/>

## Gantt Charts

Example Gantt chart:

![Gantt Chart](source/gantt/gantt.png)

[(source PlantUML code)](source/gantt.md)

<a name="mindmap-diagram"/>

## Mind Map Diagram

Mind map diagrams are a great way to quickly break a problem or concept down into smaller parts.

Here is a simple example:

![Mind Map Simple](source/mindmap/mindmap.png)

[(source PlantUML code)](source/mindmap.md)

<a name="mindmap-diagram-tasks"/>

## Mind Map Diagram of Tasks

Here we create a Mind Map to track tasks, with visual tags for urgent and completed:

![Mind Map of Tasks ](source/mindmap-tasks/mindmap-tasks.png)

[(source PlantUML code)](source/mindmap-tasks.md)

<a name="sequence-diagram"/>

## Sequence Diagrams

Sequence diagrams present ordered events that occur between participants (actors) over time (which runs top-to-bottom)

Here is a simple example:

![Sequence Simple](source/sequence-simple/sequence-simple.png)

[(source PlantUML code)](source/sequence-simple.md)

There are multiple types of participant that can be used to trigger a sequence diagram, as per the types in the example below:

![Sequence Participants](source/sequence-participants/sequence-participants.png)

[(source PlantUML code)](source/sequence-participants.md)

The order that that participants is declared determines their order left to right in the diagram, and the order of the events is the order top to bottom

Here is the same diagram, but with simpler set-up code, thanks to use of a theme:

![Sequence Participants](source/sequence-participants-theme/sequence-participants-theme.png)

[(source PlantUML code)](source/sequence-participants-theme.md)

Another example showing setting colours etc:

![Sequence Another Example](source/sequence-another-example/sequence-another-example.png)

[(source PlantUML code)](source/sequence-another-example.md)

<a name="use-case-diagram"/>

## Use Case Diagram

TBD

Auto detect use case diagram type by TBD

