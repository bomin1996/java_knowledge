# JavaScript 스코프

JavaScript의 스코프는 변수와 함수가 접근 가능하고 존재하는 범위를 의미합니다. 스코프는 코드의 구조와 실행 흐름에 따라 결정됩니다.

## 글로벌 스코프 (Global Scope)
- **설명**: 전역에 선언된 변수나 함수는 어디에서든 접근할 수 있는 글로벌 스코프를 가집니다.
- **예시**:
  ```javascript
  var globalVar = "This is a global variable";

  function test() {
      console.log(globalVar); // 접근 가능
  }


함수 스코프 (Function Scope)
설명: 함수 내부에서 선언된 변수는 해당 함수와 그 하위 함수에서만 접근 가능합니다.
특징: var 키워드로 선언된 변수는 함수 스코프를 가집니다.
예시:
javascript
Copy code
function test() {
    var functionScopedVar = "Accessible within this function";
    console.log(functionScopedVar); // 접근 가능
}
console.log(functionScopedVar); // 접근 불가능 (에러 발생)


  
블록 스코프 (Block Scope)
let과 const로 선언된 변수는 블록 스코프를 가집니다. 이들은 해당 블록(예: if 문, for 문 등) 내에서만 접근 가능합니다.

javascript
Copy code
if (true) {
    let blockScopedVar = "Accessible within this block";
    console.log(blockScopedVar); // 접근 가능
}
console.log(blockScopedVar); // 접근 불가능 (에러 발생)


스코프 체인 (Scope Chain)
자바스크립트에서는 함수가 중첩되어 있을 때 외부 함수의 스코프에 접근할 수 있습니다. 이를 스코프 체인이라고 합니다.

javascript
Copy code
var outerVar = "Outer variable";

function outerFunc() {
    var innerVar = "Inner variable";

    function innerFunc() {
        console.log(outerVar); // 외부 함수의 변수에 접근 가능
        console.log(innerVar); // 현재 함수의 변수에 접근 가능
    }
    innerFunc();
}
outerFunc();
