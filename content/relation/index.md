---
title: "Realationship Config "
date: 2018-07-11T11:21:23+03:00
  weight = 60
---
we can use the following example:

![Color palette](/images/sample.PNG)

## mtm 
weakness  : ```true ```

```php
	{
          "name": "name the relation ",
          "type": "relation",
          "relation": {
           "type": "mtm",
		    "weakness":true,
		    "field_view":"view field in related table",
            "relatedEntity": "related tabel nane",
             "relatedModelName": "related model name",
            "middleTable": "related  middle table",
            "foreignKey": "foreign Key for current entity",
            "otherKey": "foreign Key for related entity",
            "localKey": "id"
          },
```
Note: 

weakness  : ```true ```
 for the weak junction table that it doesn't have any real data except
 foreign keys (collection data), and this entity doesn't appear as an independent entity in a frontend, and its data added by parent entity such as ```notifications``` table in previous example.

Example 
```php
	 "name": "Article",
      "fields": [],
       "relations": [
     	{
          "name": "tags",
          "type": "relation",
          "relation": {
           "type": "mtm",
		    "weakness":true,
		    "field_view":"type",
            "relatedEntity": "tags",
             "relatedModelName": "Tag",
            "middleTable": "notifications",
            "foreignKey": "article_id",
            "otherKey": "tag_id",
            "localKey": "id"
          },
        ]
```


weakness : ```false ```

for the strong junction table that it  has  real data and foreign keys and this entity appears as an independent entity in a frontend, and its data added by Independent form such as ```suggestions``` table in previous example..

Example 
```php
	 "name": "Article",
      "fields": [],
       "relations": [
     	{
          "name": "users",
          "type": "relation",
          "relation": {
           "type": "mtm",
		    "weakness":false,
		    "field_view":"name",
            "relatedEntity": "users",
             "relatedModelName": "User",
            "middleTable": "suggestions",
            "foreignKey": "article_id",
            "otherKey": "user_id",
            "localKey": "id"
          },
        ]
```

##  1tm
 
```php
		{
              "name": "name the relation ",
              "type": "relation",
              "relation": {
               "type": "1tm",
                "relatedEntity": "related tabel nane",
                 "relatedModelName": "related model name",
                "foreignKey": "foreign Key for current entity",
                "otherKey": "id",
                "localKey": "id"
              },

```

Example 
```php
	 "name": "Article",
      "fields": [],
       "relations": [
     	{
          "name": "comments",
          "type": "relation",
          "relation": {
           "type": "1tm",
            "relatedEntity": "comments",
             "relatedModelName": "Comment",
            "foreignKey": "article_id",
            "otherKey": "id",
            "localKey": "id"
          },
        ]
```


## mt1 
It is enough to define foreign keys fields.
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


Example 
```php
	 "name": "Comment",
      "fields": [
      {
      },
      {
               "title": "Article",
               "name": "article_id",
               "dbType": {
                 "type": "Integer",
                 "foreign": {
                   "table": "articles",
     			  "field_view": "type",
                   "related_field": "id"
                 }
     
               },
               "viewType": {
                 "type": "text"
       
               },
               "validations": "required",
               "searchable": true,
               "fillable": true,
               "inForm": false,
               "inIndex": false
      },	
      
     ],
     "relations": [
  
     ]
```
