[<-Diagram Types](../diagram-types.md)

Gantt Chart Example:

![Gantt](gantt/gantt.png)

Source code:

```plantuml
@startgantt
<style>
ganttDiagram {
    unstartedTask {
        FontName Helvetica
        FontColor Black
        FontSize 12
        FontStyle bold
        BackGroundColor DeepSkyBlue
        LineColor DeepSkyBlue
    }
    task {
        FontName Helvetica
        FontColor Black
        FontSize 12
        FontStyle bold
        BackGroundColor DeepSkyBlue
        LineColor DeepSkyBlue
    }
    milestone {
        FontColor black
        FontSize 12
        FontStyle bold
        BackGroundColor yellow
        LineColor FireBrick
    }
    note {
        FontColor DarkGreen
        FontSize 10
        LineColor OrangeRed
    }
    arrow {
        FontName Helvetica
        FontColor red
        FontSize 18
        FontStyle bold
        BackGroundColor GreenYellow
        LineColor blue
        LineStyle 8.0;13.0
        LineThickness 3.0
    }
    separator {
        BackgroundColor OliveDrab
        LineStyle 8.0;3.0
        LineColor Gray
        LineThickness 1.0
        FontSize 16
        FontStyle bold
        FontColor White
        Margin 5
        Padding 6
    }
    timeline {
        BackgroundColor Snow
    }
    closed {
        BackgroundColor pink
        FontColor red
    }
}
</style>
projectscale weekly
Project starts the 1st of December 2023
' saturday are closed
' sunday are closed
2023/12/24 to 2024/01/12 are colored in grey

-- Design Stream --

[Document Requirements (BA)] as [design-reqs] lasts 7 days and is 100% completed
[Detailed Design Doc (Ben)] as [design-doc] lasts 60 days and is 40% completed
[Web Design (Sam)] as [design-ui] lasts 21 days and is 20% completed
[Design Sign-Off (Julia)] as [design-signoff] lasts 7 days and starts after [design-ui]'s end and is 0% completed
[design-signoff] starts after [design-doc]'s end
[Design Complete] as [design-complete] happens at [design-signoff]'s end

-- Testing Stream -- 

[Build Test Environment (Mario)] as [test-build] lasts 54 days and is 50% completed
[Test Env Shakedown (Testers)] as [test-shakedown] lasts 14 days and starts at [test-build]'s end and is 0% completed
[test-shakedown] starts at [design-complete]'s end 
[System Testing (Testers)] as [testing] lasts 28 days and starts at [test-shakedown]'s end and is 0% completed
[Testing Completed] happens at [testing]'s end

-- Prod Stream --
[Prod Build (DevOps Team)] as [prod-build] lasts 14 days and starts at [testing]'s end and is 0% completed
[Prod Built] happens at [prod-build]'s end
[Internal Pilot (PM, DevOps)] as [prod-internal-pilot] lasts 14 days and starts at [prod-build]'s end and is 0% completed
[Customer Pilot (Account Managers)] as [prod-customer-pilot] lasts 14 days and starts at [prod-internal-pilot]'s end and is 0% completed
[Internal Migration (PMs)] as [prod-internal-migrate] lasts 28 days and starts at [prod-internal-pilot]'s end and is 0% completed
[Customer Migration (PMs)] as [prod-customer-migrate] lasts 28 days and starts at [prod-customer-pilot]'s end and is 0% completed
[Old Decommission] as [decom] lasts 7 days and starts at [prod-customer-migrate]'s end and is 0% completed
[Project Completed] happens at [decom]'s end
@endgantt
```
