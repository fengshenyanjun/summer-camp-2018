## JS笔记

#### 数组字符串操作

+ 在 JavaScript 中，当 `+` 操作符与 `字符串` 一起使用的时候，它被称作 连接 操作符。 

  > var ourName = "Summer Camp";
  >
  > var ourStr = "Hello, our name is " + ourName + ", how are you?";

+ 可以通过在字符串变量或字符串后面写上 `.length`来获得字符串变量 `字符串` 值的长度。 

  > "Alan Peter".length;                                                                                                  // 10 

+ 为了得到一个字符串的最后一个字符，可以用`[字符串的长度减去一]`。 

  > 在 `var firstName = "Charles"` 中，可以这样操作 `firstName[firstName.length - 1]` 来得到字符串的最后的一个字符。 

+ `.push()` 接受把一个或多个参数，并把它“推”入到数组的末尾。

  > var arr = [1,2,3];
  > arr.push(4);
  > // 现在arr的值为 [1,2,3,4]

+ `.unshift()` 函数用起来就像 `.push()` 函数一样, 在数组的头部添加元素。 

  ————————————————————————————————————

+ `.pop()` 函数用来“抛出”一个数组末尾的值。

  > `var oneDown = [1, 4, 6].pop();` 
  >
  > 现在 `oneDown` 的值为 `6` ，数组变成了 `[1, 4]`。 

+ `.shift()` 的 工作原理就像 `.pop()`，它移除的是第一个元素。 

  ————————————————————————————————————

#### 函数

+ `局部变量` 优先级更高。 

+ 在计算机科学中 队列（queue）是一个抽象的数据结构，队列中的条目都是有秩序的。新的条目会被加到 `队列` 的末尾，旧的条目会从 `队列` 的头部被移出。

  > 写一个函数 `queue` ，用一个数组`arr`和一个数字`item`作为参数。数字`item`添加到数组的结尾，然后移出数组的第一个元素，最后队列函数应该返回被删除的元素。
  >
  > :
  >
  > function queue(arr, item) {
  >   arr.push(item);
  >   item = arr.shift();
  >   return item; 
  > }
  >
  > var testArr = [1,2,3,4,5];
  >
  > console.log("Before: " + JSON.stringify(testArr));
  > console.log(queue([5,6,7,8,9], 1));                                       // 你可以修改这一行来测试你的代码
  > console.log("After: " + JSON.stringify(testArr));

#### 运算符

- 抽象相等（==）`1`   与严格相等（===）`2`  的区别：
  1. Type(x)为Undefined, Type(y)为Null, 返回true；即 *undefined==null* 为**true**
  2. 如果 Type(x) 与 Type(y) 的结果不一致，返回 false，即只要类型不一样，则返回false,例子：

     > 1===“1”   **false**
     >
     > undefined===null  **false**

- 严格相等运算符（`===`）是相对于相等操作符（`==`）的一种操作符。
  - 与相等操作符不同的是：它会同时比较元素的值和   ` 数据类型` 。 

    > 3 === 3   // true
    >
    > 3 === '3' // false 

- 注意 `+=` 和 `=+` 的区别。

  > var myArr = [ 2, 3, 4, 5, 6];
  >
  > var total=0;
  > for(var i=0;i<myArr.length;i++){
  >   total  **+=**  myArr[i];                                                                total  **=+**  myArr[i];
  > }                             //total = 20                                                                            //total = 6

#### 逻辑运算

+ 如果`switch`语句中的`case`分支的`break` 语句漏掉了，后面的 `case`语句会一直执行直到遇到`break`。如果你有多个输入值和输出值一样，可以试试下面的`switch`语句： 

  > switch(val) {  
  >
  >  case 1: 
  >
  >  case 2:
  >
  >  case 3: 
  >
  > ​     result = "1, 2, or 3";
  >
  > ​     break;   
  >
  > case 4:
  >
  > ​     result = "4 alone"; 
  >
  > } 

#### 对象object

+ *数组是通过索引来访问和修改数据*， 对象是通过属性来访问和修改数据的。 

  + 有两种方式访问对象属性，一个是点操作符(`.`)，一个是中括号操作符(`[]`)。

    1.  当你知道属性的名称的时候，使用点操作符。 

    > var myObj = {
    >
    >    prop1: "val1",
    >
    >    prop2: "val2" 
    >
    > }; 
    >
    > var prop1val = myObj.prop1;                // val1 
    >
    > var prop2val = myObj.prop2;                // val2 

    2. 如果你想访问的属性的名称有一个空格，这时你只能使用中括号操作符(`[]`)。 

    > var myObj = {
    >
    >    "Space Name": "Kirk",
    >
    >    "More Space": "Spock" 
    >
    > }; 
    >
    > myObj["Space Name"];                            // Kirk 
    >
    > myObj['More Space'];                              // Spock 

    + *tips:  属性名称中如果有空格，必须把属性名称用单引号或双引号包裹起来。* 

