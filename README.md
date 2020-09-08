<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8"/>
        <meta name="viewport" content="width=device-width,initial-scale=1.0"/>
        <meta http-equiv="X-UA-Compatible" content="ie=edge"/>
        <title>Water InTake Calculator</title>
        <link href="https://fonts.googleapis.com/css2?family=Courgette&display=swap" rel="stylesheet">
        <style>
        *{
            margin:0;
            box-sizing:border-box;
        }
            body{
                background-color:lightgreen;
                height:100vh;
                display:flex;
                justify-content:center;
                align-items:center;
                flex-direction:column;
                font-family: 'Courgette', cursive;;
            }
            p{
                margin-top:17px;
            }
            input{
                width:auto;
                height:23px;
                padding:16px;
            }
            div{
                max-width:600px;
                max-height:1500px;
                background-color:pink;
                padding:28px;
                box-shadow:1px 1px 15px 3px #2d3436;
            }
            h1{
                margin-bottom:10px;
                text-transform:capitalize;
                color:black;
                text-align:center;
            }
            .container input {
                width: 100%;
            }
            }
        </style>
    </head>
    <body>
        <h1>Water Intake Calculator</h1>
        <div class="container">
<form name="Form">
            <p>Gender </p><select id="gender">
            <option disabled selected value="0">-- Choose an Option --</option>
            <option value="female">Female</option>
            <option value="male">Male</option>
            <option value="others">Others</option>
            </select>
             <p>Age</p><input id="age" type="number" min="1" max="100" placeholder="Your Age..">
             <p>Weight</p><input id="weight" type="number" min="1" placeholder="Weight in kg's..">
             <p>Exercise</p><input id="exer" type="number" min="0" placeholder="Exercise in minutes..">
             
             
             <br>
             <br>
<input type="button" value="Calculate" onClick="calculate()">
<br>
<br>
<input type="reset" value="Reset" />
<p id="demo"></p>
</form>
</div>
<script language="JavaScript">
function calculate() {
var gender = document.Form.gender.value
var age = document.Form.age.value
var weight=document.Form.weight.value
var erer=document.Form.exer.value
if(gender==" " || age>0||weight>0||exer>=0){	
var final =(weight*2.205)/2.2
if(age>0 && age<=30){
    var fin=final*40
}else if(age>30 && age<=35){
    var fin=final*35
}
else{
    var fin=final*30
}
    var sum=(fin/28.3)
    var su=(sum*0.0296);
    var outa=su.toFixed(2);
    if(document.getElementById("gender").value=="male"){
        outa=parseFloat(outa)+0.5;
    }
    if(erer>0){
        outa=parseFloat(outa)+(erer)*0.01
    }
    var ou=parseFloat(outa).toFixed(2)
document.getElementById("demo").innerHTML =
"Minimum Water you need to drink is: " + ou+"litres";
}
else{
alert("Please Fill in everything correctly")
}
}
//-->
</script>
</body>
</html>


 
