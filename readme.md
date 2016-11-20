
 ![Master Build status](https://tfsaggregator.visualstudio.com/_apis/public/build/definitions/2e747373-c780-4b2c-823d-98a3fd2b4e99/6/badge)
![Develop Build status](https://tfsaggregator.visualstudio.com/_apis/public/build/definitions/2e747373-c780-4b2c-823d-98a3fd2b4e99/1/badge)

This server side plugin, for TFS 2013 update 2 up to TFS 2017 RTM, enables running custom script when Work Items change,
allowing dynamic calculation of field values in TFS and more. (For example: Dev work + Test Work = Total Work).

# Changelog

## What's new in v2.2
 * Support for TFS 2017
 * Support for TFS 2017
 * Macro snippets and Functions for Rules and make code more modular
 * Ability to specify server URL
 * Support for multiple workitem Ids in Console application (issue [#178](https://github.com/tfsaggregator/tfsaggregator/issues/178))
 * Ability to Send email from Rules
 * Migrated CI build from AppVeyor to VSTS
 * Use of GitVersion to manage [Semantic Versioning](http://semver.org/)

## What's new in v2.1.1
 * Fixes important bug causing very high CPU usage (see [#160](https://github.com/tfsaggregator/tfsaggregator/issues/160)).

## What's new in v2.1

 * Support for TFS 2015.2, TFS 2015.2.1 and TFS 2015.3
 * Extended logging in debug version
 * Ability to override base Uri of the aggregator
 * Improvements in the setup
 * Adds `PreviousRevision`/`NextRevision` properties to Work Items to navigate history
 * Adds `Uri` field to Work Items
 * Removed policyscope on Workitem template GUID and revision (didn't work anyway)

## What's new in v2

 * A 'real' Scripting language (C#, VB, Powershell)
 * Scoping allows select which rules apply to which Team Project
 * Enhanced filtering to trigger rules when conditions are met
 * Console application to quickly test new rules
 * Richer logging
 * Test harness and modularity to ease adding new features
 * Create new Work Items and Links using rules
 * and more...

## Example Uses

 - Update the state of a Bug, PBI (or any parent) to "In Progress" when a child gets moved to "In Progress"
 - Update the state of a Bug, PBI (or any parent) to "Done" when all children get moved to "Done" or "Removed"
 - Update the "Work Remaining" on a Bug, PBI, etc with the sum of all the Task's "Work Remaining".
 - Update the "Work Remaining" on a Sprint with the sum of all the "Work Remaining" of its grandchildren (i.e. tasks of the PBIs and Bugs in the Sprint).
 - Sum up totals on a single work item (i.e. Dev Estimate + Test Estimate = Total Estimate)
 - Create new work items
 - Create new work item links

Documentation
================================================

The complete documentation is available on the [project's Wiki](https://github.com/tfsaggregator/tfsaggregator/wiki).
A snaphost is available when you install TFS Aggregator using the MSI.

# Contributing to the Project

Please read the [Contributing](CONTRIBUTING.md) document.