---
date: 2016-03-09T00:11:02+01:00
title: Getting started
weight: 20
---

## Installation

### Installing Laravel CRUD Generator

```
$ php 
```


### Usage
After downloading this package open the terminal and  use this command line in your project root :
 ```
 php artisan admin:generate:all --sourceType=json --config="sample.json" --force=true
 ```
 - sourceType: Type of input ```json```,```db ```
 - config: Path of config file, if type of source type is a ```json```
 - force: Generate the entity strongly after deleting the old entity
