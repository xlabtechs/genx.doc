---
title: "Fields Config "
date: 2018-07-11T11:21:23+03:00
  weight = 17
---


## ID
```php
{
          "title": "Id",
          "name": "id",
          "dbType": {
            "type": "Integer",
            "primary": true
          },
          "viewType": {
            ....
 
          },
        ....
        },
```

##  Integer
```php
{
        
		"title": "Integer Value",
          "name": "int_value",
          "dbType": {
            "type": "Integer",
            ....
          },
          "viewType": {
            "type": "Integer"
          },
         ..........
        }
```
## double
```php
{
          "title": "Double Value",
          "name": "double_value",
          "dbType": {
            "type": "double",
          ...
          },
          "viewType": {
            "type": "decimal",
            ...
          },
          ...
        }
```
##  default
```php
{
        
		...
          "dbType": {
            "type": "...",
            "default": "default value"
          },
          "viewType": {
        ...
          },
         ..........
        }
```
##  foreign
 ```php
 	{
          "title": "field Name",
          "name": "field_id",
          "dbType": {
            "type": "Integer",
            "foreign": {
              "table": "related table name",
			  "field_view": "view field in related table",
             ...
            }
          },
          "viewType": {
            "type": "text"
          },
        .....
        }
  ```


## enum

  
 ```php
     {
       ....
          "dbType": {
            "type": "enum"
          },
          "viewType": {
              "type": "select",
            "enums": [
              {
                "label": "Label Value1",
                "value": "val1"
              },
              {
                "label": "Label Value2",
                "value": "val2"
              }
              {
              ....
              }
            ]
          },
        ....
        }
  ```
  
  

  
##   validations    

   -``` required ```
 
      
      { 
      ....
     "validations": "required|...",
     ....
     }
 
 -``` maximum ```
 
  
      { 
      ....
     "validations": "max:max_value|...",
     ....
     }
   
 
   -``` minimum ```
   
      
      { 
      ....
     "validations": "min:min_value|...",
     ....
     
      
  -``` searchable```      
     
      
      { 
        ....
        "searchable": "true",
        ....
       }
      
 -``` fillable```      
     
     
      { 
        ....
        "fillable": "true",
        ....
       }
    
 -``` inForm```      
     
    
      { 
        ....
        "inForm": "true",
        ....
       }
    
 -``` inIndex```      
     
     
      { 
        ....
       "inIndex": "true",
       ....
       }
      
      
##   view type
  -```text```:
   ```php
   {
      ....
      "viewType": {
      "type": "text"
          },
      ....
   },
  ```
   -```textarea```:
   ```php
   {
      ....
      "viewType": {
      "type": "textarea"
          },
      ....
   },
  ```
  -```password```:
   ```php
   {
      ....
      "viewType": {
      "type": "password"
          },
      ....
   },
  ```
   -```hidden```:
   ```php
   {
      ....
      "viewType": {
      "type": "hidden"
          },
      ....
   },
  ```
   -```email```:
   ```php
   {
      ....
      "viewType": {
      "type": "email"
          },
      ....
   },
  ```
   -```datetime```:
   ```php
   {
      ....
      "viewType": {
      "type": "datetime"
          },
      ....
   },
  ```
   -```date```:
   ```php
   {
      ....
      "viewType": {
      "type": "date"
          },
      ....
   },
  ```
  - ```select```:
  
   ```php
   {
      ....
      "viewType": {
      "type": "select"
          },
      ....
   },
  ```
   -```ckeditor```:
   ```php
   {
      ....
      "viewType": {
      "type": "ckeditor"
          },
      ....
   },
  ```
