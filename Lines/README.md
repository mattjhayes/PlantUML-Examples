# Lines

[<-Home](../README.md)

## Contents
[Vertical Line](#vertical_line)<br>
[Vertical Dashed Line](#vertical_dashed_line)<br>
[Horizontal Line](#horizontal_line)<br>
[Line Color](#line_color)<br>
[Line Notes](#line_notes)<br>

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

<a name="line_color"/>

## Line Color

Specify line color in square brackets in the line characters:

```plantuml
@startuml
skinparam interface {
	BorderColor black
	BackgroundColor white
}
() " " as u1
() " " as u2
u1 -[#blue] u2
u1 -[#green]-> u2
u1 <-[#mediumvioletred]-> u2
@enduml
```

![Line Color](line-color.png)

To change line color for *all* lines, use *skinparam ArrowColor*:

```plantuml
@startuml
skinparam interface {
	BorderColor black
	BackgroundColor white
}

' Use this to set color on all lines:
skinparam ArrowColor blue

() " " as u1
() " " as u2
u1 - u2
u1 --> u2
u1 <--> u2
@enduml
```

![Line Color all Lines](line-color-change-default.png)

<a name="line_notes"/>

## Line Notes

Add note for line after a colon:

```plantuml
@startuml
skinparam interface {
	BorderColor black
	BackgroundColor white
}
() " " as u1
() " " as u2
() " " as u3
u1 -[#blue] u2 : Blue Line
u2 -[#green]-> u3 : Green Line
u3 <-[#red]-> u1 : Red Line
@enduml
```

![Line Color](line-notes.png)