# Diagram Features

[<-Home](../README.md)

## Contents
[Title](#title)<br>
[Header](#header)<br>
[Footer](#footer)<br>
[Note](#note)<br>

<a name="title"/>

## Title

```plantuml
@startuml
title This is a Title
() " " as u1
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
() " " as u1
@enduml
```

![Header](header.png)

<a name="footer"/>

## Footer

```plantuml
@startuml
() " " as u1
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