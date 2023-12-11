# 2023-JS-testing 面試題目
### 1. JavaScript: 字串反轉

```javascript
function reverseString(str) {
    // 實作你的解答	
    if (str === "")
        return "";
    else
        return reverseString(str.substr(1)) + str.charAt(0);
  }
  
console.log(reverseString("Hello")); // 預期輸出: "olleH”
```

***
### 2. JavaScript: 陣列過濾
問題：寫一個JavaScript函式，接受一個數字陣列，並返回該陣列中所有大於5的數字。
```javascript
function filterNumbersGreaterThanFive(numbers) {
    // 實作你的解答
    return numbers.filter(num => num > 5)
}
const numbers = [2, 8, 4, 10, 1, 7];
console.log(filterNumbersGreaterThanFive(numbers)); // 預期輸出: [8, 10, 7]
```
***
### 3. JavaScript: 重構
問題：重構這段程式碼並說明原因
```javascript
function formatName(firstName, lastName) {
  let formattedName = '';

  if (firstName) {
    formattedName += firstName;
  }

  if (lastName) {
    formattedName += ' ' + lastName;
  }

  return formattedName;
}

```
**重構：**  
```javascript
function formatName1(firstName, lastName) {
    return [firstName, lastName].filter(name => name).join(' ');
}
```
**原因：先前的function在只提供lastName時，會造成return的字串前會有空格，重構後可以避免此問題。**
***
### 4. React: 條件渲染
問題：在React中，如何根據條件渲染兩種不同的內容？

```javascript
function ConditionalRendering({ isLoggedIn }) {
  // 實作你的條件渲染
return (
    isLoggedIn ? <h1>Loggedin</h1> : <h1>notLoggedIn</h1>
  );
}

```
***
### 5. React: 組件
問題：使用React創建一個簡單的計數器組件，具有增加和減少計數的按鈕。

```javascript
import { useState } from 'react'

function App() {
  const [count, setCount] = useState(0)
  return (
    <>
      <div>
        <h1>count: {count}</h1>
        <button onClick={() => setCount((count) => count + 1)}>
          count + 1 
        </button>
        <button onClick={() => setCount((count) => count - 1)}>
          count  - 1  
        </button>
      </div>
    </>
  )
}

export default App

```
***
