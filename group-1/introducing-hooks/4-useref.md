---
description: شرح useRef
---

# 4 - useRef

## <mark style="color:blue;">useRef</mark>

* بتستخدم علشان تـ Access الـ DOM مباشرة

خلينا نقول لو أنت محتاج تجيب Element من الـ Dom ذى input من الـ Html بالـ Plain Js هتبقى كدة

```javascript
const inputElement = document.getElementById('input-element-id');
inputElement.focus();
```

لاكن الموضوع فى React إسهل بكتير

{% code title="useRef.js" %}
```jsx
import React, { useRef } from "react";

export default function UseRef() {
  const inputRef = useRef(null);

  const getInputValue = () => {
    console.log(inputRef.current.value);
    inputRef.current.focus();
    inputRef.current.value = "";
  };

  return (
    <div className="App">
      <div className="inrement_decrement">
        <h1>useRef</h1>
        <input placeholder="Ex..." ref={inputRef} />
        <button onClick={getInputValue}>Change Name</button>
      </div>
      <hr />
    </div>
  );
}
```
{% endcode %}

{% hint style="info" %}
`console.log(inputRef.current.value);`

هيجبلى القيمة اللى بتتكتب فى الـ Input فى الـ `console`
{% endhint %}

{% hint style="info" %}
`inputRef.current.focus();`

لما أضغط على الـ Button هيعملى Focus على الـ Input
{% endhint %}

{% hint style="info" %}
`inputRef.current.value = "";`

هيمسح القيمة من الـ Input بعد كل كتابة
{% endhint %}

{% embed url="https://codesandbox.io/s/hooks-jto950?file=%2Fsrc%2FuseRef.js%3A216-244" %}
