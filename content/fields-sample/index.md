---
title: "Fields Sample"
date: 2018-07-11T14:19:46+03:00
   weight = 50
---

## Fields Sample
this is simple sample "Customer"
```php
      {
        "name": "Customer",
        "fields": [
  	  	       {
            "title": "Id",
            "name": "id",
            "dbType": {
              "type": "Integer",
  			
              "primary": true
  			
            },
            "viewType": {
            
            },
  		  
             "searchable": false,
            "fillable": false,
            "inForm": false,
            "inIndex": false
          },
          {
            "title": "Name",
            "name": "name",
            "dbType": {
              "type": "string"
            },
            "viewType": {
              "type": "text"
   
            },
            "validations": "required|min:4",
            "searchable": true,
            "fillable": true,
            "inForm": true,
            "inIndex": true
          },
  			       {
            "title": "Email",
            "name": "email",
            "dbType": {
              "type": "string"
            
            },
            "viewType": {
              "type": "email"
   
            },
            "validations": "required",
            "searchable": false,
            "fillable": true,
            "inForm": true,
            "inIndex": true
          },
  			        {
            "title": "Age",
            "name": "age",
            "dbType": {
              "type": "Integer",
              "default": "18"
            },
            "viewType": {
              "type": "Integer"
   
            },
            "validations": "required|min:10",
            "searchable": false,
            "fillable": true,
            "inForm": true,
            "inIndex": true
          },
  		     {
            "title": "Title",
            "name": "title",
            "dbType": {
              "type": "string"
            
            },
            "viewType": {
              "type": "textarea"
   
            },
            "validations": "",
            "searchable": false,
            "fillable": true,
            "inForm": false,
            "inIndex": false
          },
  				{
            "title": "Balance",
            "name": "balance",
            "dbType": {
              "type": "double"
            
            },
            "viewType": {
              "type": "decimal"
   
            },        
            "searchable": false,
            "fillable": true,
            "inForm": true,
            "inIndex": true
          }
        ],
        "relations": [	
        ],
        "extraProperties": {
          "softdelete": true,
          "metable": true,
          "cachable": true,
          "sluggable": "name ,slug"
        },
  	  "generation":{
  	  
  	  "generate_model":true,
  	  "generate_create_event":true,
  	  "generate_update_event":true,
  	  "generate_delete_event":true,
  	  "generate_listener":true,
  	  "generate_repository":true,
  	   "generate_table_migrate":true,
  	  "generate_migrate":true,
  	  "generate_create_request":true,
  	  "generate_update_request":true,
  	  "generate_controller":true,
  	  "generate_route":true,
  	  "generate_breadcrumbs":true,
  	  "generate_lang":true,
  	  "generate_view":true,
  	  "generate_api_create_request":true,
  	  "generate_api_update_request":true,
  	  "generate_api_controller":true,
  	  "generate_api_route":true
  	  
  	  }
  	  
  	}

```

