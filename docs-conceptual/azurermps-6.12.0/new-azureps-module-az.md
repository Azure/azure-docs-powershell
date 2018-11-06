---
title: Introducing the Azure PowerShell Az module
description: Introducing the new Azure PowerShell module Az, the replacement for the AzureRM module.
ms.date: 10/22/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
---
# Introducing the new Azure PowerShell Az module

Starting in November 2018, the Azure PowerShell `Az` module is available for full public preview.
This module is an improvement in the stability and portability of the old `AzureRM` module. It
offers feature parity and an easy migration path through familiar, but shorter, cmdlet names.

`Az` is built on the .NET Standard library, which means that it runs under both PowerShell 5.x on
Windows and PowerShell Core on any platform. Using .NET Standard allows us to unify the code base of Azure
PowerShell with minimal impact on users.

This is a new module, so the version has been reset. The first stable release will be 1.0.

## Upgrade to Az

It's recommended that users upgrade to the new `Az` module. To do so:

* [Uninstall the Azure PowerShell AzureRM module](/powershell/azure/uninstall-azurerm-ps)
* [Install the Azure PowerShell Az module](/powershell/azure/install-az-ps)
* Enable compatibility mode for AzureRM with `Enable-AzureRMAlias` while you become familiar with the new command set.

## Migrate existing scripts to Az

Major updates like this can be inconvenient. However, the `Az` module has a compatibility mode to
help you use existing scripts while you work on updates to the new syntax. Use the
`Enable-AzAlias` cmdlet to enable the `AzureRM` compatibility mode. This cmdlet defines
`AzureRM` cmdlet names as aliases for the new `Az` cmdlet names.

The new cmdlet names have also been designed to be easy to learn. Instead of using `AzureRM` in cmdlet names,
use `Az`. For most cmdlets, this should be the only change required. For example, the old command `New-AzureRMVM`
has become `New-AzVM`.

For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).

## The future of support for AzureRM

The existing `AzureRM` module enters maintenance mode when `Az` version 1.0 is released in December
2018. At that time, the `AzureRM` module will continue to receive important bug fixes. New features will only
be added to the `Az` module. To keep up with the latest Azure services and features, you should
switch to the `Az` module.