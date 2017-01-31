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

### 7. menginputkan 5 data data ke dalam collection department
```
db.department.insert([
{code:"1",name:"satu",major:"it"},
{code:"2",name:"dua",major:"it"},
{code:"3",name:"tiga",major:"it"},
{code:"4",name:"empat",major:"it"},
{code:"5",name:"lima",major:"it"}])
```


### 8. menginputkan 3 data ke dalam collection student beserta reference ke department.
```
db.student.insert([
{
    studentId:"1",
    name:"Satu",
    address:"Jakarta",
    department:[{
        $ref: "department",
        $id: ObjectId("534009e4d852427820000002"),
        $db: "academic"
    }]
},
{
    studentId:"2",
    name:"Dua",
    address:"Jakarta",
    department:[{
        $ref: "department",
        $id: ObjectId("589017554ea152b89baf0417"),
        $db: "academic"
    }]
},
{
    studentId:"3",
    name:"Tiga",
    address:"Jakarta",
    department:[{
        $ref: "department",
        $id: ObjectId("589017554ea152b89baf0418"),
        $db: "academic"
    }]
}
])
```

### 9. Melihat isi collection student
```
db.getCollection('student').find({})
```
