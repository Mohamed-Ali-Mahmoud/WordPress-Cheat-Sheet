---
description: ِشرح useEffect Hook
---

# 3 - useEffect

## <mark style="color:blue;">useEffect</mark>

* الـ useEffect بتخليك تستخدم الـ Side Effects
  * ذى تـFetch الداتا من الـApi و تعمل الـUpdate للـDom والـ Timers ذى `()setTimeout`

```jsx
import React, { useEffect, useState } from "react";
import axios from "axios";
export default function UseEffect() {

  const [data, setData] = useState("");
  const [count, setCount] = useState("");
  
  useEffect(() => {
    // Apiهنجيب الداتا من الـ 
    axios 
      .get("https://jsonplaceholder.typicode.com/comments")
      .then((response) => {
      
        console.log("Api Was Called");
        
// هنخلى الـsetCount تاخود الإستجابة من الـ Api اللى هى الايميل         
        setData(response.data[0].email);
      });
  }, [count]); // Click  كل مرة اضغط Call هيتعملة  Api  الـ  

  return (
    <div className="App">
      <div className="inrement_decrement">
        <h1>useEffect</h1>
        <h4>Email : {data}</h4>
        <button
          onClick={() => {
            setCount(count + 1); 
          }}
        >
          Click
        </button>
      </div>
    </div>
  );
```

{% hint style="info" %}
```jsx
  }, [count]); Click  كل مرة اضغط Call هيتعملة  Api  الـ  
```
{% endhint %}

{% hint style="info" %}
```jsx
         هنخلى الـsetCount تاخود الإستجابة من الـ Api اللى هى الايميل         
        setData(response.data[0].email);
```
{% endhint %}

```jsx
useEffect(() => {
  //Runs on every render
});
```

> هيتعملة Call فى كل render

```jsx
useEffect(() => {
  //Runs only on the first render
}, []);
```

> هيتعملة Call مرة واحدة

```jsx
useEffect(() => {
  //Runs on the first render
  //And any time any dependency value changes
}, [prop, state]);
```

> هيتعملة Call مرة واحدة وفى كل مرة القيمة تتغير ذى ما أستخدمناه فى الكود

{% embed url="https://codesandbox.io/s/hooks-jto950?file=%2Fsrc%2FuseEffect.js%3A0-726" %}
