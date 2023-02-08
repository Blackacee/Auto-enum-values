# Auto-enum-values

var testEnum = function() {
 // Initializes the enumerations
 var enumList = [
"One",
 "Two",
 "Three"
 ];
 enumObj = {};
 enumList.forEach((item, index)=>enumObj[item] = index + 1);
 
 // Do not allow the object to be changed
 Object.freeze(enumObj);
 return enumObj;
}();
console.log(testEnum.One); // 1 will be logged
var x = testEnum.Two;
switch(x) {
 case testEnum.One:
 console.log("111");
 break;
 case testEnum.Two:
 console.log("222"); // 222 will be logged
 break;
}
