# Diagram Features

[<-Home](../README.md)

## Contents
[Title](#title)<br>
[Header](#header)<br>
[Footer](#footer)<br>
[Note](#note)<br>
[Caption](#caption)<br>
[Legend](#legend)<br>

<a name="title"/>

## Title

```plantuml
@startuml
title This is a Title
rectangle {
    () " " as u1
    component foo
}
@enduml
```

![Title](title.png)

<a name="header"/>

## Header

```plantuml
@startuml
header
<font color=red>Notice:</font>
This is a header
endheader
rectangle {
    () " " as u1
    component foo
}
@enduml
```

![Header](header.png)

<a name="footer"/>

## Footer

```plantuml
@startuml
rectangle {
    () " " as u1
    component foo
}
center footer This is an example footer
@enduml
```

![Footer](footer.png)

<a name="note"/>

## Note

Add comments (notes) to your diagram

```plantuml
@startuml
() " " as u1
note as n1
    Add notes to your diagrams
end note
n1 -left- u1
@enduml
```

![Note](note.png)

<a name="caption"/>

## Caption

Add caption to your diagram

```plantuml
@startuml
rectangle {
    () " " as u1
    component foo
}
caption Figure 1
@enduml
```

![Caption](caption.png)

<a name="legend"/>

## Legend

Add legend to your diagram

```plantuml
@startuml
() " " as u1
legend right
  Enter legend
  info here
endlegend
@enduml
```

![Legend](legend.png)