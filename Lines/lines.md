# Lines

[<-Home](../README.md)

## Contents
[Vertical Line](#vertical_line)<br>
[Vertical Dashed Line](#vertical_dashed_line)<br>
[Horizontal Line](#horizontal_line)<br>

<a name="vertical_line"/>

## Vertical Line

Double dash

```plantuml
@startuml
() " " as u1
() " " as u2
u1 -- u2
@enduml
```

![Vertical Line](vertical-line.png)

<a name="vertical_dashed_line"/>

## Vertical Dashed Line

Double dot or *dashed* keyword in square brackets

```plantuml
@startuml
() " " as u1
() " " as u2
() " " as u3
u1 .. u2
u2 -[dashed]- u3
@enduml
```

![Vertical Line](vertical-dashed-line.png)

<a name="horizontal_line"/>


## Horizontal Line

Single dash

```plantuml
@startuml
() " " as u1
() " " as u2
u1 - u2
@enduml
```

![Horizontal Line](horizontal-line.png)