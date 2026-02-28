#рксп 
Хотим написать абстрактные классы для объекта в БД

```
class DBO:
	dbInsert(self)
	dbUpdate(self)
	dbDelete(self)
	
class User: public DBO
	def __init__(self)
	.
	.
	.
	getUsername() return self.username
	setUsername() self.username = value
```

Теперь саму модельку, видимо:
```
class UserDBO
	User(int ID, bool Lock = False)
	SELECT * FROM USERS WHERE ID + {ID}
```

Зачем это нужно:
1) Единообразие объектов
2) Упрощение тестирования
3) Человекочитаемый код

Напишем запросы для поиска. В формате XML.
```
1) params: Username
2) output: UserBO
3) SELECT * FROM USERS WHERE USERNAME = {username}
   
hasPermission()
	UserID, PermissionID
	
	SELECT * FROM (SELECT UserRoleID FROM USERS WHERE UserID = {UserID}) AS P1;
	(SELECT RoleID FROM PERMISSIONS WHERE PermissionID = {PermissionID}) AS P2 WHERE P1 = P2
```

И потом будем писать в питоновском коде:
```
cursor.execute()
if cursor.fetchone() is None:
#или
True if c.fetchone is not None else False
```

## ДЗ:
Создать класс DBO, наследовать от него классы для каждой таблички. Реализовать методы

Замечания:
- У нас есть еще таблички Users \_H и \_D
- В Users создать self.attributes = dict()
- self.attributes\["table_name"\] = 'USERS'

Реализация методов:
dbUpdate():
	INSERT INTO {self.attributes\['table_name'\] + '\_H'} self.\_\_dict\_\_
	self.change_cnt += 1
	self.last_change = datetime.now()
	self.last_editor("system")
	UPDATE Users WHERE USERID = self.ID

И потом написать кодогенератор, который по описанию таблиц из ямла и абстрактному классу DBO.py напишет нам файлы с другими классами.

Для конструктора надо достать все поля из ямла.
Для инсерта надо написать запрос:
"INSERT INTO 'TABLE_NAME' (?, ?, ?, ?, ...)", fields_size, (self.username, ...)

Для делита то же самое, просто сначала в \_D закидываем