+ 中括号操作符的另一个使用方式是**用变量来访问一个属性**。当你需要遍历对象的属性列表或查表时，这种方式极为有用。 

  > var myDog = "Hunter";                                          var testObj = { 
  >
  > var dogs = {                                                     		12: "Namath",
  >
  >    Fido: "Mutt",                                                		16: "Montana",
  >
  >    Hunter: "Doberman",                                 		19: "Unitas"
  >
  >    Snoopie: "Beagle" 					   	   };
  >
  > } 
  >
  > var breed = dogs[myDog];                                    var playerNumber=16;
  >
  > console.log(breed)         // "Doberman"              var player = testObj[playerNumber];    //"Montana"

  + *tips:     当我们通过变量名访问属性的时候，不需要给变量名包裹引号。因为实际上我们使用的是变量的值，而不是变量的名称。*

+ 可以像更改属性一样给对象添加属性。 

  > /*                    更改属性                        */
  >
  > var ourDog = {
  >
  >    "name": "Camper",
  >
  >    "legs": 4,
  >
  >    "tails": 1,
  >
  >    "friends": ["everything!"] 
  >
  > }; 
  >
  > ourDog.name = "Happy Camper"; 
  >
  > 或
  >
  > ourDog["name"] = "Happy Camper"; 

+ 删除对象的属性 

  > delete ourDog.bark; 

##### 错题<1>：

function phoneticLookup(val) {

​    var result = ""; 

​    var lookup = {

​    	alpha:"Adams",

​	bravo:"Boston",

​	charlie:"Chicago",

​	delta:"Denver",

​	echo:"Easy",

​	foxtrot:"Frank"
   };

   **result=lookup[val];**                                                      *//最初因为缺少该语句而出错* 

   return result;
} 

phoneticLookup("charlie");



+ 可以用 `.hasOwnProperty(propname)`  方法来检查对象是否有该属性。如果有返回`true`，反之返回 `false`。 

##### 错题<2>:

var myObj = {

​	gift: "pony",

​	pet: "kitten",

​	bed: "sleigh"

};

function checkObj(checkProp) {

​	if(myObj.hasOwnProperty(checkProp))

​		return **myObj[checkProp]**;                                                  *//开始写的“checkProp”，输出不了属性值* 

​	else

​		return "Not Found";

}

checkObj("gift");

## JSON 

+ JavaScript Object Notation  简称 `JSON`，它使用JavaScript对象的格式来存储数据。

  JSON是灵活的，因为它允许 *数据结构*  是 *字符串* ，*数字* ，*布尔值* ，*字符串* ，和 *对象*  的任意组合。 

  > var myMusic = [
  >   {                                  ------------------------------------------------
  >     "artist": "Billy Joel",                                                      
  >     "title": "Piano Man",                                                    
  >     "release_year": 1973,                                                  
  >     "formats": [                                                                  专
  >       "CS",                                                                            辑
  >       "8T",                                                                            ① 
  >       "LP" ],                                                                           
  >     "gold": true                                                                   
  >   },                                  -------------------------------------------------
  >
  >
  > {                                     -------------------------------------------------
  >     "artist": "Billy Joel",                                                      
  >     "title": "Piano Man",                                                    
  >     "release_year": 1973,                                                  
  >     "formats": [                                                                  专
  >       "CS",                                                                            辑
  >       "8T",                                                                            ② 
  >       "LP" ],                                                                          
  >     "gold": true                                                                   
  >   }                                   -------------------------------------------------
  >
  > ];

+ 嵌套的JSON对象： 

  > var ourStorage = {
  >   "desk": {
  >     "drawer": "stapler"
  >   },
  >   "cabinet": {
  >     "top drawer": { 
  >       "folder1": "a file",
  >       "folder2": "secrets"
  >     },
  >     "bottom drawer": "soda"
  >   }
  > }
  > ourStorage.cabinet["top drawer"].folder2;                          // "secrets"
  > ourStorage.desk.drawer;                                                        // "stapler"

+ #### 任务

  检索JSON对象 `myStorage` 中嵌套属性 `glove box` 的值。因为属性的名字带有空格，请使用中括号操作符来访问属性的值。

  > var myStorage = {
  >   "car": {
  >     "inside": {
  >       "glove box": "maps",
  >       "passenger seat": "crumbs"
  >      },
  >     "outside": {
  >       "trunk": "jack"
  >     }
  >   }
  > };
  >
  > **var gloveBoxContents = myStorage.car.inside["glove box"];** 

+ JSON对象可以嵌套对象和数组 ，用中括号操作符同样可以访问嵌套数组。 

  > var myPlants = [
  >   { 
  >     type: "flowers",
  >     list: [
  >       "rose",
  >       "tulip",
  >       "dandelion"
  >     ]
  >   },
  >   {
  >     type: "trees",
  >     list: [
  >       "fir",
  >       "pine",
  >       "birch"
  >     ]
  >   }  
  > ];
  >
  > var secondTree = myPlants[1].list[1];                      输出结果：secondTree = pine
