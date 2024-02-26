import React from 'react'
import Document1 from './Components/Document1/Document1'

const App = () => {
  return (
    <div>
      <Document1/>
    </div>
  )
}

export default App






import React, { useState } from 'react'
import './Document1.css'

const Document1 = () => {
  const [result, setResult] = useState([]);

  const ClickHandler = (event) => {
    setResult([...result, event.target.value]);
  }

  const clearDisp = () => {
    setResult([]);
  }

  const calculate = () => {
    // Join the array elements into a string
    const expression = result.join('');
    // Evaluate the expression and set the result
    setResult([eval(expression).toString()]);
  }

  return (
    <div>
      <div className='main'>
      <div className='calc'>   
     <div className='name'> <b> CASIO</b></div>  <input type='text'  value={null} className='inp'/>
        <input type='text' placeholder='0' id='answer' value={result.join('')} />
        <input type='button' value='7' className='button' onClick={ClickHandler} />
        <input type='button' value='8' className='button' onClick={ClickHandler} />
        <input type='button' value='9' className='button' onClick={ClickHandler} />
        <input type='button' value='+' className='button button2' onClick={ClickHandler} />
        <input type='button' value='4' className='button' onClick={ClickHandler} />
        <input type='button' value='5' className='button' onClick={ClickHandler} />
        <input type='button' value='6' className='button' onClick={ClickHandler} />
        <input type='button' value='-' className='button button2' onClick={ClickHandler} />
        <input type='button' value='1' className='button' onClick={ClickHandler} />
        <input type='button' value='2' className='button' onClick={ClickHandler} />
        <input type='button' value='3' className='button' onClick={ClickHandler} />
        <input type='button' value='*' className='button button2 ' onClick={ClickHandler} />

        
        
        <input type='button' value='C' className='button button1' onClick={clearDisp} />
        <input type='button' value='0' className='button' onClick={ClickHandler} />
        <input type='button' value='=' className='button button2' onClick={calculate} />
        <input type='button' value='/' className='button button2' onClick={ClickHandler} />
     
      </div>
      </div>
    </div>
  );
}

export default Document1;






   body {
    justify-content: center;
    background-color: gray;
    
    
    
   }
  .calc {
    width: 320px;
    margin: 50px auto; /* Adjust vertical margin */
    padding: 15px; /* Add padding */
    border: 2px solid #4FC3F7; /* Add border with grey color */
    background-color: #4FC3F7;
    border-radius: 15px;
   text-align: right;
  }

  .name{
    font-size: 25px;
    text-align: left;
    margin-bottom: 10px; /* Adjust as needed to bring it closer */
    float: left;
  }
    
  
  .inp {
    height: 20px;
    background-color: #333;
    padding: 8px;
    margin: 10px;
    text-align: right;
    border-radius: 5px;
  }   

  #answer {
    background-color: white;
    border: 3px solid #333;
    padding: 10px;
    font-size: 35px;
    width: 295px;
    height: 45px;
    text-align: right;
    margin-bottom: 10px; /* Add margin at the bottom of the input display */
    border-radius: 8px;
  }
  
  .button {
    color: #333;
    background:#BDBDBD;
    width: 70px;
    height: 60px;
    font-size: 30px;
    border: 1px solid black;
    margin: 5px; /* Add margin between buttons */
    border-radius: 5px;
  }
  
  .button1 {
    width: 70px;
    background-color: red;
    color: white;
  }
  
  .button2 {
    width: 70px;
    background: #424242;
    color: white;
  }
  
