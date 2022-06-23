## Typescript
  
### Resource
https://www.tutorialsteacher.com/typescript


### Declare Variables
```
function addNumbers(num1: number, num2: number) {
    console.log(num1 + num2);
}
addNumbers(10,20);
```
### Concatination
```
function user(){
    let userid:number = 10;
    let firstname:string = "Rakib";
    let lastname:string = "Hossain";

    let fullname = firstname.concat(' '+ lastname
        );
 
    console.log(`User ID : ${userid}, Name : ${fullname}`);
    console.log(fullname.split(" "))
}
user();
```


### Void Function
```
// Void
function show() : void{
    console.log("This is a void function");
}
show(); 
```
### Union Data Type
```
// User Defined Type: union type
function union(userid : string | number){ 
    console.log(`Union Data type : User ID is ${userid}`);
}
union("10"); 
```

### Work with Arrays
```
// Array Data Type
function array():void{
    let users : (string|number)[]; // let users : Array<string>
    users =["Sakib", "Mehedi", "Salam"];
    users.sort();
    console.log(users[0]);
}
array();
```
### Work with Tuple
```
// Tuple
function tuple():void{
    let data : [number, string];
    data = [1, "Class 1"];
    data.push(2, "Class 2", 3, "Class 3", 4, "Class 4");

    console.log(data);
}

 tuple(); 
```
### Enum Data Type
Enum Data type: no duplicate data, helps to store constants. Types: numeric, string, heterogenous \
```
// Numerics Enum
function nenum():void{
   enum days{ 
    Sunday = 1, 
    Monday, 
    Tuesday, Wednesday, Thursday, Friday  }
    console.log(days);
}
nenum();

// String Enum
function senum():void{
    enum days{ 
     Sunday = "Sun", 
     Monday = "Mon", 
     Tuesday = "Tue", Wednesday ="Wed" , Thursday ="Thu", Friday ="Fri" }
     console.log(days);
 }
 senum();

 // Heterogenous
 function henum():void{
    let data : any;  // Any type data
    data = "hello";
    console.log(data);
    
    enum days{ 
     Sunday = 1,   Monday = "Mon",   Tuesday = 3, Wednesday ="Wed" , Thursday ="Thu", Friday ="Fri" }
     console.log(days);
 }

henum();
```

### Object 
```
// Object Data Type
function obj():void{
    let user : object;
    user = {id:1, name : "Rakib", phone: "01735056898"}

    let user1 :  object[];
    user1 =[];    
    let user2: {id : number, name: string, phone? : string}; // (?) sign - optional
    user2 = {id: 3, name : "Rahat", phone: "01735065695"}

    user1.push(user2);
    
    console.log(user);

    for (const key in user1) {
        console.log(user1[key]["name"]);
      }

    }
     
obj();
```

### Create Custom Data Type
```
 // Create Custom data type
 function custom():void{
    type User = {id : number, name: string, phone? : string}; // Custom Data type
    let user : User[];
    user = [];

    let user1 : User;
    user1 = {id: 1, name : "Rakib", phone: "01735056898"}
    
    let user2: User; 
    user2 = {id: 3, name : "Rahat", phone: "01735065695"}

    user.push(user1);
    user.push(user2);
    
    console.log('Custom Data Type Array of Objects:', user);

    for (const key in user) {
        console.log(user[key]["name"]);
      }
 }

 custom();


// Another Custom Data Type
type RequestType = "GET" | "POST";
function requesthandler(RequestType:RequestType){    
    console.log(RequestType);
}
requesthandler("GET");
 ```
 
