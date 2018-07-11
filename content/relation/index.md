---
title: "Realationship Config "
date: 2018-07-11T11:21:23+03:00
  weight = 19
---
## mtm 
 ```weakness ``` : ```true ```
```json
	{
          "name": "Tags",
          "type": "relation",
          "relation": {
           "type": "mtm",
		    "weakness":true,
		    "field_view":"name",
            "relatedEntity": "tags",
             "relatedModelName": "Tag",
            "middleTable": "middles",
            "foreignKey": "comment_id",
            "otherKey": "tag_id",
            "localKey": "id"
          },
```
 for the weak junction table that it doesn't have any real data except
 foreign keys (collection data), and this entity doesn't appear as an independent entity in a frontend, and its data added by parent entity

 Example:
![picture](C/img.1.PNG)

```weakness ``` : ```false ```
```json
example




```
for the strong junction table that it  has  real data and foreign keys and this entity appears as an independent entity in a frontend, and its data added by Independent form.
 Example:
![picture](C/img.2.PNG)

##  1tm
 
```json
	Example

```


 Example:
![picture](C/img.1.PNG)

## mt1 
 must define foriegn keys.
```json
	Example

```


 Example:
![picture](C/img.1.PNG)