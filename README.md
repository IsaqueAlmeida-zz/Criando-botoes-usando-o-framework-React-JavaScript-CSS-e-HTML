# Criando botões usando o framework React, JavaScript, CSS e HTML.💥

#### Nessa aplicação, usamos os efeitos que o JavaScript tem, o framework React, o CSS e o HTML para dar um design mais bonito e mais elaborado. Abaixo temos os comandos usados na aplicação:



1. ###Index.js (pasta Card):###

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

2. ###Index.js (pasta Button):###

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

3. ###App.js:###

   ​	import Item from './components/item';

   import Card from './components/Card';

   const App = () =>{

     return(

   ​    <>

   ​      <p>Minha Primeira aplicação com React</p>

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

4. ###Index.js (pasta src):###

   ​	import React from 'react';

   import ReactDOM from 'react-dom';

   import App from './App';

   ReactDOM.render(  

   ​    <App />,

     document.getElementById('root')

   );

5. ###Index.js (pasta Item):###

   const Item = (props) => {
    return(
        <a href="/" className="list-group-item list-group-item-action list-group-item-dark">
          {props.children}
        </a>
    )
};

export default Item;
