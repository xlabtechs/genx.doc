---
title: " File Config"
date: 2018-07-10T21:53:36+03:00
weight: 30
---

 ## Multiple Entities
 You can generate  many entities as the following sample:
 
```json 
{
  "entities": [
    {
       // data of first entity
    }
    {
       // data of second entity
    }
    ]
}
```
## Entity Content
Inside every entity, you must define the following keys and values:

### Name:
 Name of Entity ```Model Name```
 
 
### Fields: 
Contain fields of the entity:

 -  title: lable name
 - name: field name
 - dbType:
       - type: ```Integer```, ```string```, ```double```, ```enum```, ```blob``` ...etc
       - primary: ```true```, ```false```
       - default: default value
       - foreign : foreign key: 
             
          - table: name of related tablel.
          - field_view: the field that you want view it.
                
 - viewType:
    - type: ```Integer```,```text```,```textarea```,```password```,```hidden```, ```datetime```, ```date```, ```select```,  ```ckeditor```  ...etc
 - validations:  ```required```, ```email```,```min:value```,```max:value```  ...etc
 - searchable: ```true```, ```false``` 
 - fillable: ```true```, ```false```
 - inForm: ```true```, ```false```
 - inIndex ```true```, ```false```
 
###  Relations: 

 - name: constraint name
 - type: relation
 - relation:
       - type: ```mtm```,   ```1tm```,  ```mt1```  
       if the type is a ```mtm``` must  determine this fields:
          - middleTable : name of the junction table
          - weakness:```true```, ```false```
      
       ```true``` : for the weak junction table, 
      ```false```: for the strong junction table.
           
      - field_view:the field that you want view it
      - relatedEntity: name of the related table
      - relatedModelName: name of the related model
     - foreignKey: name of foreign Key field for current entity
     - otherKey: name of foreign Key field for related entity
               
### Extra Properties: 

  - softdelete: ```true```, ```false```
  - metable: ```true```, ```false```
  - cachable: ```true```, ```false```
  - sluggable: ```field name```,```slug``` or ``` null``` 
     


### Generation: 
   - generate_model:  ```true```, ```false```
   - generate_create_event:  ```true```, ```false```
   - generate_update_event:  ```true```, ```false```
   - generate_delete_event:  ```true```, ```false```
   - generate_listener: ```true```, ```false```
   - generate_repository: ```true```, ```false```
   - generate_table_migrate: ```true```, ```false```
   - generate_migrate: ```true```, ```false```
   - generate_create_request: ```true```, ```false```
   - generate_update_request: ```true```, ```false```
   - generate_controller: ```true```, ```false```
   - generate_route: ```true```, ```false```
   - generate_breadcrumbs: ```true```, ```false```
   - generate_lang: ```true```, ```false```
   - generate_view: ```true```, ```false```
   - generate_api_create_request: ```true```, ```false```
   - generate_api_update_request: ```true```, ```false```
   - generate_api_controller: ```true```, ```false```
   - generate_api_route: ```true```, ```false```
    



