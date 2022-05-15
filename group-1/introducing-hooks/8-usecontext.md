---
description: شرح useContext
---

# 8 - useContext

## <mark style="color:blue;">useContext</mark>

* للتوضيح الـ Hooks دى أتعملت علشان لو عندك **Nested Component** يعنى Component داخل Component وعاوز تبعت الداتا ليهم وتم من خلالهم فى الحالة دى هتفضل تمرر props لكل Component ودا هيتعبك جدا وهيصعب الموضوع ودا بيسموة prop drilling
* الحل فى **useContext** من خلالها هنعمل `creatContext` داخل الـ Parent Component وهنعملة `useContext` داخل الـNested Component

{% code title="useContext.js - ( Parent Component )" %}
```jsx
import React, { useState, createContext } from "react";
import User from "./user";
import LogIn from "./login";

export const AppContext = createContext(null);

export default function UseContext() {
  const [userName, setUserName] = useState("");

  return (
    <AppContext.Provider value={{userName, setUserName }}>
      <div className="App">
        <h1>useContext</h1>
        <User />
        <LogIn />
        <hr />
      </div>
    </AppContext.Provider>
  );
}
```
{% endcode %}

{% code title="user.js - ( Nested Component )" %}
```jsx
import React, { useContext } from "react";
import { AppContext } from "./useContext";

export default function User() {
  const { userName } = useContext(AppContext);

  return (
    <div className="App">
      <div>
        <h1>User: {userName}</h1>
      </div>
      <hr />
    </div>
  );
}
```
{% endcode %}

{% code title="logIn.js - ( Nested Component )" %}
```jsx
import React, { useContext } from "react";
import { AppContext } from "./useContext";

export default function LogIn() {
  const { setUserName } = useContext(AppContext);

  return (
    <div className="App">
      <div>
        <h1>Log In</h1>
        <input
          onChange={(event) => {
            setUserName(event.target.value);
          }}
        />
      </div>
      <hr />
    </div>
  );
}
```
{% endcode %}
