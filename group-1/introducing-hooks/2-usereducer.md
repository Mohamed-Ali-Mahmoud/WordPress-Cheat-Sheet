---
description: ِشرح useReducer Hook
---

# 2 - useReducer

## <mark style="color:blue;">useReducer</mark>

* مشابهة للـ useState
* مكونة من Array الـ State الحالية والـ Dispatch Function ودى الـ Function اللى هتخلينى أعمل Update للـState
* لو لقيت نفسك بتستخدم useState كثير وبدأ الكود يبقى معقد إستخدم useReduce

> هنا بدل ما أعمل أتنين State بـ useState لأ هعمل واحدة بس بـ useReducer

{% code title="useReducer.js" %}
```jsx
import React, { useState } from "react";

export default function useReducer() {

  const [count, setCount] = useState(0);
  const [showText, SetShowText] = useState(true);

  return (
    <div className="App">
      <div className="inrement_decrement">
        <h2> Increment & Decrement </h2>
        {count}
        <button
          onClick={() => {
            setCount(count + 1);
            SetShowText(!showText);
          }}
        >
          Click Here
        </button>
        {showText && <p> This Is a Text </p>}
        <hr />
      </div>
    </div>
  );
}
```
{% endcode %}

{% code title="useReducer.js" %}
```jsx
import React, { useReducer } from "react";

const reducer = (state, action) => {

  switch (action.type) {

    case "increment":

      return { count: state.count + 1, showtext: state.showText };

    case "toggleShowText":

      return { count: state.count, showText: !state.showText };

    default:

      return state;
  }
};
export default function UseReducer() {
  
  const [state, dispatch] = useReducer(reducer, { count: 0, showText: true });

  return (
    <div className="App">
      <div className="inrement_decrement">
        <h2> useReducer </h2>
        {state.count}
        <button
          onClick={() => {
            dispatch({ type: "increment" });
            dispatch({ type: "toggleShowText" });
          }}
        >
          Click Here
        </button>
        {state.showText && <p> This Is a Text </p>}
        <hr />
      </div>
    </div>
  );
}
```
{% endcode %}

{% embed url="https://codesandbox.io/s/useestate-hooks-jto950?file=%2Fsrc%2FuseReducer.js" %}
sandboxedeee
{% endembed %}

{% embed url="https://beta.reactjs.org/apis/usereducer" %}
