---
Date: 2022-08-12
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Type/Meta", "#Topic/Obsidian"]
Alias: ["About"]
---

# ABOUT

> About this vault.

[TOC]

## Overview

This vault is a template vault serving the purpose of housing my commonly used settings for [Obsidian](https://obsidian.md).

## Setup

The setup has four main components:

- Settings, Configuration, and Plugins
- Folder Structure
- Tag Structure
- Content

### Settings, Configuration, and Plugins

### Folder Structure

Based off of [[Tiago Forte]]'s [[PARA Method]].

### Tag Structure

```mermaid
flowchart TB
	subgraph Type
	Folder[Folder]
	MOC[MOC]
	Ref[Reference]
	Slip[Slipbox]
	Daily[DailyNote]
	Person[Person]
	Meta[Meta]
	Readme[Readme]
	Tool[Tool]
	Code[Code]
	Code --> Bash[Bash]
	Code --> VBA[VBA]
	Code --> GHA[GHA]
	Code --> PWSH[PowerShell]
	Code --> MISC[etc.]
	end
	
	subgraph Topic
	Dev[Dev]
	Dev --> Linux[Linux]
	Dev --> Code2[Code]
	Dev --> CLI[CLI]
	Dev --> etc[etc.]
	Data[Data] --> DB[Database]
	Data --> D
	PKM[PKM] --> Obsidian[Obsidian]
	end
```



***

## Appendix: Links and References

***

Jimmy Briggs <jimmy.briggs@jimbrig.com> | 2022