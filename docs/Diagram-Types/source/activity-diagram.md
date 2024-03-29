[<-Diagram Types](../diagram-types.md)

# Activity Diagram

![Activity Diagram](activity-diagram/activity-diagram.png)

Source code:
```plantuml
@startuml
skinparam shadowing false

title Activity Diagram Example\n

skinparam activity {
    StartColor limegreen
    EndColor darkblue
    BackgroundColor #d4de5e
    BorderColor #5e94de
    ArrowColor black
}
skinparam activityDiamond {
    BackgroundColor #5ede68
    BorderColor #5e94de
    fontSize 16
}

start
:choose diagram type to suit 
message and audience;
:choose example diagram
and copy code;

while (Is diagram finished?) is (not finished)
    :update diagram code;
    :render and review diagram;
endwhile (finished)

:publish diagram;

stop

@enduml
```