# Styles

* [Home](../README.md)

## Contents
[Default](#default)<br>
[Monochrome](#monochrome)<br>
[Reverse Monochrome](#reverse_monochrome)<br>
[Handwritten](#handwritten)<br>
[Monochrome Handwritten](#monochrome_handwritten)<br>
[No Shadow](#no_shadow)<br>

<a name="default"/>

## Default

```plantuml
@startuml
' Default style
() " " as u1
() " " as u2
() " " as u3
u1 -- u2
u1 - u3
@enduml
```

![Diagram layout without hidden lines](default.png)

<a name="monochrome"/>

## Monochrome

```plantuml
@startuml
' Monochrome style:
skinparam monochrome true
() " " as u1
() " " as u2
() " " as u3
u1 -- u2
u1 - u3
@enduml
```
![Diagram layout without hidden lines](monochrome.png)

<a name="reverse_monochrome"/>

## Reverse Monochrome

```plantuml
@startuml
' Reverse monochrome style:
skinparam monochrome reverse
() " " as u1
() " " as u2
() " " as u3
u1 -- u2
u1 - u3
@enduml
```

![Diagram layout without hidden lines](reverse-monochrome.png)

<a name="handwritten"/>

## Handwritten

Note: can combine handwritten with other styles such as monochrome

```plantuml
@startuml
' Handwritten style:
skinparam handwritten true
() " " as u1
() " " as u2
() " " as u3
u1 -- u2
u1 - u3
@enduml
```

![Diagram layout without hidden lines](handwritten.png)

<a name="monochrome_handwritten"/>

## Monochrome Handwritten

```plantuml
@startuml
' Monochrome Handwritten style:
skinparam handwritten true
skinparam monochrome true
() " " as u1
() " " as u2
() " " as u3
u1 -- u2
u1 - u3
@enduml
```

![Diagram layout without hidden lines](monochrome-handwritten.png)

<a name="no_shadow"/>

## No Shadow

Note: can combine no shadow with other styles

```plantuml
@startuml
' No shadow style:
skinparam shadowing false
() " " as u1
() " " as u2
() " " as u3
u1 -- u2
u1 - u3
@enduml
```

![Diagram layout without hidden lines](no-shadow.png)