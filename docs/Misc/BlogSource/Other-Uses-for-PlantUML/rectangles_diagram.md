```plantuml
@startuml

skinparam handwritten true
skinparam RectangleBackgroundColor white
skinparam NoteBackgroundColor APPLICATION
skinparam NoteBorderColor black

rectangle Legacy_System {
    rectangle "Legacy App" as legapp
}
rectangle Reporting {
    rectangle "New Reports App" as livecharts
}
rectangle "Customer Systems" {
    rectangle "CRM (Refreshed)" as crmRefresh #Gold
}
rectangle Compliance {
    rectangle "Compliance Engine" as ce
}
rectangle Infrastructure {
    rectangle "Compute/storage" as hyperconverged
    rectangle "LB" as lb
}
rectangle "System of Record" {
    rectangle "SoR App and DB" as sor
}
livecharts -[#black]-> crmRefresh
ce -[#black]-> sor
legapp -[#black]-> hyperconverged
sor -[#black]-> hyperconverged
crmRefresh -[#black]-> hyperconverged
crmRefresh -[#black]-> lb
@enduml
```