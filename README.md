# mongodb-query

### 1. Membuat database academic
```
use academic
```

### 2. Menampilkan semua collection dan data dalam database
```
show collections
```

### 3. Membuat dan mengaktifkan database
```
use academic
```

### 4. Membuat collection department
```
> db.createCollection("department")
{ "ok" : 1 }
```

### 5. Membuat collection student
```
> db.createCollection("department")
{ "ok" : 1 }
```

### 6. Melihat struktur collection student
```
var col_list= db.student.findOne();
for (var col in col_list) { print (col) ; }
```
