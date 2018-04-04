# CMMI_4_SpiraTeam_Integration
This is a Process template for TFS 2017.2 that is compatible with SpiraTeam 5.3.x integration.  These process templates will probably work with newer versions of TFS and SpiraTeam, with little or no changes.

Microsoft gives plenty of instructions on how to import a process template via Visual Studio into TFS so I won't cover that here.  Since there is already a CMMI process template in TFS you will need to give this one a different name.  Another practical tip is that these are all XML files that can be easily edited in your favorite XML editor (mine is Visual Studio Code).  Just be sure to follow the format already in these files and consult Microsoft documentation if you plan any major deviations from these templates.  TFS will validate your import, so you don't have to worry so much.  If it does not pass validation (on the TFS server) check the TFS log and try again.
Worse case, you can always go back to a default process template, and start again.

All the Microsoft Test work item types have been removed.  Instead this template serves to separate Developers from Testers by TFS permissions.  Testers do their work on SpiraTeam mostly and Developers do all their work with TFS.  More details later.  If there are any questions, please create an issue.

-The ISO 62304 standard was kept in mind when editing this process template and the software development environment is a modified Waterfall in that we plan, then code, then test, then release.

-Developers are denied certain transition states without Administrator action.  

-The proper working of this template will also require the appropriate configuration of TFS permissions.

-Bug has been renamed Problem

-Epic has been removed

-Feature has been changed into Change Request so that on the Work Backlog, we see a new order, first Change Request, then Requirement, then Tasks.  Tasks and Problems show up on the Kanban board view with their Requirement in the same row.  For us this made sense, since Requirements came out of Change Requests that have to be approved first.

-Fields on some forms have been customized.

-A TFS_Denied_Users group should be created in TFS and is supported by this template.  All non-administrator users are to be added to this group (i.e. actually the developer group) to deny certain state transitions to all developers such as Requirement = "Active to Closed" state transitions.  This ensures only the team leader (and administrator) can close a requirement, and so on.  It is important that TFS permissions (groups and users) are setup in TFS as an action in harmony with this process template, or lots of features in the template won't work.

(SpiraTeam integrates with TFS as mentioned before.  The synchronization of data to/from TFS is mostly configured on the SpiraTeam side, but works well with this template.  Requirements synchronize over from TFS to SpiraTeam.  Testers create Test Cases on these requirements in SpiraTeam.  When a test case fails a SpiraTeam Incident is created and synchronizes over to TFS as a new Problem Report.  The developer Resolves the Problem Report in TFS.  The Problem Report in Resolved state synchronizes back over to SpiraTeam where the testers re-test the problem and mark it as closed. The administrator oversees all this activity on both systems to ensure work is complete and traceability is maintained throughout the whole process.)

Readme not yet finished ...
