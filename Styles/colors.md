# Colors

[<-Home](../README.md)

List the colors with:

```plantuml
@startuml
colors
@enduml
```

Which gives something like this:

![Colors](colors.png)

Change the color of all objects of a particular type, use skinparam for the type, example:

```plantuml
@startuml
skinparam artifact {
	BorderColor black
	BackgroundColor lightskyblue
}
artifact "software project" as softproj
artifact "infrastructure config" as infra
@enduml
```

![skinparam](skinparam.png)

Change the color of a single item, specify color at end after a hash. Example:

```plantuml
@startuml
artifact "software project" as softproj #darkkhaki
@enduml
```

![single item](single_item_color.png)
