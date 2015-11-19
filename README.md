#	Overview
## Protocol Definition  
### Client to Server 
####	PUT: put an entry into server database 
put [name] [value] [type] \r\n  
  type: A, NS. Type should be UPPERCASE  
####	GET: query an entry from server  
get	[name] [type] \r\n  
####	DELETE: delete an entry  
del [name] [type] \r\n  
####	BROWSE: return all the records  
browse \r\n


###	Server to Client  
####	OK: successfully put and delete  
ok [name] [type] \r\n  
####	REPLACED: server record updated due to put conflict  
replaced [name] [type] \r\n  
####	FOUND: return one record upon get query  
found [name] [value] [type] \r\n
####	NOTFOUND: server cannot find the record queried upon get or delete request
notfound [name] [type] \r\n  
####	ALL: return all records from server upon browse request  
all [count] [name] [value] [type] & [name] [value] [type] .... \r\n  
####	EMPTY: the server database is empty  
empty \r\n  


