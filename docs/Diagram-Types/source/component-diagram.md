[<-Diagram Types](../diagram-types.md)

# Component Diagram

![Component Diagram](component-diagram/component-diagram.png)

Source code:
```plantuml
@startuml

title Component Diagram Example

skinparam shadowing false
skinparam component {
	BorderColor black
	BackgroundColor #goldenrod
}
skinparam interface {
	BorderColor black
	BackgroundColor #5e94de
}
skinparam ArrowColor black
skinparam noteBorderColor black

component user_mgmt [
    User Management Service
]
component svc_book [
    Book Service
]
rectangle "Database" {
    component db_user [
        User Database
    ]
    component db_book [
        Book Database
    ]
}
() "book\ninterface" as if_book
note left: Need to make\nthis interface\nprivate
() "customer\ninterface" as if_cust

if_cust -> user_mgmt
user_mgmt --> if_book
if_book -> svc_book
svc_book -> db_book
user_mgmt -> db_user
db_user --[hidden]> db_book
@enduml
```