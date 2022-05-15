---
description: شرح useImperativeHandle
---

# 7 - useImperativeHandle

## <mark style="color:blue;">useImperativeHandle</mark>

* بتعمل بشكل مشابهة تماماً لـ `useRef`
* فكرتها ان هى بتمرر فنكشن عنى طريق useRef من الـChild Component للـ Parent Component
* بتستخدم مع [`forwardRef`](https://reactjs.org/docs/react-api.html#reactforwardref)
* بتستخدم فى حالات نادرة جداً وفيها Functions متقدمة جدا

## <mark style="color:blue;">forwardRef</mark> <a href="#how-to-use-forwardref" id="how-to-use-forwardref"></a>

* بتقبل أتنين Argument الـ props والـ ref

{% code title="button.js" %}
```jsx
import React, { forwardRef, useImperativeHandle, useState } from "react";

export default function Button(props, ref) {
  const [toggle, setToggle] = useState(false);

  useImperativeHandle(ref, () => ({
    alterToggle() {
      setToggle(!toggle);
      console.log("Text Toggle From Parent Button");
    }
  }));

  return (
    <div className="App">
      <button>Button From Child Component</button>
      {toggle && <div>Text Toggle From Parent Button</div>}
    </div>
  );
}
Button = forwardRef(Button);
```
{% endcode %}

> ممكن كتابتها بالشكل التالى عن طريق Arrow Function
>
> * هنعمل Wrrap للـ Function كلها عن طريق `forwardRef`

{% code title="button.js" %}
```jsx
import React, { forwardRef, useImperativeHandle, useState } from "react";

const Button = forwardRef((props, ref) => {
  const [toggle, setToggle] = useState(false);

  useImperativeHandle(ref, () => ({
    alterToggle() {
      setToggle(!toggle);
      console.log("Text Toggle From Parent Button");
    }
  }));

  return (
    <div className="App">
      <button>Button From Child Component</button>
      {toggle && <div>Text Toggle From Parent Button</div>}
    </div>
  );
});
export default Button;
on.js
```
{% endcode %}

{% code title="useImperativeHandle.js" %}
```jsx
import React, { useRef } from "react";
import Button from "./button";

export default function UseImperativeHandle() {
  const buttonRef = useRef(null);

  return (
    <div className="App">
      <h1>useImperativeHandle</h1>
      <button
        onClick={() => {
          buttonRef.current.alterToggle();
        }}
      >
        Button From Parent Component
      </button>
      <Button ref={buttonRef} />
      <hr />
    </div>
  );
}
```
{% endcode %}

> هنا لما أضغط على الـ Button اللى موجود فى useImpreative Component هيجبلى الرسالة اللى موجودة فى الـ Button Componen

{% hint style="info" %}
مثال ثانى على Code Sand Box
{% endhint %}

{% embed url="https://codesandbox.io/s/hooks-jto950?file=%2Fsrc%2FuseImperativeHandle.js&from-embed=" %}
