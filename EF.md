# Neo Particle [NEP]
### Generic Smart Contract which can be utilized to build Smart Contract!!!

---
**[NEP5 Token Methods](http://docs.neoparticle.com)**<br /><br />
**EF Methods:**<br /><br />

>**ef-create**<br />
This method is used create any entity and insert. This is like creating a table and inserting in rows. <br />
The entity created by logged in user can be accessed only by the same user.  <br />
(*Yet to come*) Assign permission to account to access with CRUD specific permissions.  <br />
*Parameter*(`byte[] scriptHash, byte[] entityName, byte[] name`)
&nbsp;&nbsp;&nbsp;`byte[] scriptHash` => Script hash of the logged in user.
&nbsp;&nbsp;&nbsp; `byte[] entityName` => Name of the entity. e.g. Project, ProjectChild1, Role etc...
&nbsp;&nbsp;&nbsp;`byte[] name` => Value inserted into the entity. e.g. Project - NEPGUI, ProjectChild1 - UIDevelopment etc...<br /><br />

>**ef-list**<br />
This method is used to list values of a single entity. By default 10 value will be listed and the start id will be 1.<br />
For now listing is based on ID and not count. e.g. Available index in an entity is 1 to 100. By default 1 to 10 will be listed. If Start Id is 12 than Item per view is 10 than 12 to 21 will be listed.<br />
*Parameter*(`byte[] scriptHash, byte[] entityName, int itemPerView, int startId`)
&nbsp;&nbsp;&nbsp;`byte[] scriptHash` => Script hash of logged in user.
&nbsp;&nbsp;&nbsp;`byte[] entityName` => Name of the entity for which value has to be fetched.
&nbsp;&nbsp;&nbsp;`int itemPerView`(optional) => No of item value to be fetched. If any Id deleted in between than only 9 value will be fetched.
&nbsp;&nbsp;&nbsp;`int startId`(optional) => Start index of the entity from which value has to be Listed.<br /><br />

>**ef-get**<br />
This method is used to get value of single value in an entity. <br />
*Parameter*(`byte[] scriptHash, byte[] entityName, int id`)
&nbsp;&nbsp;&nbsp;`byte[] scriptHash` => Script hash of logged in user.
&nbsp;&nbsp;&nbsp;`byte[] entityName` => Name of the entity for which value has to be fetched.
&nbsp;&nbsp;&nbsp;`int id` => Id of the value in an entity. 

>**ef-update**<br />
This method is used to update value of particular Id in an entity.<br />
*Parameter*(`byte[] scriptHash, byte[] entityName, int id, byte[] value`)
&nbsp;&nbsp;&nbsp;`byte[] scriptHash` => Script hash of logged in user.
&nbsp;&nbsp;&nbsp;`byte[] entityName` => Name of the entity for which value has to be fetched.
&nbsp;&nbsp;&nbsp;`int id` => Id of the value in an entity. 
&nbsp;&nbsp;&nbsp;`byte[] value` => New value for updating. 
---
