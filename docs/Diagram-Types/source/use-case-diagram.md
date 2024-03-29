[<-Diagram Types](../diagram-types.md)

# Use Case Diagram

![Use Case Diagram](use-case-diagram/use-case-diagram.png)

Source code:
```plantuml
@startuml

title Use Case Diagram Example

skinparam shadowing false
skinparam actor {
	BorderColor black
	BackgroundColor white
}
skinparam usecase {
    BackgroundColor #94de5e
    BorderColor DarkSlateGray
    ArrowColor Olive
}
skinparam noteBorderColor black

actor Dev as dev
actor "Business\nAnalyst" as ba
(Diagram as Code\nin Wiki) as wiki
note right: Easy to find\nand update
(Diagram as Code\nin Repo) as repo
(Traditional Diagram\non Fileshare) as trad
(Project code) as sourcecode

dev -> wiki: update\ndiagram\ncode
dev --> repo: update\ndiagram\ncode
dev -> trad
ba --> wiki: view\ndiagram
ba --> repo: view\ndiagram
sourcecode --> repo: autogenerate\ndiagram 

@enduml
```