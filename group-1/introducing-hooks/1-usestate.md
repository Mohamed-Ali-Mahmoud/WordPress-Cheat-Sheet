---
description: ِشرح useState Hook
---

# 1 - useState

## <mark style="color:blue;">useState</mark>

* بتقبل Array - الـ State الحالية و الـ SetFunction اللى هتغير قيمة الـState الحالية

{% hint style="success" %}
الـ State هنا معناها إى بيانات هتتبعها فى الـApplication
{% endhint %}

### <mark style="color:blue;">**المثال الأول**</mark>

* هنا عملنا State بسيطة بتخلينا نعمل Increment للقيمة الحالية يعنى نزود القيمة لو هى 0 خليها 1 وهكذا

### <mark style="color:blue;">**المثال الثانى**</mark>

* بناخود قيمة الـ Input واضيفها فى div

{% code title="" %}
```jsx
import React, { useState } from "react";

export default function useEffect() {
  const [counter, setCounter] = useState(1);

  // Increment and Decrement Function

  const increment = () => {
    setCounter(counter + 1);

    console.log(counter);
  };

  const dncrement = () => {
    setCounter(counter - 1);

    console.log(counter);
  };

  // Input Value Function

  const [inputValue, setInputValue] = useState("pedro");

  let onChange = (event) => {
    const newValue = event.target.value;
    setInputValue(newValue);
  };

  return (
    <div className="App">
      <div className="inrement_decrement">
        <h2>useState</h2>
        <h3>Increment & Decrement</h3>
        {counter}
        <button onClick={increment}>Increment</button>
        <button onClick={dncrement}>Dacrement</button>
        <hr />
      </div>

      <div className="input_value">
        <h2>Input Value</h2>
        <input placeholder="enter somthing..." onChange={onChange} />
        <div>{inputValue}</div>
        <hr />
      </div>
    </div>
  );
}
```
{% endcode %}

{% embed url="https://codesandbox.io/s/useestate-hooks-jto950?file=%2Fsrc%2FuseState.js%3A0-1051" %}
