# Other Layout Tricks

[<-Home](../../README.md)

Here are some other tricks, if you've already tried [hidden lines](hidden-lines.md), for fixing layout issues. Your mileage may vary...

## Change Component Order

Let's assume we want Box 1 on the left. We used the 'right' tag, however this isn't working:

```plantuml
@startuml

skinparam monochrome true
skinparam handwritten true

title Wrong layout

rectangle "Grouping" {
    rectangle "Box 1" {
        rectangle "Apples"
    }
    rectangle "Box 2" {
        rectangle "Pears"
    }
}

Apples -right-> Pears

@enduml
```

![wrong_way_around](wrong_way_around.png)

A fix is to reverse the order of the components in the code:

```plantuml
@startuml

skinparam monochrome true
skinparam handwritten true

title Layout fixed by Changing Component Order

rectangle "Grouping" {
    rectangle "Box 2" {
        rectangle "Pears"
    }
    rectangle "Box 1" {
        rectangle "Apples"
    }
}

Apples -right-> Pears

@enduml
```

![fixed_order](reversed_order.png)

## Left to Right

TBD

```plantuml
@startuml
left to right direction
```

## Together

TBD

```plantuml
@startuml
together {
    rectangle "Box 1" as box_1
    rectangle "Box 2" as box_2
}
```

## Longer Lines

Can try extending lengths of lines by adding dashes, examples starting with normal length lines:

```plantuml
@startuml

title Ugly Layout

skinparam monochrome true

component [component 1] as myComponent
component [component 2] as myComponent2
component [component 3] as myComponent3
component [component 4] as myComponent4

myComponent -> myComponent2
myComponent2 -> myComponent3
myComponent2 -> myComponent4
myComponent -> myComponent4

@enduml
```

![standard_lines](standard_lines.png)

Add dashes to lines to make them longer to change layout:

```plantuml
@startuml

title Possibly Better Layout

skinparam monochrome true

component [component 1] as myComponent
component [component 2] as myComponent2
component [component 3] as myComponent3
component [component 4] as myComponent4

myComponent -> myComponent2
myComponent2 ----> myComponent3
myComponent2 ---> myComponent4
myComponent -> myComponent4

@enduml
```

![longer_lines](longer_lines.png)

## No Rank

TBD, see https://stackoverflow.com/questions/48712801/how-to-correct-plantuml-line-path/61795202#61795202

## Transparent Nodes

TBD, see https://stackoverflow.com/questions/48712801/how-to-correct-plantuml-line-path/48735216#48735216

## Orthogonal Mode

TBD, see https://stackoverflow.com/questions/48712801/how-to-correct-plantuml-line-path/48735216#48735216

