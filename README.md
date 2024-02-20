<!DOCTYPE html>
<html>
    <head>
        <title>Calculator</title>
        <style>
            body{
                text-align: center;
                 
           background-image: linear-gradient(to bottom right,rgb(175, 34, 138),rgb(243, 245, 245),rgb(4, 162, 219));
              
            }
            
            button{
                border-radius: 20px;
                background-color: white;
                color: rgb(2, 2, 2);
                font-size: 30px;
                width: 60px; 
                height: 60px;
                margin: 5px;
                cursor: pointer;

            }
            #blue{
                color: blue;
            }
            input{
                background-color: rgb(254, 253, 253);
                color: rgb(6, 11, 11);
                font-size: x-large;
                cursor: text;
            }h1{
                color: rgb(0, 2, 4);
            }
            #container{
               
                background-image: linear-gradient(to bottom right,rgb(175, 34, 138),rgb(243, 245, 245),rgb(4, 162, 219));
           
                
                align-items: center;
                display: flex;
                flex-direction: column;
                height:85vh;
                width:50vh;
                margin-left: 40%; 
                 margin-right: 40%;
                padding-top: 5%;
            }
           
        </style>
    </head>
    <body>
        <div id="container">
        <h1>CALCULATOR</h1>
        <input type="text" id="display">
        <br>
        <br>
        <div id="one">
        <button id="blue" onclick="allclear()">AC</button>
        <button  id="blue" onclick="deleting()">X</button>
        <button  id="blue" onclick="signchange()">+/-</button>
        <button  id="blue" onclick="append('/')">/</button>
        </div>
        <div>
        <button onclick="append('7')">7</button>
        <button onclick="append('8')">8</button>
        <button onclick="append('9')">9</button>
        <button  id="blue" onclick="append('*')">*</button>
        </div>
        <div>
        <button onclick="append('4')">4</button>
        <button onclick="append('5')">5</button>
        <button onclick="append('6')">6</button>
        <button  id="blue" onclick="append('-')">-</button>
        </div>
        <div>
        <button onclick="append('1')" >1</button>
        <button onclick="append('2')">2</button>
        <button onclick="append('3')">3</button>
        <button  id="blue" onclick="append('+')">+</button>
        </div>
        <div>
        <button onclick="calculate()">%</button>
        <button onclick="append('0')">0</button>
         <button onclick="append('.')">.</button>
        <button  id="blue" onclick="display.value=eval(display.value)">=</button>
        </div>
       
        <script>
            function append(value) {
            document.getElementById('display').value += value;
              
        }
        function allclear(){
            document.getElementById("display").value="0";
        }
        function deleting(){
            let Value1 = document.getElementById('display').value;
    document.getElementById('display').value = Value1.substring(0,Value1.length - 1);

        }
        function signchange(){
            let Value2 = document.getElementById('display').value;
    document.getElementById('display').value = -parseFloat(Value2);
   }
            function calculate(){
                let value3=document.getElementById('display').value;
                document.getElementById('display').value=parseFloat(value3/100);
            }
        </script>
        </div>
    </body>
</html>
