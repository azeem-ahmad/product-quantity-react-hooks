# Product Quantity / Increment Decrement - with React Hooks
`App.js` file:
```
import React, {useState} from 'react';
import './App.css';

function App() {

  const [count, setCount] = useState(1);

  const decHandler = () => {
    if (count > 1) {
      setCount(count - 1);
    }
  }

  const incHandler = () => {
    if (count < 10) {
      setCount(count + 1);
    }
  }

  // const onChangehandler = (e) => {
  //   let intCount = parseInt(e.target.value); 
  //   setCount(intCount);
  // } 

  return (
    <div className="App">
      {/* <h2>Quantity: {count}</h2> */}
      <button onClick={decHandler}>-</button>
      {/* <input type="text" value={count} onChange={onChangehandler} /> */}
      <span className="countlabel">{count}</span>
      <button onClick={incHandler}>+</button>
      <br />
      <button className="reset" onClick={() => setCount(1)}>Reset</button>
      <p class="note">(Note: Not more than 10 products)</p>

    </div>
  );
}

export default App;

```
