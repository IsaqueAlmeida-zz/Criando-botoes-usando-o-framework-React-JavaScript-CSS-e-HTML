# Criando botões usando o framework React, JavaScript, CSS e HTML.💥

#### Nessa aplicação, usamos os efeitos que o JavaScript tem, o framework React, o CSS e o HTML para dar um design mais bonito e mais elaborado. Abaixo temos os comandos usados na aplicação:



1. ### _*Index.js (pasta Card):*_

   ​	import { useState } from "react";

   import Button from '../Button';

   const Card = () =>{

   ​    const [valor, setValor] = useState(0);

   ​    

   ​    function Adicionar (){

   ​        setValor(valor + 1)

   ​    }

   ​    function Remover (){

   ​        setValor(valor - 1)

   ​    }

   ​    return (

   ​        <div className="card">

   ​            <div className="card-header">

   ​               Meu primeiro card

   ​            </div>

   ​            <div className="card-body">

   ​                <Button

   ​                    className = "btn btn-success"

   ​                    onClick = {Adicionar}

   ​                >

   ​                    Adicionar

   ​                </Button>

   ​                

   ​                <Button

   ​                    className = "btn btn-danger"

   ​                    onClick = {Remover}

   ​                >

   ​                    Remover

   ​                </Button>

   ​                <p>{valor}</p>

   ​            </div>

   ​        </div>

   ​    )

   };

   export default Card;

2. ###_Index.js (pasta Button):_

   ​	const Button = ( {children, className, onClick} ) =>{

   ​    return (

   ​        <button

   ​            type = "button"

   ​            className = {className}

   ​            onClick = {onClick}

   ​        >

   ​            {children}

   ​        </button>    

   ​    )

   };

   export default Button; 

3. ### _App.js:_

   ​	import Item from './components/item';

   import Card from './components/Card';

   const App = () =>{

     return(

   ​    <>

   ​      <h1>Minha Primeira aplicação com React</h1>

   ​      <ul>

   ​        <Item>

   ​          Item 1

   ​        </Item>

   ​        <Item>

   ​          Item 2

   ​        </Item>

   ​        <Item>

   ​          Item 3

   ​        </Item>

   ​      </ul>

   ​      <Card />

   ​    </>

     )

   };

   export default App;

4. ### _Index.js (pasta src):_

   ​	import React from 'react';

   import ReactDOM from 'react-dom';

   import App from './App';

   ReactDOM.render(  

   ​    <App />,

     document.getElementById('root')

   );

5. ### _Index.js (pasta Item):_

   ​	const Item = (props) => {

   ​    return(

   ​        <a href="/" className="list-group-item list-group-item-action list-group-item-dark">

   ​          {props.children}

   ​        </a>

   ​    )

   };

   export default Item;
