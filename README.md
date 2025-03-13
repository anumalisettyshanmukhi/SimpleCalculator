# SimpleCalculator
#Performs basic arithmetic operations
<!DOCTYPE HTML>
<html>
<head>
<title>SimpleCalculator</title>
<style type="text/css">
  .calculator{
       width: 400px;
       height:380px;
       background-color:#A5C4A6;
       padding: 10px;
       margin: auto;
       border-radius: 10px;
       box-shadow: 11px 10px 5px 0px rgba(0,0,0,0.75);
-webkit-box-shadow: 11px 10px 5px 0px rgba(0,0,0,0.75);
-moz-box-shadow: 11px 10px 5px 0px rgba(0,0,0,0.75);
}
  .display-box{
      width:98%;
      height:65%;
      background-color: gray;
      border-radius: 5px;
      color: white;
      font-weight:bolder;
      font-size: 20px;
}
   #btn{
       background-color:palevioletred;
  }
   input[type=button]{
        width:100%;
        height:70%;
        border: 1px solid white;
        border-radius: 5px;
        outline: none;
}
   input:active[type=button]{
        color: white;
        background-color: gray;
 }
 </style>
</head>
<body>
<table class="calculator">
<tr>
  <td colspan="3"><input type="text" class="display-box" id="result" disabled></td>
  <td><input type="button" value="AC" id="btn" onclick="clearScreen()"></td>
</tr>
<tr>
  <td><input type="button" value="1" onclick="display(1)"></td>
  <td><input type="button" value="2" onclick="display(2)"></td>
  <td><input type="button" value="3" onclick="display(3)"></td>
  <td><input type="button" value="/" onclick="display('/')"></td>

</tr>
<tr>
   <td><input type="button" value="4" onclick="display(4)"></td>
   <td><input type="button" value="5" onclick="display(5)"></td>
   <td><input type="button" value="6" onclick="display(6)" ></td>
   <td><input type="button" value="-" onclick="display('-')"></td>

</tr>
<tr>
  <td><input type="button" value="7" onclick="display(7)"></td>
  <td><input type="button" value="8" onclick="display(8)"></td>
  <td><input type="button" value="9" onclick="display(9)"></td>
  <td><input type="button" value="+" onclick="display('+')"></td>

</tr>
<tr>
  <td><input type="button" value="." onclick="display('.')"></td>
  <td><input type="button" value="0" onclick="display(0)"></td>
  <td><input type="button" value="=" id="btn" onclick="calculator()"></td>
  <td><input type="button" value="*" onclick="display('*')"></td>

</tr>
</table>
<script >
   function display(value){
      document.getElementById('result').value+=value;
   }
   function clearScreen(){
      document.getElementById('result').value=""
   }
   function calculator(value){
      var x=document.getElementById('result').value;
      var output=eval(x);
      document.getElementById('result').value=output;
   }
</script>
</body>
</html>
