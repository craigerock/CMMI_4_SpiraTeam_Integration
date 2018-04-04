# CMMI_4_SpiraTeam_Integration
This is a Process template for TFS 2017 that is compatible with SpiraTeam integration
All the Microsoft Test processes have been removed.  Instead this template serves to separate Developers from Testers by TFS permissions.  Testers do their work on SpiraTeam mostly and Developers do all their work with TFS.  More details later.  If there are any questions, please create an issue.
The ISO 62304 standard was kept in mind when editing this process template.  

-Developers are denied certain transition states without Administrator action.  
-The proper working of this template will also require the appropriate configuration of TFS permissions.
-Bug has been renamed Problem
-Epic has been removed
-Feature has been changed into Change Request so that on the Work Backlog, we see a new order, first Change Request, then Requirement, then Tasks.  Tasks and Problems show up on the Kanban board view with their Requirement in the same row.  For us this made sense, since Requirements came out of Change Requests that have to be approved first.
-Fields on some forms have been customized.

Readme not yet finished ...
