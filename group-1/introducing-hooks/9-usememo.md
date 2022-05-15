---
description: شرح من الـ useMemo
---

# 9 - useMemo

## <mark style="color:blue;">UseMemo</mark>

* هى بترجع قيمة من نوع memoized value
* فكر فى memoization أنها ذاكرة تخزين مؤقتة
* فكرتها أنها بتحفظ القيمة بدون إستدعئها فى كل Render
* يعنى لو لاقى القيمة موجودة مش هيروح يحسبها تانى لأنة حفظها مؤقتاً لحين إستدئعها مرة ثانية

{% code title="useMemoExplain.js" %}
```jsx
import { useState, useMemo, useRef } from "react";

const memoObj = {};

const sumFn = (x, y) => {
  console.log(memoObj);
  return new Promise((resolve, reject) => {
    if (memoObj[x + "*" + y]) resolve(memoObj[x + "*" + y]);
    setTimeout(() => {
      const res = x + y; // هنا بيجمع الرقيمن
      //يعنى لو لقى القيمة مش هيحسبها من تانى ويفضل ثانية مستنى الرقيمن يتجمعه - هيجبلك الرقيمن مجمعين بسرعة مش هيستنى ثانية Memoization هنا هنعمل
      memoObj[x + "*" + y] = res;
      resolve(res);
    }, 1000);
  });
};

export default function App() {
  // جديدة State  هعمل
  const [num, setNum] = useState(0);

  const firstInput = useRef(null);

  const lastInput = useRef(null);

  //  Inputهنجيب الرقم من الـ
  const HandelNumber = (x, y) => {
    sumFn(+firstInput.current.value, +lastInput.current.value).then((res) => {
      setNum(res); // useState اللى هى موجودة فى setNum  هنبعت القيمة للـ
    });
  };

  return (
    <div className="App">
      <h1>useMemoExplaination</h1>
      <h3>{num}</h3>

      <button
        onClick={() => {
          HandelNumber();
        }}
      >
        Calculate
      </button>
      <input placeholder="enter number" ref={firstInput} />
      <input placeholder="enter number" ref={lastInput} />
      <hr />
    </div>
  );
}
```
{% endcode %}
