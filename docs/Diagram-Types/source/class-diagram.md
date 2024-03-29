[<-Diagram Types](../diagram-types.md)

# Class Diagram

![Class Diagram](class-diagram/class-diagram.png)

Source code:
```plantuml
@startuml
skinparam shadowing false

title Class Diagram Example

skinparam class {
    BackgroundColor #94de5e
    ArrowColor #darkblue
    BorderColor black
}

class Vehicle {
	speed
    direction
	make
    model
	run()
}
class Car {
    driver_name
    road
	run()
}
class Plane {
    pilot_name
    altitude
	run()
}
class Ship {
    captain_name
    ocean
	run()
}
Vehicle <|-- Car
Vehicle <|-- Plane : inherits
Vehicle <|-- Ship

legend 
    <size:18>Key</size>
    |<#94de5e> Class |
endlegend
@enduml
```